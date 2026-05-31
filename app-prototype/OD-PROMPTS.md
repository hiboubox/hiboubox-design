# HIBOUBOX App — prompts OD (un par écran)

> Projet OD unique, design system **HIBOUBOX** actif, skill **`mobile-app`**.
> Génère un écran par session. Voir [APP-SPEC.md](APP-SPEC.md) pour la trame.
> Mets à jour le statut dans APP-SPEC.md §5 après chaque écran.

Les écrans II→VII commencent par la **ligne de cohérence** :
*« Reprends exactement le cadre iPhone, la tab bar et l'échelle typo de l'écran
Accueil déjà dans ce projet. »*

---

## Nº I — ACCUEIL  *(session 1 — le gabarit de référence)*

```
Écran « ACCUEIL » de l'app mobile HIBOUBOX, cadré dans un iPhone 15 Pro
(390×844 : encoche, status bar, home indicator). Applique le design system
HIBOUBOX en version mobile (fond ink, texte cream, accent ORANGE max 2/écran,
Bungee display, Special Elite mono pour dates/prix, eyebrows Barlow 0.22em,
cadres « tampon postal » orange + corner ticks, copy FR sobre, cibles ≥ 44px,
aucune image externe → placeholders). Cet écran SERT DE GABARIT aux suivants :
soigne le cadre device et la tab bar.

TAB BAR en bas (5 onglets, « Accueil » actif en orange + marqueur picto-chouette,
autres cream 60 %, icônes line-art) : Accueil · Programmation · Menus · Infos ·
Réserver.

Contenu vertical :
1. Bandeau « InfoLive » pleine largeur (fond ink-1000, point orange pulsant +
   texte mono) : « ◉ OUVERT · CONCERT CE SOIR 20H30 ». (Affordance UI.)
2. Hero « Prochain concert » = card featured avec HALO orange pulsant + cadre
   tampon : eyebrow « ◉ JAZZ MANOUCHE · VERCORS », titre Bungee « TRIO MARLOWE »
   (MARLOWE en accent orange), datetime mono « VEN 17 MAI · 20H30 », stamp
   « ◉ ENTRÉE LIBRE ». (Tap → détail concert.)
3. Card « Exposition en cours » : eyebrow « ◉ SUR NOS MURS », titre œuvre, nom
   artiste, placeholder visuel, petit CTA « Découvrir ».
4. Bloc « message d'ambiance » : citation Cormorant italique pleine largeur
   « le voyage commence à table », guillemet orange géant en filigrane.
5. CTA primary pleine largeur « → Réserver une table ».

Accent orange = halo du hero + CTA (2 max). Coord badge ◉ 45°04′N · 5°33′E
discret. Cartouche « Nº I » bas-droite.
```

---

## Nº II — PROGRAMMATION

```
Reprends exactement le cadre iPhone, la tab bar et l'échelle typo de l'écran
Accueil déjà dans ce projet. Écran « PROGRAMMATION », tab bar onglet
« Programmation » actif.

Header : eyebrow « ◉ L'AGENDA À VENIR », titre Bungee « PORTÉE · NAVIGATION »
(NAVIGATION accent orange), décor portée musicale + clé de sol 𝄞 en filigrane.

Liste de 5 concerts (cards boarding-pass cliquables → Détail) : badge date mono
« VEN 17 MAI », eyebrow genre, titre artiste Bungee 22px (1 mot accent), meta
mono « 20H30 · ENTRÉE LIBRE », chevron ↗.
Données : VEN 17 Trio Marlowe (manouche) · SAM 18 Quartet Ribérol (moderne) ·
DIM 19 Jam Session (scène ouverte · 19H30) · VEN 24 Duo Margaux (chanson FR) ·
SAM 25 Céline & Groupe (folk).

Accent orange ≤ 2. Cartouche « Nº II » bas-droite.
```

---

## Nº III — DÉTAIL CONCERT  *(SANS tab bar)*

```
Reprends exactement le cadre iPhone et l'échelle typo de l'écran Accueil, mais
SANS tab bar (écran poussé en stack). Header avec chevron retour « ‹ ».

1. Visuel affiche plein cadre (placeholder) + cadre tampon (outline solid orange
   + dashed offset + 4 corner ticks) + stamp intégré top-right rotated -6°
   « ◉ DANS 3 JOURS ».
2. Eyebrow « ◉ JAZZ MANOUCHE · VERCORS ».
3. Titre Bungee « TRIO MARLOWE » (MARLOWE accent orange).
4. Script Cormorant italique « guitare · contrebasse · violon ».
5. Datetime stamp centré (cadre tampon) : « VEN 17 MAI » / « 20H30 → 22H30 » /
   mono « ◉ DEUX SETS · ENTRÉE LIBRE · PRIX LIBRE ».
6. Description : 2-3 phrases sobres (voix HIBOUBOX).
7. Bouton PRIMARY pleine largeur « → Être notifié » (au tap : état abonné
   « ◉ Vous serez prévenu le jour J »).
8. Bouton outline « → Ajouter à l'agenda ».

Accent orange = datetime stamp + bouton « Être notifié » (2). Cartouche « Nº III ».
```

