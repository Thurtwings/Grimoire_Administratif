# Google Play Data Safety — Grimoire Inventaire / Grimoire Inventory

Document préparatoire basé sur le comportement actuel de la version candidate **1.5.1** de Grimoire Inventaire / Grimoire Inventory.

Les réponses finales dans Google Play Console doivent être revérifiées contre le comportement exact de l'AAB soumis et les définitions Google Play en vigueur au moment de la soumission.

## Application

- Développeur : **Thurtwings Games**
- Package Android : `com.thurtwings.grimoire.money`
- Version candidate : **1.5.1** (`versionCode 10`)
- Contact : **thurtwings.games@gmail.com**

## Comportement général

- Compte utilisateur : **non**
- Publicité : **non**
- Analytics : **non**
- Tracking : **non**
- Permission Internet : **non**
- Serveur ou cloud Thurtwings Games : **non**
- Stockage local : **oui**
- Partage local volontaire entre appareils : **oui, via Bluetooth Low Energy**
- Presse-papiers : **uniquement après action explicite via Copier rapport**
- Sauvegarde Android : **possible via le système Android**, car `android:allowBackup="true"`

## Données locales

L'application peut conserver localement :

- personnages créés ;
- objets d'inventaire ;
- quantités ;
- catégories et emplacements ;
- poids éventuels ;
- notes ;
- système monétaire choisi ;
- montants et dénominations ;
- coffres de groupe ;
- dettes ;
- historique ;
- préférences et réglages d'accessibilité.

Ces données ne sont pas envoyées à Thurtwings Games.

## Partage local BLE

Le partage du coffre est facultatif et activé par l'utilisateur.

Un appareil manager peut rendre son coffre détectable à proximité. Un spectateur doit demander l'accès et être autorisé avant de recevoir une vue en lecture seule.

Le snapshot partagé peut contenir :

- nom du personnage manager ;
- système monétaire du coffre ;
- montant du coffre ;
- objets du coffre, avec quantités, catégories, poids éventuels et notes ;
- dettes actives appartenant au coffre.

Ne sont pas transmis :

- bourse personnelle ;
- objets personnels ou dans le sac ;
- dettes personnelles ;
- journal financier ;
- préférences ;
- autres personnages.

Le transfert est direct entre appareils proches et n'utilise aucun serveur Thurtwings Games.

### Point à vérifier dans Google Play Console

La classification finale de ce transfert BLE dans les rubriques **Données collectées** et **Données partagées** doit être vérifiée contre les définitions Google Play applicables lors de la soumission. Ce document décrit le comportement technique sans préjuger de la qualification finale demandée par la Play Console.

## Permissions

Version candidate actuelle :

### Android 12+

- `android.permission.BLUETOOTH_SCAN`
- `android.permission.BLUETOOTH_ADVERTISE`
- `android.permission.BLUETOOTH_CONNECT`

Le scan récent utilise `neverForLocation` et n'est pas utilisé pour déterminer la position physique.

### Android 11 et antérieurs

- `android.permission.BLUETOOTH` avec `maxSdkVersion="30"`
- `android.permission.BLUETOOTH_ADMIN` avec `maxSdkVersion="30"`
- `android.permission.ACCESS_FINE_LOCATION` avec `maxSdkVersion="30"`

Android exige historiquement cette permission de localisation pour certains scans BLE sur ces versions. Grimoire ne l'utilise pas pour déterminer, enregistrer ou transmettre la position physique.

### Permissions non demandées

- Internet ;
- contacts ;
- caméra ;
- microphone.

## Presse-papiers

La fonction **Copier rapport** place un rapport généré dans le presse-papiers Android uniquement à la demande de l'utilisateur. L'application ne lit pas le presse-papiers pour collecter des données et ne transmet pas ce rapport à un serveur.

## Sauvegarde Android

L'application autorise la sauvegarde Android. Selon la configuration de l'appareil et du compte Android, certaines données locales peuvent être sauvegardées ou restaurées par le système. Cette sauvegarde n'est pas opérée par un service cloud de Thurtwings Games.

## Politique de confidentialité

https://thurtwings.github.io/Grimoire_Administratif/legal/grimoire-bourse/privacy-policy.html

## Checklist avant soumission

- vérifier le Manifest final de l'AAB ;
- confirmer l'absence de permission Internet ;
- confirmer les permissions Bluetooth réellement présentes ;
- vérifier les formulations Data Safety contre les définitions Google Play du moment ;
- synchroniser la politique embarquée et la politique publique ;
- vérifier le nom public Grimoire Inventaire / Grimoire Inventory ;
- vérifier les descriptions FR/EN ;
- vérifier que les captures correspondent réellement à l'interface 1.5 finale ;
- ne pas annoncer de distribution automatique de récompenses via BLE tant qu'elle n'existe pas ;
- ne pas annoncer que plusieurs managers simultanés sont validés tant que ce test n'est pas confirmé.
