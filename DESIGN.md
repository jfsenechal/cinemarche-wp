<!-- SEED: re-run $impeccable document once there's code to capture the actual tokens and components. -->
---
name: Cinémarche ASBL
description: Le site de la salle de cinéma culturelle de Marche-en-Famenne : programmation hebdomadaire, ciné-clubs et événements.
---

# Design System: Cinémarche ASBL

## 1. Overview

**Creative North Star: "Le fronton et le programme"**

Deux objets réels tiennent tout le système. Le **fronton** : la devanture éclairée du CineXtra, les lettres sur cadre, l'annonce faite dans la rue à hauteur de passant. C'est le registre de la bannière et des titres : grand, franc, adressé à quelqu'un qui passe. Le **programme** : la feuille pliée en trois qu'on garde dans la poche de manteau, tramée, dense, où l'on trouve son horaire sans rien déplier de plus. C'est le registre de la grille hebdomadaire et de tout le texte courant : dense mais jamais serré, tabulaire, lisible du premier coup.

Entre les deux, une troisième exigence, venue de la Cinémathèque : **le film est un document**. Titre, réalisateur, année, durée, affiche d'origine. On ne recadre pas une affiche pour qu'elle rentre dans une vignette carrée, on ne remplace pas des crédits par un slogan. Les crédits sont de l'information, au même titre qu'un horaire.

