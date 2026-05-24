---
version: alpha
name: HIBOUBOX
description: >
  Brand book et système de design pour HIBOUBOX — restaurant-concert-bar-galerie
  à Villard-de-Lans (Vercors). Esthétique vintage jazz club × carte ancienne ×
  passeport × cuisine du monde. Palette ink profond × orange laiton × cream
  parchemin avec or filigrane. Tagline « le voyage commence à table ». Inclut
  la sous-marque Le Festin du Hibou (activité traiteur, accent doré).

# ============================================================
# COLORS — palette exhaustive
# Tokens nommés par fonction (ink/cream/orange/gold/olive/paper/warm)
# avec scale numérique. Référencer via {colors.token} dans les composants.
# ============================================================
colors:
  # Backgrounds — dark taupe / warm grey (jamais froid)
  ink-1000: "#0a0908"           # deepest — full bleed (Footer)
  ink-900:  "#16140f"           # page background default
  ink-800:  "#211e19"           # raised surface, header
  ink-700:  "#2d2925"           # card surface on dark
  ink-600:  "#3a3530"           # hover surface, borders
  ink-500:  "#4a4540"           # divider, muted border

  # Cream / paper — texte sur fond sombre + supports print
  cream-50:   "#faf3e2"         # primary text on ink
  cream-100:  "#f0e6ce"         # body text on ink (default)
  warm-300:   "#c2b39a"         # secondary muted on ink
  warm-500:   "#897a63"         # disabled only — WCAG-exempté (4.41:1, non-conforme si texte actif)
  paper-100:  "#f5ecd6"         # warm cream — fond print clair
  paper-200:  "#e8dcc0"         # paper aged
  paper-300:  "#d6c79e"         # paper darker / kraft

  # Text on paper/cream (3 niveaux de hiérarchie)
  on-paper-1: "#1a1108"
  on-paper-2: "#4a3422"
  on-paper-3: "#7a5b3f"

  # Primary — Orange (stage light, candle flame, logo)
  orange-300: "#f5b074"         # hover soft
  orange-400: "#ea934a"         # hover state primary
  orange-500: "#d97a2a"         # PRIMARY — accent unique CTAs
  orange-600: "#b35e1a"         # pressed / deep
  orange-700: "#7e3f10"         # darkest, sur fond cream

  # Gold — accent secondaire cartographique, filigrane stamps
  # ⚠ Réservé : stamps origines pays + grammaire Festin du Hibou.
  # Ne PAS utiliser comme accent UI général (orange-500 garde ce rôle).
  gold-400: "#d4af5a"
  gold-500: "#b88f3a"

  # Olive / mustard — ink de poster vintage (usage rare, alternative)
  olive-400: "#a8b04a"
  olive-500: "#818825"          # SECONDARY CTA (variant Btn.olive)
  olive-600: "#5e6519"

  # Semantic — états système (admin, forms)
  success:    "#6f8a3e"
  success-bg: "#2a3318"
  warning:    "#d4a13a"
  danger:     "#d85535"         # corrigé WCAG AA (#c14f2c était 3.88:1 → FAIL)
  danger-bg:  "#3a1612"
  info:       "#6b8aa8"

  # Interaction aliases (dérivés)
  primary:          "{colors.orange-500}"
  primary-hover:    "{colors.orange-400}"
  primary-pressed:  "{colors.orange-600}"
  primary-disabled: "#6a4824"
  primary-fg:       "#1a0e04"   # texte sur orange (lisible)
  secondary:        "{colors.olive-500}"
  secondary-hover:  "{colors.olive-400}"
  secondary-pressed:"{colors.olive-600}"
  secondary-fg:     "#0f1404"

# ============================================================
# TYPOGRAPHY — 6 familles, rôles spécialisés
# ============================================================
typography:
  fontFamilies:
    display: '"Bungee", "Bowlby One", "Ultra", "Arial Black", sans-serif'
    poster:  '"Rubik Wet Paint", "Bowlby One", "Arial Black", sans-serif'
    serif:   '"Cormorant Garamond", "EB Garamond", Georgia, serif'
    body:    '"Lato", "Source Sans 3", -apple-system, BlinkMacSystemFont, "Segoe UI", system-ui, sans-serif'
    label:   '"Barlow Condensed", "Oswald", "Arial Narrow", sans-serif'
    stamp:   '"Special Elite", "Courier Prime", "Courier New", monospace'

  scale:
    display-xl:
      fontFamily: "{typography.fontFamilies.display}"
      fontSize:    "92px"
      lineHeight:  "0.9"
      letterSpacing: "-0.01em"
      textTransform: "uppercase"
      color: "{colors.cream-50}"
    display-lg:
      fontFamily: "{typography.fontFamilies.display}"
      fontSize:    "64px"
      lineHeight:  "0.92"
      letterSpacing: "-0.005em"
      textTransform: "uppercase"
      color: "{colors.cream-50}"
    display-md:
      fontFamily: "{typography.fontFamilies.display}"
      fontSize:    "44px"
      lineHeight:  "1.05"
      letterSpacing: "-0.005em"
      textTransform: "uppercase"
      color: "{colors.cream-50}"
    poster-xl:
      fontFamily: "{typography.fontFamilies.poster}"
      fontSize:    "120px"
      lineHeight:  "0.92"
      letterSpacing: "-0.005em"
      textTransform: "uppercase"
    script-lg:
      fontFamily: "{typography.fontFamilies.serif}"
      fontSize:    "60px"
      fontStyle:   "italic"
      fontWeight:  500
      color: "{colors.cream-100}"
    script-md:
      fontFamily: "{typography.fontFamilies.serif}"
      fontSize:    "34px"
      fontStyle:   "italic"
      fontWeight:  600
    script-sm:
      fontFamily: "{typography.fontFamilies.serif}"
      fontSize:    "22px"
      fontStyle:   "italic"
      fontWeight:  500
    h3:
      fontFamily: "{typography.fontFamilies.display}"
      fontSize:    "28px"
      lineHeight:  "1.05"
      textTransform: "none"
    h4:
      fontFamily: "{typography.fontFamilies.display}"
      fontSize:    "22px"
      textTransform: "none"
    lead:
      fontFamily: "{typography.fontFamilies.body}"
      fontSize:    "20px"
      lineHeight:  "1.55"
      fontWeight:  500
      color: "{colors.cream-50}"
    body:
      fontFamily: "{typography.fontFamilies.body}"
      fontSize:    "16px"
      lineHeight:  "1.55"
      fontWeight:  400
      color: "{colors.cream-100}"
    small:
      fontFamily: "{typography.fontFamilies.body}"
      fontSize:    "14px"
      lineHeight:  "1.55"
    micro:
      fontFamily: "{typography.fontFamilies.body}"
      fontSize:    "12px"
    eyebrow-hero:
      fontFamily: "{typography.fontFamilies.label}"
      fontSize:    "22px"
      letterSpacing: "0.22em"
      textTransform: "uppercase"
      fontWeight:  600
      color: "{colors.orange-400}"
    eyebrow-section:
      fontFamily: "{typography.fontFamilies.label}"
      fontSize:    "19px"
      letterSpacing: "0.22em"
      textTransform: "uppercase"
      fontWeight:  600
      color: "{colors.orange-400}"
    eyebrow-card:
      fontFamily: "{typography.fontFamilies.label}"
      fontSize:    "13px"
      letterSpacing: "0.22em"
      textTransform: "uppercase"
      fontWeight:  600
      color: "{colors.orange-500}"
    stamp:
      fontFamily: "{typography.fontFamilies.stamp}"
      fontSize:    "10px"
      letterSpacing: "0.12em"
      textTransform: "uppercase"
      color: "{colors.orange-500}"
    coord:
      fontFamily: "{typography.fontFamilies.stamp}"
      fontSize:    "13px"
      letterSpacing: "0.16em"
      textTransform: "uppercase"
      color: "{colors.orange-400}"

# ============================================================
# SPACING — base 4px
# ============================================================
spacing:
  sp-0:  "0"
  sp-1:  "4px"
  sp-2:  "8px"
  sp-3:  "12px"
  sp-4:  "16px"
  sp-5:  "24px"
  sp-6:  "32px"
  sp-7:  "48px"
  sp-8:  "64px"
  sp-9:  "96px"
  sp-10: "128px"
  section-y-desktop: "100px"
  section-y-mobile:  "56px"
  content-pad-x:     "clamp(20px, 4vw, 64px)"

# ============================================================
# SHAPES — radii souples, candle-soft
# ============================================================
rounded:
  none:  "0"
  xs:    "2px"
  sm:    "4px"
  md:    "8px"
  lg:    "16px"
  xl:    "24px"
  full:  "999px"
  blob:  "48% 52% 60% 40% / 55% 45% 55% 45%"  # owl-silhouette

# ============================================================
# ELEVATION — shadows warm + glows stage-light
# ============================================================
elevation:
  shadow-sm:    "0 1px 2px rgba(0,0,0,.4)"
  shadow-md:    "0 6px 24px rgba(0,0,0,.55)"
  shadow-lg:    "0 24px 60px rgba(0,0,0,.7)"
  glow-orange:  "0 0 40px rgba(217,122,42,.35)"
  glow-stage:   "0 -30px 80px rgba(217,122,42,.25) inset"

# ============================================================
# LAYOUT — containers & breakpoints
# ============================================================
layout:
  container-max:    "1280px"
  container-narrow: "880px"
  hit-target:       "44px"
  artboard-desktop: "1440px"
  artboard-mobile:  "390px"

# ============================================================
# BORDERS — niveaux d'opacité orange/cream
# ============================================================
borders:
  faint:  "1px solid rgba(245,236,214,.08)"
  soft:   "1px solid rgba(245,236,214,.14)"
  line:   "1px solid rgba(245,236,214,.22)"
  cream:  "1px solid {colors.paper-300}"
  orange-soft:   "1px dashed rgba(217,122,42,.35)"
  orange-strong: "1.5px solid {colors.orange-500}"
  orange-gold:   "1.5px solid {colors.gold-400}"

# ============================================================
# ANIMATION — durations et easings
# ============================================================
animation:
  fade-in:     "0.8s ease both"
  hover-link:  "0.18s ease"
  hover-card:  "0.25s ease"
  halo-pulse:  "4.5s ease-in-out infinite"
  drawer-slide:"0.32s cubic-bezier(0.35, 0, 0.25, 1)"
  reduced-motion-fallback: true

# ============================================================
# COMPONENTS — primitives canoniques
# Spec exhaustive : voir section markdown Components ci-dessous.
# ============================================================
components:
  button-primary:
    fontFamily: "{typography.fontFamilies.label}"
    fontSize: "12px"
    fontWeight: 700
    letterSpacing: "0.18em"
    textTransform: "uppercase"
    padding: "11px 18px"
    rounded: "{rounded.full}"
    backgroundColor: "{colors.orange-500}"
    border: "1.5px solid {colors.orange-500}"
    textColor: "{colors.primary-fg}"
  button-primary-hover:
    backgroundColor: "{colors.orange-400}"
    borderColor: "{colors.orange-400}"
  button-outline:
    fontFamily: "{typography.fontFamilies.label}"
    fontSize: "12px"
    fontWeight: 600
    letterSpacing: "0.18em"
    textTransform: "uppercase"
    padding: "11px 18px"
    rounded: "{rounded.full}"
    backgroundColor: "transparent"
    border: "1.5px solid {colors.cream-100}"
    textColor: "{colors.cream-100}"
  button-outline-hover:
    backgroundColor: "rgba(240,230,206,.08)"
    borderColor: "{colors.orange-400}"
    textColor: "{colors.orange-300}"
  button-gold:
    fontFamily: "{typography.fontFamilies.label}"
    fontSize: "12px"
    fontWeight: 700
    letterSpacing: "0.18em"
    textTransform: "uppercase"
    padding: "11px 18px"
    rounded: "{rounded.full}"
    backgroundColor: "{colors.gold-400}"
    border: "1.5px solid {colors.gold-400}"
    textColor: "{colors.primary-fg}"
    usage: "Réservé sous-marque Le Festin du Hibou (traiteur)."
  button-xl:
    fontFamily: "{typography.fontFamilies.label}"
    fontSize: "17px"
    fontWeight: 700
    letterSpacing: "0.16em"
    textTransform: "uppercase"
    padding: "20px 36px"
    rounded: "{rounded.full}"
    backgroundColor: "{colors.orange-500}"
    border: "1.5px solid {colors.orange-500}"
    textColor: "{colors.primary-fg}"
  button-incard:
    fontFamily: "{typography.fontFamilies.label}"
    fontSize: "18px"
    fontWeight: 700
    letterSpacing: "0.16em"
    textTransform: "uppercase"
    padding: "16px 20px"
    width: "100%"
    rounded: "{rounded.full}"
    backgroundColor: "{colors.orange-500}"
    border: "1.5px solid {colors.orange-500}"
    textColor: "{colors.primary-fg}"
    note: "Min 18px desktop / 15px mobile, weight 700 — règle stricte"
  card:
    backgroundColor: "{colors.ink-700}"
    border: "1px solid rgba(217,122,42,.15)"
    rounded: "{rounded.md}"
    padding: "{spacing.sp-5}"
  card-hover:
    transform: "translateY(-4px)"
    borderColor: "rgba(217,122,42,.5)"
    shadow: "0 12px 40px rgba(0,0,0,.5), 0 0 30px rgba(217,122,42,.15)"
  card-featured:
    backgroundColor: "{colors.ink-700}"
    border: "1px solid rgba(217,122,42,.45)"
    rounded: "{rounded.md}"
    padding: "{spacing.sp-5}"
    boxShadow: >
      0 0 0 1px rgba(217,122,42,.25),
      0 0 28px 2px rgba(217,122,42,.18),
      0 0 70px 12px rgba(217,122,42,.10)
    animation: "{animation.halo-pulse}"
    note: >
      Halo pulsant in-place — JAMAIS transporter l'item en tête, JAMAIS ribbon
      en haut. L'item reste à sa position naturelle dans la liste.
  stamp:
    fontFamily: "{typography.fontFamilies.stamp}"
    fontSize: "10px"
    letterSpacing: "0.12em"
    textTransform: "uppercase"
    padding: "4px 8px"
    border: "1.5px solid {colors.orange-500}"
    rounded: "{rounded.xs}"
    backgroundColor: "rgba(245,176,116,.05)"
    color: "{colors.orange-500}"
    transform: "rotate(-5deg)"
  badge:
    fontFamily: "{typography.fontFamilies.label}"
    fontSize: "10px"
    letterSpacing: "0.18em"
    textTransform: "uppercase"
    padding: "4px 9px"
    border: "1px solid {colors.orange-500}"
    rounded: "{rounded.full}"
    backgroundColor: "rgba(217,122,42,.1)"
    color: "{colors.orange-400}"
  eyebrow:
    fontFamily: "{typography.fontFamilies.label}"
    fontSize: "18px"
    letterSpacing: "0.18em"
    textTransform: "uppercase"
    fontWeight: 800
    color: "{colors.orange-400}"
    marginBottom: "{spacing.sp-5}"

# ============================================================
# ASSETS — chemins relatifs (proto + future intégration prod)
# ============================================================
assets:
  logos:
    full:        "assets/logo-full-orange.png"
    wordmark:    "assets/wordmark-orange.png"
    picto:       "assets/picto-owl-orange.png"
    stamp:       "assets/hiboubox-stamp-logo.png"
    festin:      "assets/festin-du-hibou-black.png"
  signature-svg:
    compass-rose:      "assets/compass-rose.svg"
    world-map:         "assets/world-map.svg"
    coord-stamp:       "assets/coord-stamp.svg"
    stamp-vercors:     "assets/stamp-vercors.svg"
    stamp-entree:      "assets/stamp-entree-libre.svg"
    stamp-par-avion:   "assets/stamp-par-avion.svg"
  origins:
    folder:           "assets/origins/"
    folder-vins:      "assets/origins/vins/"
    count-countries:  60
    count-vins:       15
    format:           "ovale 140×80 viewBox SVG"
    recolor-method:   "filter chain (PAS mask-image — voir Don'ts)"
  tabs:
    folder:    "assets/tabs/"
    count:     15
    style:     "line-art stroke 1.4-1.6"

# ============================================================
# BRAND IDENTITY
# ============================================================
brand:
  legal:        "HibouJazz SARL"
  address:      "41 rue des Pionniers, 38250 Villard-de-Lans"
  phone:        "04 56 00 09 56"
  email-main:   "contact@hiboubox.fr"
  coordinates:  "45°04′N · 5°33′E"
  tagline:      "le voyage commence à table"
  edition:      "ÉD. MMXXIV"
  values:
    - "10 % HT reversés aux artistes · pas un geste ponctuel, un choix structurel"
    - "Accueil exclusivement à table (jamais debout, bar inclus)"
    - "Cuisine internationale faite maison, tout cuit à la minute"
    - "Une scène vivante : 5-6 soirs/semaine en saison"
  sub-brands:
    festin-du-hibou:
      name:     "Le Festin du Hibou"
      type:     "Activité traiteur · même structure juridique HibouJazz SARL"
      accent:   "{colors.gold-400}"
      email:    "contact@lefestinduhibou.fr"
      logo:     "{assets.logos.festin}"
      note:     "Même site web, inbox dédiée. Grammaire visuelle = HIBOUBOX + accent gold remplaçant l'orange."
---

# HIBOUBOX — Brand book & système de design

> Document de référence pour la création de tous supports HIBOUBOX :
> web, print, signalétique, réseaux sociaux, packaging, supports presse.
> Format **DESIGN.md** suivant la convention officielle Google Stitch
> (front matter YAML machine-readable + prose markdown human-readable).
>
> **Version** : alpha · **Dernière mise à jour** : 21 mai 2026
> **Maintenu par** : équipe HIBOUBOX (Nicolas Dionisius)
> **Statut** : brand book medium-agnostic — applicable à tous supports
> (print · digital · social · packaging · signalétique · packaging emporter).

---

## Overview

### Identité de marque

**HIBOUBOX** est un restaurant-concert-bar-galerie situé à Villard-de-Lans
au cœur du Vercors. Le lieu réunit quatre activités sous une même adresse :

- **Restaurant** — cuisine internationale faite maison, fumaisons artisanales, woks, currys.
- **Salle de concert** — musique live tous les soirs à 20h30 (5-6 soirs/semaine en saison).
- **Bar** — happy hour 16h-18h, accueil exclusivement à table.
- **Galerie** — expositions en rotation tous les ~2 mois, accès libre pendant les heures du restaurant.

Le lieu est porté par la SARL **HibouJazz** (Nicolas Dionisius).

### Sous-marque · Le Festin du Hibou

