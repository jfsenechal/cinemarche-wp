---
name: Cinémarche ASBL
description: Le site de la salle de cinéma culturelle de Marche-en-Famenne, programmation hebdomadaire, ciné-clubs et événements.
colors:
  bleu-cinemarche: "#2596be"
  bleu-bouton: "#1a7ba1"
  bleu-bouton-survol: "#186382"
  bleu-lien: "#1a526b"
  bleu-clair: "#a7d9e3"
  bleu-ciel: "#83c9f4"
  bleu-controle: "#4fb3d8"
  rouge-programme: "#c0161d"
  rouge-libelle: "#9f1219"
  rouge-pastille: "#fde3e1"
  rouge-colonne: "#fef3f2"
  noir-de-salle: "#0a1720"
  noir-de-cadre: "#1a2e39"
  blanc: "#ffffff"
  gris-de-pied: "#fafafa"
  encre-titre: "#18181b"
  encre: "#27272a"
  encre-secondaire: "#52525c"
  clair-sur-sombre: "#d4d4d8"
  indication-sur-sombre: "#9f9fa9"
typography:
  display:
    fontFamily: "Oswald, ui-sans-serif, system-ui, sans-serif"
    fontSize: "clamp(2.25rem, 5vw, 3.75rem)"
    fontWeight: 600
    lineHeight: 1.05
  headline:
    fontFamily: "Oswald, ui-sans-serif, system-ui, sans-serif"
    fontSize: "2.25rem"
    fontWeight: 600
    lineHeight: 1.11
  title:
    fontFamily: "Oswald, ui-sans-serif, system-ui, sans-serif"
    fontSize: "1.5rem"
    fontWeight: 500
    lineHeight: 1.33
  body:
    fontFamily: "InterVariable, ui-sans-serif, system-ui, sans-serif"
    fontSize: "1.125rem"
    fontWeight: 400
    lineHeight: 1.556
    fontFeature: "'cv02', 'cv03', 'cv04', 'cv11', 'ss03'"
  label:
    fontFamily: "InterVariable, ui-sans-serif, system-ui, sans-serif"
    fontSize: "1rem"
    fontWeight: 500
    lineHeight: 1.5
rounded:
  md: "6px"
  lg: "8px"
  xl: "12px"
  2xl: "16px"
  full: "9999px"
spacing:
  gouttiere: "16px"
  gouttiere-sm: "24px"
  gouttiere-lg: "32px"
  carte: "24px"
  section: "64px"
  section-sm: "96px"
components:
  button-primary:
    backgroundColor: "{colors.bleu-bouton}"
    textColor: "{colors.blanc}"
    typography: "{typography.label}"
    rounded: "{rounded.lg}"
    padding: "10px 12px"
  button-primary-hover:
    backgroundColor: "{colors.bleu-bouton-survol}"
  button-light:
    backgroundColor: "{colors.blanc}"
    textColor: "{colors.noir-de-salle}"
    rounded: "{rounded.lg}"
    padding: "10px 12px"
  chip-seance:
    backgroundColor: "{colors.rouge-pastille}"
    textColor: "{colors.rouge-libelle}"
    typography: "{typography.label}"
    rounded: "{rounded.full}"
    padding: "4px 8px"
  grille-film:
    backgroundColor: "{colors.rouge-programme}"
    textColor: "{colors.blanc}"
    rounded: "{rounded.md}"
    padding: "6px 8px"
  card-film:
    backgroundColor: "{colors.blanc}"
    textColor: "{colors.encre-secondaire}"
    rounded: "{rounded.2xl}"
    padding: "24px"
  input-sombre:
    textColor: "{colors.blanc}"
    rounded: "{rounded.lg}"
    padding: "10px 12px"
---

# Design System: Cinémarche ASBL

Ce document décrit le design **retenu par le porteur du projet : la version 2**. Il est extrait du code du site (`index.html`, tokens dans `src/css/app.css`), repris de la maquette v2 et mis à niveau pour l'accessibilité. Les tokens du frontmatter sont normatifs ; la prose explique comment les appliquer.

## Overview

