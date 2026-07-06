# TrailMark

TrailMark est une application web mono-page pour suivre la progression sur des sentiers de randonnée : importez le tracé de référence d'un sentier (GPX), puis ajoutez vos sorties GPS pour visualiser ce qui a été parcouru et ce qu'il reste à faire.

## Fonctionnalités

- **Import GPX** : ajoutez un tracé de référence complet pour un sentier, puis associez-y une ou plusieurs traces GPS de sorties réelles.
- **Calcul de couverture** : la portion du sentier parcourue est calculée par un quadrillage spatial (cellules de 20 m) qui déduplique les points de vos traces.
- **Carte interactive** (Leaflet) : visualisation des segments parcourus (vert), restants (gris) et des portions de trace hors-sentier (rouge).
- **Sauvegarde locale** : les données sont stockées dans le `localStorage` du navigateur.
- **Export / import JSON** : sauvegardez et restaurez l'ensemble de vos sentiers et sorties.

## Utilisation

Ouvrez `index.html` dans un navigateur (aucune installation ni serveur requis).

1. Onglet **+ Import** → section "Ajouter un sentier de référence" → choisissez un fichier GPX du tracé complet.
2. Onglet **+ Import** → section "Ajouter une sortie effectuée" → choisissez le fichier GPX de votre sortie et associez-la au sentier.
3. Cliquez sur un sentier dans la liste pour voir la carte détaillée et les statistiques de progression.

Utilisez les icônes 💾 (sauvegarder) et 📂 (restaurer) de l'en-tête pour exporter/importer vos données.

## Stack technique

Application front-end statique : HTML/CSS/JavaScript vanilla + [Leaflet](https://leafletjs.com/) pour la carte, sans dépendance de build.
