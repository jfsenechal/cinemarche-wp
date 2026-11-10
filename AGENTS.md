# AGENTS

Site officiel de **Cinémarche ASBL**, la salle de cinéma d'art et d'essai et culturelle de Marche-en-Famenne (partenaires : MCFA, Tiroir des Saveurs, CineXtra). Interface en français.

## Design Context

Deux fichiers à la racine font autorité. **Les lire avant toute modification d'interface.**

- **[PRODUCT.md](PRODUCT.md)** — registre, public, but du produit, personnalité de marque, anti-références, principes de conception, accessibilité.
- **[DESIGN.md](DESIGN.md)** — système visuel : palette, typographie, élévation, composants, do's and don'ts. Actuellement un **seed** (le projet n'a pas encore de code) ; à régénérer en mode scan une fois le CSS réel en place.

En résumé, pour ne pas avoir à deviner :

- **Registre : brand.** La page d'accueil est le produit ; le design porte l'identité, il ne se contente pas de servir un outil.
- **Public prioritaire : le public local large, séniors inclus.** Cible d'accessibilité : WCAG 2.2 AA partout, texte courant poussé à AAA (contraste ≥ 7:1), corps à 18px minimum, zoom 200 % sans casse.
- **Personnalité : chaleureux, exigeant, voisin.** On dit « nous », on donne les détails concrets, on ne fait pas de promotion.
- **Anti-références (les quatre) :** site institutionnel communal, multiplexe commercial, plateforme de streaming, template SaaS lisse.
- **Composant signature : la grille de programmation hebdomadaire**, en `<table>` sémantique. Jamais une image.
- **Le brief d'origine est dans [data/prompt-init.txt](data/prompt-init.txt)** ; les photos du lieu, les logos et les exemples de grille sont dans `data/images/`.

## État du projet

Aucun code applicatif pour l'instant. Base technique retenue : **HTML/CSS statique d'abord**, sans build, à commencer par la page d'accueil.