Ce système rejette explicitement, dans l'ordre des risques réels pour ce projet : le **site institutionnel communal** (le piège d'un `.marche.be` : liens gris en colonnes, programmation en PDF, aucune hiérarchie), le **multiplexe commercial** (fond noir, dégradés, boutons « RÉSERVER »), la **plateforme de streaming** (carrousels de vignettes à faire défiler à l'infini) et le **template SaaS lisse** (cartes identiques très arrondies, icônes pastel, sur-titres en majuscules au-dessus de chaque section). Le rendu « fait par une IA » est un échec de marque, pas un détail.

**Key Characteristics:**
- Palette de quatre rôles nommés, chacun codant une fonction précise, jamais une décoration.
- Une seule famille typographique, hiérarchie portée par l'échelle et le poids (400 → 800).
- Chiffres tabulaires obligatoires : la grille horaire est le cœur fonctionnel de la page.
- Plat par défaut ; la profondeur vient de la couleur et du trait, pas de l'ombre.
- Mouvement au service du retour d'information, aucune chorégraphie de défilement.
- Densité de programme papier : beaucoup d'information par écran, aucune sensation d'entassement.
- Le lieu et les films sont photographiés, jamais illustrés.

## 2. Colors

Quatre rôles nommés, ancrés sur le **rouge du logo Cinémarche, `#D80000`**, échantillonné directement dans les trois fichiers du logo (`logo-cinemarche-red.png`, `Cinemarche-logo.jpg`, `Cinémarche-asbl-Logo-carre.jpg`) : hue 0, saturation 1.00, valeur identique dans les trois. La grille papier de l'ASBL (`grille pgm 2.jpeg`) est la même couleur passée en presse (`#C02818`).

Le brief proposait de partir du bleu (`#A7D9E3`, `#2596be`, `#84CDD9`, `#A6D8E2`). L'inventaire des fichiers l'a contredit : le fichier « logo bleu » est une déclinaison monochrome délavée (saturation 0.41) du même dessin, et le bleu vif appartient au **CineXtra**, le complexe qui héberge les séances. Arbitrage confirmé par le porteur du projet : **le rouge identifie qui programme, le bleu identifie où l'on va.**

Toutes les valeurs ci-dessous sont vérifiées par calcul de contraste, pas estimées.

### Primary
- **Rouge Cinémarche** `#D80000` · `oklch(0.554 0.227 29.2)` : la couleur du logo. Réservée au logo lui-même, aux traits d'accent et aux gros titres. **5.36:1 sur blanc** : suffisant pour du grand texte et des libellés, jamais pour du texte courant.
- **Rouge de fronton** `#B00000` · `oklch(0.475 0.195 29.2)` : la version qui porte du texte. C'est elle qui remplit le bandeau haut, les colonnes de la grille et le pied de page. **7.38:1 avec le blanc, dans les deux sens** : conforme à la cible AAA.

### Secondary
- **Bleu CineXtra** `#0F6386` · `oklch(0.471 0.092 232.8)` : le lieu, et rien d'autre. Texte et filet du badge indiquant où se tient la séance. **6.67:1 sur blanc.**
- **Bleu de badge** `#E3F1F8` · `oklch(0.950 0.018 229.0)` : fond du badge de lieu, sous de l'encre (**15.75:1**).

### Tertiary
- **Ocre CinéAnimés** `#8A5A00` · `oklch(0.508 0.108 73.3)` : le jeune public. CinéAnimés, séances scolaires, ateliers. Teinte 73 contre teinte 29 pour le rouge : l'écart reste lisible en vision dichromate, et le libellé écrit reste obligatoire de toute façon.
- **Ocre de badge** `#FBEED2` · `oklch(0.952 0.039 86.1)` : fond du badge jeune public, sous de l'encre (**15.80:1**).

### Neutral
- **Blanc franc** `#FFFFFF` : cases libres de la grille, surfaces de lecture.
- **Blanc de page** `#FCFAFA` · `oklch(0.987 0.002 17.2)` : fond général. Chroma 0.002 tiré vers la teinte du rouge, pas vers le chaud. Ce n'est pas un crème.
- **Encre** `#1A1416` · `oklch(0.199 0.010 356.1)` : tout le texte courant. **18.17:1 sur blanc, 17.48:1 sur le blanc de page.**
- **Gris de trait** `#8E8288` · `oklch(0.619 0.017 345.8)` : un seul gris, pour les filets et les bordures. **3.69:1 sur blanc**, au-dessus du minimum de 3:1 exigé pour un élément non textuel.

### Named Rules

**La règle des quatre rôles.** Quatre couleurs, quatre fonctions : identité, exception, jeune public, lecture. Une cinquième couleur ne s'ajoute pas « pour varier ». Si une nouvelle catégorie de séance apparaît, elle se distingue par le mot et la position, pas par une teinte de plus.

**La règle du libellé.** Aucune information n'est portée par la seule couleur. Le type de séance est toujours écrit en clair (CinéSéniors, CinéAnimés, Midi-documentaire, Avant-première). La couleur accélère le repérage pour ceux qui la voient ; elle n'est jamais le canal unique.

**La règle des deux rouges.** Le rouge du logo (`#D80000`) ne porte jamais de texte courant blanc : il est trop clair pour ça (5.36:1). Dès qu'une surface rouge doit porter du texte, c'est le rouge de fronton (`#B00000`, 7.38:1). Test d'audit : un aplat rouge avec du blanc dessus qui n'est pas `#B00000` est un défaut.

**La règle du bleu réservé.** Le bleu ne signifie qu'une chose sur ce site : le lieu CineXtra. Il n'habille pas un bouton, ne souligne pas un titre, ne colore pas une section. Si le bleu apparaît ailleurs que dans un badge de lieu, c'est une erreur.

**La règle du crème interdit.** Aucun fond crème, sable, beige, papier ou parchemin. La chaleur de cette marque vient des photos de la salle et de la voix, jamais d'un fond blanc teinté de jaune.

## 3. Typography

**Display Font:** Atkinson Hyperlegible Next (variable 400–800), auto-hébergée
**Body Font:** la même famille, poids inférieurs
**Label/Mono Font:** aucune. Pas de monospace ; ce n'est pas une marque technique.

**Character:** Atkinson Hyperlegible Next est dessinée par le **Braille Institute** dans un seul but : rester lisible pour les personnes malvoyantes. Ses lettres sont désambiguïsées une à une (le `1`, le `l` et le `I` ne se confondent pas, le `0` porte une contre-forme distincte du `O`, les apertures sont ouvertes). Ce n'est pas un choix décoratif : c'est le principe n°2 du projet (« lisible d'abord, et pour de vrai ») traduit en typographie, pour un public sénior prioritaire qui lit une grille horaire.

Elle est **auto-hébergée** dans `assets/fonts/` (53 Ko pour les deux sous-ensembles latin et latin-ext). Aucun appel au CDN Google : une ASBL belge n'envoie pas l'adresse IP de ses visiteurs à un tiers pour afficher une police.

La hiérarchie se fait par l'échelle et le poids (400 pour le courant, 600 pour les titres de section et les jours, 800 pour la bannière et les titres de film), pas par un second caractère.

### Hierarchy
- **Display** (800, `clamp()` plafonné à 6rem, interlettrage ≥ -0.03em, line-height ~1.0) : titre de bannière, uniquement. Un seul par page.
- **Headline** (800, environ 2 à 2.5rem) : titres de film dans la présentation détaillée.
- **Title** (600, environ 1.35 à 1.6rem) : titres de section, en-têtes de jour dans la grille.
- **Body** (400, **18px plancher**, line-height 1.55 à 1.65, longueur de ligne 65–75ch) : résumés de film, informations pratiques, tout le texte courant. Aucun texte informatif en dessous de 16px, y compris les mentions du pied de page.
- **Label** (600, environ 0.95rem, casse normale) : types de séance, lieux, tarifs. **Pas de petites capitales espacées.**

### Named Rules

**La règle des chiffres tabulaires.** `font-variant-numeric: tabular-nums` sur toute la grille horaire et sur les tarifs. Les colonnes d'heures doivent s'aligner verticalement au pixel ; un `18h15` qui ne s'aligne pas avec le `20h00` du dessous casse la lecture en un coup d'œil.

**La règle du plancher 18px.** Le corps de texte ne descend pas sous 18px, sur aucun écran. Ce n'est pas un réglage esthétique : c'est le public prioritaire, séniors inclus.

**La règle du sur-titre unique.** Pas de petite étiquette en majuscules espacées au-dessus de chaque section. Si un sur-titre existe, c'est un système de marque nommé et délibéré, appliqué une fois, pas une grammaire répétée à chaque bloc.

## 4. Elevation

**Plat par défaut.** Ce système ne construit pas sa profondeur avec des ombres. Elle vient de trois choses : les aplats de couleur (le bleu de salle contre le blanc franc), le trait franc (les filets de la grille, une bordure nette), et la photographie à fond perdu. Une page peut n'avoir aucune `box-shadow` et être parfaitement structurée : c'est même l'état attendu au repos.

L'ombre, si elle apparaît, est **une réponse à un état**, jamais un ornement au repos : un léger relief au survol d'une affiche, rien de plus. Énergie de mouvement retenue à « responsive » : les transitions servent le retour d'information.

### Named Rules

**La règle anti ghost-card.** Interdit de combiner `border: 1px solid` et une `box-shadow` large et diffuse (≥ 16px de flou) sur un même élément. On choisit : soit une bordure franche à la couleur de marque, soit une ombre définie de 8px de flou maximum. Jamais les deux comme décor.

**La règle du rayon court.** Cartes, sections et champs plafonnent à 12–16px de rayon. La pastille complète est réservée aux étiquettes et aux boutons. Un rayon de 24, 32 ou 40px sur une carte est un défaut, pas un style.

## 5. Components

**[Aucun composant à documenter : rien n'est encore construit.]** Cette section se remplit au prochain passage de `$impeccable document`, en mode scan, depuis le vrai code.

Un composant est déjà identifié comme signature et devra être documenté en premier : **la grille de programmation hebdomadaire**, en `<table>` sémantique (`<caption>`, `<th scope="col">` pour les films, `<th scope="row">` pour les jours), fond bleu de salle et blanc franc, chiffres tabulaires, jamais une image, jamais une grille CSS sans sémantique.

## 6. Do's and Don'ts

### Do:
- **Do** ancrer la palette sur le bleu du logo Cinémarche et tenir les quatre rôles nommés : bleu de salle (identité), rouge (exception datée), ocre (jeune public), neutres (lecture).
- **Do** écrire la grille hebdomadaire en HTML sémantique, jamais en image : « En html, pas en image (accessibilité) » est une contrainte du brief, pas une préférence.
- **Do** tenir un contraste ≥ 7:1 sur le texte courant et ≥ 4.5:1 partout ailleurs, y compris les libellés secondaires, les placeholders et les mentions du pied de page.
- **Do** doubler chaque code couleur d'un libellé écrit : le type de séance se lit, il ne se devine pas à la teinte.
- **Do** utiliser `font-variant-numeric: tabular-nums` sur tous les horaires et tarifs.
- **Do** garder le corps de texte à 18px minimum et vérifier la page à 200 % de zoom avant de la considérer terminée.
- **Do** montrer les vraies photos du lieu (`data/images/` : la salle, le public, la devanture du CineXtra, l'atelier CinéAnimés) et les vraies affiches des films.
- **Do** traiter les crédits comme de l'information : titre, réalisateur, année, durée.
- **Do** fournir une alternative `prefers-reduced-motion` pour chaque transition, sans exception.
- **Do** rendre le focus clavier franc et visible sur tous les éléments interactifs, avec des cibles tactiles ≥ 48px.

### Don't:
- **Don't** ressembler à un **site institutionnel communal** : pas de colonnes de liens gris, pas de programmation en PDF à télécharger, pas de bandeau administratif.
- **Don't** ressembler à un **multiplexe commercial** (Kinepolis, UGC) : pas de fond noir, pas de dégradés, pas de gros bouton « RÉSERVER », pas de bandeau promotionnel.
- **Don't** ressembler à une **plateforme de streaming** : pas de carrousel de vignettes à faire défiler, pas de rangs horizontaux. Une salle programme une sélection courte et datée, pas un catalogue.
- **Don't** ressembler à un **template SaaS lisse** : pas de grille de cartes identiques, pas d'icônes pastel dans des carrés arrondis, pas de sur-titre en petites majuscules espacées au-dessus de chaque section, pas d'ombres douces partout.
- **Don't** utiliser les dégradés fournis dans le brief (`$gradient-top`, `$gradient-radial` et les autres). Aucun dégradé décoratif, et jamais de dégradé sur du texte (`background-clip: text` est interdit).
- **Don't** poser un fond crème, sable, beige ou « papier ». Ni un fond bleu ciel pâle sous du texte gris.
- **Don't** choisir une typographie par réflexe : Inter, DM Sans, Plus Jakarta Sans, Instrument Sans, IBM Plex Sans, Space Grotesk, Outfit, Playfair Display, Fraunces, Cormorant sont écartées d'office. La famille se choisit dans un vrai catalogue, avec les critères ci-dessus.
- **Don't** utiliser de bordure latérale colorée de plus de 1px (`border-left` accent) sur une carte, une alerte ou un élément de liste.
- **Don't** dépasser 16px de rayon sur une carte, une section ou un champ.
- **Don't** poser d'illustration SVG « dessinée à la main », de trame de papier simulée, de rayures en `repeating-linear-gradient`. S'il n'y a pas d'image réelle disponible, il n'y a pas d'image.
- **Don't** imbriquer une carte dans une carte.
- **Don't** écrire de tiret cadratin dans les textes de l'interface, ni de superlatif promotionnel (« une expérience cinématographique unique », « incontournable »).
- **Don't** faire porter une information par la couleur seule, ni masquer du contenu derrière une animation de dévoilement déclenchée au défilement.
