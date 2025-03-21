
# Introduction au Développement Web

Ma chaine YT: https://www.youtube.com/overconsulting

## Comment fonctionne le web ?

Un **site web** est un ensemble de fichiers (HTML, CSS, JavaScript, images, etc.) accessibles via Internet et affichés par un navigateur. Il peut être **statique** (contenu fixe) ou **dynamique** (contenu généré en fonction des actions de l’utilisateur et/ou d’une base de données).

Le **client** est un appareil (ordinateur, smartphone, tablette) qui demande et affiche des pages web via un navigateur comme **Google Chrome, Firefox, Edge ou Safari**.  
Son rôle est d’envoyer des **requêtes HTTP** et d’afficher les réponses reçues sous forme de pages HTML.

Le **serveur web** est un ordinateur connecté à Internet qui stocke et fournit des fichiers aux clients lorsqu’ils en font la demande.  
Il reçoit des **requêtes HTTP**, traite les demandes et envoie des **réponses HTTP** contenant les pages web demandées.

Comme il est plus facile de retenir un nom de domaine (ex : `www.exemple.com`) pour les humains, mais que pour les ordinateurs, il est plus facile de travailler avec des chiffres (ex : `93.184.216.34`), aussi appelé adresse IP. C'est le **DNS (Domain Name System)** qui traduit les noms de domaine en adresses IP compréhensibles par les serveurs.

Dans l'informatique il faut toujours codifier et documenter comment des services interagissent ensemble. C'est le **HTTP (HyperText Transfer Protocol)** qui est le protocole utilisé pour la communication entre le client (navigateur) et le serveur. Il fonctionne en **requêtes** et **réponses**.

Lorsqu’un utilisateur entre une URL (`https://www.exemple.com`), le navigateur envoie une **requête HTTP** au serveur.  
Une requête HTTP comprend :

- **Une méthode HTTP** (GET, POST, PUT, DELETE…).
- **Une URL** (`www.exemple.com/page.html`).
- Transformation en adresse IP via le **DNS**
- **Des en-têtes HTTP** (informations sur le navigateur, cookies, langue…).
- **Des données (facultatif)** (ex : données d’un formulaire envoyé au serveur).

## Explication du Processus :

1. **L'utilisateur saisit une URL** dans le navigateur (ex : `https://www.exemple.com`).
2. **Le navigateur interroge le DNS** pour obtenir l'adresse IP du serveur.
3. **Le DNS renvoie l’adresse IP** associée au domaine (`93.184.216.34`).
4. **Le navigateur envoie une requête HTTP(S)** au serveur web correspondant à cette IP.
5. **Le serveur traite la requête** et cherche la ressource demandée (fichier HTML, API, etc.).
6. **Le serveur renvoie une réponse HTTP** contenant le contenu demandé.
7. **Le navigateur affiche la page web** à l'utilisateur.

![[HTTP diagramme.jpeg]]

Le **développement web** se divise en deux parties principales :

- **Le frontend** (côté client) : ce que l’utilisateur voit et avec quoi il interagit.
- **Le backend** (côté serveur) : la logique, les bases de données et le traitement des requêtes.

Ces deux parties travaillent ensemble pour offrir une expérience utilisateur fluide et dynamique.

## Les différents navigateurs

