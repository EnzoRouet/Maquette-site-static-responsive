# 🌿 Nature Emoi - Advanced Responsive Layout (CSS Grid)

**Projet d'étude** focalisé sur l'intégration HTML5/CSS3 moderne et la maîtrise du responsive design "Mobile-First" via les grilles CSS.
Une landing page vitrine pour une boutique de plantes, mettant l'accent sur une mise en page visuelle asymétrique et adaptative.

![Aperçu du site](./images/Previous.png)

## 🎯 Contexte & Objectifs Pédagogiques

Ce projet a été réalisé dans le cadre de mon **parcours de formation en autodidacte** pour poser des bases solides en intégration web. L'enjeu principal était de sortir des structures linéaires classiques pour explorer la puissance de **CSS Grid**.

L'objectif était de créer une interface capable de se restructurer totalement selon la taille de l'écran, sans altérer la sémantique HTML.

**Objectifs validés :**

- Utilisation experte de **CSS Grid Areas** pour créer des compositions asymétriques.
- Maîtrise des **Media Queries** sur plusieurs points de rupture (breakpoints).
- Mise en œuvre du **Responsive Design** (passage de 4 colonnes à une colonne unique).
- Utilisation des **pseudo-éléments** (`::after`) pour la décoration d'interface.
- Implémentation du **Scroll Behavior** fluide pour la navigation interne.

## 🛠️ Stack Technique

- **Structure :** HTML5 Sémantique.
- **Style :** CSS3 (Grid, Flexbox, Positioning).
- **Design :** Mobile-First Approach, Effets d'opacité et superpositions.

## ✨ Fonctionnalités Développées

### 1. Grille de Produits Dynamique

Développement d'une section "Meilleures ventes" utilisant `grid-template-areas`. La disposition change intelligemment de 4 colonnes (Desktop) à 2 colonnes (Tablette) puis à 1 colonne (Mobile) pour garantir la lisibilité des prix et des noms de produits.

### 2. Layout Asymétrique "Nos Plantes"

Conception d'une double grille (`gridTop` et `gridBottom`) avec des zones de tailles variées. Ce système permet de mettre en avant certains produits (comme l'image `g1` qui prend deux lignes de hauteur) pour casser la monotonie visuelle.

### 3. Navigation Adaptative

Mise en place d'un header responsive où le menu de navigation et le logo se repositionnent automatiquement (passage d'un alignement `flex` horizontal à un bloc centré) sur les petits écrans pour optimiser l'espace vertical.

## 🏗️ Architecture du Style

Le fichier `style.css` est organisé par sections logiques pour faciliter la maintenance :

- **Variables & Global :** Reset CSS et comportements de base.
- **Layouts :** Définition des structures de grilles principales.
- **Responsiveness :** Blocs de Media Queries dédiés à chaque composant pour une lecture granulaire.

## 🧠 Challenges Techniques Résolus

### La restructuration des Grid Areas

Le plus grand défi a été de redéfinir les zones de grille (`grid-template-areas`) sans toucher au code HTML lors du passage en mode tablette.

- _Solution :_ Ré-ordonnancement complet des identifiants de zones dans les media queries (ex: passer de `"g1 g2" "g1 g3"` à `"g1 g2" "g3 g3"`). Cette méthode permet de transformer une image verticale en une bannière horizontale en une seule ligne de CSS.

### Superposition d'éléments (Overlay)

Afficher les informations de prix par-dessus les images de fond de manière lisible.

- _Solution :_ Utilisation du positionnement `absolute` combiné à une opacité sur l'arrière-plan du texte, permettant de conserver un contraste élevé quel que soit le visuel en fond.

## ⚙️ Installation & Lancement

1. **Cloner le dépôt :**

```bash
git clone [https://github.com/EnzoRouet/Maquette-site-static-responsive]
```

2. **Lancer le projet :**
   Ouvrez simplement le fichier index.html dans votre navigateur.
