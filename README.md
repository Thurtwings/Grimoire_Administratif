# Grimoire — Administratif

Dépôt public des documents administratifs de la suite **Grimoire**, publiée par **Thurtwings Games**.

Ce dépôt centralise les documents destinés à être consultés publiquement ou référencés depuis les boutiques d'applications :

- politiques de confidentialité ;
- informations Google Play / stores ;
- textes de fiche d'application ;
- notes Data Safety ;
- informations de contact publiques.

## Site public

Le dépôt héberge également le site public de **Thurtwings Games / Suite Grimoire** via GitHub Pages.

- Site : https://thurtwings.github.io/Grimoire_Administratif/
- Politique Grimoire Inventaire / Grimoire Inventory : https://thurtwings.github.io/Grimoire_Administratif/legal/grimoire-bourse/privacy-policy.html

## Contact

**Thurtwings Games**  
E-mail : **thurtwings.games@gmail.com**

## Structure

```text
assets/
  grimoire-bourse/
    app-icon.png
    coin_pc.png
    coin_pa.png
    coin_pe.png
    coin_po.png
    coin_pp.png

legal/
  grimoire-bourse/
    privacy-policy.md
    privacy-policy.html

play-store/
  grimoire-bourse/
    listing-fr.md
    listing-en.md
    data-safety.md
```

Le nom historique `grimoire-bourse` est conservé dans certains chemins afin de ne pas casser les URLs publiques et intégrations existantes. Le nom public de l'application est désormais **Grimoire Inventaire / Grimoire Inventory**.

D'autres applications de la suite pourront être ajoutées avec la même organisation.

## Règles du dépôt

Ce dépôt est **public**. Il ne doit jamais contenir :

- de clé privée ou de keystore ;
- de mot de passe ;
- de fichier `keystore.properties` ;
- de secret de publication ;
- de données personnelles non destinées à être publiques ;
- de code source privé des applications.

Les applications peuvent conserver une copie locale de leur politique afin qu'elle reste consultable hors ligne. Cette copie et la version publique présente ici doivent rester synchronisées.

## Applications documentées

### Grimoire Inventaire / Grimoire Inventory

- Version publique annoncée : **1.7** (`versionCode 17`), disponible sur Google Play selon le développeur le 11/11/2026.
- Package Android : `com.thurtwings.grimoire.money`
- Développeur : Thurtwings Games
- **21 systèmes monétaires** compatibles avec le moteur local, dont les variantes de D&D, Pathfinder, Shadowrun, Fallout, Cyberpunk RED, 13th Age et Starfinder 1e/2e.
- **16 langues** d'interface ; site vitrine disponible en français, anglais et espagnol.
- Inventaire local par personnage avec **choix persistant entre affichage Grille et Liste** en version 1.7, quantités, catégories, emplacements, poids optionnel et notes.
- Vue grille adaptative, boutons de modification/suppression accessibles, texte agrandi pris en charge.
- Bourse personnelle, paiements intelligents, coffre de groupe, récompenses, dettes, historique et rapports.
- Partage volontaire du coffre à proximité via Bluetooth Low Energy, avec spectateurs en lecture seule.
- Fonctionnement hors ligne, sans compte, publicité, analytics, tracking ni permission Internet.
- Fiche Google Play : https://play.google.com/store/apps/details?id=com.thurtwings.grimoire.money
- Politique de confidentialité : [`legal/grimoire-bourse/privacy-policy.md`](legal/grimoire-bourse/privacy-policy.md)
- Documents Google Play : [`play-store/grimoire-bourse/`](play-store/grimoire-bourse/)

Les chemins historiques `grimoire-bourse` restent inchangés pour préserver les liens publics existants. Les fonctions initialement envisagées pour 1.7 mais non livrées (notamment les actions rapides avancées sur consommables) ne sont pas annoncées comme disponibles.
