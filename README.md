# Grimoire — Administratif

Dépôt public des documents administratifs et du site officiel de la suite **Grimoire**, publiée par **Thurtwings Games**.

Ce dépôt centralise les documents destinés à être consultés publiquement ou référencés depuis les boutiques d'applications :

- politiques de confidentialité ;
- informations Google Play / stores ;
- textes de fiche d'application ;
- notes Data Safety ;
- informations de contact publiques ;
- site public Thurtwings Games / Grimoire.

## Site public

Le dépôt contient un site statique bilingue FR/EN prêt pour GitHub Pages.

URL prévue :

`https://thurtwings.github.io/Grimoire_Administratif/`

Politique de confidentialité publique de Grimoire Bourse / Grimoire Wallet :

`https://thurtwings.github.io/Grimoire_Administratif/legal/grimoire-bourse/privacy-policy.html`

Le site est volontairement sans framework, sans analytics, sans publicité et sans dépendance externe.

## Contact

**Thurtwings Games**  
E-mail : **thurtwings.games@gmail.com**

## Structure

```text
index.html
styles.css
404.html
.nojekyll

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

D'autres applications de la suite pourront être ajoutées avec la même organisation.

## GitHub Pages

Configuration recommandée :

1. `Settings` → `Pages` ;
2. `Build and deployment` → `Deploy from a branch` ;
3. branche `main` ;
4. dossier `/(root)` ;
5. `Save`.

Le fichier `.nojekyll` force GitHub Pages à servir directement les fichiers statiques du dépôt.

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

### Grimoire Bourse / Grimoire Wallet

- Package Android : `com.thurtwings.grimoire.money`
- Développeur : Thurtwings Games
- Politique source : [`legal/grimoire-bourse/privacy-policy.md`](legal/grimoire-bourse/privacy-policy.md)
- Politique web : [`legal/grimoire-bourse/privacy-policy.html`](legal/grimoire-bourse/privacy-policy.html)
- Documents Google Play : [`play-store/grimoire-bourse/`](play-store/grimoire-bourse/)