L'activité **traiteur** s'appelle « Le Festin du Hibou ». Elle partage la
structure juridique, le site web, l'équipe et la cuisine — mais possède
un logo distinct et un accent chromatique propre (**or** au lieu d'orange).
Son différenciateur clé : animation musicale via le réseau d'artistes HIBOUBOX.

### Tagline & voix de marque

> **« le voyage commence à table »**

La phrase signature, en italique serif, conclut systématiquement les
heros, les drawers mobile, les emails. Elle synthétise le positionnement :
on ne sert pas seulement un repas, on emmène en voyage — cuisine du monde,
musique du monde, ouverture culturelle, accueil chaleureux.

### Valeurs éditoriales (à protéger en copy)

1. **10 % HT reversés aux artistes** — pas un geste ponctuel, un choix structurel. Le modèle économique se construit autour de cette redistribution.
2. **Accueil à table** — la salle a une capacité limitée, on ne tasse jamais debout devant la scène. Même les personnes qui viennent juste boire un verre s'installent à table selon les places assises disponibles. **La mention « non-attablés » ne doit jamais apparaître dans la copy.**
3. **Cuisine sans frontières** — woks Asie du Sud-Est, currys Inde, tapas Méditerranée, fumaisons Nord. Aucune cuisine de référence n'écrase les autres.
4. **Programmation tous styles** — dominante jazz / blues / chanson française / musiques du monde. Jamais une niche fermée.
5. **Une seule expo à la fois** — sur le mur principal, rotation ~2 mois. Pas de chevauchement.

### Audience & ton

- **Audience primaire** : habitants du Vercors et alentours (Grenoble · Lyon ~1h-1h30), touristes en saison (hiver/été), amateurs de jazz régionaux.
- **Ton** : sobre, éditorial, jamais commercial. On évite les superlatifs, les "10× faster", les emojis dans les manifestos. On préfère le silence ou une bonne phrase serif italique à un slogan publicitaire.
- **Niveau de langue** : français soigné, vocabulaire évocateur (voyage, escale, fumaisons, cartouche, route, table) sans préciosité.

### Esthétique globale

Trois influences combinées, à parts égales :

1. **Carte ancienne / cartographie de voyage** — grilles lat/long, croisillons sextants, isohypses (lignes de niveau), routes dashed, placenames latins, rose des vents, cartouches numérotés `CARTE Nº I → XIV`.
2. **Club de jazz international** — clé de sol, portées musicales, vinyles, boarding-pass timelines, cachets d'oblitération « par avion », typographie display géométrique compacte (Bungee).
3. **Passeport vintage** — tampons postaux, dot-leaders, perforations ticket déchiré, scotch tape, drop caps presse, signature cartographe.

Palette : **ink profond × orange laiton × cream parchemin × or filigrane**.
Aucune palette froide, aucun gradient violet, aucune photo stock générique.

---

## Logos & Wordmarks

5 fichiers logo officiels HIBOUBOX. Tous portent leur grammaire propre —
**ne jamais en créer de nouveaux** sans validation. Pour usages spéciaux
(monochrome, négatif, sur fond clair print), recolorer via `filter` CSS
chain plutôt que régénérer un nouvel asset.

### Inventaire des fichiers

| Fichier | Usage canonique | Format |
|---|---|---|
| `assets/logo-full-orange.png` | Logo complet — footer site, supports print pleine taille, signalétique extérieure | PNG ~180×180 |
| `assets/wordmark-orange.png` | Wordmark seul (lettres « HIBOUBOX ») — bandeaux étroits, headers compacts, watermark hero | PNG horizontal |
| `assets/picto-owl-orange.png` | Picto chouette seul — favicon, OG image, badges réseaux sociaux, post Instagram avatar | PNG carré |
| `assets/hiboubox-stamp-logo.png` | Logo tampon-stamp (chouette + nom dans un cadre cerclé) — header sticky, signature documents | PNG noir (filter chain pour recolorer) |
| `assets/festin-du-hibou-black.png` | Logo Festin du Hibou (sous-marque traiteur, wordmark + chouette stylisée) — supports traiteur, signature mail Festin | PNG noir |

### Recoloration via filter CSS

Tous les logos PNG sont fournis en **noir originel**. Pour les rendre
orange ou or selon le contexte, utiliser la chain `filter` CSS — JAMAIS
re-exporter un nouveau PNG :

```css
/* Recolorer un logo noir vers orange-500 #d97a2a */
.logo-orange img {
  filter: brightness(0) saturate(100%) invert(56%) sepia(73%) saturate(652%)
          hue-rotate(348deg) brightness(89%) contrast(89%);
}

/* Recolorer un logo noir vers gold-400 #d4af5a (réservé Festin) */
.logo-gold img {
  filter: brightness(0) saturate(100%) invert(73%) sepia(20%) saturate(852%)
          hue-rotate(2deg) brightness(91%) contrast(85%);
}

/* Recolorer un logo noir vers cream-50 #faf3e2 (négatif sur ink-1000) */
.logo-cream img {
  filter: brightness(0) saturate(100%) invert(94%) sepia(11%) saturate(540%)
          hue-rotate(335deg) brightness(96%) contrast(89%);
}
```

**Pourquoi `filter` et pas `mask-image`** : voir section Don'ts (règle 7).
Le `brightness(0)` force le SVG/PNG en noir absolu, puis les filtres
suivants recolorent. Marche aussi sur les SVG qui contiennent du `<text>`
(les stamps origines pays par exemple) — `mask-image` perd ce texte.

### Règles d'usage par contexte

#### Logo full (`logo-full-orange.png`)
- **Taille minimale** : 120px de largeur (en deçà : utiliser le wordmark seul ou le picto).
- **Espace de protection** : un carré équivalent à la hauteur du `H` de HIBOUBOX autour du logo, sans aucun élément.
- **Fonds autorisés** : `ink-1000`, `ink-900`, `ink-800`, `cream-50` (sur cream : recolorer vers `orange-700` pour le contraste).
- **Fonds interdits** : photo plein cadre sans calque sombre, gradient saturé, couleur primaire concurrente (rouge, bleu, vert vif).

#### Wordmark (`wordmark-orange.png`)
- **Usage** : bandeaux étroits où le logo full prendrait trop de hauteur.
- **Taille minimale** : 80px de largeur.
- **Espace de protection** : hauteur d'une lettre `H` au-dessus et en-dessous.

#### Picto (`picto-owl-orange.png`)
- **Usage** : favicon, OG image (1200×630 avec picto centré), avatar Instagram/Facebook, badge réseaux sociaux.
- **Taille minimale** : 32px (favicon 32×32).
- **Variantes** : favicon 16×16, 32×32, 192×192 (Android), 512×512 (PWA).

#### Logo tampon-stamp (`hiboubox-stamp-logo.png`)
- **Usage** : header sticky, navigation mobile (recoloré via filter chain en cream/orange tamponné), signature documents PDF, supports formels (mentions légales, CGV).
- **Taille minimale** : 38px de hauteur (mobile) · 48px desktop.
- **Recolor par défaut** : sépia warm via `filter: invert(1) sepia(0.18) saturate(0.45) brightness(0.86) contrast(0.92) opacity(0.92)` (cf. § Stamps & Tampons pour les recettes filter chain complètes).

#### Logo Festin du Hibou (`festin-du-hibou-black.png`)
- **Usage** : exclusivement sur supports Festin du Hibou (traiteur) — pages dédiées, devis traiteur, signatures email `contact@lefestinduhibou.fr`, étiquettes/packaging emporter, supports événementiel sortants.
- **Accent obligatoire** : recolor vers `gold-400 #d4af5a` via filter chain. Jamais en orange (cohérence chromatique sous-marque).
- **Taille minimale** : 200px de largeur (le wordmark est intégré dans le logo, illisible en dessous).

### Espace de protection visuel

Tous les logos respectent une zone de respiration minimale :

```
┌─────────────────────────┐
│       espace H          │
│   ┌─────────────────┐   │
│ H │     LOGO        │ H │
│   └─────────────────┘   │
│       espace H          │
└─────────────────────────┘
```

Où **`H` = hauteur de la lettre H du wordmark HIBOUBOX**. Ne pas
empiéter sur cette zone avec du texte, des CTAs, des bordures, des
filets décoratifs.

---

## Colors

### Philosophie chromatique

La palette HIBOUBOX est **chaude, candlelit, jamais froide**. Trois rôles
chromatiques :

1. **Fond profond** — `ink` (taupe sombre warm-grey). Toute la base UI vit sur fond `ink-900`. Le footer descend en `ink-1000`. Les cards se posent en `ink-700`. Les sections alternent `ink-900 / ink-800` pour le rythme tonal.
2. **Texte clair** — `cream` (parchemin) sur fond ink. Le texte primaire est `cream-50`, le body `cream-100`. Les supports print sur fond clair utilisent `paper-100/200/300` avec texte `on-paper-1/2/3`.
3. **Accent unique** — **`orange-500 #d97a2a`** : couleur du logo, de la flamme de bougie, du stage light. Réservé aux CTAs principaux, aux eyebrows, aux liens, aux ribbons cartographe, aux stamps. **Maximum 2 occurrences par écran** — c'est la règle de restraint.

Un quatrième accent **gold (`gold-400 #d4af5a`)** est réservé à deux usages :
- Filigrane des **stamps origines pays** (recolorés via filter — 60 pays + 15 régions vins).
- Grammaire visuelle de la sous-marque **Le Festin du Hibou** (traiteur) — remplace l'orange-500 dans ses CTAs et accents.

Un cinquième accent **olive** existe en tokens (`olive-400/500/600`) mais est
**rarement utilisé en proto** — réservé en backup pour une future variante
"vintage poster ink" ou pour différencier le CTA secondaire d'un CTA primary
quand deux CTAs ne peuvent pas être l'un orange et l'autre outline.

### Palette complète — tokens & usages canoniques

#### Ink — fonds sombres (warm taupe / dark grey, jamais brun-rouge)

| Token | Hex | OKLch approx. | Usage canonique |
|---|---|---|---|
| `ink-1000` | `#0a0908` | `oklch(7% 0.003 60)` | Full-bleed background, footer, drawer mobile, fond modal |
| `ink-900` | `#16140f` | `oklch(11% 0.005 70)` | Page background default — base de toute UI |
| `ink-800` | `#211e19` | `oklch(15% 0.006 70)` | Raised surface, header sticky, section alternée |
| `ink-700` | `#2d2925` | `oklch(20% 0.007 70)` | Card surface on dark, hover state |
| `ink-600` | `#3a3530` | `oklch(25% 0.008 70)` | Hover surface, borders forts |
| `ink-500` | `#4a4540` | `oklch(31% 0.008 70)` | Divider, muted border |

**Règle** : alterner `ink-900 / ink-800` entre sections de page, jointes par un `Wave` divider qui porte le passport-stitch dashed orange. Ne jamais sauter deux niveaux d'un coup (`ink-1000 → ink-700` casse le rythme).

#### Cream — texte clair sur fond sombre + parchemin print

| Token | Hex | Usage canonique |
|---|---|---|
| `cream-50` | `#faf3e2` | Primary text on ink — display, titres, eyebrows hero |
| `cream-100` | `#f0e6ce` | Body text on ink (default `<body>`) |
| `warm-300` | `#c2b39a` | Secondary muted text, captions, sub-lines |
| `warm-500` | `#897a63` | État **disabled uniquement** — ⚠ WCAG-exempté (4.41:1 < 4.5 — non-conforme si texte actif) |
| `paper-100` | `#f5ecd6` | Warm cream — fond principal des supports print (menu, cartes de visite) |
| `paper-200` | `#e8dcc0` | Paper aged — variation print, fond card sur fond paper |
| `paper-300` | `#d6c79e` | Paper darker / kraft — étiquettes emporter, packaging |

#### Text on paper — hiérarchie 3 niveaux pour supports clairs

| Token | Hex | Usage |
|---|---|---|
| `on-paper-1` | `#1a1108` | Texte principal sur fond cream/paper |
| `on-paper-2` | `#4a3422` | Texte secondaire sur fond cream/paper |
| `on-paper-3` | `#7a5b3f` | Texte tertiaire / captions sur fond cream/paper |

#### Orange — accent unique (CTAs, liens, eyebrows, stamps)

| Token | Hex | Usage canonique |
|---|---|---|
| `orange-300` | `#f5b074` | Hover soft, états transitoires |
| `orange-400` | `#ea934a` | Hover state primary — eyebrows, accent text hover |
| **`orange-500`** | **`#d97a2a`** | **PRIMARY — accent unique : CTAs, ribbons, stamps, dot-leaders, dividers** |
| `orange-600` | `#b35e1a` | Pressed state, deep variant |
| `orange-700` | `#7e3f10` | Darkest — orange sur fond cream (lisibilité) |

**Règle d'or** : maximum 2 occurrences orange par écran. Eyebrow + CTA primary suffit en hero. Si tu sens le besoin d'un troisième orange, c'est probablement un bug de composition — passer le 3ème en cream-100 ou en outline.

#### Gold — accent filigrane (stamps origines + sous-marque Festin)

| Token | Hex | Usage strict |
|---|---|---|
| `gold-400` | `#d4af5a` | Filigrane des 75 stamps origines pays/régions vins (filter recolor) · accent CTAs/borders sous-marque Festin du Hibou |
| `gold-500` | `#b88f3a` | Gold deep — hover Festin CTAs |

**⚠ Ne PAS utiliser gold comme accent UI général.** L'orange-500 garde le rôle d'accent unique sur HIBOUBOX. Le gold n'apparaît que :
- En filigrane décoratif (opacity 0.72 desktop, watermark dans les cards menu).
- Sur les surfaces Festin du Hibou (page traiteur, signatures, supports événementiel).

#### Olive — accent secondaire vintage (backup, peu utilisé en proto)

| Token | Hex | Usage |
|---|---|---|
| `olive-400` | `#a8b04a` | Hover state secondary |
| `olive-500` | `#818825` | Secondary CTA — variant `Btn.olive` (alternative au primary orange) |
| `olive-600` | `#5e6519` | Pressed olive |

#### Semantic — états système (admin, forms, validation)

| Token | Hex | Usage |
|---|---|---|
| `success` | `#6f8a3e` | Validation form, état accepté |
| `success-bg` | `#2a3318` | Background success card |
| `warning` | `#d4a13a` | Avertissement non bloquant |
| `danger` | `#d85535` | Erreur, état refusé, suppression — corrigé WCAG AA (ex. `#c14f2c` → 3.88:1) |
| `danger-bg` | `#3a1612` | Background danger card |
| `info` | `#6b8aa8` | Information neutre (bleu sourd, jamais saturé) |

### Combinaisons autorisées

✅ **Hero** : `bg ink-900` + `eyebrow orange-400` + `display cream-50` + `CTA orange-500` (1 seul) + `mini-infos cream-100`.

✅ **Card** : `bg ink-700` + `eyebrow orange-500` (size card) + `title cream-50` + `body cream-100` + `CTA orange-500 full-width` (1 seul).

✅ **Section bascule** : si une section signale une bascule vers une page de destination, son **accent peut être celui de la page de destination** (pattern Traiteur S8 qui passe en orange car bascule vers Privatisation). C'est un signal narratif.

✅ **Festin du Hibou** : `bg ink-800/900` + `eyebrow gold-400` + `display cream-50` + `CTA gold-400` + accents `gold-400` partout.

### Combinaisons interdites

❌ **Orange + olive** dans le même écran — deux verts/oranges concurrents.
❌ **Orange + gold** comme deux accents égaux — gold n'est qu'un filigrane décoratif (sauf sur Festin).
❌ **Cream-50 sur paper-100** — contraste insuffisant (cream sur cream).
❌ **Texte orange-500 sur fond ink-700** — contraste insuffisant pour body text (OK pour eyebrow uppercase 13px car le tracking améliore la lisibilité).

### Ratios de contraste (WCAG)

Vérifiés sur les combinaisons canoniques (WCAG 2.2 — AA = 4.5:1 texte normal, 3:1 grand texte ≥ 18px ou 14px bold).
Ratios calculés par formule WCAG officielle (IEC 61966-2-1, gamma 2.4).

#### Texte sur fonds sombres (usage principal)

| Foreground | Background | Ratio | Verdict |
|---|---|---|---|
| `cream-50 #faf3e2` | `ink-1000 #0a0908` | **18.0 : 1** | AAA |
| `cream-50` | `ink-900 #16140f` | **16.6 : 1** | AAA |
| `cream-50` | `ink-800 #211e19` | **15.0 : 1** | AAA |
| `cream-100 #f0e6ce` | `ink-900` | **14.8 : 1** | AAA |
| `cream-100` | `ink-700 #2d2925` | **11.6 : 1** | AAA |
| `warm-300 #c2b39a` | `ink-900` (captions, sub-lines) | **9.0 : 1** | AAA |
| `warm-500 #897a63` | `ink-900` (disabled only — exempté WCAG) | **4.4 : 1** | exempté |
| `orange-500 #d97a2a` | `ink-900` | **5.9 : 1** | AA |
| `orange-400 #ea934a` | `ink-900` | **7.7 : 1** | AAA |
| `gold-400 #d4af5a` | `ink-900` | **8.8 : 1** | AAA |

#### Texte sur fonds clairs (print, paper)

| Foreground | Background | Ratio | Verdict |
|---|---|---|---|
| `on-paper-1 #1a1108` | `paper-100 #f5ecd6` | **15.8 : 1** | AAA |
| `on-paper-2 #4a3422` | `paper-100` | **9.9 : 1** | AAA |
| `on-paper-3 #7a5b3f` | `paper-100` | **5.3 : 1** | AA |
| `orange-700 #7e3f10` | `paper-100` | **6.9 : 1** | AA |

#### Texte sur composants colorés (boutons)

| Foreground | Background | Ratio | Verdict |
|---|---|---|---|
| `primary-fg #1a0e04` | `orange-500 #d97a2a` (btn primary) | **6.1 : 1** | AA |
| `primary-fg #1a0e04` | `gold-400 #d4af5a` (btn Festin) | **9.1 : 1** | AAA |
| `secondary-fg #0f1404` | `olive-500 #818825` (btn.olive) | **4.9 : 1** | AA |

#### Couleurs sémantiques sur ink-900

| Token | Hex | Ratio | Verdict |
|---|---|---|---|
| `success` | `#6f8a3e` | **4.7 : 1** | AA |
| `danger` | `#d85535` | **4.6 : 1** | AA ✓ (corrigé — ex. `#c14f2c` = 3.88:1 FAIL) |
| `warning` | `#d4a13a` | **7.9 : 1** | AAA |
| `info` | `#6b8aa8` | **5.1 : 1** | AA |

**Règle stricte** : sur les textes critiques (CTAs, body, captions, messages d'erreur), toujours viser AA minimum. Pour les éléments décoratifs (stamps watermark, atmospheres, filigrane), opacity 0.20-0.50 peut tomber sous AA — c'est intentionnel (décor).

---

## Typography

### Stack typographique — 6 familles, rôles spécialisés

HIBOUBOX utilise un système de **6 familles typographiques** chargées via
Google Fonts. Chaque famille a un rôle strict — ne jamais l'utiliser
hors de son rôle.

| Famille | Usage | Caractère |
|---|---|---|
| **Bungee** | Display titres XXL | Signage géométrique compact arrondi, hyper-impact, jamais discret |
| **Rubik Wet Paint** | Poster concert XL | Textured grunge, peinture-pochoir, exclusif affiches concert |
| **Cormorant Garamond** | Script italique | Pull-quotes, taglines, citations, ligne compagne — italic only |
| **Lato** | Body + UI + mobile | Long-form lisible, neutre, system-like sans être Arial |
| **Barlow Condensed** | Eyebrows + labels + CTAs in-card | Uppercase tracking 0.22em, weight 600 |
| **Special Elite** | Stamps, coords, ticket stubs, dates | Typewriter monospace, ticket-stub, vintage |

**Import via Google Fonts** :

```css
@import url("https://fonts.googleapis.com/css2?family=Bungee&family=Bowlby+One&family=Rubik+Wet+Paint&family=Cormorant+Garamond:ital,wght@0,500;0,700;1,400;1,500;1,700&family=Lato:ital,wght@0,300;0,400;0,500;0,700;1,400&family=Barlow+Condensed:wght@500;600;700&family=Special+Elite&display=swap");
```

**Fallbacks** (ordre de la pile CSS) :

```css
--font-display: "Bungee", "Bowlby One", "Ultra", "Arial Black", sans-serif;
--font-poster:  "Rubik Wet Paint", "Bowlby One", "Arial Black", sans-serif;
--font-serif:   "Cormorant Garamond", "EB Garamond", Georgia, serif;
--font-body:    "Lato", "Source Sans 3", -apple-system, BlinkMacSystemFont, "Segoe UI", system-ui, sans-serif;
--font-label:   "Barlow Condensed", "Oswald", "Arial Narrow", sans-serif;
--font-stamp:   "Special Elite", "Courier Prime", "Courier New", monospace;
```

### Scale typographique complète

#### Display (Bungee) — titres principaux

| Token | Taille desktop | Taille mobile | Letter-spacing | Line-height | Usage |
|---|---|---|---|---|---|
| `display-xl` | **92px** | 44-56px | -0.01em | 0.9 | Hero principal (page d'accueil, hero de page-étalon) |
| `display-lg` | **64-72px** | 36-44px | -0.005em | 0.92 | Hero secondaire, section heads majeures |
| `display-md` | **44-48px** | 28-32px | -0.005em | 1.05 | Section heads standard, card headlines featured |
| `h3` | **28px** | 22px | 0 | 1.05 | Card titles, sub-section heads (textTransform: none) |
| `h4` | **22px** | 18px | 0 | 1.2 | Card titles secondaires, info-card titles |

**Règle** : tous les Display sont en `text-transform: uppercase` sauf `h3`/`h4`. Tous portent `color: var(--cream-50)`. Le `letter-spacing` négatif compacte le glyphe Bungee qui est déjà géométrique.

**Pattern d'accent** : un mot du Display est passé en `<span class="accent">` qui le colore en `orange-500`. Typiquement le 2ᵉ mot du titre (ex. `TRIO <span class="accent">MARLOWE</span>`, `LE <span class="accent">FESTIN</span> DU HIBOU`, `<span class="accent">PRIVATISEZ</span> LE HIBOUBOX`). Un seul mot accent par Display.

#### Poster (Rubik Wet Paint) — affiches concert XL

| Token | Taille | Usage |
|---|---|---|
| `poster-xl` | **120px+** | Réservé aux affiches concert print A3 et hero-affiches du Détail concert. Style grunge texturé, lisibilité réduite — toujours sur fond ink sombre, jamais sur paper clair. |

#### Script italique (Cormorant Garamond) — taglines, pull-quotes

| Token | Taille desktop | Taille mobile | Usage |
|---|---|---|---|
| `script-lg` | **60px** | 38px | Tagline hero (« le voyage commence à table »), Script en sous-titre Display |
| `script-md` | **34px** | 17-24px | Phrases compagnes (« notre cuisine se déplace chez vous »), citations encart |
| `script-sm` | **22px** | 16-18px | Sous-titres de section discrets, captions élégants |

**Règle** : le Script est **toujours en italique**. Jamais en uppercase. Letter-spacing à 0. Color `cream-100` par défaut, peut passer en `orange-400` pour une emphase rare. Pour les pull-quotes pleines largeur, utiliser `script-md` avec un guillemet `«` géant orange opacity 0.55 en `::before`.

#### Eyebrow (Barlow Condensed) — labels au-dessus des titres

| Token | Taille desktop | Taille mobile | Letter-spacing | Usage |
|---|---|---|---|---|
| `eyebrow-hero` | **22px** | 16px | 0.22em | Eyebrow au-dessus du Display hero (`◉ MMXXVI · ANS DEUX`) |
| `eyebrow-section` | **19px** | 15px | 0.22em | Eyebrow au-dessus des Display de section (standard HIBOUBOX) |
| `eyebrow-card` | **13-16px** | 12-14px | 0.22em | Eyebrow dans une card (`◉ JAZZ MANOUCHE · VERCORS`) |

**Règle** : tous les eyebrows sont en `font-weight: 600-800`, `text-transform: uppercase`, color `orange-400` ou `orange-500` selon le contexte. Le tracking `0.22em` est non négociable — c'est ce qui transforme un texte uppercase en signal "label" plutôt qu'en "cri". Sur mobile, tracking peut redescendre à `0.18em` pour éviter les wraps disgracieux.

#### Body (Lato) — texte courant

| Token | Taille | Line-height | Usage |
|---|---|---|---|
| `lead` | **20px** | 1.55 | Phrase d'introduction sous un Display |
| `body` | **16px** | 1.55 | Texte courant des sections |
| `small` | **14px** | 1.55 | Captions, sub-lines, meta |
| `micro` | **12px** | 1.45 | Footnotes, légales, ticker |

**Règle** : color `cream-100` par défaut sur fond ink, `on-paper-1` sur fond cream/paper. Les paragraphes éditoriaux longs (manifesto, lettre, double-page magazine) portent `text-align: justify` + `hyphens: auto` + `text-wrap: pretty` pour un rendu façon presse.

#### Stamp / Coord (Special Elite) — typewriter monospace

| Token | Taille | Letter-spacing | Usage |
|---|---|---|---|
| `stamp` | **10-12px** | 0.12em | Tampons décoratifs, ticket stubs, dates, numérotation `Nº I/II/III` |
| `coord` | **13-16px** | 0.16em | Coord badges (`◉ 45°04′N · 5°33′E`), ribbon cartographe header |

**Règle** : color `orange-400` ou `orange-500`. Toujours uppercase. Le Special Elite **doit toujours apparaître monospace** — si la police ne charge pas (offline), le fallback `"Courier Prime", "Courier New", monospace` préserve le rythme typewriter.

### Hierarchy patterns canoniques

#### Hero standard HIBOUBOX

```
[CoordBadge mono orange-400 13px]    ← ◉ 45°04′N · 5°33′E
[Eyebrow Barlow 22px orange-400 tracking 0.22em]   ← ◉ MMXXVI · ANS DEUX · DEPUIS LA REPRISE
[Display Bungee 92px cream-50 uppercase]            ← LE HIBOUBOX (avec un mot accent orange)
[Script Cormorant italic 60px cream-100]            ← « le voyage commence à table »
[Lead Lato 20-24px cream-50 weight 500]             ← Une phrase d'introduction.
[Btn primary 17-22px feature]                        ← → RÉSERVER UNE TABLE
```

#### Card head canonical (Info Pratiques pattern)

```
[Icône cerclée dashed orange 56×56]
[Eyebrow Barlow 22px orange-400 tracking 0.22em]   ← SE RENDRE À HIBOUBOX
[Séparateur dashed orange — 22px en dessous]
```

#### Card content standard

```
[Photo placeholder 240-360px height]
[Eyebrow Barlow 13-16px orange-500]                 ← JAZZ MANOUCHE
[Display Bungee 28-32px cream-50 uppercase]         ← TRIO MARLOWE
[Meta-row mono 22px weight 700 orange-500]          ← VEN 17 MAI · 20H30
[Body Lato 16px cream-100 1-2 lignes]               ← Description courte.
[Btn primary full-width 18px feature]               ← → DÉTAILS DU CONCERT
```

### Variants `font-variant-numeric`

- **Tables, listes de prix, scores** : `font-variant-numeric: tabular-nums` (chiffres alignés en colonne).
- **Coordonnées, dates ticket stub** : `tabular-nums` également — le Special Elite a déjà des chiffres tabulaires natifs mais on force pour cohérence.
- **Body text courant** : `proportional-nums` (default) — chiffres au pas naturel de la police.

### Règles inviolables (typo)

1. ❌ **Jamais Bungee en body text** — c'est un display, illisible en dessous de 22px.
2. ❌ **Jamais Lato en Display** — c'est un body, manque d'impact pour les hero.
3. ❌ **Jamais Cormorant Garamond hors italique** — la famille n'est utilisée qu'en `font-style: italic`.
4. ❌ **Jamais d'eyebrow sans tracking ≥ 0.16em** — sans tracking, ça lit comme du texte normal en majuscules (criant).
5. ❌ **Jamais Inter / Roboto / Arial comme display** — c'est la signature AI-slop. Le seul fallback Arial autorisé est `"Arial Black"` dans la stack Bungee si la connexion Google Fonts échoue.
6. ❌ **Jamais une preview qui simule la typo avec Iowan Old Style / Georgia / serif** — le glyphe est ~30 % plus large que Bungee, fausse les calculs d'overflow (bug identifié 21 mai sur l'outil extraction texte).

### Mobile responsiveness

Sur tout support digital (web, email, app), les tailles desktop doivent
être réduites pour la lisibilité à bout de bras. La règle est de bumper
**toutes les tailles éditoriales à la hausse** quand on passe en mobile
— jamais à la baisse. Un titre Display qui passe de 92px à 48px wrap
correctement avec line-height ajusté de 0.9 à 1.15.

**Bumps typo mobile transverse** (calage acté) :
- Eyebrows section : 19px desktop → **15px mobile** (tracking 0.18em).
- Hero eyebrow : 22px desktop → **16px mobile** (tracking 0.22em conservé).
- Display section : 60-72px desktop → **38-44px mobile** (line-height 1.15 vs 1.02 desktop pour éviter wraps tassés).
- Body : 16px desktop → **14-15px mobile** (line-height 1.55 conservé).
- CTAs in-card : 18px desktop → **15px mobile** (weight 700 conservé).

---

## Layout & Spacing

### Philosophie d'espacement

HIBOUBOX utilise une **base 4px** stricte. Tous les paddings, gaps, margins
sont des multiples de 4. C'est ce qui donne la sensation de rigueur
cartographique du proto — rien ne flotte, tout est aligné sur une grille
implicite.

### Spacing scale

| Token            | Valeur | Usage canonique                                              |
|------------------|--------|--------------------------------------------------------------|
| `--sp-0`         | `0`    | Reset                                                        |
| `--sp-1`         | `4px`  | Espacement très serré : icône + label inline, dividers       |
| `--sp-2`         | `8px`  | Gap par défaut entre meta-row items, padding badge           |
| `--sp-3`         | `12px` | Padding card-head ico, gap CTAs in-card                      |
| `--sp-4`         | `16px` | Padding cell mini-info, gap form fields                      |
| `--sp-5`         | `20px` | Padding standard pill, padding intra-card                    |
| `--sp-6`         | `24px` | Padding card body, gap entre cards row                       |
| `--sp-7`         | `32px` | Margin entre paragraphes éditorial, padding section ribbon   |
| `--sp-8`         | `48px` | Margin entre sub-sections, padding card spacieuse            |
| `--sp-9`         | `64px` | Padding section bottom standard                              |
| `--sp-10`        | `96px` | Padding section bottom large (hero, manifesto)               |

### Section paddings (canoniques)

| Token              | Valeur          | Usage                                          |
|--------------------|-----------------|------------------------------------------------|
| `--sec-pad-y`      | `96px`          | Padding vertical section standard desktop      |
| `--sec-pad-y-lg`   | `128px`         | Hero, section éditoriale longue                |
| `--sec-pad-x`      | `clamp(20px, 4vw, 64px)` | Padding horizontal fluide              |

**Mobile transverse** : ces valeurs sont **halved** sur mobile —
section padding 96→64px, hero padding 128→80px, padding horizontal
clamp(16px, 4vw, 32px). En print A5+ : valeurs réduites de 30 % pour
préserver les marges techniques d'impression.

### Containers

| Class               | Max-width   | Usage                                       |
|---------------------|-------------|---------------------------------------------|
| `.container`        | `1280px`    | Container principal sections standard       |
| `.container-narrow` | `880px`     | Container éditorial (article, manifesto)    |
| —                   | `720px`     | Colonne éditoriale serrée (À propos S2/S3)  |
| —                   | `1180px`    | Container Festin/CTA section (large)        |
| —                   | `1440px`    | Hero (déborde le container)                 |

**Règle d'or** : un texte éditorial long (`<p>`) **ne dépasse jamais 720px
de largeur** (~70 caractères par ligne, lisibilité optimale). Pour les
grids et cards, on monte à 1180-1280px.

### Grille de section

```
┌────────────────────────────────────────────────────────────┐
│  [sec-pad-y]                                                │
│                                                              │
│  ┌──────────────────────────────────────────────────────┐  │
│  │  [Eyebrow]                                           │  │
│  │  [Display]                                           │  │
│  │  [Lead]                                              │  │
│  │  [Content — grid 1fr / 1fr ou stack]                 │  │
│  └──────────────────────────────────────────────────────┘  │
│  ← max-width container, sec-pad-x left+right →             │
│                                                              │
│  [sec-pad-y]                                                │
└────────────────────────────────────────────────────────────┘
```

### Grids canoniques

| Pattern              | Desktop                          | Mobile                 |
|----------------------|----------------------------------|------------------------|
| Hero split           | `1.18fr / 1fr` gap 36px          | `1fr` stack            |
| Map + Coords         | `1fr / 1fr` gap 28-32px          | `1fr` stack            |
| 3 cards features     | `repeat(3, 1fr)` gap 24-32px     | `1fr` stack            |
| 4 cells mini-info    | `repeat(4, 1fr)` gap 16px        | `repeat(2, 1fr)` gap 12px |
| 5 cards profils      | `repeat(5, 1fr)` gap 18px        | `flex-wrap calc(50%-9px)` 2×2 + 5ᵉ full-width |
| Newsletter strip     | `1.4fr / 1fr` gap 32px           | `1fr` stack            |
| Section bascule      | `1fr / 1fr` gap 48px             | `1fr` stack            |

### Section rhythm — alternance tonale

Convention HIBOUBOX : **les sections alternent `--ink-900` et `--ink-800`**
pour créer un rythme visuel. Le footer est toujours `--ink-1000` (plus
sombre). Pattern type pour une page de 6 sections :

```
Section 1 (Hero)         → ink-900
─ Wave ink-900 → ink-800
Section 2                → ink-800
─ Wave ink-800 → ink-900
Section 3                → ink-900
─ Wave ink-900 → ink-800
Section 4                → ink-800
─ Wave ink-800 → ink-900
Section 5                → ink-900
─ Wave ink-900 → ink-1000
Footer                   → ink-1000
```

Si une section "bascule" (signal de transition vers une grammaire
adjacente, ex. Privatisation depuis Traiteur), on **rompt l'alternance**
volontairement avec une teinte qui appartient à la grammaire de
destination.

---

## Elevation & Depth

### Philosophie de l'élévation

HIBOUBOX évite les ombres "soft UI" génériques (drop-shadow flou bleuté).
Les seules profondeurs autorisées sont :
1. **Ombre fonctionnelle** sur modales / dropdowns / overlay popovers
2. **Glow signature** orange pulsant sur les items featured (halo)
3. **Glow stage** inset rouge profond pour les surfaces "sous éclairage
   de scène" (poster hero concert, atmospheres jazz)

Pas de shadow sur les cards de body standard. C'est le **dashed orange
border + outline offset** qui crée le relief (cf. Shapes).

### Shadows tokens

| Token              | Valeur                                            | Usage                                          |
|--------------------|---------------------------------------------------|------------------------------------------------|
| `--shadow-sm`      | `0 1px 2px rgba(0,0,0,.3)`                        | Très subtil (rare)                             |
| `--shadow-md`      | `0 4px 12px rgba(0,0,0,.4)`                       | Modale, dropdown, popover                      |
| `--shadow-lg`      | `0 12px 36px rgba(0,0,0,.32)`                     | Festin card hero, lift modale plein écran      |
| `--shadow-xl`      | `0 24px 64px rgba(0,0,0,.5)`                      | Lift maximum (rare)                            |
| `--glow-orange`    | `0 0 24px rgba(217,122,42,.4)`                    | Featured item halo, CTA hover ponctuel         |
| `--glow-stage`     | `inset 0 0 80px rgba(179,94,26,.18)`              | Surfaces "sous éclairage scène" (poster hero)  |

### Halo featured pulsant (pattern signature)

L'item featured (concert du jour, plat star, expo en cours) reçoit un
halo orange doux qui pulse à 4.8s. **Ne JAMAIS modifier la taille ou la
position de l'item featured** — le halo se rend in-place autour de sa
position naturelle. Recette CSS canonique :

```css
.item.featured {
  background: linear-gradient(135deg,
    rgba(217,122,42,.04) 0%,
    rgba(217,122,42,.07) 50%,
    rgba(217,122,42,.04) 100%
  );
  box-shadow: inset 0 0 0 1px rgba(217,122,42,.28);
  animation: hi-featured-halo 4.8s ease-in-out infinite;
}

@keyframes hi-featured-halo {
  0%, 100% { box-shadow: inset 0 0 0 1px rgba(217,122,42,.28); }
  50%      { box-shadow: inset 0 0 0 1px rgba(217,122,42,.42), 0 0 24px rgba(217,122,42,.18); }
}

@media (prefers-reduced-motion: reduce) {
  .item.featured { animation: none; }
}
```

### Règles d'élévation

1. ❌ **Jamais de shadow flou bleuté générique** (`box-shadow: 0 4px 20px rgba(0,0,0,.1)`) — c'est la signature soft-UI moderne, anti-HIBOUBOX.
2. ❌ **Jamais de shadow colorée hors orange** — pas de glow violet, vert, cyan.
3. ❌ **Jamais de translateY au hover sur les cards Info Pratiques** — bug constaté en polish 12a (la card collapse visuellement). Override : `transform: none !important` au hover.
4. ✅ **`prefers-reduced-motion: reduce` désactive toute animation** — règle d'accessibilité non négociable.
5. ✅ **Modales** (galerie plein écran, photo modale) : `backdrop-filter: blur(8px) + background: rgba(10,9,8,.94)` + z-index 9000.

---

## Shapes

### Philosophie des formes

HIBOUBOX préfère les **angles francs** aux radii généreux. Les seules
zones où on tolère du radius :
- Les **pills** (CTAs, chips, badges) en `border-radius: 999px`
- Les **cards body** en `border-radius: 12px` max
- Le **logo blob** organique en `border-radius: 60% 40% 55% 45% / 50% 60% 40% 50%` (silhouette owl)

Pas de radius sur les sections, headers, dividers, eyebrows, stamps
(les stamps ont leur propre forme SVG ovale).

### Radii tokens

| Token        | Valeur                                                       | Usage                                          |
|--------------|--------------------------------------------------------------|------------------------------------------------|
| `--r-none`   | `0`                                                          | Eyebrows, dividers, sections                   |
| `--r-sm`     | `4px`                                                        | Inputs, mini-badges                            |
| `--r-md`     | `8px`                                                        | Tooltips, mini-cards intra                     |
| `--r-lg`     | `12px`                                                       | Cards body standard                            |
| `--r-xl`     | `20px`                                                       | Cards spacieuses (rare)                        |
| `--r-full`   | `999px`                                                      | Pills, chips, CTAs, contact pills              |
| `--r-blob`   | `60% 40% 55% 45% / 50% 60% 40% 50%`                          | Logo owl silhouette, mask organique            |

### Borders tokens

| Token              | Valeur                              | Usage                                          |
|--------------------|-------------------------------------|------------------------------------------------|
| `--border-thin`    | `1px`                               | Standard partout                               |
| `--border-medium`  | `1.5px`                             | Cadres orange forts (address-block, festin)    |
| `--border-thick`   | `2px`                               | Stamps signature, bandeau ENGAGEMENT massif    |
| `--border-stroke`  | `3px`                               | Borders accents très lourds (rare)             |

### Patterns border canoniques

| Pattern                    | CSS                                                              |
|----------------------------|------------------------------------------------------------------|
| **Dashed orange faible**   | `1px dashed rgba(217,122,42,.28)`                                |
| **Dashed orange medium**   | `1px dashed rgba(217,122,42,.55)`                                |
| **Dashed orange fort**     | `1.4px dashed var(--orange-500)`                                 |
| **Solid orange medium**    | `1.5px solid var(--orange-500)`                                  |
| **Outline dashed offset**  | `outline: 1px dashed rgba(217,122,42,.55); outline-offset: 4px;` |
| **Inner shadow border**    | `box-shadow: inset 0 0 0 1px rgba(217,122,42,.28)`               |

### Pattern "tampon postal officiel" (signature)

Combinaison qui revient ~40 fois dans le proto :

```css
.stamp-officiel {
  border: 1.5px solid var(--orange-500);
  outline: 1px dashed rgba(217,122,42,.55);
  outline-offset: 4px;
  position: relative;
}
.stamp-officiel::before, .stamp-officiel::after {
  content: '';
  position: absolute;
  width: 12px;
  height: 12px;
  border: 1.2px dashed var(--orange-500);
}
.stamp-officiel::before { top: 6px; left: 6px; border-right: none; border-bottom: none; }
.stamp-officiel::after  { bottom: 6px; right: 6px; border-left: none; border-top: none; }
```

Donne le feel "encadré + tampon postal" sans shadow. Utilisé sur :
address-block hero, bandeau ENGAGEMENT MMXXII, info-card heads, datetime
stamps concert, festin card, bandeau GRATUITÉ, etc.

### Textures CSS pures

3 textures additives, à appliquer en classe sur n'importe quel container :

| Class         | Effet                                                  | Usage                                     |
|---------------|--------------------------------------------------------|-------------------------------------------|
| `.tex-grain`  | Bruit aléatoire SVG 240×240 opacity 0.07               | Fond hero pour éviter aplats massifs      |
| `.tex-paper`  | Pattern radial cream 1px tous les 24×24                | Fonds cream-50 (page mentions/CGV)        |
| `.tex-vinyl`  | Grooves concentriques répétés                          | Fond section "diffusion / musique"        |

### Masks grunge

| Class           | Effet                                                                  |
|-----------------|------------------------------------------------------------------------|
| `.grunge`       | Masque SVG turbulence (frequency 0.9, baseFrequency 0.65, opacity 1)   |
| `.grunge-soft`  | Variante adoucie (frequency 0.5, opacity 0.7)                          |

À utiliser parcimonieusement sur les tampons signature (`stamp-vercors`,
`stamp-entree-libre`) pour leur donner un feel "encre tamponnée à la
main". Pas en background-image full-section.

---

## Grammaire visuelle (cartographie · passport · jazz club)

### Vocabulaire signalétique

HIBOUBOX puise dans **3 univers combinés**. Chaque section choisit son
sous-vocabulaire dominant selon le thème :

| Univers              | Vocabulaire                                                                                       |
|----------------------|---------------------------------------------------------------------------------------------------|
| **Cartographie**     | Grille lat/long · croisillons sextants · isohypses (lignes niveau) · sommets cotés ▲ · rose des vents · routes dashed · placenames latins · cartouches `CARTE Nº X` · coord stamps |
| **Passport / Postal**| Cachet d'oblitération rond · scotch tape rotated · perforation ticket déchiré · 4 corner ticks dashed · enveloppes vintage · tampons `PAR AVION · VIA AIR MAIL` · bandes hachurées rouge/bleu aéropostale · numéros romains `Nº I → Nº XIV` |
| **Jazz club**        | Portée musicale 5 lignes · clé de sol `𝄞` · notes ♩♪♬♫ · vinyle grooves · boarding-pass timeline · halo orange pulsant featured · stamp `STAGE · MMXXVI` |

### Règles d'orchestration de la grammaire

1. **1 atmosphere par section** — l'écosystème décoratif est unique par
   contexte
2. **Vocabulaire varié par section** — éviter de répéter le même
   artefact 2 sections d'affilée
3. **Opacités très basses** : 0.05-0.30 max sur tout élément décoratif
4. **Décor en arrière-plan pur** — toujours ignoré par les lecteurs
   d'écran sur supports digitaux
5. **Concentre le décor sur les zones visibles** — pas de décor "perdu
   derrière les cards"
6. **Pas plus d'un artefact signature dominant** par section (cartouche
   XOR rose des vents XOR croisillon central XOR route principale)

### Placenames latins canoniques (banque de noms réutilisable)

| Latin                  | Contexte d'usage                              |
|------------------------|-----------------------------------------------|
| `VIA · COQUINA`        | Route cuisine (Traiteur)                      |
| `VIA · SPECIARUM`      | Route épices (Menus sur place)                |
| `VIA · LITTERIS`       | Route lettres (Contact clients)               |
| `VIA · NUNTIORUM`      | Route messagers (Contact)                     |
| `VIA · REGULAE`        | Route règles (Réservation lettre)             |
| `VIA · DOMUS`          | Route maison (Privatisation)                  |
| `VIA · COMMANDA`       | Route commande (Menus emporter)               |
| `PORTUS · DOMUS`       | Port maison                                   |
| `PORTUS · LITTERIS`    | Port lettres                                  |
| `PORTUS · OFFICII`     | Port services                                 |
| `PORTUS · MAISONIS`    | Port de la maison                             |
| `TERRA · GASTRONOMICA` | Terre gastronomique (Menus food)              |
| `TERRA · CONVIVIA`     | Terre conviviale (Privatisation)              |
| `TERRA · ITINERIS`     | Terre du voyage                               |
| `DOMUS · NOSTRA`       | Notre maison (Privatisation)                  |
| `AULA · MAGNA`         | Grande salle (Privatisation)                  |
| `MARE · APERITIVI`     | Mer apéritive (Menus drink)                   |
| `NUNTIUS · MISSIO`     | Mission messager (Home contact)               |

**Règle** : utiliser le latin **avec parcimonie** (1-2 placenames par
section atmosphere). C'est une signature éditoriale, pas un effet de
manche.

### Cartouches `CARTA Nº` / `CARTE Nº`

Chaque section reçoit un cartouche cartographe en signature bas-droite
(ou top-left selon composition). Numérotation **romaine séquentielle
dans la page** (`Nº I → Nº XIV`).

```jsx
<SectionCartouche
  title="CARTA Nº V · DOMUS NOSTRA"
  subtitle="HIBOUBOX · ÉDITION MMXXVI"
  side="right"
/>
```

### Cardinaux & coordonnées (canonical HIBOUBOX)

- **Coord HIBOUBOX** : `45°04′27″N · 5°33′12″E`
- **Format court** : `◉ 45°04′N · 5°33′E · VILLARD-DE-LANS`
- **Altitude** : `ALT · 1050 M`
- **Bearing labels** (style portolan) : `350°` / `0°` / `010°` / `020°` / `030°` au bord haut des cartes

### Cotes Vercors (réutilisables atmospheres)

| Sommet              | Altitude  |
|---------------------|-----------|
| Grande Moucherolle  | 2284m     |
| Cornafion           | 2049m     |
| Roc d'Arguille      | 1768m     |
| HIBOUBOX (lieu)     | 1050m     |
| Isohypses standard  | 1050 / 1768 / 1968 / 2049 / 2284 m |

### Music staff (jazz vocabulary)

```jsx
<MusicStaff position="bottom" rotation="-3deg" />
```

Composant primitive : 5 lignes dashed orange, clef de sol `𝄞` en tête,
4-6 notes avec tiges, label optionnel `PORTÉE · NAVIGATION` ou
`DIFFUSIO ♪`. **Utiliser uniquement en atmosphere** (section À propos
diffusion, drawer mobile décor), pas en composant fonctionnel.

### Rose des vents (compass-rose)

Asset SVG dans `assets/compass-rose.svg`, rendu via primitive `<Compass />`.
**Toujours** positionnée via `top` / `right` / `bottom` / `left` directly :

```jsx
<Compass top={28} right={28} size={110} opacity={0.32} />
```

❌ **NE JAMAIS** utiliser `position="bottom-right"` — la prop n'existe pas
(API inventée, ignorée silencieusement). Bug récurrent corrigé sur 8
occurrences page À propos.

---

## Stamps & Tampons

### Inventaire complet

| Type                       | Fichier                                  | Quantité | Format SVG          |
|----------------------------|------------------------------------------|----------|---------------------|
| **Compass rose**           | `assets/compass-rose.svg`                | 1        | viewBox 100×100     |
| **Coord stamp**            | `assets/coord-stamp.svg`                 | 1        | inline-stamp        |
| **World map**              | `assets/world-map.svg`                   | 1        | viewBox 1000×500    |
| **Stamp Vercors**          | `assets/stamp-vercors.svg`               | 1        | tampon rond         |
| **Stamp Entrée Libre**     | `assets/stamp-entree-libre.svg`          | 1        | tampon ovale        |
| **Stamp Par Avion**        | `assets/stamp-par-avion.svg`             | 1        | bande hachurée      |
| **Stamps origines pays**   | `assets/origins/<slug>.svg`              | **56**   | viewBox 140×80      |
| **Stamps régions vins FR** | `assets/origins/vins/<slug>.svg`         | **15**   | viewBox 140×80      |

### Origines pays (56 stamps disponibles)

**Pays internationaux (52)** :
afriquesud · algerie · allemagne · antilles · argentine · australie · autriche · belgique · bresil · cambodge · chili · chine · colombie · coree · cuba · dominicaine · egypte · espagne · etats-unis · ethiopie · france · grece · inde · indonesie · irlande · israel · italie · jamaique · japon · laos · liban · madagascar · malaisie · maroc · mexique · nouvelle-zelande · pays-bas · perou · philippines · portugal · reunion · senegal · singapour · sri-lanka · suisse · syrie · tahiti · thailande · tunisie · turquie · uk · vietnam

**Régions françaises (4)** :
dauphine · provence · savoie · vercors-region

### Régions vins (15 stamps)

alsace · beaujolais · bordeaux · bourgogne · bugey · champagne · corse · jura · languedoc · loire · provence · rhone · roussillon · savoie · sud-ouest

### Structure SVG canonique (origins format ovale)

Tous les stamps origines suivent **strictement la même structure** pour
recolorisation et alignement homogènes :

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 140 80" width="140" height="80" aria-label="FRANCE">
  <!-- 1. Anneau extérieur ovale -->
  <ellipse cx="70" cy="40" rx="66" ry="36" fill="none" stroke="currentColor" stroke-width="1.4"/>
  <!-- 2. Anneau intérieur dashed -->
  <ellipse cx="70" cy="40" rx="60" ry="30" fill="none" stroke="currentColor" stroke-width="0.7" stroke-dasharray="2 2.4" opacity="0.55"/>
  <!-- 3. Plaque rectangulaire dashed en haut (encadre le nom) -->
  <rect x="30" y="23" width="80" height="16" fill="none" stroke="currentColor" stroke-width="0.9" stroke-dasharray="2.6 2" opacity="0.95"/>
  <!-- 4. Texte nom du pays (Special Elite mono) -->
  <text x="70" y="34.5" text-anchor="middle" font-family="'Special Elite','Courier New',monospace,serif" font-size="12" letter-spacing="0.4" fill="currentColor" font-weight="700">FRANCE</text>
  <!-- 5. Emblème distinctif (Tour Eiffel, Tour Pise, Fuji, kangourou, etc.) -->
  <g transform="translate(70 55) scale(0.78)">
    <!-- ... paths emblème ... -->
  </g>
  <!-- 6. Ornements (2 points latéraux ou autres) -->
  <circle cx="10" cy="40" r="1.2" fill="currentColor" opacity="0.6"/>
  <circle cx="130" cy="40" r="1.2" fill="currentColor" opacity="0.6"/>
</svg>
```

**Tailles de texte adaptées au script** :

| Script                         | Font-size | Letter-spacing |
|--------------------------------|-----------|----------------|
| CJK (中國, 日本, 한국)         | 13-15     | 0.5-1          |
| Latin court (FRANCE, ITALIA)   | 12-13     | 0.4-0.6        |
| Latin long (NOUVELLE-ZÉLANDE)  | 8-9       | 0.2-0.3        |
| Devanagari (भारत)              | 11-13     | 0.3-0.5        |
| Arabe (المغرب)                 | 11-13     | 0.4-0.7        |
| Hébreu (ישראל)                 | 12-14     | 0.5-0.8        |
| Grec (ΕΛΛΆΣ)                   | 12-14     | 0.4-0.6        |

### Recolorisation via filter chain (CRITIQUE)

❌ **NE JAMAIS utiliser `mask-image: url(...)` + `background-color`** pour
recolorer ces SVG. La couche alpha extraite par `mask-image` n'inclut pas
le rendu du `<text>` → l'élément apparaît invisible (pas de message
d'erreur, débuggable uniquement à l'inspection). Bug vécu en session
16 mai : 56 stamps + 15 tabs n'apparaissaient pas.

✅ **Pattern correct** : `<img>` + `filter` CSS chain.

**Recette `--gold-400`** (`#d4af5a`) — filigrane stamps origines menus :

```css
.stamp-origin img {
  filter: brightness(0) saturate(100%) invert(73%) sepia(20%) saturate(852%)
          hue-rotate(2deg) brightness(91%) contrast(85%);
}
```

**Recette `--orange-500`** (`#d97a2a`) — accent CTAs, eyebrows actifs :

```css
.icon-orange img {
  filter: brightness(0) saturate(100%) invert(56%) sepia(73%) saturate(652%)
          hue-rotate(348deg) brightness(89%) contrast(89%);
}
```

**Recette `--cream-50`** (`#faf3e2`) — version sur fond noir :

```css
.icon-cream img {
  filter: brightness(0) saturate(100%) invert(94%) sepia(11%) saturate(540%)
          hue-rotate(335deg) brightness(96%) contrast(89%);
}
```

**Recette `--cream-50` opacity 0.6** — inactif/disabled :

```css
.icon-cream-faded img {
  filter: brightness(0) saturate(100%) invert(94%) sepia(11%) saturate(540%)
          hue-rotate(335deg) brightness(96%) contrast(89%);
  opacity: 0.6;
}
```

Le `brightness(0)` force tout en noir (peu importe stroke/fill/text/
textPath) puis le reste recolore par teinte. Marche sur tout SVG
monochrome qui contient du `<text>`.

### Variants stamps origines

| Variant       | Taille                  | Rotation | Opacity | Position canonique           |
|---------------|-------------------------|----------|---------|------------------------------|
| **watermark** | 218×124 desktop         | -9°      | 0.72    | `top:46px right:18px`        |
|               | 190×108 mobile          | -9°      | 0.72    | (caché desktop only)         |
| **inline**    | 38×22                   | 0°       | 1       | Inline avec Nº item mobile   |

### Stamps signature (6 SVG, usage transverse)

| Asset                          | Usage canonique                                        |
|--------------------------------|--------------------------------------------------------|
| `assets/compass-rose.svg`      | Rose des vents 32 rhumbs, partout (sections, atmospheres) |
| `assets/coord-stamp.svg`       | Badge coordonnées `45°04′N · 5°33′E` inline            |
| `assets/world-map.svg`         | Carte du monde filigrane fond `.hi-worldmap`            |
| `assets/stamp-vercors.svg`     | Tampon rond `◉ VERCORS · 1050M` rotated -6°            |
| `assets/stamp-entree-libre.svg`| Bandeau ovale `◉ ENTRÉE LIBRE` cards concerts          |
| `assets/stamp-par-avion.svg`   | Bande hachurée rouge/bleu `PAR AVION · VIA AIR MAIL`   |

### Règle d'or stamps

**1 stamp watermark grand format par section maximum.** Au-delà, on satue
visuellement. Pour les pages denses (Menus 13 catégories), 1 stamp par
ligne d'item est OK car il est en filigrane derrière le texte (opacity
0.72) — il ne concurrence ni le nom du plat ni le prix.

