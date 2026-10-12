# Carnet BPJEPS — notes de cours & devoirs

Appli compagnon de la plateforme « BPJEPS MAPST — Mon prof » : un carnet de notes organisé par bloc et par cours (même découpage que la plateforme), et un suivi des devoirs à rendre. Version 2026.10.09-1633.

## Mettre en ligne (GitHub Pages)

1. Crée un dépôt (par ex. `carnet-bpjeps`) et dépose dedans **tout le contenu de ce dossier** : `index.html`, `manifest.webmanifest`, `sw.js`, `icons/`, `.nojekyll`.
2. Dans le dépôt : Settings → Pages → Source « Deploy from a branch » → branche `main`, dossier `/ (root)`.
3. Ouvre l'adresse indiquée (`https://<ton-compte>.github.io/carnet-bpjeps/`). Sur PC (Chrome/Edge), l'icône d'installation dans la barre d'adresse en fait une appli ; sur téléphone, « Ajouter à l'écran d'accueil ».

Le fichier `index.html` marche aussi tout seul, ouvert directement depuis l'ordinateur (sans installation ni service worker).

## Relier le carnet à la plateforme

Réglages → colle l'adresse GitHub Pages de la plateforme « Mon prof ». Chaque note liée à un cours affiche alors un bouton « Ouvrir le cours sur la plateforme » (lien `#/lecon/<id>` de la plateforme).

## Tes données

Tout est enregistré dans le navigateur (clé `bpjeps_carnet_v1` du localStorage) : rien n'est stocké sur un serveur. Seuls les boutons de l'assistant envoient le texte d'une note, au moment où tu les utilises (voir plus bas). Deux moyens de ne rien perdre :

- **Exporter** un fichier `.json` (Réglages) et le garder dans un cloud ;
- **Code de synchro** : générer le code sur un appareil, le coller sur l'autre (fusion ou remplacement).

## L'assistant (barre au-dessus de chaque note)

- **✨ Mettre au propre** : réorganise la note (titres, listes, idées regroupées) et corrige les fautes, ou seulement les fautes. Options : « garder mes mots » ou « reformuler proprement », et un résumé « À retenir » en bas.
  - Sans clé API : l'appli copie la note avec les consignes et ouvre Claude ; tu envoies, tu copies sa réponse et tu la colles dans l'appli. Si tu quittes l'appli entre-temps, un bandeau te propose de coller la réponse à ton retour.
  - Avec une clé API Anthropic (Réglages) : tout se fait en un clic, sans quitter la note. La clé est payée à l'usage (environ 1 centime par note avec le modèle conseillé) et reste dans ce navigateur : elle n'est jamais dans les fichiers GitHub, les exports ou les codes de synchro.
  - Avant de remplacer, un écran « avant / après » te laisse vérifier.
- **✓ Corriger les fautes** : correcteur LanguageTool (gratuit, sans compte ; le texte de la note est envoyé à leur serveur pour être vérifié). Tu choisis chaque correction ou « Tout corriger ». « ＋ Mon dictionnaire » pour ne plus voir signaler un mot (sigles, noms propres).
- **📂 Ranger** : propose le bloc et le cours qui correspondent au contenu de la note, d'après le vocabulaire des cours de la plateforme.
- **🕘 Historique** : une version est gardée avant chaque mise au propre, correction ou restauration (les 8 dernières) ; tu peux revenir en arrière.

## Mes dossiers (BC1, BC2, BC3)

Menu « 📁 Mes dossiers » → « Commencer un dossier » : BC1 (projet d'animation, ~25 pages), BC2 (supports des deux actions de valorisation), BC3 · 1 (document des trois cycles) et BC3 · 2 (support des deux nouvelles activités). Chaque dossier est découpé selon le plan attendu par le jury ; chaque section est une note du carnet, avec un panneau qui dit ce qu'on attend, les questions à se poser, les preuves à joindre, le piège classique et une liste à cocher avant de dire « terminé ».

- **Avancement** : chaque section est « à écrire », « brouillon », « relue » ou « terminée » (menu en haut de la note) ; le dossier affiche son pourcentage, les mots écrits et l'objectif approximatif par section (environ 400 mots par page).
- **Échéance** : la date « à rendre le » crée automatiquement un devoir (priorité haute) dans la liste des devoirs.
- **Fiche d'identité** : titre du projet, structure, tuteur, public, dates… sert à la page de garde du Word et donne le contexte à Claude.
- **👨‍⚖️ Relire comme le jury** : Claude relit la section comme un jury (ce qui est bien, ce qui manque, trois questions d'oral, les fautes) sans réécrire à ta place. **💡 Me débloquer** : il pose les questions utiles et propose un plan de section ; tu peux ajouter sa réponse en bas de la note. Comme pour « Mettre au propre », ça marche en copier-coller (sans clé) ou en un clic (clé API).
- **📄 Exporter en Word** : un fichier `.docx` avec page de garde, sommaire et une partie par section (les sections vides sont marquées « à rédiger »). Reste à relire et à mettre en forme dans Word.

Les plans et les attentes viennent du référentiel BPJEPS (arrêtés de la mention MAPST) et de la méthode des cours de la plateforme : le nombre exact de pages et les dates de rendu sont ceux de ton organisme de formation, vérifie-les avec ton formateur.

## Choisir (projet BC1, activité APEN)

Menu « 🧭 Choisir » : deux questionnaires courts (ton club, tes moyens, ton public, le terrain, ce que tu maîtrises…) qui donnent un classement argumenté de 3 projets d'animation ou de 3 activités de pleine nature, avec pour chacun ce que le jury aimera, le risque, les indicateurs possibles, ou la sécurité et la réglementation à vérifier. « Demander son avis à Claude » envoie tes réponses et le classement pour une comparaison détaillée ; « Enregistrer dans une note » garde le classement dans le bloc concerné.

## Astuces dans l'éditeur

- `-` puis espace → liste à puces ; `1.` puis espace → liste numérotée ; `[]` puis espace → case à cocher.
- Sélectionne un mot puis ✎ pour le surligner (re-clic pour enlever).
- Ctrl+B / Ctrl+I / Ctrl+U pour gras / italique / souligné, Ctrl+S pour forcer l'enregistrement (il est de toute façon automatique).
