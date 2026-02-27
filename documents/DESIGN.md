# Design System - La Cigale

Ce document rassemble les spécifications design extraites de l'écran Stitch d'accueil de **La Cigale**.

## 🎨 Palette de couleurs et rôles

La charte graphique repose sur une alliance entre modernité et éléments classiques (Art Nouveau), avec des contrastes profonds (mode sombre principalement) et des touches dorées luxueuses.

| Nom de la couleur | Code Hex | Rôle |
| :--- | :--- | :--- |
| **Primary** | `#1152d4` | Couleur d'action principale (ex: bouton de réservation de la barre principale, icône de l'assistant IA). |
| **Accent Gold** | `#c5a059` | Couleur d'accentuation pour les éléments de prestige, typographie fine (ex: `Date`, `Heure`), icônes décoratives, et bordures. |
| **Background Dark** | `#101622` | Couleur de fond principale (thème sombre), utilisée pour les sections et les verrières (glassmorphism). |
| **Background Light**| `#f6f6f8` | Couleur de base en mode clair. |

* **Gradients & Effets** :
  * **Glass-effect** : Fond `rgba(16, 22, 34, 0.8)` avec un filtre de flou (`backdrop-filter: blur(12px)`), utilisé principalement pour le header persistant afin de garder une visibilité sur le contenu qui défile.
  * **Surfaces secondaires** : Utilisation de nuances bleutées sombres (`slate-900`, `slate-800`) pour les conteneurs (cartes, barre de réservation) et les bordures discrètes, pour un design "Dark Mode" élégant avec de la profondeur.

## ✍️ Typographie et règles

Les polices combinées reflètent le côté lisible, moderne et raffiné de la brasserie.

* **Police Display (Sans-serif)** : `Manrope` (Poids : 300, 400, 500, 700, 800)
  * **Rôle** : Corps de texte, éléments d'interface (boutons, champs de formulaires, petits labels, barre de navigation).
  * **Mise en forme signature** : Les sous-titres, labels (comme les jours et les heures) et les éléments du menu utilisent un texte très petit (`text-xs` ou `text-sm`), en **majuscules** (`uppercase`), en gras (`font-bold`) avec un très large espacement des lettres (`tracking-widest` ou `tracking-[0.4em]`) pour un aspect premium incontestable.

* **Police Serif** : `Playfair Display` (Poids : 400 normal/italic, 700)
  * **Rôle** : Titres principaux de l'interface (H1, H2, H3), grands titres de section et citations pour donner l'identité "Art Nouveau" et patrimoniale (Ex: "L'Art de vivre en héritage").
  * **Mise en forme signature** : L'intégration systématique de portions de textes en **italique fin** (`italic font-normal`) au milieu de très grands titres en gras, typique des lignes éditoriales des marques de luxe.

* **Icônes** : `Material Symbols Outlined`
  * Couplées à des couleurs variées (ex: doré pour l'accentuation, gris pour les compléments d'info).

## 🧩 Composants et patterns

1. **Navigation (Header)**
   * **Pattern** : Navigation flottante avec effet miroir translucide. Elle souligne en finesse le haut de l'écran avec une fine ligne en dessous (`border-b border-slate-800/50`).
   *  Bouton d'appel à l'action (Réserver) visible en permanence.

2. **Hero Section (Bannière d'accueil)**
   * **Pattern** : Photo pleine taille (100vh) assombrie avec un dégradé dégressif (`linear-gradient(to bottom, rgba, rgba)`) pour mettre en exergue le texte en blanc brillant par-dessus.
   * **Boutons principaux** : Utilisation de très grands boutons avec de grandes marges (`px-10 py-4`).
     * Bouton plein : Fond blanc et texte de la couleur de fond obscure.
     * Bouton creux : Bordure et texte blanc, fond pratiquement transparent.

3. **Booking Bar (Barre de réservation)**
   * **Pattern** : Module interactif de réservation qui vient s'immiscer physiquement sur le conteneur du précédent (marges négatives `-mt-16`), créant un décrochage visuel.
   * **Design** : Coins arrondis (`rounded-xl`), ombre énorme derrière pour détacher l'élément très sombre (`shadow-2xl`).

4. **Grilles de présentation (Heritage / Menu)**
   * **Pattern "Hover Reveal"** : Affichage d'images de plats dans un aspect vertical type portrait (`aspect-[3/4]`). 
   * **Animation** : Le texte est en grande partie masqué en bas de la carte, et au passage du curseur de la souris, il remonte doucement (`translate-y`) tandis que l'image à l'intérieur s'agrandit de 5% de façon très douce (`scale-105 duration-500`).

5. **Conciergerie Digitale (IA / Chatbot contextualisé)**
   * **Pattern** : Intégration d'un assistant "Smart" directement dans l'interface, plutôt qu'une pop-up standard.
   * **Design** : Le bloc est mis en valeur avec un fin fond en dégradé, surmonté d'une lumière radiale subtile (un halo doré de fond : `bg-accent-gold/5 blur-3xl`).
   * **Composants d'aide** : Utilisation de "tags / bulles de sélection" arrondis (`rounded-full`) en mode Glass permettant à un utilisateur d'interagir d'un clic avec l'IA.

## 📱 Écrans documentés

Aperçu final de l'interface générée depuis le document HTML fourni :

![La Cigale Homepage](../public/homepage.png)