# 🗺️ Interactive Rent Visualization – Bordeaux Metropolitan Area

This project provides an **interactive SVG map** to visualize **median and average rents** by zones in the Bordeaux metropolitan area.  
The application is **responsive**, compatible with **mobile and desktop**, and uses JSON data.

---

## 🚀 Main Features

### 🗺️ Interactive Map
- Loads two SVG layers:
  - **Main map** (interactive zones)
  - **Aggregation layer** (`Agglo.svg`) non-interactive but synchronized with zoom/pan
- Select a zone:
  - By **click** or **touch tap** on the map
  - Via the **dropdown menu** (zone selector)
- Zoom **+ / - / reset** and **drag** using mouse or finger

### 📊 Dynamic Data
- Zone data loaded from `datas/datas.json`
- Automatic display of indicators:
  - Median / average rent  
  - Average surface area  
  - Number of surveyed dwellings  
- Illustration for each category (specific images: `images/maison.png`, `images/appartement.png`, etc.)
- Background color and titles synchronized with the zone color on the map

### 💡 User Experience
- Introduction block (`#intro`) visible until a zone is selected
- Smooth animation when cards appear

---

## 📱 Responsive Design

- **SVG map**: height reduced to `300px` on mobile
- **Zoom buttons (+, -, reset)**: stacked vertically in the top-right corner
- **Introduction images** (`#intro-container`): fixed height of `80px`
- **Data cards**: adaptive width, background color matching the zone with reduced opacity

---

## 📁 Project Structure
```
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
```

---

## 🧱 Technologies Used

- HTML5, CSS3, Vanilla JavaScript for interface and interactivity  
- SVG for vector maps  
- JSON for data storage  
- Compatible with desktop and mobile (responsive design)  
- Animations via CSS transitions  

---

## 🎨 Customization

- **Zone colors**: defined in the CSS file (`.zone_1`, `.zone_2`, …)  
- **Card opacity**: configurable in the `colorToRgba(color, opacity)` function in JS  
- **Category images**: filenames must match the cleaned category name (without accents or spaces)  
- **Animations**: duration and delay can be modified in the JS card creation  

---

## 🛠️ Possible Improvements

- Add an **automatic color legend**  
- Filter by dwelling type or rent range  
- Export current view as PDF/image  
- Improve **accessibility** (ARIA, keyboard navigation)  
- Multi-language support (French / English)  
- Add charts or histograms for each zone  

---

## 👨‍💻 Author

**Nicolas Peyrebrune**  
📧 Contact : [n.peyrebrune@sudouest.fr | nicolas.peyrebrune@gmail.com]  
🌐 GitHub : [https://github.com/Superchick-87](https://github.com/Superchick-87) 

---
---

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

---

## 📱 Responsive Design

- **Carte SVG** : hauteur réduite à `300px` sur mobile
- **Boutons de zoom (+, -, reset)** : empilés verticalement dans le coin supérieur droit
- **Images du bloc d’introduction** (`#intro-container`) : hauteur fixe de `80px`
- **Cartes de données** : largeur adaptative, fond couleur correspondant à la zone avec opacité réduite

---

## 📁 Structure du projet
```
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
```

---

## 🧱 Technologies utilisées

- HTML5, CSS3, JavaScript Vanilla pour l’interface et l’interactivité  
- SVG pour les cartes vectorielles  
- JSON pour le stockage des données  
- Compatible desktop et mobile (responsive design)  
- Animations via CSS transitions  

---

## 🎨 Personnalisation

- **Couleurs des zones** : définies dans le fichier CSS (`.zone_1`, `.zone_2`, …)  
- **Opacité des cartes** : configurable dans la fonction `colorToRgba(color, opacity)` du script JS  
- **Images des catégories** : nom des fichiers doit correspondre à la catégorie nettoyée (sans accents ni espaces)  
- **Animations** : durée et décalage modifiables dans la création des cartes JS  

---

## 🛠️ Améliorations possibles

- Ajouter une **légende colorimétrique automatique**  
- Filtrage par type de logement ou tranche de loyers  
- Export PDF / image de la vue actuelle  
- Amélioration de l’**accessibilité** (ARIA, navigation clavier)  
- Support multi-langues (français / anglais)  
- Ajout de graphiques ou histogrammes pour chaque zone  

---

## 👨‍💻 Auteur

**Nicolas Peyrebrune**  
📧 Contact : [n.peyrebrune@sudouest.fr | nicolas.peyrebrune@gmail.com]  
🌐 GitHub : [https://github.com/Superchick-87](https://github.com/Superchick-87)  

