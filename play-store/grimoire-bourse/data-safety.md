# Google Play Data Safety — Grimoire Bourse / Grimoire Wallet

Document préparatoire basé sur le comportement actuel de l'application **Grimoire Bourse / Grimoire Wallet**.

## Application

- Développeur : **Thurtwings Games**
- Package Android : `com.thurtwings.grimoire.money`
- Version candidate : `1.3.0` (`versionCode 5`)
- Contact : **thurtwings.games@gmail.com**

## État actuel

- Données collectées par Thurtwings Games : **non**
- Données partagées avec des tiers : **non**
- Compte utilisateur : **non**
- Publicité : **non**
- Analytics : **non**
- Tracking : **non**
- Communication réseau de l'application : **non**
- Permission Internet : **non**
- Données locales : **oui**
- Presse-papiers : **uniquement après action explicite de l'utilisateur via Copier rapport**
- Sauvegarde Android : **possible via le système Android**, car `android:allowBackup="true"`

## Données locales utilisées par l'application

L'application peut conserver localement :

- personnages créés dans l'application ;
- système monétaire choisi pour chaque personnage ;
- montants de monnaie et dénominations ;
- coffres de groupe ;
- dettes ;
- historique des opérations ;
- préférences et réglages d'accessibilité.

Ces données ne sont pas transmises à Thurtwings Games.

## Presse-papiers

La fonction **Copier rapport** place un rapport généré dans le presse-papiers Android uniquement à la demande de l'utilisateur. L'application ne lit pas le presse-papiers pour collecter des données et ne transmet pas ce rapport à un serveur.

## Sauvegarde Android

L'application autorise la sauvegarde Android. Selon la configuration de l'appareil et du compte Android, certaines données locales peuvent être sauvegardées ou restaurées par le système. Cette sauvegarde n'est pas opérée par un service cloud de Thurtwings Games.

## Permissions

La version candidate ne demande pas de permission Internet, de localisation, de contacts, de caméra ou de microphone.

## Politique de confidentialité

https://thurtwings.github.io/Grimoire_Administratif/legal/grimoire-bourse/privacy-policy.html

## Note

Ce document sert d'aide à la saisie dans Google Play Console. Les réponses finales doivent toujours être revérifiées contre le comportement réel de la version effectivement soumise.
