# 🗺️ Visualisation interactive des loyers – Agglomération Bordelaise

Ce projet propose une **carte SVG interactive** permettant de visualiser les **loyers médians et moyens** selon les zones de l’agglomération bordelaise.  
L’application est **responsive**, compatible **mobile et desktop**, et repose sur des données JSON.

---

## 🚀 Fonctionnalités principales

### 🗺️ Carte interactive
- Chargement de deux calques SVG :
  - **Carte principale** (zones interactives)
  - **Calque d’agrégation** (`Agglo.svg`) non interactif mais synchronisé au zoom/déplacement.
- Sélection d’une zone :
  - Par **clic** ou **tap tactile** sur la carte
  - Par le **menu déroulant** (sélecteur de zones)
- Zoom **+ / - / reset** et **déplacement (drag)** au doigt ou à la souris

### 📊 Données dynamiques
- Données des zones chargées depuis un fichier `datas/datas.json`
- Affichage automatique des indicateurs :
  - Loyer médian / moyen  
  - Surface moyenne  
  - Nombre de logements enquêtés  
- Illustration de chaque catégorie (image spécifique : `images/maison.png`, `images/appartement.png`, etc.)
- Couleur de fond et titres synchronisés avec la couleur de la zone sur la carte

### 💡 Expérience utilisateur
- Bloc d’introduction (`#intro`) visible tant qu’aucune zone n’est sélectionnée
- Animation fluide à l’apparition des cartes
- Design **responsive** : carte adaptative, boutons repositionnés, images redimensionnées

---

## 📁 Structure du projet
project/
│
├── css/
│ └── style.css # Feuille de styles principale
│
├── datas/
│ └── datas.json # Données des zones (loyers, surfaces, etc.)
│
├── images/
│ ├── zone-test.svg # Carte SVG principale (zones interactives)
│ ├── Agglo.svg # Calque d’agrégation (non interactif)
│ ├── maison.png # Exemple d’illustration (catégorie)
│ ├── appartement.png # Autres catégories d’images
│ ├── default.png # Image de secours
│ └── visu_intro.png # Illustration d’introduction
│
├── index.html # Fichier principal du projet
└── README.md # Documentation du projet

