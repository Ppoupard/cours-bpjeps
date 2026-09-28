# Carnet BPJEPS — notes de cours & devoirs

Appli compagnon de la plateforme « BPJEPS MAPST — Mon prof » : un carnet de notes organisé par bloc et par cours (même découpage que la plateforme), et un suivi des devoirs à rendre. Version 2026.09.28-0626.

## Mettre en ligne (GitHub Pages)

1. Crée un dépôt (par ex. `carnet-bpjeps`) et dépose dedans **tout le contenu de ce dossier** : `index.html`, `manifest.webmanifest`, `sw.js`, `icons/`, `.nojekyll`.
2. Dans le dépôt : Settings → Pages → Source « Deploy from a branch » → branche `main`, dossier `/ (root)`.
3. Ouvre l'adresse indiquée (`https://<ton-compte>.github.io/carnet-bpjeps/`). Sur PC (Chrome/Edge), l'icône d'installation dans la barre d'adresse en fait une appli ; sur téléphone, « Ajouter à l'écran d'accueil ».

Le fichier `index.html` marche aussi tout seul, ouvert directement depuis l'ordinateur (sans installation ni service worker).

## Relier le carnet à la plateforme

Réglages → colle l'adresse GitHub Pages de la plateforme « Mon prof ». Chaque note liée à un cours affiche alors un bouton « Ouvrir le cours sur la plateforme » (lien `#/lecon/<id>` de la plateforme).

## Tes données

Tout est enregistré dans le navigateur (clé `bpjeps_carnet_v1` du localStorage) : rien ne part sur un serveur. Deux moyens de ne rien perdre :

- **Exporter** un fichier `.json` (Réglages) et le garder dans un cloud ;
- **Code de synchro** : générer le code sur un appareil, le coller sur l'autre (fusion ou remplacement).

## Astuces dans l'éditeur

- `-` puis espace → liste à puces ; `1.` puis espace → liste numérotée ; `[]` puis espace → case à cocher.
- Sélectionne un mot puis ✎ pour le surligner (re-clic pour enlever).
- Ctrl+B / Ctrl+I / Ctrl+U pour gras / italique / souligné, Ctrl+S pour forcer l'enregistrement (il est de toute façon automatique).