---

## Icônes

### Inventaire — 15 icônes line-art catégories menu

Dans `assets/tabs/` :

**Food (8)** :
- `tapas.svg` — assiette + ramequins + olivier
- `planches.svg` — planche + saucisson + couteau
- `fumaison.svg` — poisson + volutes
- `currys.svg` — bol + piment + anis
- `pates.svg` — assiette + spaghetti + basilic
- `woks.svg` — wok + flammes
- `salades.svg` — saladier + feuilles + couverts
- `desserts.svg` — coupe + boules + cerise

**Drink (5)** :
- `vins.svg` — verre + carafe + grappe
- `bieres.svg` — mug + mousse + bulles
- `cocktails.svg` — verre triangle + olive + paille
- `softs.svg` — verre + citron + bulles
- `bar.svg` — tasse + vapeur

**Emporter (2)** :
- `sandwichs.svg` — baguette + ingrédients + kraft
- `bowls.svg` — bol + baguettes + vapeur

### Style line-art HIBOUBOX

| Paramètre              | Valeur                                       |
|------------------------|----------------------------------------------|
| **Stroke width**       | `1.4-1.6px` (jamais en dessous, jamais au-dessus) |
| **Stroke linecap**     | `round`                                      |
| **Stroke linejoin**    | `round`                                      |
| **Fill**               | `none` (line-art pur, pas de surface pleine) |
| **Opacity layers**     | Détails décoratifs en `opacity="0.55"`, accents principaux en `opacity="1"` |
| **Decorative dots**    | `<circle r="1.2" opacity="0.6">` (points de bornage) |

