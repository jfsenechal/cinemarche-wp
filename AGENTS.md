# AGENTS

Site officiel de **Cinémarche ASBL**, la salle de cinéma d'art et d'essai et culturelle de Marche-en-Famenne (partenaires : MCFA, Tiroir des Saveurs, CineXtra). Interface en français.

## Design Context

**Le design retenu est la version 2** (décision du porteur du projet, 10/11/2026). Ses fichiers ont été copiés à la racine du projet, où le travail se poursuit : [index.html](index.html) fait autorité pour le visuel. Voir la section « Design retenu : version 2 » plus bas. **La lire avant toute modification d'interface.**

**`sources/cinemarche-v1/` et `sources/cinemarche-v2/` sont en lecture seule** (dépôts GitHub d'origine, ignorés par git ici). Ne jamais y écrire, ni y lancer `npm install` ou un build. La v2 d'origine ne contient pas la mise à niveau d'accessibilité.

- **[PRODUCT.md](PRODUCT.md)** — registre, public, but du produit, personnalité de marque, anti-références, principes de conception, accessibilité. Toujours valable.
- **[DESIGN.md](DESIGN.md)** — système visuel de la v2, extrait du code le 10/11/2026 : palette, typographie, mise en page, composants, do's and don'ts. Fait autorité avec la maquette. Son complément pour les outils est `.impeccable/design.json`.

En résumé, pour ne pas avoir à deviner :

- **Registre : brand.** La page d'accueil est le produit ; le design porte l'identité, il ne se contente pas de servir un outil.
- **Public prioritaire : le public local large, séniors inclus.** Cible d'accessibilité : WCAG 2.2 AA partout, texte courant poussé à AAA (contraste ≥ 7:1), corps à 18px minimum, zoom 200 % sans casse.
- **Personnalité : chaleureux, exigeant, voisin.** On dit « nous », on donne les détails concrets, on ne fait pas de promotion.
- **Anti-références (les quatre) :** site institutionnel communal, multiplexe commercial, plateforme de streaming, template SaaS lisse.
- **Composant signature : la grille de programmation hebdomadaire**, en `<table>` sémantique. Jamais une image.
- **Le brief d'origine est dans [data/prompt-init.txt](data/prompt-init.txt)** ; les images préparées (logos, photos, affiches) sont dans `assets/img/`. Les photos brutes du lieu (44 Mo) n'ont pas été copiées : elles restent dans `sources/cinemarche-v2/data/images/`.

## Design retenu : version 2

Fichiers à la racine : `index.html`, tokens dans `src/css/app.css`, CSS compilé dans `assets/css/app.css`. Origine : `sources/cinemarche-v2/`. La version 1 (`sources/cinemarche-v1/`) est écartée ; ne pas s'en inspirer.

- **Technique : Tailwind CSS v4** via `@tailwindcss/cli`. `npm run build` compile `src/css/app.css` vers `assets/css/app.css`, `npm run dev` surveille, `npm run serve` sert sur le port 8777. HTML statique, pas de framework JS.
- **Couleurs** (définies dans `@theme`) :
  - `brand` : bleu du logo, couleur d'ambiance du site (`brand-500` `#2596be`). Boutons (`brand-600`), liens, focus.
  - `rouge` : rouge du logo (`rouge-600` `#c0161d`). Grille de programmation, sur-titres de section, horaires, étiquettes de séance.
  - `nuit` : noir de salle bleuté (`nuit-950` `#0a1720`). En-tête collant, bannière, bloc lettre d'info.
  - Neutres `zinc` de Tailwind sur fond blanc pour les zones de lecture.
- **Typographie :** Oswald (`font-display`, 500–600) pour les titres, sur-titres et horaires ; Inter variable (`font-sans`) pour le texte courant. Les deux sont auto-hébergées.
- **Structure de la page d'accueil :** en-tête sombre collant avec infobulles (menu `<details>` en mobile) → **phrase d'introduction** (« Depuis plus de 25 ans, … mais pas uniquement… ! », demandée par le porteur du projet le 12/11/2026, texte fourni par lui) → **grille de la semaine juste après** (décision du porteur du projet) → bannière sombre avec logo, titre (niveau 2 ; le `<h1>` de la page est en `sr-only` en tête de `<main>`), lien « Nos rendez-vous » (vers la pellicule) et montage « pellicule » des six ciné-clubs (utilitaire `film-perfs`) → « Nos Xtras » en cartes affiche → lettre d'info sur fond sombre → pied de page clair (partenaires, contact).
- **Menu** (décision du porteur du projet) : Accueil (`/`), À l'affiche, Nos rendez-vous, Nos Xtras, Archive, Contact. « Nos rendez-vous » mène à la pellicule des ciné-clubs dans la bannière (`id="rendez-vous"`). « Nos Xtras » mène à la section des films à venir en cartes affiche (`id="xtras"`, ancienne « Prochainement », puis « Nos rendez-vous » jusqu'au 12/11/2026). « Archive » pointe sur `#` en attendant son contenu, sans infobulle ni description ; à compléter quand la page existera.
- **Phrase d'introduction :** un seul `<p>` en trois temps, sur blanc, fermé par un filet fin. L'ouverture « Depuis plus de 25 ans, » en Oswald 600 `brand-800` (36 à 60px ; à partir de `lg`, à gauche sur trois lignes, séparée du reste par un filet vertical), le corps en Inter `zinc-800` (20 à 22px), la chute « mais pas uniquement… ! » sur sa ligne en Oswald 500 `rouge-600`. Pas de sur-titre, pas de fond coloré. Elle doit rester courte : la grille doit apparaître dans le premier écran. La marge haute de la section de la grille a été réduite pour cela (`pt-12 sm:pt-16`).
- **Pellicule des ciné-clubs** (décision du porteur du projet, 12/11/2026 : version « avec l'extrait » retenue) : six cases, dans l'ordre CinéAnimés, CinéSéniors, Midis-docus, Ciné-débats, CinéScolaires, CinéXtra. Chaque case est un lien entier (`href="#"` en attendant les pages) : photo en 3:2, titre en Oswald, extrait d'une phrase en `text-base` `zinc-300` sur `nuit-950`. Une colonne en mobile, deux à partir de `sm`, trois à partir de `lg`. Les textes viennent du porteur du projet (celui du CinéXtra a été raccourci à sa demande). Les photos sont provisoires, prises dans `assets/img/` faute de photos attitrées ; à remplacer quand elles existeront.
- **Grille de la semaine :** `<table>` sémantique à partir de `md` (films en colonnes avec affiche et titre sur fond rouge, jours en lignes, colonnes alternées `rouge-50`, première colonne collante, `tabular-nums`) ; sous `md`, liste par jour avec horaires en rouge et étiquettes en pastille.
- **Formes :** rayons `rounded-lg` (boutons, champs) et `rounded-2xl` (cartes, blocs), contours en `ring-1`, halo bleu flouté dans les zones sombres.

### Mise à niveau d'accessibilité (10/11/2026)

À la demande du porteur du projet, la copie de la v2 à la racine a été ramenée à la cible de PRODUCT.md. Ces réglages font partie du design ; ne pas revenir en arrière.

- **Polices auto-hébergées** dans `assets/fonts/` (Inter et Oswald variables, sous-ensemble latin). Plus aucun appel à rsms.me ni à Google Fonts.
- **Échelle de texte relevée** dans `@theme` : `text-sm` = 16px, `text-base` = 18px, `text-lg` = 20px, `text-xl` = 22px. Une phrase à lire est en `text-base` au moins ; `text-sm` est réservé aux libellés.
- **Contrastes :** le texte secondaire sur clair est en `zinc-600` (plus de `zinc-500`), sur sombre en `zinc-300` ; le bouton principal est en `brand-600` (le blanc sur `brand-500` ne passait pas).

- **Textes alternatifs des affiches :** descriptifs dans les cartes « Nos Xtras ». Dans l'en-tête de la grille, la miniature garde volontairement `alt=""` : le titre du film est écrit juste en dessous, et un lecteur d'écran répète l'en-tête de colonne à chaque case.
- **Bouton du menu mobile :** 48px de côté, avec un contour de focus.

## État du projet

La page d'accueil existe à la racine (copie de la v2, mise à niveau pour l'accessibilité). `npm install` puis `npm run build` après toute modification de `index.html` ou de `src/css/app.css`. Les autres pages restent à faire.
