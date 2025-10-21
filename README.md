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

**[Ton Nom ou Organisation]**  
📧 Contact : [ton.email@exemple.com]  
🌐 GitHub : [https://github.com/<ton-utilisateur>](https://github.com/<ton-utilisateur>)  

---

## 📝 Licence

Ce projet est distribué sous licence **MIT**.  
Vous êtes libres de le réutiliser, le modifier et le distribuer à condition de conserver les mentions d’auteur.