| Nom du Navigateur   | Lien de Téléchargement                                                       |
| ------------------- | ---------------------------------------------------------------------------- |
| **Google Chrome**   | [Télécharger Chrome](https://www.google.com/intl/fr_fr/chrome/)              |
| **Mozilla Firefox** | [Télécharger Firefox](https://www.mozilla.org/fr/firefox/new/)               |
| **Microsoft Edge**  | [Télécharger Edge](https://www.microsoft.com/edge)                           |
| **Apple Safari**    | [Télécharger Safari (Mac)](https://support.apple.com/fr_FR/downloads/safari) |
| **Opera**           | [Télécharger Opera](https://www.opera.com/fr/download)                       |
| **Brave**           | [Télécharger Brave](https://brave.com/fr/download/)                          |
| **Vivaldi**         | [Télécharger Vivaldi](https://vivaldi.com/fr/download/)                      |
**Note** : Safari est disponible uniquement sur macOS et iOS. Les autres navigateurs sont compatibles avec Windows, macOS et Linux.

## Les IDEs (Integrated Development Environment)

  c'est un logiciel qui regroupe un ensemble d'outils pour aider les développeurs à écrire, tester et déboguer du code de manière efficace. Il sert de plateforme centralisée pour le développement de logiciels, en combinant plusieurs fonctionnalités essentielles dans une seule interface.

| **IDE**                | **Lien de Téléchargement**                       | **Langages Supportés**                               | **Caractéristiques Principales**                                                                          | **Plateformes Supportées** |
| ---------------------- | ------------------------------------------------ | ---------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | -------------------------- |
| **Visual Studio Code** | [VS Code](https://code.visualstudio.com/)        | HTML, CSS, JavaScript, TypeScript, Python, PHP, etc. | Extensions personnalisables, débogage intégré, Git intégré, multi-plateforme, léger et rapide.            | Windows, macOS, Linux      |
| **Sublime Text**       | [Sublime Text](https://www.sublimetext.com/)     | HTML, CSS, JavaScript, Python, PHP, etc.             | Interface minimaliste, performances élevées, plugins personnalisables, multi-cursor editing.              | Windows, macOS, Linux      |
| **Atom**               | [Atom](https://atom.io/)                         | HTML, CSS, JavaScript, Python, PHP, etc.             | Open-source, personnalisable, intégration Git, packages et thèmes disponibles.                            | Windows, macOS, Linux      |
| **NetBeans**           | [NetBeans](https://netbeans.apache.org/)         | HTML, CSS, JavaScript, PHP, Java, etc.               | Support pour les frameworks web, débogage intégré, gestion de projets complexes.                          | Windows, macOS, Linux      |
| **IntelliJ IDEA**      | [IntelliJ IDEA](https://www.jetbrains.com/idea/) | Java, JavaScript, TypeScript, HTML, CSS              | Intelligence artificielle intégrée, refactoring avancé, support pour les frameworks web.                  | Windows, macOS, Linux      |

## A présent qu'est-ce que le HTML ?

Le HTML (HyperText Markup Language) est le langage fondamental de création de pages web. C'est un langage de balisage qui permet de structurer et organiser le contenu d'une page web. Contrairement aux langages de programmation, HTML utilise des balises pour définir la structure et le sens des différents éléments d'une page. Chaque balise a un rôle spécifique : certaines définissent des titres, d'autres des paragraphes, des liens, des images, etc.

#### Comprendre la structure de base

Un document HTML est comme un squelette qui donne forme et organisation à votre contenu web. Il se compose de plusieurs parties essentielles :

- `<!DOCTYPE html>` déclare que le document est un fichier HTML5
- La balise `<html>` englobe tout le contenu de la page
- `<head>` contient les métadonnées et informations techniques
- `<body>` contient le contenu visible de la page

### Exemple de Structure de Base

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>Ma Première Page Web</title>
</head>
<body>
    <h1>Bienvenue sur ma page</h1>
    <p>Ceci est mon premier paragraphe.</p>
</body>
</html>
```

### Titre et paragraphe

#### Les balises de titres

En HTML, les balises de titres (`<h1>` à `<h6>`) sont cruciales pour la hiérarchie et la structure du contenu. `<h1>` représente le titre principal le plus important, tandis que `<h6>` est le moins important. Cette hiérarchie est essentielle non seulement pour la mise en page visuelle, mais aussi pour le référencement (SEO) et l'accessibilité. Les moteurs de recherche et les lecteurs d'écran utilisent ces balises pour comprendre la structure de votre contenu.

#### Les paragraphes

La balise `<p>` sert à délimiter des paragraphes de texte. Elle permet de séparer logiquement différents blocs de texte et donne du sens à votre contenu. Un bon usage des paragraphes améliore la lisibilité et la compréhension de votre texte.

#### Exercice
- Créez un document sur un sujet qui vous passionne
- Utilisez au moins 3 niveaux de titres différents
- Écrivez au moins 3 paragraphes

```html
<h1>Titre Principal</h1>
<h2>Sous-titre</h2>
<p>Un paragraphe de texte explicatif.</p>
<h3>Section secondaire</h3>
<p>Un autre paragraphe avec plus de détails.</p>
```

### Lien HTML

Il y a trois sortes de lien:
- Lien interne à la page
- Lien interne au site web
- Lien externe

```html
<h1>Mes Liens Préférés</h1>


<!-- Lien site interne -->
<a href="page2.html">Lien Interne</a>

<!-- Lien extene -->
<a href="https://google.com" title="google.Fr">Lien Externe</a>

<!-- Lien extene avec ouverture d'un onglet -->
<a href="https://www.ece.fr" target="_blanck>Lien Externe</a>

<p></p>
<p></p>
<p></p>

<h2 id="test">Test</h2>
<p>Vous avez vu on c'est déplacer dans la page !</p>
```

### Les listes

#### Ordonnées

```html
<h2>Étapes d'une Recette</h2>
<ol>
	<li>Préchauffer le four</li>
	<li>Mélanger les ingrédients</li>
	<li>Cuire pendant 30 minutes</li>
</ol>
```

#### Non ordonnées

```html
<h2>Liste de Courses</h2>
<ul>
	<li>Pain</li>
	<li>Lait</li>
	<li>Œufs</li>
</ul>
```
### Les images

Le plus souvent pour rendre un site jolie on ajoute des images ! Voici comment faire:

```html
<h1>Mon Album Photo</h1>
<img src="lion.jpg" alt="Un lion dans la savane" width="300" height="200">
<p>Description : Mon chat adoré</p>
```

Pour aller plus loin, on va ajouter une légende à notre image

```html
<h1>Galerie d'Images</h1>

<!-- Image avec tous les attributs -->
<img 
    src="paysage.jpg" 
    alt="Un magnifique paysage de montagne" 
    width="500" 
    height="300"
>

<!-- Image avec légende -->
<figure>
    <img src="chat.png" alt="Un chat noir">
    <figcaption>Mon chat Moustache</figcaption>
</figure>
```


### Les éléments neutres: Div et span

#### `<div>` : Un conteneur de bloc

- `<div>` est une **balise de type bloc**.
- Elle **occupe toute la largeur** disponible de son parent.
- Utilisée pour regrouper plusieurs éléments et appliquer du style ou des scripts.

```html
<div class="section">
    <h2>Titre de la section</h2>
    <p>Ceci est un paragraphe dans une div.</p>
</div>
```

#### `<span>` : Un conteneur en ligne

- `<span>` est une **balise en ligne**.
- Elle **n’affecte pas la mise en page** en occupant une largeur spécifique.
- Sert à appliquer du style à **une partie de texte ou un élément inline**.

```html
<p>Ce mot est <span class="important">très important</span> dans la phrase.</p>
```
#### Différences entre `<div>` et `<span>`

| **Caractéristique**            | **`<div>`**                               | **`<span>`**                                     |
| ------------------------------ | ----------------------------------------- | ------------------------------------------------ |
| **Type de balise**             | Bloc                                      | En ligne                                         |
| **Prend toute la largeur**     | Oui                                       | Non                                              |
| **Utilisation principale**     | Regrouper plusieurs éléments              | Modifier une partie d'un texte ou élément inline |
| **Peut contenir…**             | Titres, paragraphes, images, listes, etc. | Texte, liens, icônes, etc.                       |
| **Impact sur la mise en page** | Crée une nouvelle ligne                   | Aucun impact sur la structure                    |


## Projet : Page de Présentation Personnelle

Créez une page complète incluant :

- Un titre principal
- Une photo de vous (ou avatar)
- Une liste de vos compétences
- Des liens vers vos réseaux sociaux
- Un paragraphe de présentation

### Les tableaux

A présent, nous allons voir les éléments un peu plus complexe ! les tableaux !

Un tableau est une structure de données qui organise l'information en lignes et colonnes. En HTML, les tableaux permettent de présenter des données de manière structurée et lisible.

#### Définitions balises nécessaires:
- **`<table>` :** Balise conteneur pour un tableau
- **`<tr>` :** Table Row, représente une ligne du tableau
- **`<td>` :** Table Data, représente une cellule
- **`<th>` :** Table Header, utilisé pour les en-têtes de colonnes ou lignes

#### Petit exemple:

```html
<table border="1">
    <thead>
        <tr>
            <th>Nom</th>
            <th>Âge</th>
            <th>Ville</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Marie</td>
            <td>28</td>
            <td>Paris</td>
        </tr>
        <tr>
            <td>Jean</td>
            <td>35</td>
            <td>Lyon</td>
        </tr>
    </tbody>
</table>
```

#### Exercices

1. Créez un tableau de votre collection personnelle (livres, films, etc.)
2. Utilisez `<thead>` et `<tbody>`
3. Ajoutez au moins 5 lignes de données
4. Expérimentez avec la mise en forme basic

### Les formulaires

Un formulaire est un ensemble d'éléments interactifs permettant aux utilisateurs de saisir et d'envoyer des données à un serveur web.

#### Définitions balises nécessaires:
- **`<form>` :** Balise conteneur de tous les éléments de formulaire
- **`<input>` :** Élément de saisie polyvalent
- **Types d'input :** text, password, email, number, date, checkbox, radio
- **`<label>` :** Étiquette associée à un champ de formulaire
- **`<button>` :** Bouton de soumission ou d'action
- `<fieldset>`: Petit encadrer pour créer des blocks

#### Petit exemple

```html
<form>
    <h2>Formulaire de Contact</h2>
    
    <label for="nom">Nom :</label>
    <input type="text" id="nom" name="nom" required>
    
    <label for="email">Email :</label>
    <input type="email" id="email" name="email" required>
    
    <label for="message">Message :</label>
    <textarea id="message" name="message" rows="4"></textarea>
    
    <fieldset>
        <legend>Préférences</legend>
        <input type="checkbox" id="newsletter" name="newsletter">
        <label for="newsletter">Abonnement newsletter</label>
    </fieldset>
    
    <button type="submit">Envoyer</button>
</form>
```

#### Exercices
1. Créez un formulaire d'inscription à un site
2. Incluez différents types de champs
3. Utilisez `<label>` et `id` correspondants
4. Ajoutez des champs obligatoires

### Éléments Sémantiques

Les éléments sémantiques donnent du sens à la structure d'une page web, au-delà de sa simple apparence visuelle.

#### Définitions balises nécessaires:
- **`<header>` :** En-tête de page ou de section
- **`<nav>` :** Zone de navigation
- **`<section>` :** Section thématique de contenu
- **`<article>` :** Contenu autonome et indépendant
- **`<footer>` :** Pied de page

#### Petit exemple

```html
<!DOCTYPE html>
<html lang="fr">
	<head>
	    <meta charset="UTF-8">
	    <meta name="viewport" content="width=device-width, initial-scale=1.0">
	    <title>DEV WEB | index.html</title>
	</head>
	<body>
	    <header>
	        <h1>Mon Site Web</h1>
	        <nav>
	            <a href="#accueil">Accueil</a>
	            <a href="#about">À propos</a>
	            <a href="#contact">Contact</a>
	        </nav>
	    </header>
	
	    <main>
	        <section id="accueil">
	            <h2>Bienvenue</h2>
	            <article>
	                <h3>Dernière actualité</h3>
	                <p>Contenu de l'article...</p>
	            </article>
	        </section>
	    </main>
	
	    <footer>
	        <p>© 2024 Mon Site</p>
	    </footer>
	</body>
</html>
```

## CSS

### Qu'est-ce que le CSS ?

Le CSS (Cascading Style Sheets ou Feuilles de Style en Cascade) est un langage de stylisation qui permet de mettre en forme et de présenter du contenu HTML. Il contrôle l'apparence visuelle des éléments web.

#### Définitions clés
- **Sélecteur :** Identifie les éléments HTML à styliser
- **Propriété :** Caractéristique à modifier (couleur, taille, etc.)
- **Valeur :** Spécification de la modification
- **Syntaxe CSS :** `selecteur { propriete: valeur; }`

### Comment écrire le CSS ?

Soit dans un élément HTML

```html
<p style="color: red;">Texte en rouge</p>
```

Soit dans le html à l'intérieur de balise

```html
<style> p { color: red; } </style>
```

Soit dans une fichier css

main.css
```css
p { color: red; }
```

Par contre il faudra dire au fichier HTML d'inclure le fichier CSS.

```html
<link rel="stylesheet" href="main.css">
```

#### Petit exemple

```html
<!DOCTYPE html>
<html lang="fr">
    <head>
        <style>
            /* CSS */ 
            .carte {
                border: 1px solid #ccc; 
                padding: 15px; 
            } 
            
            #titre-principal { 
                color: navy; 
                text-align: center;
            }
            
            p { font-size: 16px; line-height: 1.5; }
        </style>
    </head>
    <body>
        <!-- HTML -->
        <div class="carte">
            <h1 id="titre-principal">Mon Titre</h1>
            <p>Un paragraphe de texte.</p>
        </div>
    </body>
</html>
```

#### Types de Sélecteurs

**Sélecteur de balise :** Cible tous les éléments d'un type

`p { color: blue; }`

**Sélecteur de classe :** Cible des éléments avec une classe spécifique

`.titre { font-weight: bold; }`

**Sélecteur d'ID :** Cible un élément unique

`#entete { background-color: gray; }`

### Formats de Couleurs

#### Mots-clés Prédéfinis

```css
.texte-rouge { color: red; } 
.fond-vert { background-color: green; } 
.bordure-bleu { border-color: blue; }
```

#### Notation Hexadécimale

Format le plus courant, représente les couleurs par des codes hexadécimaux

```css
.couleur-perso { 
	color: #FF0000; /* Rouge vif */ 
	background-color: #00FF00; /* Vert vif */ 
	border-color: #00F; /* Bleu vif */ 
}
```

**Structure du code hexadécimal**
- 6 caractères : `#RRGGBB` ou trois #RGB attention alors la valeur R, G et B sera doublé
- Chaque paire représente l'intensité (00 à FF)
- `#000000` = Noir
- `#FFFFFF` = Blanc
- 

#### RGB et RGBA

Permet de définir les couleurs par leurs composantes Rouge, Vert, Bleu.

```css
.couleur-rgb { 
	color: rgb(255, 0, 0); /* Rouge vif */ 
	background-color: rgb(0, 255, 0); /* Vert vif */ 
} 

.couleur-rgba { 
	background-color: rgba(0, 0, 255, 0.5); /* Bleu semi-transparent */ 
}
```

**Caractéristiques**
- Valeurs de 0 à 255 pour chaque couleur
- `rgba()` ajoute un canal alpha (transparence)
- 0 = aucune intensité
- 255 = intensité maximale

#### HSL et HSLA

Représente les couleurs par Teinte, Saturation, Luminosité.

```css
.couleur-hsl {
    color: hsl(0, 100%, 50%);     /* Rouge vif */
    background-color: hsl(120, 100%, 50%);  /* Vert vif */
}

.couleur-hsla {
    background-color: hsla(240, 100%, 50%, 0.7);  /* Bleu semi-transparent */
}
```

**Composantes**

- Teinte (0-360°) : position sur le cercle chromatique
    - 0/360° = Rouge
    - 120° = Vert
    - 240° = Bleu
- Saturation (0-100%) : intensité de la couleur
- Luminosité (0-100%) : clarté de la couleur
- Canal alpha (0-1) optionnel pour la transparence

### Ressources

Adobe: https://color.adobe.com/fr/
Palette: https://colorhunt.co/

### Tailles en CSS : px, em, rem, %, vw, vh, etc.

#### Les unités absolues

**Pixel (`px`)**
- 1 `px` correspond à un point sur l'écran.
- Il est couramment utilisé pour définir des tailles précises.

```css
h1 {
  font-size: 32px; /* La taille du texte est de 32 pixels */
}
```
#### Les unités relatives

**`em` : relatif à la taille de la police du parent**
- `1em` correspond à la taille de la police du parent direct.
- `2em` signifie **deux fois** la taille de la police du parent.

```css
p {
  font-size: 16px;
}
button {
  font-size: 1.5em; /* 1.5 fois la taille du texte du parent */
}
```

**`rem` : relatif à la taille de la police du `<html>` (root)**
- `1rem` est basé sur la taille définie pour l’élément `<html>`.
- Par défaut, la taille du texte dans `<html>` est de `16px`, donc `1rem = 16px`.

```css
html {
  font-size: 20px;
}
h1 {
  font-size: 2rem; /* 2 * 20px = 40px */
}
```

**Pourcentages (`%`)**
- Dépend de la taille de son parent.
- Très utile pour rendre les mises en page **responsives**.

```css
div {
  width: 50%; /* Prend la moitié de la largeur du parent */
}
```

**`vw` et `vh` : unités basées sur la taille de l’écran**
- `vw` (viewport width) : 1 `vw` = 1% de la largeur de l’écran.
- `vh` (viewport height) : 1 `vh` = 1% de la hauteur de l’écran.

```css
h1 {
  font-size: 10vw; /* 10% de la largeur de l’écran */
}
```

**`min()` et `max()` : tailles adaptatives**

Ces fonctions permettent de définir des tailles qui s’adaptent dynamiquement.

```css
p {
  font-size: min(5vw, 24px); /* Ne dépassera pas 24px même si 5vw est plus grand */
}
```

#### Quand utiliser quelle unité ?

|**Unité**|**Usage recommandé**|
|---|---|
|`px`|Petits éléments fixes (bordures, icônes)|
|`em`|Espacements internes (`padding`, `margin`)|
|`rem`|Tailles de texte principales|
|`%`|Largeurs et hauteurs flexibles|
|`vw`, `vh`|Tailles dynamiques selon l’écran|
|`min()`, `max()`|Pour des tailles adaptatives|

### Modèle de boîte (Box Model)

Chaque élément HTML est une boîte avec :
- `content` (le contenu)
- `padding` (espace intérieur)
- `border` (bordure)
- `margin` (espace extérieur)

```css
div {
  width: 200px;
  padding: 20px;
  border: 5px solid black;
  margin: 10px;
  box-sizing: border-box;
}

```

### Positionnement des éléments

Les valeurs de `position` :
- `static` (par défaut)
- `relative` (par rapport à sa position normale)
- `absolute` (par rapport à l’élément parent positionné)
- `fixed` (fixé à l’écran)


```css
.box { position: absolute; top: 50px; left: 50px; }
```

### Les fonts

```css
.font {
    color : red; /* Couleur du text */
    font-size: 14px; /* Tailles de la police */
    font-family: Arial, Helvetica, sans-serif; /* choix de police */
    font-weight: bold; /* Grosseur de la police */
    font-style: italic; /* Pour mettre en italic */
    text-align: center; /* Pour centrer du texte */
}
```

### Les bordures

#### border-width

```css
p {
    border-width: 2px;
}
```

#### border-style

```css
div {
    border-style: "dotted";
}
```

#### border-color

```css
div {
    border-color: red;
}
```

#### border-radius

```css
div {
    border-radius: 2px;
}
```

Exemple complet

```css
.box1 {
    border: 2px silver dotted;
}

.box2 {
    border: 5px pink dashed;
}

.out-bordered {
    padding: 10px 20px;
    border-radius: 15px;
    color: lightcoral;
    border: 1px solid lightcoral;
}
```

```html
<!DOCTYPE html>
<html lang="fr">
    <head>
        <title>Test CSS bordure</title>
    </head>
    <body>
        <div class="box1"></div>
        <div class="box2"></div>
        <div class="out-bordered"></div>
    </body>
</html>
```


### Flexbox (Flexible Box Layout)

Flexbox est un modèle de mise en page **unidimensionnel** qui aligne les éléments **horizontalement** ou **verticalement** de manière efficace.

```css
.container {
    display: flex;
}
```

#### Direction des éléments : `flex-direction`

```css
.container {
    display: flex;
    flex-direction: row; /* Par défaut : en ligne */
}
```

**Valeurs possibles** :
- `row` (par défaut) → de gauche à droite
- `row-reverse` → de droite à gauche
- `column` → de haut en bas
- `column-reverse` → de bas en haut

#### Alignement des éléments : `justify-content` (axe principal)

```css
.container {
    display: flex;
    justify-content: center;
}
```

**Valeurs possibles** :
- `flex-start` (par défaut) : alignés au début
- `flex-end` : alignés à la fin
- `center` : centrés
- `space-between` : espace entre les éléments
- `space-around` : espace autour des éléments

#### Alignement vertical : `align-items` (axe secondaire)

```css
.container {
    display: flex;
    align-items: center;
}
```

**Valeurs possibles** :
- `flex-start` (en haut)
- `flex-end` (en bas)
- `center` (au milieu)
- `stretch` (prend toute la hauteur)
- `baseline` (alignement sur la ligne de base du texte)

#### Gestion du retour à la ligne : `flex-wrap`

Si les éléments ne rentrent pas sur une seule ligne, ils peuvent passer à la ligne suivante.

```css
.container {
    display: flex;
    flex-wrap: wrap;
}
```

**Valeurs possibles** :
- `nowrap` (par défaut) : tous les éléments restent sur une seule ligne
- `wrap` : les éléments passent à la ligne si besoin
- `wrap-reverse` : les lignes sont inversées

#### Contrôle individuel des éléments : `flex-grow`, `flex-shrink`, `flex-basis`

```css
.item {
    flex-grow: 1; /* L'élément prend tout l’espace disponible */
}
```

**Valeurs possibles** :
- `flex-grow: 1;` → L’élément s’agrandit pour occuper tout l’espace.
- `flex-shrink: 1;` → L’élément peut se réduire en cas de manque de place.
- `flex-basis: 200px;` → Taille de base de l’élément.

#### Exercice Centrer un élément en Flexbox

Crée un `div` centré en plein écran.

```css
.container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: lightgray;
}
.box {
    width: 200px;
    height: 200px;
    background-color: blue;
}
```

## Projet : Page de Présentation Personnelle (suite)

1. Modifier votre portfolio pour le rendre plus moderne
2. Ajouter une section projets
3. Ajouter un ou deux projets
4. Créez une page par projet qui met en avant ce projet


### Responsive Design et Media Queries

```css
@media (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```

## Projet : Page de Présentation Personnelle

Rendre votre portfolio responsive