**Creative North Star: "Le programme, puis la salle"**

La page s'ouvre comme le programme qu'on garde dans la poche : sous un en-tête bleu nuit très mince, une phrase dit d'abord qui programme (« Depuis plus de 25 ans, … mais pas uniquement… ! »), puis la grille de la semaine arrive tout de suite, sur fond blanc, encre foncée. Quoi, quand, où : l'horaire se trouve sans faire défiler. Le rouge du logo porte tout ce qui touche à la programmation, des titres de film en tête de colonne aux horaires et aux types de séance.

Ensuite seulement, la lumière baisse. La bannière plonge dans le noir de salle, un bleu nuit presque noir avec un halo comme la lumière du projecteur : le logo bleu, un titre en capitales étroites, puis une bande de pellicule 35 mm perforée qui présente les six ciné-clubs, chacun avec une vraie photo du lieu, son nom et une phrase : CinéAnimés, CinéSéniors, Midis-docus, Ciné-débats, CinéScolaires, CinéXtra. C'est le moment où l'on dit qui programme, et où l'on donne envie de venir.

Puis le clair revient pour les films à venir et le pied de page, et le noir de salle une dernière fois pour la lettre d'info.

Le partage est donc simple : **le clair renseigne d'abord, le sombre donne envie ensuite**. Le bleu donne l'ambiance et porte les actions, le rouge porte le programme. La densité est celle d'un programme qu'on lit d'un coup d'œil, avec de grandes respirations entre les sections.