### Recolorisation icônes (filter chain)

Même mécanique que les stamps origines (cf. ci-dessus).

**État actif `--orange-500`** :
```css
.subtab.active .subtab-ico {
  filter: brightness(0) saturate(100%) invert(56%) sepia(73%) saturate(652%) hue-rotate(348deg) brightness(89%) contrast(89%);
}
```

**État inactif `--cream-50` opacity 0.6** :
```css
.subtab .subtab-ico {
  filter: brightness(0) saturate(100%) invert(94%) sepia(11%) saturate(540%) hue-rotate(335deg) brightness(96%) contrast(89%);
  opacity: 0.6;
}
```

### Tailles canoniques icônes

| Contexte                  | Taille desktop | Taille mobile |
|---------------------------|----------------|---------------|
| Sub-tabs menu             | 38px           | 28px          |
| Card head ico cercle      | 56×56 padding 14px | 44×44 padding 10px |
| Mini-info band cell       | 46×46 padding 12px | 30×30 padding 10px |
| CmRhythmIcon (bandeau 4 cells) | 56×56 padding 7-8px | 48×48 padding 7-8px |
| Pill téléphone ico        | 18-20px        | 18px          |
| Inline contact ico        | 12-14px        | 12px          |

### Icônes inline composées (non-fichier SVG)

Pour les icônes ultra-simples (◉ ◯ ▾ ↗ ✸ ★ ▴ ▸ ⟶), on utilise des
**glyphes Unicode** directement, **jamais en marker de bullet ou step au
milieu d'un texte éditorial**. Usage canonique :

- `◉` — Stamp eyebrow / cartouche / marker actif
- `◯` — Stamp variant alternatif / état non-actif
- `▾` / `▴` — Chevron dropdown collapsed / expanded
- `↗` — CTA arrow pointing out (lien externe, "voir sur Instagram")
- `→` — CTA arrow primary action
- `✸` / `★` — Marker featured / important
- `‹` / `›` — Navigation prev/next modale/calendar
- `𝄞` — Clef de sol musique
- `♩ ♪ ♬ ♫` — Notes musique
- `▾ ▴ ▸ ▴ ▾` — Spinner number field custom

❌ **JAMAIS d'emoji décoratif** (🚀 ✨ 🎯 ⚠ ✓ ☕ 📷 📅) dans une copy
HIBOUBOX qui se présente comme lettre / manifesto / éditorial / dossier.
Pictos typographiques uniquement (`◉ ✸ ▾ ↗`).

---

## Components

Cette section décrit les **composants visuels** du brand HIBOUBOX en
prose pure — sans API ni langage d'implémentation. Chaque composant est
un atome de composition réutilisable sur tous les médiums (web · print ·
social · packaging · signalétique).

### Inventaire des composants

| Composant            | Rôle visuel                                                            |
|----------------------|------------------------------------------------------------------------|
| Bouton               | Appel à l'action — 3 niveaux d'intensité et 3 tailles                 |
| Tampon (Stamp)       | Badge décoratif passport (rond/ovale, dashed border)                  |
| Carte (Card)         | Conteneur de contenu (passport paper)                                 |
| Badge inline         | Étiquette mono compacte                                               |
| Chip / Pill          | Étiquette pill-shaped (filtres, genres, tags)                         |
| Eyebrow              | Label mono uppercase orange au-dessus d'un titre                      |
| Display              | Titre Bungee massif                                                   |
| Script               | Tagline cursive italique (Cormorant Garamond)                         |
| Wave                 | Séparateur courbé entre deux sections                                 |
| Compass / Rose des vents | Décor cartographique                                              |
| Music staff          | 5 lignes + clef de sol en décor jazz                                  |
| Coord Badge          | Pill mono coordonnées géographiques                                   |
| Section cartouche    | Signature cartographe en marge de section                             |
| Halo featured        | Aura orange pulsante autour d'un élément à la une                     |

### Bouton — matrice complète

Le bouton porte deux dimensions : son **niveau d'intensité** (primary /
outline / ghost / gold) et sa **taille** (compact / base / feature).

**Niveaux** :

| Niveau    | Fond                   | Texte         | Bordure                   | Au survol                                 |
|-----------|------------------------|---------------|---------------------------|-------------------------------------------|
| Primary   | `#d97a2a` (orange-500) | `#0a0908` (ink-1000) | aucune              | fond `#ea934a` (orange-400) + scale 1.02  |
| Outline   | transparent            | `#d97a2a`     | `1.5px solid #d97a2a`     | wash orange `rgba(217,122,42,.10)`        |
| Ghost     | transparent            | `#faf3e2` (cream-50) | `1px dashed cream-50/40` | wash cream `rgba(250,243,226,.06)`  |
| Gold      | `#d4af5a` (gold-400)   | `#0a0908`     | aucune                    | fond `#b88f3a` (gold-500) + scale 1.02    |

*La variante `gold` est réservée à la sous-marque Festin du Hibou et
aux supports artisanaux/cuisine. Sur le brand HIBOUBOX principal,
toujours `primary` ou `outline` (orange).*

**Tailles** :

| Taille    | Font-size | Padding     | Hauteur | Letter-spacing | Usage canonique                            |
|-----------|-----------|-------------|---------|----------------|--------------------------------------------|
| Compact   | `12px`    | `8px 18px`  | `36px`  | `0.16em`       | Header / nav / petites actions             |
| Base      | `14px`    | `12px 22px` | `44px`  | `0.14em`       | CTAs inline secondaires                    |
| Feature   | `16px`    | `16px 26px` | `54px`  | `0.12em`       | CTA principal hero / fin de section        |
| In-card † | `18-26px` | `16-22 × 22-38` | auto | `0.10-0.14em`  | CTA dans une carte (voir ci-dessous)       |

