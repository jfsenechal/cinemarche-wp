# Product

## Register

brand

## Users

**Le public local de Marche-en-Famenne et de la Famenne-Ardenne**, qui consulte le site depuis chez lui, souvent le matin ou en début de soirée, pour décider s'il sort ce soir ou dans la semaine. Trois profils se superposent :

- **Le public large, séniors inclus** — profil prioritaire dans les arbitrages. Beaucoup arrivent via un partage Facebook ou un lien envoyé par un proche, parfois sur un téléphone tenu à bout de bras, parfois sur un écran avec le zoom navigateur poussé. CinéSéniors est un pilier de la programmation, pas une niche.
- **Les habitués art et essai**, qui viennent vérifier ce qui passe, repérer les avant-premières et les Midis-documentaires, et savoir s'il y a un débat après la séance.
- **Les familles et les écoles**, qui cherchent les séances jeune public et les CinéAnimés, et pour les enseignants une information organisable à l'avance.

Le travail à accomplir, dans l'ordre : **savoir ce qui passe et quand**, puis **savoir où** (CinéXtra ou le Tiroir des Saveurs), puis **avoir envie**. Un visiteur qui repart sans avoir trouvé l'heure de sa séance est un échec, quelle que soit la beauté de la page.

## Product Purpose

cinemarche.marche.be est la plateforme officielle d'information et de programmation de **Cinémarche ASBL**, qui gère le cinéma d'art et d'essai et culturel de Marche-en-Famenne, en partenariat avec la Maison de la Culture Famenne-Ardenne (MCFA), le Tiroir des Saveurs et le CinéXtra.

Le site porte :

- la **programmation de la semaine** sous forme de grille horaire consultable d'un coup d'œil, en HTML et non en image ;
- la **programmation à venir** (« Prochainement ») ;
- les **séances thématiques** : Midis-documentaires, CinéSéniors, CinéAnimés, avant-premières et événements spéciaux ;
- les **informations pratiques** : lieux, tarifs, abonnements, contact ;
- l'**inscription à la lettre d'info**.

Le but de l'ASBL est de rendre un cinéma de qualité accessible à tous. Le site réussit quand un habitant qui n'a jamais entendu parler de Cinémarche comprend en dix secondes qu'il y a une vraie salle culturelle à Marche, et qu'un habitué trouve son horaire sans faire défiler.

Première étape du projet : **la page d'accueil**. Le reste des pages suivra.

## Brand Personality

**Chaleureux, exigeant, voisin.**

Un cinéma tenu par des gens qui connaissent leur public, et qui ne bradent pas pour autant la sélection. La voix est celle d'une personne qui vous parle, pas celle d'une institution qui communique.

- **On dit « nous »**, on nomme les animateurs et les partenaires, on donne les détails concrets : l'heure, le prix, si le repas est compris, s'il y a un débat après.
- **On respecte le film** : titre, réalisateur, année, durée, affiche d'origine. Les crédits font partie de l'information, pas de la décoration.
- **Le lieu existe** : la salle, l'écran, le public dans les sièges, la devanture du CinéXtra, les ateliers. Ce sont de vraies photos d'un vrai endroit à Marche.
- **Émotion visée** : l'envie de sortir de chez soi un mercredi soir, et le sentiment que c'est *notre* salle.

Interdits de voix : le superlatif promotionnel (« une expérience cinématographique unique », « incontournable »), le vocabulaire marketing, le ton neutre de communiqué, la formule creuse à la place d'un horaire.

## Anti-references

Les quatre à éviter explicitement, toutes retenues par le porteur du projet :

1. **Le site institutionnel communal.** Bandeau administratif, colonnes de liens gris, PDF à télécharger pour connaître la programmation, aucune hiérarchie. C'est le piège naturel d'un site hébergé en `.marche.be` ; c'est exactement ce qu'il ne faut pas être.
2. **Le multiplexe commercial** (Kinepolis, UGC). Fond noir, dégradés, gros boutons « RÉSERVER », bandeaux promotionnels, tout crie en même temps. Cinémarche n'est pas un point de vente.
3. **La plateforme de streaming.** Carrousels de vignettes à l'infini, rangs horizontaux à faire défiler, esthétique Netflix. Une salle programme une sélection courte et datée ; ce n'est pas un catalogue.
4. **Le template SaaS lisse.** Grilles de cartes identiques à coins très arrondis, icônes pastel, sur-titres en petites majuscules espacées au-dessus de chaque section, ombres douces partout. Le rendu « fait par une IA » est un échec de marque.

## Design Principles

1. **La séance avant tout le reste.** Quoi, quand, où : cette information gagne contre n'importe quelle intention graphique. La grille hebdomadaire est le cœur fonctionnel de la page d'accueil et doit rester lisible d'un coup d'œil, sans interaction préalable.
2. **Lisible d'abord, et pour de vrai.** L'accessibilité est une contrainte de conception, jamais un correctif de fin de projet. Si un choix visuel coûte de la lisibilité au public sénior, c'est le choix visuel qui cède.
3. **Signé par des humains.** Des noms, une voix à la première personne du pluriel, des détails vérifiables. Rien d'anonyme, rien de générique.
4. **Le lieu et les films sont fournis, pas inventés.** On montre les vraies photos de la salle et les vraies affiches des films. Un bloc de couleur ou une illustration décorative à la place d'une image réelle est un défaut, pas une option.
5. **Association, pas commerce.** Le ton, la densité et les appels à l'action sont ceux d'un acteur culturel local : on invite, on explique, on ne convertit pas.

## Accessibility & Inclusion

Cible : **WCAG 2.2 niveau AA comme plancher sur tous les critères, avec le texte courant poussé à AAA** (contraste ≥ 7:1) en raison du public sénior.

Exigences concrètes :

- Contraste ≥ 7:1 pour le texte courant, ≥ 4.5:1 sans exception pour tout le reste, y compris les libellés secondaires et les textes d'aide (jamais de gris clair « pour l'élégance »).
- Corps de texte à 17–18px minimum, et le zoom navigateur à 200 % ne doit rien casser ni rien tronquer.
- La grille de programmation est un **vrai tableau HTML** (`<table>`, `<th scope>`, `<caption>`), navigable au clavier et annonçable par un lecteur d'écran. Jamais une image, jamais une grille CSS sans sémantique.
- Aucune information portée par la seule couleur : le type de séance (CinéSéniors, CinéAnimés, Midi-documentaire, avant-première) est toujours écrit, pas seulement teinté.
- Cibles tactiles ≥ 48px, focus visible et net sur tous les éléments interactifs.
- `prefers-reduced-motion` traité comme obligatoire : chaque animation a une alternative (fondu ou transition instantanée).
- Textes alternatifs descriptifs sur les photos du lieu et les affiches (l'alt fait partie de la voix : « Le public de CinéSéniors dans la salle, bulletins de vote en main » plutôt que « photo salle »).
- Site en français ; `lang="fr"` et aucune dépendance à des libellés anglais dans l'interface.