**Key Characteristics:**
- Une phrase d'introduction, puis la grille de la semaine dans le premier écran ; la bannière vient après.
- Trois zones sombres seulement (en-tête, bannière, lettre d'info) ; toute l'information se lit sur blanc.
- Deux couleurs de marque au rôle distinct : bleu pour l'ambiance et l'action, rouge pour la programmation.
- Deux familles : Oswald, étroite et affirmée, pour les titres et les horaires ; Inter pour la lecture.
- Texte courant à 18px, rien sous 16px, contraste du texte courant au moins 7:1.
- La bande de pellicule est le seul motif décoratif, et elle encadre de vraies photos.
- Presque sans ombre : la structure vient des aplats, des filets fins et des contours d'un pixel.
- Polices auto-hébergées, aucun appel à un service tiers.

## Colors

Un bleu nuit profond, le bleu et le rouge du logo, et des gris neutres légèrement froids sur blanc.

### Primary
- **Bleu Cinémarche** (`bleu-cinemarche`, #2596be) : le bleu du logo. Couleur d'ambiance : halo flouté de la bannière et de la lettre d'info. Il ne porte **pas** de texte blanc (3.40:1).
- **Bleu de bouton** (`bleu-bouton`, #1a7ba1) : fond du bouton principal et du lien d'évitement, sous du texte blanc (4.78:1). Au survol il fonce en **bleu de survol** (`bleu-bouton-survol`, #186382, 6.68:1).
- **Bleu de lien** (`bleu-lien`, #1a526b) : lien d'adresse e-mail dans le pied de page (8.17:1 sur le gris de pied).
- **Bleu clair** (`bleu-clair`, #a7d9e3) et **bleu ciel** (`bleu-ciel`, #83c9f4) : texte et liens sur fond sombre, sur-titre de la bannière, anneau de focus (11.83:1 et 10.05:1 sur le noir de salle).
- **Bleu de contrôle** (`bleu-controle`, #4fb3d8) : bouton radio coché sur fond sombre.

### Secondary
- **Rouge programme** (`rouge-programme`, #c0161d) : le rouge du logo. Bandeau du titre de film en tête de colonne de la grille (blanc dessus, 6.22:1), sur-titres de section, horaires et dates de la liste mobile, libellé de genre des cartes.
- **Rouge de libellé** (`rouge-libelle`, #9f1219) : type de séance écrit dans une case ou une pastille (8.16:1 sur blanc, 7.50:1 sur le rouge de colonne, 6.70:1 sur le rouge de pastille).
- **Rouge de pastille** (`rouge-pastille`, #fde3e1) : fond des pastilles de type de séance.
- **Rouge de colonne** (`rouge-colonne`, #fef3f2) : une colonne sur deux de la grille, pour suivre un film de haut en bas.

### Neutral
- **Noir de salle** (`noir-de-salle`, #0a1720) : en-tête, bannière, bloc lettre d'info. Un noir bleuté, jamais un noir pur.
- **Noir de cadre** (`noir-de-cadre`, #1a2e39) : le support de la bande de pellicule.
- **Blanc** (`blanc`, #ffffff) : fond de toutes les zones de lecture.
- **Gris de pied** (`gris-de-pied`, #fafafa) : fond du pied de page.
- **Encre de titre** (`encre-titre`, #18181b) et **encre** (`encre`, #27272a) : titres et texte par défaut.
- **Encre secondaire** (`encre-secondaire`, #52525c) : chapôs, crédits des films, dates, notes, pied de page (7.73:1 sur blanc, 7.40:1 sur le gris de pied). C'est le gris le plus clair autorisé pour du texte sur fond clair.
- **Clair sur sombre** (`clair-sur-sombre`, #d4d4d8) : texte courant sur le noir de salle (12.28:1).
- **Indication sur sombre** (`indication-sur-sombre`, #9f9fa9) : texte d'exemple du champ e-mail uniquement (6.91:1).
- **Filets** : noir à 10 % d'opacité sur clair, blanc à 10 à 15 % sur sombre.

### Named Rules

**La règle du sombre qui invite.** Le noir de salle est réservé à trois zones : l'en-tête, la bannière et la lettre d'info. Aucune information de programmation ne se lit sur fond sombre. Test : si un horaire apparaît sur du bleu nuit, c'est un défaut.

**La règle des deux couleurs.** Le bleu dit « Cinémarche » et « cliquez ici » ; le rouge dit « programmation ». Un bouton n'est jamais rouge, un horaire n'est jamais bleu.

**La règle du gris plancher.** Sur fond clair, aucun texte n'est plus clair que l'encre secondaire. Sur fond sombre, aucun texte n'est plus foncé que le clair sur sombre, sauf le texte d'exemple d'un champ.

**La règle du libellé.** La couleur n'est jamais le seul canal : le type de séance (Rencontre, CinéAnimés, CinéSenior, Midi-doc) et le lieu quand ce n'est pas le CinéXtra sont toujours écrits.

## Typography

**Display Font:** Oswald (variable 200–700, utilisée en 500 et 600), avec repli sans-serif système
**Body Font:** Inter variable (100–900, utilisée en 400 et 500), avec repli sans-serif système
**Label/Mono Font:** aucune famille distincte

**Character:** Oswald est étroite, verticale, héritée des titres d'affiche et de journal : elle donne aux titres et aux horaires une voix de fronton sans prendre de place. Inter fait le travail de lecture, avec ses variantes activées (`cv02`, `cv03`, `cv04`, `cv11`, `ss03`) qui lui donnent un « a » rond et des chiffres plus ouverts.

Les deux polices sont **auto-hébergées** dans `assets/fonts/` en sous-ensemble latin (105 Ko pour Inter, 28 Ko pour Oswald), déclarées en `@font-face` avec `font-display: swap` et préchargées. Les licences OFL sont à côté des fichiers.

L'échelle de Tailwind est **relevée d'un cran** dans `@theme` : `text-sm` vaut 16px, `text-base` 18px, `text-lg` 20px, `text-xl` 22px.

### Hierarchy
- **Display** (Oswald 600, 36px en mobile, 48px puis 60px en grand écran, interligne serré) : le titre de la bannière. Un seul par page, 24 caractères par ligne au plus. C'est un titre de niveau 2 : le titre de niveau 1 de la page d'accueil est invisible à l'écran et placé en tête du contenu, pour que l'ordre des titres reste juste alors que la grille passe en premier.
- **Ouverture de l'introduction** (Oswald 600, 36px en mobile, 48px puis 60px en grand écran, interligne 1, bleu de lien) : les premiers mots de la phrase d'introduction, « Depuis plus de 25 ans, ». Ce n'est pas un titre : c'est le début d'un paragraphe.
- **Headline** (Oswald 600, 30px puis 36px) : titres de section.
- **Title** (Oswald 500, 24px pour un titre de film dans une carte ou un nom de ciné-club dans la pellicule, 22px pour un jour dans la liste mobile).
- **Body** (Inter 400, 18px, interligne 28px ; chapô à 20px en mobile) : résumés, chapôs, notes, coordonnées. Longueur de ligne plafonnée à 56 caractères.
- **Label** (Inter 500, 16px, casse normale) : types de séance, genre, libellés de formulaire, légendes des photos. En Oswald 500 : le sur-titre de section, les horaires de la liste mobile (20px) et le titre de film en tête de colonne (16px).

### Named Rules

**La règle du plancher 18px.** Toute phrase qui se lit (résumé, note, aide, infobulle) est à 18px au moins. Les 16px sont réservés aux libellés courts. Rien ne descend sous 16px, sur aucun écran.

**La règle des chiffres alignés.** Horaires et dates portent `tabular-nums` et gardent le format `20h00` et `05/08`.

**La règle du sur-titre sobre.** Le sur-titre de section est en Oswald, en casse normale, en rouge programme, sans interlettrage. Jamais de petites capitales espacées.

## Layout

Une colonne centrée de 1280px au plus (80rem), avec une gouttière de 16px en mobile, 24px à partir de 640px et 32px à partir de 1024px. Les sections sont séparées par 64px de marge verticale en mobile et 96px au-delà, et par un filet fin quand deux sections claires se suivent.

Ordre de la page d'accueil : en-tête collant, phrase d'introduction, grille de la semaine, bannière avec la bande de pellicule, « Nos rendez-vous », lettre d'info, pied de page. La grille suit immédiatement l'introduction : le titre de la semaine et les premières séances restent dans le premier écran. Pour cela, l'introduction n'a que 40px de marge verticale en mobile et 56px au-delà, et la section de la grille commence à 48px puis 64px au lieu de 64px puis 96px.

Points de rupture observés :
- **640px** : la pellicule passe d'une case par ligne à deux ; les cartes de film passent à 2 colonnes ; le pied de page à 2 colonnes.
- **768px** : la grille de la semaine passe de la liste par jour au tableau.
- **1024px** : le menu déroulant devient une barre de liens ; la phrase d'introduction passe sur deux colonnes ; la pellicule passe à trois cases par ligne ; les cartes de film passent à 3 colonnes ; la lettre d'info met le texte et le formulaire côte à côte.

Le tableau garde une largeur minimale de 768px et défile horizontalement dans son conteneur si l'écran est plus étroit ; la colonne des jours reste collée à gauche.

## Elevation & Depth

Le système est presque plat. La profondeur vient de trois choses : le contraste entre zones sombres et zones claires, les contours d'un pixel à 10 % d'opacité autour des cartes et de la pellicule, et les filets horizontaux de la grille.

Deux effets seulement dépassent ce plan. Le **halo** : un disque de bleu Cinémarche à 20 % d'opacité, très flouté, placé derrière le contenu de la bannière et dans un coin du bloc lettre d'info. Et l'en-tête collant, noir de salle à 95 % avec un flou d'arrière-plan, pour rester lisible quand la page défile dessous.

### Shadow Vocabulary
- **Ombre d'infobulle** (`box-shadow: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1)`) : uniquement sur les infobulles du menu, qui flottent au-dessus de la page.

### Named Rules

**La règle de l'ombre unique.** Seul ce qui flotte au-dessus de la page porte une ombre. Les cartes, les boutons et les blocs n'en ont pas.

**La règle du halo.** Le halo bleu n'existe que sur le noir de salle, un par zone sombre. Le site ne porte plus aucun dégradé d'habillage : dans la pellicule, le texte est sous la photo et non dessus.

## Shapes

Des coins doux et courts. 6px pour les petites pièces (affiche miniature, bandeau de titre de film dans la grille), 8px pour les boutons, les champs et les liens du menu, 12px pour les infobulles, 16px pour les cartes de film, le cadre de la pellicule et le bloc lettre d'info. La pastille complète est réservée aux types de séance et aux boutons radio. Rien ne dépasse 16px.

Les bords sont des contours d'un pixel plutôt que des bordures épaisses. La forme propre au site est la **perforation de pellicule** : une rangée de rectangles clairs répétés au-dessus et en dessous des photos (utilitaire `film-perfs`).

Les affiches gardent leur format d'origine (rapport 31:42) et ne sont jamais recadrées en carré.

## Components

### Buttons
- **Shape :** coins doux (8px), hauteur de 48px en mobile.
- **Primary :** bleu de bouton, texte blanc en Inter 500 à 18px, contour d'un pixel de la même couleur. Un seul par zone. La page d'accueil n'en affiche plus depuis que la grille est en tête ; le style sert au lien d'évitement et aux pages à venir.
- **Hover / Focus :** fonce en bleu de survol ; focus par un contour de 2px en bleu ciel, décalé de 2px.
- **Sur fond sombre (formulaire) :** bouton blanc à texte noir de salle (« Valider »), survol en bleu très pâle.
- **Lien secondaire :** texte seul en bleu clair suivi d'une flèche, blanc au survol. C'est la seule action de la bannière (« Nos rendez-vous → »).

### Chips
- **Style :** pastille complète, fond rouge de pastille, texte rouge de libellé en Inter 500 à 16px.
- **Rôle :** nommer le type de séance et, s'il y a lieu, le lieu (« Midi-doc · Tiroir des Saveurs »). Non cliquable.

### Cards / Containers
- **Carte de film :** fond blanc, coins de 16px, contour d'un pixel à 10 %, pas d'ombre. L'affiche entière occupe le haut ; dessous, 24px de marge intérieure, puis dans l'ordre : genre et série en rouge programme, titre en Oswald, crédits (réalisateur · année · durée) en encre secondaire, résumé.
- **Bloc lettre d'info :** noir de salle, coins de 16px, marge intérieure de 32 à 64px selon l'écran, halo dans le coin inférieur droit.

### Inputs / Fields
- **Champ e-mail (sur sombre) :** fond blanc à 5 %, contour d'un pixel blanc à 15 %, coins de 8px, texte blanc à 18px, libellé visible au-dessus.
- **Focus :** contour de 2px en bleu ciel.
- **Boutons radio :** cercle au contour blanc à 20 %, rempli en bleu de contrôle avec un point noir de salle quand il est coché.

### Navigation
- **En-tête :** collant, noir de salle, logo bleu à gauche, six liens à droite en Inter 500 clair, bleu clair au survol.
- **Infobulles :** au survol ou au focus d'un lien, une bulle blanche (coins de 12px, ombre d'infobulle) décrit la destination en une phrase. Un lien sans destination encore définie n'a pas d'infobulle.
- **Mobile (sous 1024px) :** un bouton à trois traits ouvre un panneau `<details>` pleine largeur ; chaque lien y est suivi de sa description.
- **Lien d'évitement :** « Aller à la programmation », visible au focus clavier.

### Phrase d'introduction
- **Structure :** un seul paragraphe en trois temps, sur blanc, fermé en bas par un filet fin. Ni sur-titre, ni fond coloré, ni image.
- **Ouverture :** « Depuis plus de 25 ans, » en Oswald 600, bleu de lien (8.17:1 sur blanc).
- **Corps :** Inter 400, 20px en mobile et 22px au-delà, encre, 60 caractères par ligne au plus.
- **Chute :** « mais pas uniquement… ! » sur sa propre ligne, en Oswald 500, 30px puis 36px, rouge programme (6.22:1 sur blanc, grand texte).
- **Grand écran (à partir de 1024px) :** l'ouverture à gauche sur trois lignes, le corps et la chute à droite, séparés par un filet vertical d'un pixel.
- **Usage :** une seule fois, en tête de la page d'accueil. Le texte est fourni par le porteur du projet ; il reste court pour ne pas repousser la grille hors du premier écran.

### Grille de la semaine (composant signature)
- **Structure :** un vrai `<table>` avec `<caption>`, les films en `<th scope="col">`, les jours en `<th scope="row">`.
- **Tête de colonne :** l'affiche miniature, puis le titre du film en bandeau rouge programme à texte blanc.
- **Corps :** un jour par ligne, séparé par un filet ; une colonne sur deux teintée en rouge de colonne ; horaire centré en encre de titre ; le type de séance écrit en dessous en rouge de libellé. Une case vide reste vide.
- **Colonne des jours :** nom du jour en encre de titre, date en encre secondaire, collée à gauche pendant le défilement horizontal.
- **Version mobile :** une liste ordonnée par jour ; pour chaque séance, l'horaire en Oswald rouge, le titre du film, puis la pastille de type de séance.
- **Note de bas de grille :** rappelle le lieu par défaut (« Sauf mention contraire, les séances ont lieu au CinéXtra »).

### Bande de pellicule
- **Structure :** cadre noir de cadre aux coins de 16px, une rangée de perforations en haut et en bas, six cases entre les deux, une par ciné-club : une colonne en mobile, deux à partir de 640px, trois à partir de 1024px.
- **Case :** un lien entier sur fond noir de salle. La photo du lieu en 3:2 en haut ; dessous, le nom du ciné-club en Oswald 500 blanc à 24px, puis un extrait d'une phrase en Inter 18px, clair sur sombre (plus de 12:1).
- **Survol / Focus :** le nom se souligne et la photo grossit légèrement (uniquement si les animations sont acceptées) ; focus par un contour de 2px en bleu ciel.
- **Contenu :** une phrase par ciné-club, de longueur comparable, sur le modèle « Le ciné-club des… : fréquence, période, ce qui s'y passe, partenaire ». Ce sont des présentations, pas des horaires : la règle du sombre qui invite est respectée.
- **Usage :** une seule fois, dans la bannière.

## Do's and Don'ts

### Do:
- **Do** garder la grille de la semaine en `<table>` sémantique avec sa version liste sous 768px. Jamais une image.
- **Do** garder la grille de la semaine en tête de la page d'accueil, juste après la phrase d'introduction et avant la bannière ; elle doit rester visible dans le premier écran.
- **Do** réserver le noir de salle à l'en-tête, à la bannière et à la lettre d'info, et mettre toute l'information sur blanc.
- **Do** utiliser le bleu pour l'ambiance et les actions, le rouge pour la programmation.
- **Do** tenir le texte courant à 18px et à 7:1 de contraste au moins ; vérifier chaque nouvelle paire de couleurs par le calcul.
- **Do** écrire le type de séance et le lieu en toutes lettres, en plus de la couleur.
- **Do** montrer les vraies photos du lieu et les affiches entières, dans leur format d'origine.
- **Do** donner les crédits du film : réalisateur, année, durée.
- **Do** servir les polices depuis `assets/fonts/`.
- **Do** garder un focus visible (contour de 2px en bleu ciel) et des cibles tactiles d'au moins 48px.
- **Do** modifier les tokens dans `src/css/app.css`, puis reconstruire avec `npm run build`.

### Don't:
- **Don't** poser de texte blanc sur le bleu Cinémarche (#2596be) : il faut le bleu de bouton ou plus foncé.
- **Don't** utiliser un gris plus clair que l'encre secondaire pour du texte sur fond clair.
- **Don't** descendre sous 16px, ni mettre une phrase à lire sous 18px.
- **Don't** charger une police, un script ou une feuille de style depuis un CDN tiers.
- **Don't** étendre le fond sombre à la grille, aux cartes de film ou au pied de page.
- **Don't** ajouter d'ombre aux cartes ou aux boutons, ni de rayon au-delà de 16px.
- **Don't** ajouter de dégradé décoratif, de dégradé sur du texte ou un second halo dans une même zone.
- **Don't** mettre de sur-titre en petites capitales espacées.
- **Don't** remplacer la grille par un carrousel, ni les cartes « Nos rendez-vous » par un rang à faire défiler.
- **Don't** écrire « RÉSERVER » en gros, ni de superlatif promotionnel.
- **Don't** recadrer une affiche en carré ou la remplacer par un aplat de couleur.