**Bouton commun à tous les niveaux** : pill complet (`border-radius:
9999px`), font Barlow Condensed weight 700, **texte en majuscules**,
flèche orientée (`→` `↗`) AVANT le label pour appeler à l'action, jamais
après. Transition `transform .25s` + `background-color .25s`.

#### Focus clavier — spec `:focus-visible` (WCAG 2.4.7 / 2.4.11)

Tout élément interactif (boutons, liens, inputs, chips, cards cliquables)
doit afficher un indicateur de focus clavier visible. Recette canonique :

```css
:focus-visible {
  outline: 2px solid var(--orange-400);   /* #ea934a — 7.7:1 sur ink-900 */
  outline-offset: 3px;
  border-radius: inherit;                  /* épouse la forme pill ou card */
}

/* Supprime l'outline pour les utilisateurs souris/tactile */
:focus:not(:focus-visible) {
  outline: none;
}
```

**Pourquoi `outline: 2px solid` et pas `1px dashed`** : WCAG 2.4.11 (AA,
nouveau en 2.2) exige une surface d'indicateur ≥ périmètre du composant ×
2px. Un trait de 1px à 55 % d'opacité ne satisfait pas ce critère. Le
`2px solid orange-400` à pleine opacité passe le ratio de changement
visuel 3:1 requis (fond ink-900 → outline orange 7.7:1).

**⚠ Ne pas confondre** le pattern décoratif "tampon postal officiel"
(`1px dashed rgba(217,122,42,.55)`) avec le focus clavier : l'un est une
texture esthétique, l'autre est une obligation d'accessibilité.

#### Bouton dans une carte — règle critique

Un bouton inscrit dans une carte d'information (concert, produit,
service, événement) **n'utilise jamais la taille compact ou base** : ces
tailles sont illisibles à bout de bras sur mobile. Tout bouton in-card
respecte ce minimum :