---

## Nº IV — MENUS · CHOIX

```
Reprends exactement le cadre iPhone, la tab bar et l'échelle typo de l'Accueil.
Écran « MENUS — CHOIX », tab bar onglet « Menus » actif. Archétype Focus.

Header : eyebrow « ◉ NOTRE CARTE », titre Bungee « SUR PLACE OU EMPORTER ? ».
Deux grandes cartes de choix empilées (≥ 88px, pleine largeur) :
1. « SUR PLACE » — icône line-art assiette, sous-texte « cuisine du monde, servie
   à table », cadre tampon. (Tap → liste menu Sur place.)
2. « À EMPORTER » — icône line-art sac kraft, sous-texte « sandwichs, bowls, à
   récupérer », cadre tampon. (Tap → liste menu Emporter.)
Note mono dessous : « ◉ Scannez le QR sur votre table pour ouvrir le menu
directement » (affordance deep-link).

Accent orange ≤ 2. Rose des vents en coin. Cartouche « Nº IV · CARTA ».
```

---

## Nº V — MENU SUR PLACE (liste)

```
Reprends exactement le cadre iPhone, la tab bar et l'échelle typo de l'Accueil.
Écran « MENU SUR PLACE », tab bar onglet « Menus » actif. (Atterrissage du
deep-link QR table.)

En haut : sous-onglets catégories scrollables horizontaux, icônes line-art :
Tapas · Woks · Currys · Salades · Desserts · Vins · Bières (« Woks » actif orange,
autres cream 60 %). Chips filtres régime (Végé · Sans gluten), toggle actif orange.

Liste d'items de la catégorie active : « nom du plat …… (dot-leaders) prix mono
16,00 € » (.num tabular) + courte description cream muted. Stamp origine pays en
filigrane gold (opacity 0.5) derrière la catégorie : « ◉ THAÏLANDE ».
Exemples (Woks) : Wok bœuf basilic thaï 16,00 € · Pad thaï crevettes 17,50 € ·
Wok légumes & tofu fumé 14,00 €.

Accent orange ≤ 2. Cartouche « Nº V · TERRA · GASTRONOMICA ».
```

---

## Nº VI — INFOS

```
Reprends exactement le cadre iPhone, la tab bar et l'échelle typo de l'Accueil.
Écran « INFOS », tab bar onglet « Infos » actif. Archétype Profile (sections).

Section 1 « VENIR » (eyebrow « ◉ SE RENDRE À HIBOUBOX ») : bloc adresse encadré
dashed « 41 rue des Pionniers » (Cormorant 24px) / « 38250 · Villard-de-Lans » /
mono « ◉ 45°04′N · 5°33′E · ALT 1050 M » ; widget carte (grille cartographique +
pin orange) → « Ouvrir dans Google Maps » ; liste k/v mono : Horaires « Mar → Dim
· 18-22h » · Concerts « 20h30 · entrée libre » · Happy hour « 16h → 18h · -20% ».

Section 2 « NOUS CONTACTER » (eyebrow « ◉ VIA · LITTERIS ») : pill ☎ « 04 56 00
09 56 » · pill « contact@hiboubox.fr » · rangée Instagram · Facebook line-art ·
petit CTA « → Nous écrire ».

Accent orange ≤ 2 (un/section). Cartouche « Nº VI · PORTUS · DOMUS ».
```

---

## Nº VII — RÉSERVER

```
Reprends exactement le cadre iPhone, la tab bar et l'échelle typo de l'Accueil.
Écran « RÉSERVER », tab bar onglet « Réserver » actif. Archétype Focus.

WebView CoverManager habillée en « cadre passport encastré » :
- topstrip orange « ◉ RÉSERVATION · COVERMANAGER »,
- grand cadre (1.5px solid orange + outline dashed offset + 4 corner ticks),
  fond ink-1000, avec un MOCK de formulaire de réservation (date · couverts ·
  créneau · nom) — pas le vrai widget,
- état de chargement discret « chargement de la réservation… » en mono,
- foot note Cormorant italique « réservation sécurisée via CoverManager · widget
  tiers habillé en prod ».

Accent orange ≤ 2 (topstrip + cadre). Cartouche « Nº VII · VIA · REGULAE ».
```