- **Font-size ≥ 18px desktop / 15px mobile**
- **Weight 700**
- **Padding minimum 16×20px**
- **Largeur** : full-width de la carte la plupart du temps (un seul CTA
  par carte, prend toute la largeur du body, devient une zone d'appel
  claire au lieu d'un bouton perdu)

Les CTA hero peuvent monter jusqu'à 26px desktop / 18px mobile pour
imposer leur autorité sans se confondre avec le corps de texte.

### Tampon (Stamp)

Badge décoratif passport — la signature visuelle HIBOUBOX. Format
**rond, ovale, ou rectangulaire arrondi** (mais jamais carré net),
bordure `1.5px solid orange-500` doublée d'un anneau dashed offset 4px
intérieur, fond `--ink-1000` ou transparent.

**Composition canonique** :
- Cœur du tampon : 1 ligne mono uppercase orange-500 ou cream-50 (ex.
  `◉ NOUVEAU · CONCERT`, `◉ ENGAGEMENT · MMXXII`, `↗ EXPÉDIÉ`)
- Optionnel : sub-line italique Cormorant en dessous (`édition mai 2026`)
- Rotation entre `-9°` et `+9°` (jamais 0° en signature, toujours 0°
  en signalétique fonctionnelle)
- Tailles canoniques : `S` 28×28, `M` 56×56, `L` 92×92, `XL` 140×140

Usages : signature en marge de section (`SectionCartouche`), overlay
sur photo hero (top-left/right rotated), tampon de date sur affiche
concert, sceau d'authenticité sur carte de visite, marker sur carte
géographique.

### Carte (Card)

Conteneur de contenu — bloc d'information dense avec habillage passport.

**Variants chromatiques** :
- Card sur fond `--ink-900` : fond `--ink-800`, bordure `1px solid
  rgba(255,255,255,.04)`
- Card sur fond `--ink-800` : fond `--ink-900`, bordure idem
- Card featured (à la une) : bordure remplacée par `1.5px solid
  --orange-500` + halo pulsant (cf. plus bas)

**Padding standard** : `24-32px` desktop, `18-22px` mobile.
**Border-radius** : `12px` (lg).

**Composition canonique en 3 zones** :
1. Card head (haut) — icône cerclée dashed orange + eyebrow + séparateur
   dashed orange en dessous
2. Card body (milieu) — titre Display + body Lato + liste k/v si
   pertinent
3. Card foot (bas) — CTA full-width (bouton in-card 18px+), push à
   `margin-top: auto` pour aligner sur d'autres cards côte à côte

Pour aligner deux cards côte à côte à la même hauteur (typique d'un
grid 2 colonnes) : laisser le grid en `align-items: stretch`, la card
en `flex direction column height 100%`, et un élément central absorber
le surplus en `flex: 1 1 auto`.

### Badge inline

Petite étiquette mono Special Elite, padding `4×10px`, font-size
`10-12px`, bordure `1px solid` ou `1px dashed` selon contexte. Variants
de couleur : orange (dominante), cream sur fond sombre, gold (Festin).
Usage : numéro de fiche (`FICHE Nº 04`), étiquette de catégorie
(`SCULPTURE`), marqueur de date.

### Chip / Pill

Étiquette pill-shaped `border-radius: 9999px`, fond `--ink-700` ou
transparent + dashed border, padding `8-12 × 14-22px`, font-size
`11-14px`. Plus voyant qu'un badge, sert pour les **filtres
toggleables** (genres, médiums, régimes), les **tags de classification**
(jazz manouche, blues), ou les pills de contact (téléphone, email).

### Eyebrow

Petit label posé **au-dessus** d'un titre Display, en mono uppercase
Barlow Condensed `11-14px` (hero `18-22px`), color `--orange-500`,
letter-spacing `0.20-0.28em`, weight 600. **Toujours majuscules**.

Standard HIBOUBOX (à respecter scrupuleusement) :
- Section standard : 19px desktop / 15px mobile
- Hero de page : 22px desktop / 16px mobile
- Card head : 22px desktop / 18px mobile (calage canonical Info card)
- Card content : 14-15px desktop / 12-13px mobile

### Display

Titre serif Bungee. Tailles canoniques :
- Hero page : `92px` desktop / `48px` mobile, line-height `0.9`,
  letter-spacing `-0.01em`
- Section : `60-68px` desktop / `38-42px` mobile
- Card hero : `38-44px` desktop / `26-30px` mobile

**Accent inline** — pattern brand HIBOUBOX : **un mot du titre passe en
accent coloré** (orange-500 sur HIBOUBOX, gold-400 sur Festin) pour
créer un rythme visuel. Exemple : `TRIO MARLOWE` avec MARLOWE en
orange, ou `Le Festin du Hibou` avec "Festin du Hibou" en gold.

### Script

Tagline cursive italique Cormorant Garamond. Tailles canoniques :
- Hero accompagnement : `38-60px` desktop / `22-34px` mobile, italic
  mandatory
- Citation pleine largeur : `26px` desktop / `19px` mobile
- Section sub-line : `22-32px` italic

`text-wrap: balance` recommandé pour équilibrer le wrap. Toujours en
italique (jamais regular).

### Wave

Séparateur courbé entre deux sections de tonalité ink différente
(ink-900 ↔ ink-800), construit comme une courbe sinusoïdale douce en
SVG, **complétée par un dashed orange passport-stitch en
superposition** (effet "ticket déchiré").

Hauteur standard `80px`, peut monter à `120px` sur les sections hero ou
fin de page pour plus de respiration. Inversion verticale possible
(`flip`) selon le sens de la transition tonale.

### Compass / Rose des vents

Rose des vents SVG cartographique posée en décor de section (`opacity
0.15 - 0.40`). Position absolue dans la section, dimensionnée entre
`70px` (mobile) et `140px` (hero), rotation au choix selon composition.

**Règle d'orchestration** : 1 compass par section maximum, position
roulante (top-right → top-left → bottom-right → bottom-left) pour
éviter la monotonie. Jamais 2 compass sur la même section.

### CoordBadge

Pill mono Special Elite, bordure dashed orange, padding `4×12px`,
font-size `11-13px` (hero `15px`). Format texte canonique :
`◉ {LAT}°{MIN}′{SEC}″N · {LONG}°{MIN}′{SEC}″E`.

Variant transparent (sur fond ink) ou plein (fond `--ink-1000`). Usage :
hero (juste sous l'eyebrow), card Accès, hero atmo, signature
cartographe.

### Section cartouche

Signature cartographe posée en bas de section ou en marge, format
canonique :
```
{ROLE} Nº {N ROMAIN} · {SUB-LATIN}
{HIBOUBOX} · {ED. MMXXVI}
```
Exemples : `CARTA Nº V · DOMUS NOSTRA` / `HIBOUBOX · ÉD. MMXXVI`.

Position absolue, côté gauche ou droit, rotation entre `-3°` et `+3°`
maximum (toujours légèrement penché, signal "écrit à la plume"). Font
mono Special Elite, opacity 0.62-0.78, color cream-50.

### Music staff

5 lignes dashed orange en fond décoratif évoquant une portée musicale,
augmentée d'une clef de sol `𝄞` + 4 à 6 notes avec tiges et drapeaux.
Posée en `top` ou `bottom` de section, rotation `-5°` à `+5°`. Opacity
`0.18 - 0.32`. Réservé aux pages programmation / concerts / jazz.

### Halo featured (pattern, pas composant)

Halo orange pulsant autour d'un élément à la une (plat star, concert
prochain, expo en cours). Voir section **Elevation & Depth** pour la
recette CSS complète.

**Règle d'or** : le halo **n'altère ni la position, ni la taille, ni
l'alignement** de l'élément hôte. Il s'ajoute en superposition (`box-
shadow` + `inset shadow`), sans modifier la grille de composition. Sur
support print où l'animation n'existe pas, le halo se fige en bordure
orange pleine + outline dashed offset.

---

## Patterns transverses

Cette section décrit des **patterns de composition visuels génériques**
applicables sur tous les médiums (affiche, post, page, newsletter,
signalétique, packaging). Pas d'API ni d'implémentation — uniquement la
recette de composition, les proportions, et les règles d'orchestration.

### Pattern · Anatomie d'une section

Toute section longue (page web, page magazine, panneau de signalétique,
double-page) se compose dans cet ordre :

```
┌──────────────────────────────────────────────────────────┐
│   fond ton sur ton (ink-900 ou ink-800)                  │
│   ↳ carte du monde en filigrane (opacity 0.04 - 0.08)    │
│   ↳ rose des vents en coin (opacity 0.20 - 0.35)         │
│   ↳ 1 artefact signature unique                          │
│      (route dashed · isohypses · music staff · grille)   │
│                                                          │
│      ┌─ eyebrow mono uppercase orange                    │
│      │  Display serif accent                             │
│      │  Body Lato 17-20px                                │
│      └─ contenu (cards · listes · timeline · photos)     │
│                                                          │
│   ↳ cartouche signature en bas-droite ou bas-gauche      │
│      (CARTA Nº X · SUB-LATIN · HIBOUBOX MMXXVI)          │
└──────────────────────────────────────────────────────────┘
   ↓ Wave séparateur dashed orange passport-stitch
┌──────────────────────────────────────────────────────────┐
│   section suivante (ton inverse)                         │
```

**Règles d'or de la section** :
- **Un seul artefact signature** par section (jamais 2 routes
  superposées, jamais 2 music staff)
- **Compass position roulante** : top-right → top-left → bottom-right
  → bottom-left au fil des sections
- **Wave alterne ink-900 / ink-800** pour le rythme tonal
- **Atmosphere concentrée dans les zones visibles** — pas de décor
  caché derrière une card

### Pattern · Hero standard

Composition canonique du hero de page (ou de la zone-titre d'une
affiche, d'un cartel, d'un cover newsletter) :

| Élément                    | Valeur                                         |
|----------------------------|------------------------------------------------|
| Grid (web)                 | `1.18fr / 1fr` desktop · `1fr` mobile          |
| Gap colonnes               | 36px desktop · 32px mobile                     |
| Max-width contenu          | 1280px                                         |
| Alignement vertical        | `start` (pas `center`)                         |
| Photo / visuel principal   | outline solid orange-500 1.5px + outline dashed offset 4px + 4 corner ticks aux angles |
| Stamp signature            | top-right INTÉGRÉ dans la photo, rotation `-6°` à `-9°` |
| Padding section            | `100/60/60px` desktop · `64/20/36px` mobile    |

**Composition meta colonne** (côté droit en desktop, en dessous en
mobile) :
1. Eyebrow mono uppercase orange (22px desktop / 16px mobile)
2. Coord badge dashed orange (15px desktop / 12px mobile)
3. Display Bungee massif (92px desktop / 48px mobile) avec **un mot en
   accent orange**
4. Script italique Cormorant 34-60px en sous-titre
5. Lead serif italique 22-28px (3 lignes max)
6. CTAs (max 2, primary + outline)
7. Optionnel : bandeau mini-infos plein-largeur en dessous du hero-grid
   (4 cellules dashed orange : lieu · entrée · tél · service)

### Pattern · Card information dense (canonical Info Pratiques)

Pattern d'une "carte d'information" applicable partout où il y a une
adresse + horaires + contact + CTA(s) (page web, dépliant print, carte
de visite recto, vitrine signalétique).

**Anatomie verticale** (5 zones, dans cet ordre) :

```
┌─────────────────────────────────────┐
│  CARD HEAD                          │
│  ↳ icône 56×56 dashed orange        │
│  ↳ Eyebrow 22px uppercase orange    │
│  ↳ ligne dashed orange en séparateur│
├─────────────────────────────────────┤
│  ADDRESS BLOCK (encadré dashed)     │
│  ↳ 41 rue des Pionniers (serif 24px)│
│  ↳ 38250 · Villard-de-Lans (16px)   │
│  ↳ ◉ 45°04′N · 5°33′E (mono orange) │
├─────────────────────────────────────┤
│  INFO LIST (k/v dashed orange)      │
│  ↳ HORAIRES   Mar→Sam · 18-22h      │
│  ↳ CONCERTS   20h30 · entrée libre  │
│  ↳ EMAIL      contact@hiboubox.fr   │
├─────────────────────────────────────┤
│  CONTACT ROW (pill centrée)         │
│  ↳ ☎ 04 76 95 11 79                 │
├─────────────────────────────────────┤
│  CTA FOOTER (push margin-top: auto) │
│  ↳ → RÉSERVER UNE TABLE             │
│  ↳ → PROGRAMMATION (outline)        │
└─────────────────────────────────────┘
  + 4 corner ticks dashed orange aux angles internes
```

**Sizing canonique** (à respecter sinon la carte ne lit pas) :

| Élément              | Desktop                  | Mobile          |
|----------------------|--------------------------|-----------------|
| Card-head icône      | 56×56 dashed orange      | 44×44           |
| Eyebrow              | 22px / 0.22em            | 18px / 0.18em   |
| Address-line serif   | 24px weight 600          | 19px            |
| Info-list key (mono) | 13.5px orange / 0.20em   | 12.5px          |
| Info-list value      | 16px body cream / 1.55   | 15px            |
| Contact-pill         | 19px / padding 16×22     | 16px            |
| CTA in-card          | 16-18px / padding 18×22  | 13.5px          |

### Pattern · Cadre passport encastré

Pour intégrer un contenu encastré (widget tiers, vidéo embed, formulaire
externe, QR code, carte interactive) dans la grammaire HIBOUBOX sans
renoncer à l'identité visuelle.

**Anatomie** :

```
┌──────────────────────────────────────┐
│  ◉ TOPSTRIP ORANGE · libellé court   │ ← bandeau gradient orange-600 → orange-500
├──────────────────────────────────────┤
│  ┐                                  ┌ │ ← 4 corner ticks dashed orange en débord
│                                       │
│      CONTENU ENCASTRÉ                 │   (iframe, image, QR, carte,
│      (zone neutre, fond ink-1000)     │    table de tarifs, etc.)
│                                       │
│  ┘                                  └ │
├──────────────────────────────────────┤
│  Foot note discrète — italique         │ ← mention "Widget tiers · habillé en prod"
│                                       │   ou crédit photo, ou source
└──────────────────────────────────────┘
```

**Règles** :
- Cadre extérieur `1.5px solid orange-500` doublé d'un outline dashed
  offset 4px
- Hauteur uniforme par contexte (440-560px web, A4 ratio en print)
- **Pas de drop-shadow** — c'est le dashed qui crée la profondeur
- Topstrip court (1 ligne, mono uppercase orange-foncé sur orange clair
  ou cream sur ink) — sert d'étiquette de catégorie
- Foot note italique Cormorant, opacity 0.55-0.62 — discret mais lisible

### Pattern · Lettre / manifeste (disclosure parchemin)

Pour exposer un texte long (manifesto, charte, lettre éditoriale,
politique, conditions générales) avec une grammaire visuelle papier
ancien — applicable sur page web (dépliable), affiche A3, double-page
magazine, livret d'accompagnement.

**Composition du parchemin** :

```
              ╔═════════════════════════════════╗
              ║   ◉  parchemin clip-path        ║  ← 32 points découpés main
   ╔══════════║   bords irréguliers             ║═══════════╗
   ║          ║                                 ║           ║
   ║ scotch   ║   filigrane SVG carto opacity   ║   scotch  ║   ← scotch tape rotated
   ║ tape     ║   0.16-0.32 derrière le texte    ║   tape    ║       aux 4 coins
   ║          ║                                 ║           ║
   ║          ║   TITRE serif italique          ║           ║
   ║          ║   « ouverture en sous-titre »    ║           ║
   ║          ║                                 ║           ║
   ║          ║   I.  premier mouvement         ║           ║   ← numérotation romaine
   ║          ║       texte serif justifié      ║           ║
   ║          ║                                 ║           ║
   ║          ║   II. second mouvement          ║           ║
   ║          ║                                 ║           ║
   ║          ║   III. troisième mouvement      ║           ║
   ║          ║                                 ║           ║
   ║          ║   ╭─ signature paraphe SVG ─╮   ║           ║
   ╚══════════║   ╰────────────────────────╯   ║═══════════╝
              ║                                 ║
              ╚═════════════════════════════════╝
```

**Règles** :
- Fond `--ink-800` ou `--ink-900` (jamais blanc — l'effet parchemin
  vient du contraste papier-cream sur ink-foncé)
- Double radial-gradient cream+gold très subtil pour le grain
- Filigrane carto SVG en arrière-plan opacity 0.16-0.32 (grille
  lat/long + rose des vents centrale + cartouche cartographe +
  isohypses)
- Texte serif Cormorant italique pour les leads/manifestos, Lato pour
  les paragraphes longs (lisibilité)
- **Aucun emoji décoratif** dans le corps de la lettre — la grammaire
  est plume + tampon, pas slack + memoji
- Numérotation **romaine en accent serif italique** (I/II/III/IV), pas
  arabique

### Pattern · Timeline boarding-pass (4 étapes)

Pour décrire un déroulé temporel (programme soirée, étapes d'une
commande, parcours d'une expo, jalons d'un partenariat).

**Composition horizontale 4 cellules** (web desktop) / **stack vertical
4 lignes** (mobile + print A5+) :

```
┌───────────┬───────────┬───────────┬───────────┐
│   01      │   02 ★    │   03      │   04      │
│   ▴ 18h00 │   ▴ 20h30 │   ▴ 21h10 │   ▴ 21h30 │
│           │   [HALO]  │           │           │
│ OUVERTURE │ PREMIER   │ ENTRACTE  │ SECOND    │
│ DU SERVICE│ SET       │ BAR       │ SET       │
│           │           │           │           │
│ Service   │ 30-40 min │ Pause +   │ Rappels   │
│ à table   │ acoustique│ ouverture │ usuels    │
│ dès 18h   │           │ du bar    │ fin 22h30 │
└─────·····─┴─····─[★]──┴────·····──┴───────────┘
   ↑ dashed connectors (cachés mobile)
```

**Règles** :
- **Numérotation 01/02/03/04** en badge top-left dashed orange (mono
  Special Elite 12px, weight 700)
- L'étape highlight (le moment-clé du déroulé) reçoit le **halo orange
  pulsant** + fond renforcé — toujours **une seule** étape highlightée
- Time mono Special Elite avec icône `▴` (heure de bascule) ou `◉`
  (jalon)
- Titre étape uppercase Barlow Condensed 22px weight 700 (mobile 18px)
- Description body Lato 16px line-height 1.55 (mobile 15px)
- Connecteurs `·····` dashed entre cellules — décor seulement, masqué
  en mobile/stack
- En **print** (flyer A5, programme papier) : version compacte sur 2
  colonnes plutôt que 4

### Pattern · Strip plein-largeur signature

Pour terminer une section avec un appel à l'action léger (newsletter,
soft CTA, mention partenariat) sans bloc lourd.

**Composition** :

```
╔═══════════════════════════════════════════════════════════╗
║  ┌─ Nº III · MENSUEL (stamp tilté rotated -2°)            ║
║  │                                                        ║
║  │  Une fois par mois, *rien de plus*.                    ║   ← Display 32px avec accent orange
║  │  3 lignes de contexte éditorial maximum.               ║       sur un mot
║  │                                                        ║
║  └─ [email input full-width] [→ SUBMIT]                   ║   ← form inline, 1 ligne
╠═══════════════════════════════════════════════════════════╣
║  ◉ PAS DE SPAM · ◉ DÉSINSCRIPTION 1 CLIC · ◉ DONNÉES NON CÉDÉES  ║   ← bandeau garanties full-width
╚═══════════════════════════════════════════════════════════╝
```

**Règles** :
- Cadre solid orange + outline dashed offset 4px + 4 corner ticks
- Stamp tilté `Nº III · MENSUEL` (ou équivalent : `Nº I · APPEL` /
  `Nº II · INVITATION`) en débord haut-gauche, rotation -2°
- Grid editorial / form `1.4fr / 1fr` desktop, stack 1 col mobile
- Bandeau garanties en bas (3 items mono uppercase séparés par `·`,
  opacity 0.78, fond ink-1000)
- **Pas plus de 3 garanties** — au-delà ça devient encombrant

### Pattern · Marquee partenaires / défilement infini

Pour un défilement horizontal d'éléments répétés (logos partenaires,
labels presse, certifications, mentions clients).

**Composition** :

```
   ┌─────────────────────────────────────────┐
   │  ← fondu gauche               fondu →   │   ← mask-image linear-gradient
   │                                         │       aux extrémités
   │   [logo] [logo] [logo] [logo] [logo]    │
   │      ↘ défile à vitesse constante       │
   │                                         │
   └─────────────────────────────────────────┘
```

**Règles** :
- Largeur de la marquee `66%` du parent (max 920px desktop, 100%
  mobile) — laisse de la respiration en marge
- `mask-image: linear-gradient` aux deux extrémités pour le fondu
- Animation `48s linear infinite` desktop, `30s` mobile
- **Triplé en interne** (items × 3) pour boucle invisible
- Pause au survol (`animation-play-state: paused`)
- Respect `prefers-reduced-motion: reduce` → animation: none

### Pattern · Anatomie d'une atmosphere

Une "atmosphere" est l'écosystème décoratif d'une section — l'ensemble
des éléments visuels en couches qui donnent à la section son identité
narrative.

**Couches canoniques** (de l'arrière vers l'avant) :

1. **Fond ton sur ton** (`--ink-900` ou `--ink-800`)
2. **Carte du monde** en filigrane (opacity 0.04-0.08, `mask-image`
   pour fondu aux bords)
3. **Grille lat/long sobre** (opacity 0.10-0.18, lignes hairline)
4. **Croisillons sextants** aux intersections clés (3-5 max, jamais
   centrés sur le texte)
5. **Artefact signature unique** :
   - Section musicale → music staff + clé de sol + notes
   - Section cartographique → route dashed bezier avec marqueurs ▲
   - Section éditoriale → portée romaine I/II/III/IV
   - Section postal → cachet d'oblitération + enveloppe + timbre
6. **Placenames latins** (3 maximum, opacity 0.32-0.55)
7. **Cotes Vercors** (sommets ▲ + altitudes)
8. **Cartouche signature** en bas (`CARTA Nº X · SUB-LATIN`)
9. **Rose des vents** en coin (mini ou XL selon densité)

**Toutes les couches en `aria-hidden="true"`** (décor pur, ignoré par
les lecteurs d'écran). Opacités globales 0.05 à 0.35 — le contenu
éditorial domine toujours.

---

## Atmospheres par section

Une **atmosphere** est l'écosystème décoratif qui habille une section.
Elle est composée de 6 à 10 couches superposées qui donnent à la
section son identité narrative — sans jamais concurrencer le contenu
éditorial. Sur web, en print, sur post Instagram ou sur cartel
d'exposition, la grammaire d'atmosphere est la même.

### Anatomie d'une atmosphere

Couches canoniques, de l'arrière vers l'avant :

| Ordre | Couche                      | Opacity        | Rôle                                             |
|-------|-----------------------------|----------------|--------------------------------------------------|
| 1     | Fond ton sur ton            | 1.0            | Section background (ink-900 ou ink-800)          |
| 2     | Carte du monde filigrane    | 0.04 - 0.08    | Continents en watermark global                   |
| 3     | Grille lat/long sobre       | 0.10 - 0.18    | Hairlines orange transparent                     |
| 4     | Croisillons sextants        | 0.20 - 0.32    | Marqueurs aux intersections clés                 |
| 5     | Artefact signature unique   | 0.18 - 0.42    | LE moment visuel de la section                   |
| 6     | Placenames latins (3 max)   | 0.32 - 0.55    | Toponymes narratifs `VIA · LITTERIS`             |
| 7     | Cotes Vercors (sommets ▲)   | 0.40 - 0.62    | Identité montagne (selon section)                |
| 8     | Cartouche signature         | 0.62 - 0.78    | `CARTA Nº X · SUB-LATIN`                         |
| 9     | Rose des vents              | 0.15 - 0.35    | En coin (mini ou XL selon densité)               |

### Règles d'orchestration

1. **Une seule atmosphere par section** — jamais 2 routes superposées,
   jamais 2 music staff dans la même section
2. **Vocabulaire varié entre sections d'une même page** (cf.
   § Grammaire visuelle) — alterner musical / cartographique /
   parchemin / postal pour le rythme narratif
3. **Opacités strictes** : aucun élément décoratif au-dessus de `0.55`
   sauf cartouches signature (qui peuvent monter à `0.78` pour rester
   lisibles)
4. **Décor en arrière-plan pur** — accessibilité (lecteurs d'écran)
   ignore tous les éléments décoratifs
5. **Pas d'interactivité dans l'atmosphere** — elle est observée, pas
   manipulée
6. **Concentrer le décor dans les zones visibles** — si une colonne
   s'arrête à 55 % de la section, le bas-droit est libre pour le
   cartouche signature
7. **Désactivation mobile / petit format** — si le décor encombre la
   lecture sur petit format, simplifier (ne garder que carte du monde
   + cartouche + rose des vents) plutôt que tout désactiver

### Vocabulaires par grammaire de section

| Type de section          | Vocabulaire dominant                                           |
|--------------------------|----------------------------------------------------------------|
| Hero éditorial           | Grille lat/long + sommets Vercors cotés + GR91 trail + coord stamps |
| Listing programmation    | Portée musicale + clé sol + notes + timeline boarding-pass     |
| Listing menus food       | Routes épices + tampons FAIT MAISON + recettes flottantes      |
| Listing menus drink      | Carte vinicole + grappes + isohypses                           |
| Réservation lettre       | Parchemin clip-path + rose des vents centrale + scotch tape    |
| Réservation iframe       | Cadre passport + topstrip + corner ticks                       |
| Traiteur                 | Route VIA·COQUINA + isohypses + atelier (apothicaire)          |
| Privatisation hero       | Carte topo VIA·DOMUS + bandeau capacités + croisillons         |
| À propos éditorial       | Drop caps presse + watermarks brand subtils + crêtes Vercors   |
| Contact clients          | Lettres + tampons obliteration + route VIA·LITTERIS            |
| Contact musiciens        | Portée XL + clé sol 240px + vinyle HIBOUBOX RECORDS            |
| Contact recrutement      | 5 silhouettes équipe + emblèmes métiers                        |
| Footer carta nautica     | Rose des vents 32 rhumbs + sondages + sextant + ancres         |

---

## Brand voice & copywriting

### Personnalité éditoriale

HIBOUBOX écrit comme un **café-éditorialiste**. Posture : **« papier de
magazine indépendant »** (cohérent À propos S1) — pas une fiche
commerciale, pas une plaquette, pas un brochure SaaS. Le ton est sobre,
français, légèrement formel, jamais bavard, jamais startup.

### Tonalité — 5 piliers

1. **Sobriété éditoriale** — colonnes serrées, phrases courtes-moyennes, pas de superlatifs (« le meilleur », « unique en son genre » → bannis)
2. **Singularité du lieu** — vocabulaire spécifique au lieu (voyage, escale, route, fumaisons, table, scène, accueil à table)
3. **Première personne assumée** — « j'ai repris », « ma compagne », « notre carte » (cf. texte brut intégré tel quel en À propos)
4. **Pas de geste publicitaire** — pas d'exclamation gratuite, pas de tag-line agressive, pas de « rejoignez-nous » lourd
5. **Engagement sans pose** — quand on parle des 10 % HT, c'est factuel et structurel, pas un argument marketing

### Vocabulaire signature (à privilégier)

| Mot/expression                    | Contexte                                          |
|-----------------------------------|---------------------------------------------------|
| « le voyage commence à table »    | Tagline maître                                    |
| « escale »                        | Étape, section, expérience                        |
| « route »                         | Parcours, programme, accès                        |
| « accueil exclusivement à table » | Règle d'or du lieu (bar inclus)                   |
| « fumaisons artisanales »         | Spécialité cuisine                                |
| « cuisine internationale faite maison » | Description carte                           |
| « scène vivante »                 | Programmation musicale                            |
| « accrochage »                    | Expo (singulier ou collectif, vocabulaire métier) |
| « plat du jour », jamais « du moment » | Si plat différent au quotidien               |
| « prix libre » + « 10 % HT reversés » | Modèle économique transparent                  |

### Vocabulaire à éviter

| ❌ Banni                                | Pourquoi                                |
|-----------------------------------------|------------------------------------------|
| « unique en son genre », « incomparable »| Superlatifs publicitaires               |
| « expérience inoubliable »              | Phrase générique restauration            |
| « venez nombreux »                      | Posture animateur de quartier            |
| « plat signature » (sur la carte)       | Posture chef étoilé                      |
| « plat star »                           | Marketing                                |
| « non-attablés » / « bar debout »       | Cf. règle "tout le monde s'assoit"       |
| « concert exceptionnel »                | Si chaque soir, exceptionnel ne veut plus rien dire |
| Anglicismes (foodie, hub, vibes)        | Préférer français sobre                  |

### Règles d'orthotypographie

1. **Format prix européen** : `12,00 €` (virgule, espace insécable avant €)
2. **Date FR** : `VEN 17 MAI · 20H30` (3-letter day uppercase + chiffres + mois 3-4 letter uppercase + heure format `XXhYY` ou `XXH`)
3. **Coordonnées** : `45°04′27″N · 5°33′12″E` (degrés/primes/secondes Unicode, séparateur `·`)
4. **Numéros romains** : `Nº I` (italic serif) ou `Nº I` (mono uppercase) selon contexte
5. **MAJUSCULES** sur eyebrows/cartouches/stamps/Display headlines, **tracking ≥ 0.16em**
6. **Italique** réservé Cormorant Garamond (tagline, citations, pull-quotes, captions sous photos)
7. **Tirets** : tiret cadratin `—` (longue pause), tiret demi-cadratin `–` (intervalle), trait d'union `-` (mot composé)
8. **Espace insécable** : avant `:`, `;`, `?`, `!`, et avant `€` (français standard)

### Règle "copy générique" (CRITIQUE)

❌ **JAMAIS de chiffres durs ou dates précises dans la copy de surface**.
La copy doit fonctionner **toute l'année** sans intervention éditoriale.

| ❌ Faux                                          | ✅ Bon                                                |
|--------------------------------------------------|------------------------------------------------------|
| « Trois prochaines dates d'ici fin mai »         | « Les trois prochaines dates à l'affiche. »          |
| « Concerts de juin »                             | « L'agenda à venir. »                                |
| « Vingt-quatre tirages accrochés »               | « Une sélection du parcours accroché en salle. »     |
| « Accrochage jusqu'au 28 juin »                  | (rien — la date vit dans le bloc data-bound dédié)   |
| « Six tirages sur le mur »                       | « L'accrochage. »                                    |

Les dates et chiffres restent sur les **éléments data-bound** (badges,
captions cards, modale plein écran) — pas dans les leads/intros de
section.

### Règle "pas d'emoji dans lettre" (CRITIQUE)

❌ **AUCUN emoji décoratif** (⚠ ✓ ◉ ☕ ✦ ♪ ✨ ▴ ⏸) dans un texte HIBOUBOX
qui se présente comme **lettre / manifesto / éditorial / dossier**
(parchemin Réservation, dossier artiste, citation pleine largeur,
signature).

Les emojis dans un éditorial signalent à l'œil un contenu AI-slop et
cassent la grammaire vintage carto/passport.

Grammaire correcte = **numéros romains serif italic** (`I/II/III/IV`),
**badges mono uppercase** (`Nº I`), **pictogrammes typographiques en
eyebrow/stamp seulement**.

✅ Pictos `◉ ✸ ▾ ↗` restent OK dans les contextes **UI fonctionnels**
(filtres régime menu, eyebrows de section, CTAs) — **jamais** comme
marker de bullet/step au milieu d'une lettre.

### Règle "accueil à table" (CRITIQUE)

❌ **JAMAIS** « non-attablés » / « bar debout » / « personnes qui viennent
juste boire un verre » dans la copy.

✅ La règle HIBOUBOX est : **tout le monde s'assoit**, bar intérieur
compris.

✅ Si on doit décrire le service au bar pendant l'entracte : « service
au bar exclusivement à table selon les places assises disponibles ».

### Numérotation des sections / cartouches

**Romains uppercase** : `Nº I → Nº XIV` (parfois `Nº XXX+` pour banque
de stamps). Préférer les chiffres romains :
- Sur les cartouches signature de section (`CARTA Nº V`)
- Sur les eyebrows section (`Nº III · MENSUEL`)
- Sur les drawer mobile nav (CSS counter `upper-roman`)
- Sur les step numbers de timeline (`I` `II` `III` `IV`)

Réserver les **chiffres arabes** :
- Compteurs galerie modale (`01 / 12`)
- Format dates (`17 MAI`)
- Prix (`12,00 €`)
- Code postal (`38250`)
- Capacités (`80 ASSISES`, `60-80 COUVERTS`)

---

## Sub-marque · Le Festin du Hibou

### Identité distincte mais imbriquée

**Le Festin du Hibou** = activité traiteur portée par HibouJazz SARL.
- **Logo distinct** : `assets/festin-du-hibou-black.png` (gold filter en usage)
- **Même site internet** que HIBOUBOX (pages 09 Traiteur et 10 Privatisation)
- **Mêmes supports** (carte de visite recto/verso, signalétique commune)
- **Inbox dédiée** : `contact@lefestinduhibou.fr` (signal de domaine séparé)
- **Différenciateur clé** : animation musicale via le réseau d'artistes HIBOUBOX

### Grammaire visuelle dérivée — accent gold

| Atome                  | HIBOUBOX classique     | Festin du Hibou         |
|------------------------|------------------------|--------------------------|
| Accent CTAs            | `--orange-500`         | `--gold-400`             |
| Hover CTA              | `--orange-400`         | `--gold-500`             |
| Cards borders          | dashed orange          | dashed gold              |
| Cartouches signature   | orange                 | gold                     |
| Stamps signature       | orange/cream           | gold/cream               |
| Atmospheres            | musical / cartographique | cuisine artisanale / apothicaire |

**Tous les autres atomes restent identiques** (palette ink/cream,
typographie complète, spacing, shapes, primitives UI). C'est une
**variation chromatique** d'une grammaire commune, pas une refonte.

### Vocabulaire visuel cuisine artisanale

- **Atelier · apothicaire** : étiquettes flottantes ingrédients (fumoir, herbes, épices)
- **Recettes manuscrites** : papier vieilli, écriture cursive (Cormorant italic)
- **Bocaux à conserves** : silhouettes filigrane
- **Tampons `FAIT MAISON` · `ARTISANAT`** : grammaire artisanale
- **Planches en bois** : line-art décoratif
- **Pellicule film 35mm + polaroids** : section réalisations
- **Carto VIA · COQUINA** : route cuisine (vs VIA · SPECIARUM épices)
- **Tampon postal `PAR AVION · VIA AIR MAIL`** : page Menus Emporter (correspondance)

### Vocabulaire copywriting Festin

| Phrase signature                              | Contexte                          |
|-----------------------------------------------|-----------------------------------|
| « notre cuisine se déplace chez vous »        | Tagline Traiteur                  |
| « cuisine internationale faite maison »       | Description                       |
| « fumaisons artisanales »                     | Spécialité                        |
| « tous formats de prestation »                | Formules                          |
| « animation musicale via le réseau HIBOUBOX » | Différenciateur clé               |
| « Le Festin du Hibou a son propre univers »   | Card hero de section (12a S5)     |

### Pattern card "sub-marque hero de section"

Pattern Festin promu hero de section (12a S5) — réutilisable pour toute
**présentation d'une sous-marque détachée** :

- Eyebrow `NOTRE BRANCHE TRAITEUR` (positionne le sub-domain)
- Display avec accent **gold** sur le nom de la marque (`Le Festin du Hibou`)
- Card max-width 1180px, padding 56×56 desktop, border 1.6px solid gold + outline dashed offset 6px + shadow-lg
- **Logo filigrane gold bumped** 480×170 via `<img>` + filter chain gold + opacity 0.92
- **2 tags pills mono dashed gold** (ex. `◉ Vercors · Isère` + `◯ Devis sur mesure`)
- Layout grid `1.45fr / 1fr` (description + action box centrée)
- **2 CTAs stackés** : primary mailto gold filled + secondary outline gold dashed
- Stamp top-right 1 ligne `✸ NOTRE TRAITEUR` rotated -3°
- Cartouche bas-droite `Nº V · DIRECTIO · OFFICIORUM`

### Règle de combinaison HIBOUBOX × Festin

Sur un même support combiné (carte de visite recto = HIBOUBOX,
verso = Festin · ou newsletter qui parle des deux) :
- **Header** : ink-1000 + accent ORANGE (HIBOUBOX domine)
- **Section Festin** : ink-800 + accent GOLD (signal sub-marque)
- **Transition** : bandeau "bascule éditoriale" avec route dashed
  gradient `gold → orange` (cf. pattern Traiteur S8) ou `orange → gold`
  selon sens de transition

❌ **JAMAIS** mélanger orange + gold sur un même CTA / section. Le signal
chromatique de domaine doit rester clair.

---

## Do's and Don'ts

### Do's (à respecter scrupuleusement)

✅ **Brand & identité**
- Utiliser les tokens CSS variables, jamais hex literals (`var(--orange-500)` pas `#d97a2a`)
- Stamp signature sur photo hero **intégré dans la photo top-right**, pas en débord négatif (anti-collapse mobile)
- Cartouche signature en bas de section, numérotation romaine séquentielle dans la page
- Featured items : **dériver depuis l'horloge** (`featured = UPCOMING[0]`), jamais en flag dur dans data

✅ **Typo**
- Mobile : eyebrow 19→15px / Display 60-72→38-44px / body 16→14-15px / CTA in-card 18→15px
- CTA in-card **min 18px desktop / 15px mobile** weight 700 padding ≥ 16×20
- Display avec **accent inline `<span className="accent">`** sur 1 mot pour le coloriser orange
- `text-wrap: balance` sur les titres serif et leads narratifs
- `font-variant-numeric: tabular-nums` sur tables, listes prix, ticket stubs

✅ **Layout & composition**
- Section anatomy : worldmap + Compass + 1 artefact signature + content + cartouche + Wave
- Alternance tonale `ink-900 / ink-800` entre sections, footer `ink-1000`
- 1 atmosphere par section, vocabulaire varié
- Hero ratio `1.18fr / 1fr` desktop, gap 36px, max-width 1280
- Canonical Info Pratiques card pour adresse/horaires/tel/CTAs
- Map widget habillé brand pour localiser HIBOUBOX

✅ **Stamps & icônes**
- Recolorer SVG via `<img>` + `filter` CSS chain (pas `mask-image`)
- Stamps origines : 1 watermark grand format par section max
- 4 corner ticks dashed orange pour le feel "tampon postal officiel"
- Outline dashed + offset 4px pour double-bordure passport

✅ **Comportement & accessibilité (supports digitaux)**
- Décor en `aria-hidden` (lecteurs d'écran ignorent les atmospheres)
- `prefers-reduced-motion: reduce` désactive toutes animations (halos pulsants, marquees, transitions)
- Modales / galeries : navigation flèches ← →, swipe tactile, Échap, clic backdrop, bouton ✕
- **Focus clavier** : `:focus-visible { outline: 2px solid var(--orange-400); outline-offset: 3px; }` sur tout élément interactif — WCAG 2.4.7 / 2.4.11 (voir § Focus clavier dans Components)
- **Couleur `danger`** : utiliser `#d85535` (4.6:1 AA) — jamais `#c14f2c` (3.88:1 FAIL) pour les messages d'erreur texte
- **`warm-500`** : réservé aux états `disabled` uniquement (exempté WCAG) — texte tertiaire actif → `warm-300` (9.0:1 AAA)

✅ **Copy & voice**
- Copy générique (sans dates dures) sur leads/intros de section
- Format prix `12,00 €` (virgule + insécable + €)
- Numérotation `Nº I → Nº XIV` romaine pour cartouches/section heads
- Première personne assumée sur manifesto / À propos
- Vocabulaire signature : voyage, escale, route, fumaisons, accueil à table
- "Tout le monde s'assoit" (bar intérieur exclusivement à table)

✅ **Forms (web · email · landing)**
- Champs date / sélection / nombre remplacés par popovers custom thématiques (la grammaire UI s'aligne sur la palette de la page)
- Anti-spam intégré (honeypot + challenge invisible + rate-limit IP + validation server-side)
- Mention discrète anti-spam sous chaque submit
- Cachet postal pour signaler l'inbox de destination

### Don'ts (interdits absolus)

❌ **Anti-AI-slop**
- Gradients violet/purple aggressive
- Emoji feature icons (✨ 🚀 🎯)
- Rounded cards avec left-border accent
- Inter / Roboto / Arial en Display (body OK pour Lato fallback)
- Beige/peach/pink/orange-brown page washes (sauf brand-justifié)
- Filler copy ("Feature One", lorem ipsum, stats inventées sans source)
- Icône à côté de chaque heading
- Gradient sur every background

❌ **Recolorisation & SVG**
- `mask-image` + `background-color` pour recolorer un SVG qui contient
  `<text>` ou `<textPath>` — le texte disparaît silencieusement.
  Toujours utiliser `<img>` + chaîne `filter: brightness(0) saturate(100%)
  invert(...) sepia(...) hue-rotate(...)` (cf. § Stamps).
- Inventer des emblèmes pays sans respecter la structure SVG canonique
  (anneau extérieur ovale + anneau intérieur dashed + plaque rect haute +
  emblème centré bas) — la cohérence visuelle se perd.

❌ **Composition**
- Plusieurs CTA "Réserver" rivaux dans une même section
- Email en pill cliquable rivale d'un CTA principal de section
- 2 artefacts signature dominants dans la même section
- Décor "perdu derrière les cards"
- Shadow flou bleuté générique (`0 4px 20px rgba(0,0,0,.1)`)
- Shadow colorée hors orange (violet/cyan/vert)
- `translateY(-4px)` au hover sur cards Info Pratiques (override `transform: none !important`)

❌ **Editorial & copy**
- "non-attablés" / "bar debout" / "personnes qui viennent juste boire un verre"
- Dates dures dans leads/intros de section ("Trois prochaines dates d'ici fin mai")
- Chiffres durs dans leads ("Vingt-quatre tirages accrochés")
- Mention `Accrochage jusqu'au {date}` dans copy générique
- Emoji décoratif (⚠ ✓ ◉ ☕ ✦ ♪ ✨ ▴ ⏸) dans lettre/manifesto/éditorial/dossier/signature
- "Plat du jour" featured **transporté en tête** d'une liste (toujours in-place avec halo)
- Exposer "prix majorés / concert inclus" côté client (différentiel sur place vs emporter reste implicite)
- Mention "SANS ALCOOL" sur filtres BIÈRES (l'établissement n'en propose pas)

❌ **Sub-marque & combinaisons**
- Mélanger orange + gold sur un même CTA / section
- Utiliser gold comme accent UI général (réservé filigrane stamps + grammaire Festin)
- Olive comme accent CTA (token réservé poster ink secondaire / backup)

---

## Application & exemples — cas d'usage canoniques

### Cartes brand

| Support                  | Format               | Grammaire                                         |
|--------------------------|----------------------|---------------------------------------------------|
| **Carte de visite**      | 85×55mm (recto/verso)| Recto HIBOUBOX (orange) · Verso Festin (gold) optionnel |
| **Carte de visite équipe**| 85×55mm             | Recto identique brand · Verso nom + poste + tel personnel |
| **Carton de table**      | 100×150mm verticale  | QR code menu + coord + tagline                    |
| **Carton invitation**    | A6 (105×148mm)       | Vernissage / soirée jam / privé                   |

### Print éditorial

| Support                  | Format               | Grammaire                                         |
|--------------------------|----------------------|---------------------------------------------------|
| **Carte restaurant A3**  | A3 portrait pliée    | Catalogue dense ligne-liste transparente          |
| **Carte des vins A4**    | A4 portrait          | Sous-filtres par région, stamps origines gold     |
| **Flyer concert A5**     | A5 portrait          | Poster massif + datetime stamp + meta             |
| **Affiche concert A3**   | A3 portrait          | Poster massif format collé en vitrine             |
| **Affiche concert A2**   | A2 portrait          | Poster massif format vitrine grand                |
| **Programme mensuel**    | A4 portrait          | Calendrier mois + 4-8 concerts détaillés          |
| **Catalogue expo**       | A5 portrait 8-16pp   | Dossier artiste + parcours + cartel chaque œuvre  |
| **Brochure traiteur**    | DL plié 3            | 3 formules + comment ça marche + zone + contact   |

### Signalétique

| Support                       | Format                | Grammaire                                       |
|-------------------------------|------------------------|-------------------------------------------------|
| **Enseigne extérieure**       | 800×400mm              | Logo full + tagline + coord                     |
| **Ardoise menu du jour**      | 600×900mm              | Plats du jour + prix + suggestions chef         |
| **Panneau galerie OPEN**      | 400×600mm              | `◉ GALERIE OUVERTE · ENTRÉE LIBRE`              |
| **Cartel œuvre expo**         | A6 (105×148mm)         | Titre + artiste + année + dimensions + édition  |
| **Bandeau happy hour**        | 1200×300mm horizontal  | `HAPPY HOUR · 16H → 18H · -20%`                 |
| **Panneau jam session**       | A3 portrait            | `JAM SESSION · DIMANCHE 19H30 · SCÈNE OUVERTE`  |

### Digital · Newsletters

| Support                      | Format               | Grammaire                                       |
|------------------------------|----------------------|-------------------------------------------------|
| **Newsletter mensuelle**     | 600px wide (email)   | Hero + 3-5 concerts + 1 expo + footer brand     |
| **Newsletter vernissage**    | 600px wide (email)   | Card unique vernissage + RSVP                   |
| **Newsletter open call**     | 600px wide (email)   | Dédié artistes locaux galerie                   |
| **Newsletter festin**        | 600px wide (email)   | Sub-marque gold, devis sur mesure               |

### Digital · Social media

| Support                      | Format               | Grammaire                                       |
|------------------------------|----------------------|-------------------------------------------------|
| **Post Instagram carré**     | 1080×1080            | Annonce concert/expo/plat du jour              |
| **Post Instagram portrait**  | 1080×1350            | Dense (poster concert + meta + CTA)             |
| **Story Instagram/FB**       | 1080×1920            | Vertical immersif (event teaser)                |
| **Reel cover IG**            | 1080×1920            | Mêmes contraintes Story + texte fixe top/bottom |
| **Post Facebook**            | 1200×630             | Horizontal (annonce concert/event)              |
| **Bandeau Facebook**         | 820×312              | Cover page Facebook                             |
| **Cover Twitter/X**          | 1500×500             | Cover horizontale très étirée                   |
| **OG image (sharing)**       | 1200×630             | Auto-générée pour partage URL                   |
| **Favicon**                  | 512×512 + 32×32      | Picto owl orange seul, fond transparent         |

### Packaging emporter

| Support                      | Format                | Grammaire                                       |
|------------------------------|------------------------|-------------------------------------------------|
| **Étiquette sandwich/bowl**  | 60×30mm rectangulaire  | Logo picto + nom plat + date + initiales équipe |
| **Étiquette boîte traiteur** | 80×40mm rectangulaire  | Festin gold + nom plat + ingrédients + DLC      |
| **Sac kraft brandé**         | impression directe     | Wordmark + tagline + coord                      |
| **Sticker fermeture**        | rond 40mm              | Picto owl orange + `◉ FAIT MAISON`              |

---

## Templates de génération artwork

Cette section est **machine-readable** — chaque template est une
spécification complète qu'OD peut suivre pour générer un artwork
brand-cohérent depuis un prompt utilisateur.

### Template 1 · Post Instagram carré (1080×1080)

**Usage** : annonce concert, expo, plat du jour, événement spécial, jam session.

**Spec** :

```yaml
template: post-instagram-square
dimensions: 1080×1080 px
canvas:
  background: "{colors.ink-900}"
  texture: "tex-grain opacity 0.07"
  padding: 80px
layout: vertical-stack
sections:
  - role: header
    height: 90px
    content:
      - eyebrow:
          font: "{typography.eyebrow-md}"
          color: "{colors.orange-500}"
          tracking: 0.28em
          text: "◉ {GENRE} · {DATE_LATIN}"
      - corner-stamp-top-right:
          asset: "compass-rose.svg"
          size: 70
          opacity: 0.32
  - role: main
    height: 720px
    align: center
    content:
      - display:
          font: "{typography.display-xl}"
          color: "{colors.cream-50}"
          size: clamp(72, 92)
          accent-word: 1
          accent-color: "{colors.orange-500}"
          text: "{ARTIST_NAME}"
      - script:
          font: "{typography.script-md}"
          color: "{colors.orange-400}"
          text: "« {TAGLINE_OR_INSTRUMENTS} »"
      - datetime-stamp:
          frame: "1.5px solid orange-500 + outline dashed offset 4px + 4 corner ticks"
          padding: 24×32
          content:
            - date-top: "{DAY_FR} {DATE} {MONTH_FR}"
            - time: "{TIME_START} → {TIME_END}"
            - bottom: "◉ {SUBTITLE} (ex: DEUX SETS · ENTRACTE 21H10)"
  - role: footer
    height: 110px
    align: bottom-center
    content:
      - cta:
          background: "{colors.orange-500}"
          color: "{colors.ink-1000}"
          font: "{typography.eyebrow-md}"
          padding: 16×26
          radius: "{rounded.full}"
          text: "→ RÉSERVER UNE TABLE"
      - coord-stamp:
          align: bottom-center
          color: "{colors.cream-50}"
          opacity: 0.5
          text: "◉ HIBOUBOX · 41 RUE DES PIONNIERS · VILLARD-DE-LANS"
atmosphere:
  signature-artefact-pick-one:
    - music-staff: { position: bottom, opacity: 0.18 }
    - lat-long-grid: { opacity: 0.08 }
    - placename-latin: { text: "VIA · MUSICA", rotation: -8, opacity: 0.55 }
  cartouche: { text: "POST Nº {N} · MMXXVI", side: bottom-right, opacity: 0.55 }
variables:
  - ARTIST_NAME: string required
  - GENRE: string required (ex: "JAZZ MANOUCHE")
  - DATE: number required (jour du mois)
  - DAY_FR: string required (ex: "VEN")
  - MONTH_FR: string required (ex: "MAI")
  - DATE_LATIN: string optional (ex: "XVII · V · MMXXVI")
  - TIME_START: string required (ex: "20H30")
  - TIME_END: string required (ex: "22H30")
  - TAGLINE_OR_INSTRUMENTS: string optional
  - SUBTITLE: string optional (default: "DEUX SETS · ENTRACTE 21H10")
  - N: number optional (default: 1)
```

### Template 2 · Post Instagram portrait (1080×1350)

**Usage** : poster concert dense, expo détaillée, plat du jour avec photo.

**Spec** :

```yaml
template: post-instagram-portrait
dimensions: 1080×1350 px
canvas:
  background: "{colors.ink-900}"
  padding: 60px
layout: stack-with-photo
sections:
  - role: poster-photo
    height: 720
    align: top
    content:
      - photo:
          aspect: 3/4 ou 4/5
          treatment: "filter grayscale(0.15) sepia(0.05)"
          overlay-stamp-top-left: { text: "◉ {DAYS_TO_GO} JOURS", rotation: -6, color: orange-500 }
          overlay-badge-bottom-right: { text: "◉ AFFICHE Nº {N}/{TOTAL}", color: cream-50, bg: rgba(10,9,8,.78) }
  - role: meta
    height: 530
    padding-top: 36
    content:
      - eyebrow: { text: "{GENRE} · {VERCORS · ISÈRE}" }
      - display: { text: "{ARTIST_NAME}", size: clamp(64, 92), accent-word: 1 }
      - script: { text: "{INSTRUMENTS}", size: 38 }
      - datetime-stamp: { (same as template 1) }
      - cta-pair:
          - primary: { text: "→ RÉSERVER UNE TABLE", size: 18 }
          - outline: { text: "→ AJOUTER À L'AGENDA", size: 14 }
atmosphere:
  pick-one-signature: (same as template 1)
  cartouche: { text: "AFFICHE Nº {N} · MMXXVI", side: bottom-right }
variables: (same as template 1 + N + TOTAL + DAYS_TO_GO)
```

### Template 3 · Story Instagram / Facebook (1080×1920)

**Usage** : teaser événement immersif vertical, expo en cours, jam session reminder.

**Spec** :

```yaml
template: story-vertical
dimensions: 1080×1920 px
canvas:
  background: "{colors.ink-900}"
  texture: "tex-grain opacity 0.10"
layout: full-bleed-with-safe-area
safe-area:
  top: 220px  # IG header
  bottom: 280px  # IG actions
sections:
  - role: visual-zone
    span: full
    content:
      - poster-photo: { fill: full-bleed, treatment: "filter grayscale(0.20) brightness(0.85)" }
      - gradient-overlay: "linear-gradient(180deg, rgba(10,9,8,.30) 0%, transparent 30%, transparent 60%, rgba(10,9,8,.85) 100%)"
  - role: top-stamp
    align: top within safe-area
    margin-top: 240
    content:
      - corner-coord: { text: "◉ HIBOUBOX · 1050 M", opacity: 0.7 }
  - role: middle-meta
    align: center
    content:
      - eyebrow: { text: "◉ {GENRE}" }
      - display: { text: "{ARTIST_NAME}", size: clamp(96, 140), accent-word: 1 }
      - script: { text: "« {TAGLINE} »", size: 52 }
  - role: bottom-cta
    align: bottom within safe-area
    margin-bottom: 320
    content:
      - datetime-card: { compact, padding 18×24 }
      - cta-feature: { text: "→ RÉSERVER UNE TABLE", size: 22 }
atmosphere:
  - large-music-staff: { position: middle-back, opacity: 0.10 }
  - cartouche: { text: "STORY Nº {N}", side: top-right }
```

### Template 4 · Post Facebook (1200×630)

**Usage** : annonce concert horizontale, événement, partage URL.

**Spec** :

```yaml
template: post-facebook-horizontal
dimensions: 1200×630 px
canvas:
  background: "{colors.ink-900}"
  padding: 48px
layout: split-horizontal-3-7
sections:
  - role: photo-left
    width: 540  # 45%
    content:
      - poster-photo:
          aspect: 9/10
          frame: "1.5px solid orange-500 + outline dashed offset 4px + 4 corner ticks"
          stamp-top-right-intégré: { text: "◉ {DATE_SHORT}", rotation: -6 }
  - role: meta-right
    width: 612  # 55%
    padding-left: 40
    content:
      - eyebrow: { text: "◉ {GENRE} · {DATE_LATIN}" }
      - display: { text: "{ARTIST_NAME}", size: 56, accent-word: 1 }
      - script: { text: "« {INSTRUMENTS} »", size: 28 }
      - datetime-stamp: { compact horizontal }
      - cta: { text: "→ RÉSERVER UNE TABLE" }
atmosphere:
  - lat-long-grid: { opacity: 0.06 }
  - placename-latin: { text: "VIA · MUSICA", rotation: -8 }
  - cartouche: { text: "FB Nº {N}", side: bottom-right }
```

### Template 5 · Bandeau Facebook (820×312)

**Usage** : cover page Facebook HIBOUBOX.

**Spec** :

```yaml
template: facebook-cover
dimensions: 820×312 px
canvas:
  background: "{colors.ink-900}"
  padding: 24px
layout: editorial-horizontal
sections:
  - role: main
    content:
      - wordmark-png: { src: "assets/wordmark-orange.png", height: 80, position: left-center }
      - tagline: { text: "« le voyage commence à table »", font: script, size: 24, color: orange-400, position: right-of-wordmark }
      - coord-bottom-right: { text: "◉ 45°04′N · 5°33′E · VILLARD-DE-LANS", opacity: 0.6 }
atmosphere:
  - lat-long-grid: { opacity: 0.06 }
  - compass-rose: { position: top-right, size: 70, opacity: 0.20 }
  - cartouche: { text: "FOLIO Nº I · COUVERTURE", side: bottom-left, opacity: 0.55 }
safe-area-mobile-crop:
  central: 640×312  # Facebook crop le bandeau en mobile
```

### Template 6 · Newsletter email mensuelle (600px wide)

**Usage** : newsletter mensuelle (5-6 concerts + 1 expo + footer brand).

**Spec** :

```yaml
template: newsletter-email-monthly
dimensions: width 600px (max compatible Mailchimp/Brevo/Sendgrid)
canvas:
  background: "{colors.ink-900}"
  table-html: true  # tables HTML pour compat email clients
layout: vertical-stack
sections:
  - role: header
    padding: 40 32 24
    align: center
    content:
      - logo: { src: "assets/logo-full-orange.png", height: 64 }
      - tagline: { text: "« le voyage commence à table »", size: 16, color: orange-400 }
      - issue-line: { text: "ÉDITION Nº {N} · {MONTH_FR} {YEAR}", font: stamp-sm, opacity: 0.6 }
  - role: hero-concert
    padding: 24 32
    content:
      - eyebrow: { text: "◉ CONCERT À LA UNE" }
      - poster-thumb: { aspect: 16/10, with-stamp-top-left }
      - display: { text: "{ARTIST_NAME}", size: 36 }
      - datetime: { text: "{DAY} {DATE} {MONTH} · {TIME}", color: orange-500, weight: 700, size: 20 }
      - lead: { text: "{LEAD_2_LINES}", size: 14, color: cream-100 }
      - cta: { text: "→ DÉTAILS DU CONCERT", url: "{CONCERT_URL}", size: 14 }
  - role: more-concerts
    padding: 24 32
    content:
      - eyebrow: { text: "◉ L'AGENDA À VENIR" }
      - concert-row-x4: { (date + nom + style + cta lite ‣) }
  - role: expo
    padding: 24 32
    content:
      - eyebrow: { text: "◉ SUR NOS MURS" }
      - card: { artist + dates + accroche + cta "DÉCOUVRIR L'EXPO" }
  - role: footer
    padding: 40 32
    background: "{colors.ink-1000}"
    content:
      - coord: "◉ 45°04′N · 5°33′E · 1050 M"
      - address: "41 rue des Pionniers · 38250 · Villard-de-Lans"
      - phone-email: "04 76 95 11 79 · contact@hiboubox.fr"
      - unsubscribe: "désinscription"
      - garanties: "◉ PAS DE SPAM · ◉ DÉSINSCRIPTION 1 CLIC · ◉ DONNÉES NON CÉDÉES"
constraints:
  - inline-css-only: true  # pas de <style> tag (compat email)
  - no-webfont: use Georgia/Arial fallback (Google Fonts ne loadent pas dans la majorité des clients email)
  - max-width: 600px
  - images-hosted-externally: true (CDN ou Mailchimp media library)
```

### Template 7 · Affiche concert A3 (1240×1754 @150dpi)

**Usage** : affiche concert format vitrine, distribuée en print A3 portrait.

**Spec** :

```yaml
template: poster-concert-a3
dimensions: 1240×1754 px (297×420mm @150dpi)
canvas:
  background: "{colors.ink-900}"
  bleed: 30px tout autour (1300×1814 avec bleed)
  padding: 80px
layout: vertical-massive
sections:
  - role: top
    height: 80
    content:
      - eyebrow-large: { text: "◉ CONCERT · HIBOUBOX · MMXXVI", tracking: 0.30em, size: 22 }
  - role: photo-poster
    height: 850
    content:
      - photo: { aspect: 4/3, treatment: "filter grayscale(0.15)" }
      - overlay-stamp-top-left: { text: "◉ {DAYS_TO_GO} JOURS", rotation: -6 }
      - overlay-genre-bottom-left: { text: "{GENRE}", color: orange-500, size: 36 }
  - role: title-block
    align: center
    margin-top: 60
    content:
      - display-massive: { text: "{ARTIST_NAME}", size: clamp(140, 200), accent-word: 1, color: cream-50 }
      - script-large: { text: "« {INSTRUMENTS} »", size: 72, color: orange-400 }
  - role: datetime
    align: center
    margin-top: 60
    content:
      - frame: "2px solid orange-500 + outline dashed offset 6px + 4 corner ticks"
      - date-top: { text: "{DAY_FR} {DATE} {MONTH_FR}", size: 28 }
      - time-massive: { text: "{TIME_START} → {TIME_END}", size: 88 }
      - bottom: { text: "◉ DEUX SETS · ENTRACTE 21H10 · CONCERT GRATUIT · PRIX LIBRE", size: 18 }
  - role: footer
    align: bottom
    height: 200
    content:
      - logo: { src: "assets/logo-full-orange.png", height: 100 }
      - address: { text: "41 RUE DES PIONNIERS · VILLARD-DE-LANS · 04 76 95 11 79", size: 16 }
      - cta: { text: "→ RÉSERVATION : COVERMANAGER.COM/HIBOUBOX", size: 18 }
atmosphere:
  - large-music-staff: { position: middle-back, opacity: 0.06 }
  - lat-long-grid: { opacity: 0.04 }
  - 3-placenames-latin: { positions: corners, opacity: 0.40 }
  - cartouche-large: { text: "AFFICHE Nº {N} · ÉDITION MMXXVI", side: bottom-right }
print-specs:
  - color-mode: CMYK conversion required (proto en RGB)
  - resolution: 150dpi minimum, 300dpi recommandé
  - bleed: 5mm tout autour
  - safety-margin: 5mm depuis bord de coupe
```

### Template 8 · Flyer A5 concert (874×1240 @150dpi)

**Usage** : flyer concert format A5 portrait, distribution main à main et bar.

**Spec** :

```yaml
template: flyer-concert-a5
dimensions: 874×1240 px (148×210mm @150dpi)
canvas:
  background: "{colors.ink-900}"
  bleed: 30px
  padding: 50px
layout: dense-stack
sections:
  - role: header
    height: 60
    content:
      - eyebrow: { text: "◉ HIBOUBOX · CONCERT", size: 14 }
  - role: photo-poster
    height: 520
    content: (same as A3 but compacted)
  - role: title
    content:
      - display: { text: "{ARTIST_NAME}", size: 80 }
      - script: { text: "« {INSTRUMENTS} »", size: 42 }
  - role: datetime
    content: (compact horizontal date + time block)
  - role: footer
    content:
      - logo: { height: 56 }
      - address-tel: { size: 11 }
      - cta: { text: "→ RÉSERVATION · 04 76 95 11 79", size: 14 }
print-specs:
  - bleed: 5mm
  - format-fini: A5 portrait
```

### Template 9 · Carte de visite (502×325 @150dpi)

**Usage** : carte recto HIBOUBOX, verso optionnel Festin sub-marque.

**Spec recto HIBOUBOX** :

```yaml
template: business-card-recto
dimensions: 502×325 px (85×55mm @150dpi)
canvas:
  background: "{colors.ink-900}"
  bleed: 12px
  padding: 24px
layout: editorial-card
sections:
  - role: top
    align: top-left
    content:
      - wordmark: { src: "assets/wordmark-orange.png", height: 32 }
      - tagline: { text: "« le voyage commence à table »", font: script, size: 11, color: orange-400 }
  - role: middle
    align: center
    content:
      - coord-big: { text: "◉ 45°04′27″N · 5°33′12″E", size: 14, font: stamp-sm }
  - role: bottom
    align: bottom-left
    content:
      - address: "41 rue des Pionniers · 38250 · Villard-de-Lans"
      - phone-email: "04 76 95 11 79 · contact@hiboubox.fr"
atmosphere:
  - lat-long-grid: { opacity: 0.10 }
  - compass-rose: { position: bottom-right, size: 40, opacity: 0.30 }
  - cartouche: { text: "CARTA Nº I", side: top-right, opacity: 0.55 }
print-specs:
  - bleed: 3mm
  - quadrichromie CMYK
  - papier: 350g mat ou silk recommandé
  - finition: vernis sélectif sur wordmark optionnel
```

**Spec verso Festin (variation gold)** :

```yaml
template: business-card-verso-festin
dimensions: 502×325 px
canvas:
  background: "{colors.ink-800}"
  padding: 24px
layout: festin-sub-brand
sections:
  - center:
      - festin-logo: { src: "assets/festin-du-hibou-black.png", height: 80, filter: "gold filter chain" }
      - tagline: { text: "« notre cuisine se déplace chez vous »", font: script, size: 13, color: gold-400 }
  - bottom:
      - email-dedicated: { text: "contact@lefestinduhibou.fr", color: gold-400 }
      - phone: "04 76 95 11 79"
atmosphere:
  - placename-latin: { text: "VIA · COQUINA", opacity: 0.35 }
  - cartouche: { text: "FESTIN Nº I", side: bottom-right }
```

### Template 10 · Cartel œuvre expo A6 (621×874 @150dpi)

**Usage** : plaquette d'œuvre type musée, posée sous chaque tirage galerie.

**Spec** :

```yaml
template: expo-artwork-label-a6
dimensions: 621×874 px (105×148mm @150dpi)
canvas:
  background: "{colors.cream-50}"  # PASSE en cream sur sombre — exception cartel
  border: "2px solid {colors.ink-900}"
  outline: "1px dashed {colors.ink-900}, outline-offset: 8px"
  padding: 32px
layout: cartel-museum
sections:
  - role: top
    content:
      - eyebrow: { text: "Nº {N}", color: ink-900, font: stamp-sm }
  - role: middle
    content:
      - artist-name: { text: "{ARTIST_NAME}", font: display-sm, size: 28, color: ink-900 }
      - artwork-title: { text: "« {TITLE} »", font: script-md, size: 22, color: ink-700, italic: true }
  - role: meta
    margin-top: 18
    content:
      - year: { text: "{YEAR}", font: body-md }
      - dimensions: { text: "{W} × {H} cm", font: body-sm }
      - edition: { text: "{EDITION_TYPE} · {EDITION_N}/{EDITION_TOTAL}", font: stamp-sm }
      - inedit-stamp: { text: "◉ INÉDIT", color: orange-500, opacity: 1, optional: true }
  - role: footer
    align: bottom
    content:
      - sale-info: { text: "Disponible à la vente · nous écrire", font: body-sm, color: ink-700 }
print-specs:
  - papier: 250g mat cream
  - format-fini: A6 portrait
note: |
  Seul cas où on rend du CREAM-SUR-NOIR-INVERSÉ (cream bg + ink text).
  Référence "cartel musée" — 1 occurrence max par page/expo, pour
  préserver la rareté du pattern.
```

### Template 11 · OG image / favicon

**Usage** : partage URL réseaux sociaux + onglet navigateur.

**Spec OG image** :

```yaml
template: og-image
dimensions: 1200×630 px (ratio Open Graph standard)
canvas:
  background: "{colors.ink-900}"
  padding: 60px
layout: horizontal-brand
sections:
  - left:
      - logo: { src: "assets/logo-full-orange.png", height: 120 }
      - tagline: { text: "« le voyage commence à table »", font: script, size: 28, color: orange-400 }
  - right:
      - description: { text: "{PAGE_DESCRIPTION_2_LINES}", font: body, size: 22, color: cream-50, max-width: 500 }
      - coord-bottom: { text: "◉ HIBOUBOX · VILLARD-DE-LANS", opacity: 0.6 }
atmosphere:
  - lat-long-grid: { opacity: 0.05 }
  - compass-rose: { position: top-right, size: 80, opacity: 0.25 }
```

**Spec favicon** :

```yaml
template: favicon-set
dimensions:
  - 16×16 px (legacy)
  - 32×32 px (standard)
  - 180×180 px (apple-touch-icon)
  - 512×512 px (maskable PWA)
canvas:
  background: transparent
content:
  - picto-owl: { src: "assets/picto-owl-orange.png", fill: full }
note: |
  Le picto owl seul, plein cadre, fond transparent. Marche autant en
  light mode (favicon sur onglet blanc) qu'en dark mode.
```

### Template 12 · Menu print restaurant A4 (1240×1754 @150dpi)

**Usage** : carte restaurant complète format A4 portrait, plastifiée pour les tables.

**Spec** :

```yaml
template: menu-restaurant-a4
dimensions: 1240×1754 px (A4 portrait @150dpi)
canvas:
  background: "{colors.cream-50}"   # EXCEPTION : print sur fond clair
  bleed: 30px
  padding: 60px
layout: catalog-dense
sections:
  - role: header
    content:
      - logo: { height: 90, color: ink-900 (filter chain reverse) }
      - tagline: { text: "« le voyage commence à table »", color: ink-700 }
      - section-title: { text: "NOTRE CARTE · {SAISON}", font: display, size: 48, color: ink-900 }
  - role: catalog
    layout: 2-columns
    sections-by-category:
      - tapas-planches: { items: 6-10 }
      - currys-woks: { items: 6-10 }
      - salades-pates: { items: 4-6 }
      - desserts: { items: 4-6 }
  - role: footer
    content:
      - allergens-legend: { 6 badges UE }
      - cgv-line: { text: "Prix nets TTC · format européen 12,00 €", size: 10, color: ink-700 }
typography-mapping:
  category-title: "{typography.display-sm} color {colors.orange-500}"
  item-name: "{typography.body-md} weight 600 color {colors.ink-900}"
  item-desc: "{typography.body-sm} color {colors.ink-700}"
  item-price: "{typography.stamp-md} weight 700 color {colors.orange-500} tabular-nums"
print-specs:
  - bleed: 5mm
  - papier: 250g semi-mat, plastifiable
  - quadrichromie CMYK
```

---

## Prompt patterns — instructions pour OD

Cette section liste les **prompts canoniques** à utiliser directement en
chat dans Open Design pour générer un artwork HIBOUBOX brand-cohérent.
Le système doit interpréter chaque prompt en chargeant le template
correspondant et en substituant les variables.

### Prompt 1 · Affiche concert A3

```
/affiche concert
ARTIST: TRIO MARLOWE
GENRE: JAZZ MANOUCHE
DATE: 17 mai 2026
TIME: 20H30 → 22H30
INSTRUMENTS: guitare · contrebasse · violon
```

**Comportement attendu** :
- Charge `Template 7 · Affiche concert A3` (1240×1754 @150dpi)
- Substitue les variables dans le YAML spec
- Calcule `DAYS_TO_GO = date - today`
- Génère 1 fichier HTML standalone exportable en PDF print-ready
- Atmosphere = pick parmi music-staff XL / lat-long-grid / placenames latins (varier d'un appel à l'autre)
- Cartouche `AFFICHE Nº {N+1}` (incrémenter depuis le dernier généré)

### Prompt 2 · Post Instagram concert

```
/post instagram carre concert
ARTIST: ANNA RIBÉROL QUARTET
GENRE: JAZZ MODERNE
DATE: 24 mai · 20H30
INSTRUMENTS: piano · sax · basse · batterie
```

**Comportement attendu** :
- Charge `Template 1 · Post Instagram carré (1080×1080)`
- Format ratio 1:1, optimisé feed standard
- Si l'utilisateur demande version portrait : bascule sur `Template 2`

### Prompt 3 · Story Instagram event

```
/story instagram
EVENT: VERNISSAGE EXPO
ARTIST: ANNA RIBÉROL · ALTITUDES
DATE: VEN 02 MAI · 19H
SUBTITLE: mot de l'artiste 19h30 · set acoustique 20h
```

**Comportement attendu** :
- Charge `Template 3 · Story Instagram (1080×1920)`
- Format vertical avec safe-areas IG header (220px top) / IG actions (280px bottom)

### Prompt 4 · Newsletter mensuelle

```
/newsletter mois MAI 2026
HERO: TRIO MARLOWE · 17 MAI · JAZZ MANOUCHE
CONCERTS:
  - 22 MAI · QUARTET RIBÉROL · jazz moderne
  - 24 MAI · CHANSON FRANÇAISE · DUO MARGAUX
  - 29 MAI · TRIO FOLK · CÉLINE & GROUPE
EXPO: ANNA RIBÉROL · ALTITUDES · 02 MAI → 28 JUIN
```

**Comportement attendu** :
- Charge `Template 6 · Newsletter email (600px wide)`
- Génère HTML email-safe : tables HTML, CSS inline only, no webfonts (fallback Georgia/Arial), images hostées externalement
- Stamp `ÉDITION Nº {N} · MAI MMXXVI` calculé depuis le dernier numéro

### Prompt 5 · Carte de visite

```
/carte de visite
NOM: Nicolas Dionisius
POSTE: Propriétaire · Programmation
TEL_PERSO: 06 XX XX XX XX (optionnel)
VERSO: festin (oui = recto HIBOUBOX + verso Festin, non = recto HIBOUBOX simple)
```

**Comportement attendu** :
- Charge `Template 9 · Carte de visite (502×325 @150dpi)`
- Si `VERSO: festin` → génère 2 fichiers (recto + verso gold)
- Pré-cadre les marges pour bleed 3mm + safety zone
- Si `TEL_PERSO` renseigné → ligne ajoutée sous l'adresse principale

### Prompt 6 · Cartel œuvre expo

```
/cartel expo
ARTIST: Anna Ribérol
TITLE: Altitudes I
YEAR: 2025
DIMENSIONS: 60 × 80 cm
EDITION: Tirage argentique · 3/8
INEDIT: oui
N: 03
```

**Comportement attendu** :
- Charge `Template 10 · Cartel œuvre A6`
- EXCEPTION : fond cream + texte ink (seul cas où on inverse la grammaire)
- Tampon `◉ INÉDIT` rendu en orange si `INEDIT: oui`

### Prompt 7 · OG image page web

```
/og image
PAGE_TITLE: Programmation
PAGE_DESCRIPTION: Concerts jazz, blues, chanson française et musiques du monde — tous les soirs à 20h30. Concert gratuit · prix libre · accueil exclusivement à table.
```

**Comportement attendu** :
- Charge `Template 11 · OG image (1200×630)`
- Description tronquée à 160 caractères max (limite affichage social)
- Si `PAGE_TITLE` non fourni → utilise `HIBOUBOX` par défaut

### Prompt 8 · Bandeau Facebook cover

```
/bandeau facebook
EDITION: PRINTEMPS 2026
```

**Comportement attendu** :
- Charge `Template 5 · Bandeau Facebook (820×312)`
- Centre les éléments importants dans la safe-area mobile (640×312 central)
- Cartouche `FOLIO Nº I · COUVERTURE · {EDITION}`

### Prompt 9 · Story série (multi-cards)

```
/story serie 3 concerts
WEEK: SEMAINE DU 17 MAI
CONCERTS:
  - VEN 17 · TRIO MARLOWE · JAZZ MANOUCHE
  - SAM 18 · QUARTET ZOOM · BLUES MODERNE
  - DIM 19 · JAM SESSION · SCÈNE OUVERTE
```

**Comportement attendu** :
- Charge `Template 3` x 3 stories distinctes
- Numérotation `Nº I/III` `Nº II/III` `Nº III/III` dans le cartouche
- Cohérence atmosphere entre les 3 (même grammaire signalétique, varier les positions des artefacts)

### Prompt 10 · Variation alternative

```
/variation
LAST_GENERATED: post-instagram-carre-trio-marlowe
CHANGE: essayer un autre layout avec photo en haut au lieu de la photo en bas
```

**Comportement attendu** :
- Recharge le dernier artwork généré
- Applique la variation demandée
- Garde toutes les autres specs identiques (palette, typo, copy)
- Génère un nouveau fichier `{slug}-v2.html` (ne remplace pas l'original)

### Règles génératives transverses

Pour chaque génération d'artwork :

1. **Toujours** charger la palette `{colors.*}` depuis le front matter YAML
2. **Toujours** charger les fonts via `<link>` Google Fonts (sauf newsletter qui utilise fallback Georgia)
3. **Toujours** ajouter une atmosphere (jamais un fond plat seul)
4. **Toujours** signer avec un cartouche numéroté `Nº {N}`
5. **Toujours** respecter les do/don't de la section Brand voice (pas d'emoji décoratif dans lettre, pas de chiffres durs dans copy générique, "accueil à table" pas "non-attablés", etc.)
6. **Toujours** rendre exportable en `<artifact>` HTML standalone (inline CSS, assets référencés en path relatif)
7. **Jamais** d'image hardcodée par URL externe (placeholders ou références aux assets du projet uniquement)
8. **Jamais** mélanger orange + gold sur un même artwork (sauf bandeau bascule explicite)

### Format de sortie attendu

Chaque génération d'artwork retourne :

```
<artifact identifier="{kebab-slug}" type="text/html" title="{Human title}">
<!doctype html>
<html lang="fr">
<head>
  <meta charset="utf-8">
  <title>{Page title}</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Bungee&family=Cormorant+Garamond:ital@1&family=Lato:wght@400;600;700&family=Barlow+Condensed:wght@600;700&family=Special+Elite&display=swap" rel="stylesheet">
  <style>
    /* Palette */
    :root {
      --ink-900: #16140f;
      --orange-500: #d97a2a;
      /* ... full palette ... */
    }
    /* Layout, typo, atmosphere */
    ...
  </style>
</head>
<body>
  <!-- Artwork content -->
</body>
</html>
</artifact>
```

Le fichier doit être :
- **Single-file standalone** (aucune dépendance externe sauf Google Fonts)
- **Print-ready** si template print (bleed + safety zone correctement définis)
- **Exportable en PDF** via le viewport `width="device-width"` ou `@page { size: A3 portrait }`
- **Exportable en PNG/JPG** via screenshot du viewport exact

---

## Annexe · Assets brand

Tous les assets visuels du brand HIBOUBOX sont rassemblés sous `assets/` :

| Dossier              | Contenu                                                        |
|----------------------|----------------------------------------------------------------|
| `assets/`            | Logos HIBOUBOX (5) + signature SVG (6) — voir § Logos          |
| `assets/origins/`    | 56 stamps pays + 4 stamps régions France (`vercors-region`, `savoie`, `provence`, `dauphine`) — format ovale 140×80 |
| `assets/origins/vins/` | 15 stamps régions viticoles France — format ovale 140×80     |
| `assets/tabs/`       | 15 icônes line-art catégories cuisine — format 32×32 stroke 1.4-1.6 |

Tous au format SVG vectoriel, recolorable via la chaîne `filter` CSS
décrite dans la section Stamps. Inventaire complet et structure
canonique dans les sections § Stamps & Tampons et § Icônes.

---

## Versioning & changelog

| Version | Date           | Changements                                                       |
|---------|----------------|-------------------------------------------------------------------|
| 1.0     | 2026-05-21     | Édition initiale · 16 sections · 4 batches · audit complet proto  |

### Roadmap d'évolution prévue

- **1.1** : ajout templates artwork additionnels (sticker fermeture, étiquette boîte traiteur, ardoise menu du jour)
- **1.2** : section "Animations & motion" si pattern motion devient transverse (actuellement seul le halo featured pulse)
- **2.0** : refonte si extension de la sub-marque Festin justifie un DESIGN.md séparé (actuellement intégré)

---

**Fin du DESIGN.md HIBOUBOX v1.0.**

> Édité par Claude (Open Design) avec la complicité de Nicolas Dionisius
> pour HibouJazz SARL · Villard-de-Lans · Vercors · Mai MMXXVI.
