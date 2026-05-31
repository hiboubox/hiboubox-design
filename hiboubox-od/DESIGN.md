# HIBOUBOX Brand Design System
> Category: Creative & Artistic
> Restaurant-concert-bar au Vercors. Palette ink/cream/orange, grammaire cartographie+jazz+passeport.

This is the portable Open Design package for **HIBOUBOX** — a restaurant /
concert venue / bar / gallery in Villard-de-Lans (Vercors, France), run by
HibouJazz SARL. It also covers the catering sub-brand **Le Festin du Hibou**
(gold accent variant). Every value below is self-contained: an agent with no
other context can build a brand-coherent artifact from this file plus
`tokens.css` and the assets in `assets/`.

The aesthetic combines three worlds in equal measure: **antique cartography /
travel maps**, **international jazz club**, and **vintage passport / postal
stamps**. Palette is deep ink × brass orange × parchment cream × gold filigree.
Master tagline: *« le voyage commence à table »* (the journey begins at the
table). Copy is French, sober, editorial — never commercial, never startup.

---

## 1. Visual Theme & Atmosphere

### Mood
Candlelit, warm, editorial. Think an independent magazine printed on aged
parchment, crossed with a 1950s jazz club passport and a sextant-era nautical
chart. Deep warm-taupe darkness lit by a single brass-orange flame (stage light,
candle, logo). Never cold, never neon, never corporate-SaaS.

### Three combined influences (equal weight)
1. **Cartography / travel map** — lat/long grids, sextant cross-hairs, isohypses
   (contour lines), spot-height peaks ▲, dashed routes, Latin placenames, compass
   rose, numbered cartouches `CARTE Nº I → XIV`, coordinate stamps.
2. **International jazz club** — treble clef `𝄞`, 5-line music staves, notes ♩♪♬♫,
   vinyl grooves, boarding-pass timelines, postal "par avion" cancellation marks,
   compact geometric display type (Bungee).
3. **Vintage passport / postal** — round obliteration cachets, rotated scotch tape,
   torn-ticket perforations, dot-leaders, press drop-caps, cartographer signature.

### Atmosphere construction (decorative ecosystem per section)
Each section gets ONE "atmosphere" — layered background décor that gives it a
narrative identity without ever competing with editorial content. Canonical
layers, back to front, with opacity:

| Order | Layer                      | Opacity     | Role                                       |
|-------|----------------------------|-------------|--------------------------------------------|
| 1     | Tone-on-tone background    | 1.0         | Section bg (ink-900 or ink-800)            |
| 2     | World map filigree         | 0.04–0.08   | Continents watermark                       |
| 3     | Sober lat/long grid        | 0.10–0.18   | Transparent orange hairlines               |
| 4     | Sextant cross-hairs        | 0.20–0.32   | Markers at key intersections (3–5 max)     |
| 5     | ONE signature artefact     | 0.18–0.42   | The visual moment of the section           |
| 6     | Latin placenames (3 max)   | 0.32–0.55   | Narrative toponyms `VIA · LITTERIS`        |
| 7     | Vercors spot-heights ▲     | 0.40–0.62   | Mountain identity                          |
| 8     | Signature cartouche        | 0.62–0.78   | `CARTA Nº X · SUB-LATIN`                    |
| 9     | Compass rose (corner)      | 0.15–0.35   | Mini or XL by density                      |

### Orchestration rules
- **One atmosphere per section.** Never 2 routes or 2 music staves stacked.
- **Vary vocabulary between adjacent sections** (musical → cartographic →
  parchment → postal) for narrative rhythm.
- **Strict opacities**: no decorative element above 0.55 except signature
  cartouches (up to 0.78).
- **Décor is pure background** — `aria-hidden="true"`, ignored by screen readers,
  never interactive.
- **Concentrate décor in visible zones** — never hide it behind a card.
- **One dominant signature artefact** per section (cartouche XOR compass XOR
  central cross-hair XOR main route).

### Section rhythm
Sections alternate `ink-900 / ink-800` for tonal rhythm, joined by a **Wave**
divider carrying a dashed-orange passport-stitch. Footer is always `ink-1000`.
Never skip two ink levels at once (`ink-1000 → ink-700` breaks the rhythm).

### Hard "no" list (anti-AI-slop)
Aggressive purple/violet gradients · emoji feature icons (✨🚀🎯) · rounded cards
with left-border accent · Inter/Roboto/Arial as display · beige/peach/pink page
washes · filler/lorem copy · an icon beside every heading · gradient on every
background · blurry blue soft-UI shadows · cold palettes · generic stock photos.

---

## 2. Color Palette & Tokens

Philosophy: warm, candlelit, never cold. Three chromatic roles — deep ink
background, cream parchment text, single orange accent. Gold is a restricted
filigree/sub-brand accent. Olive is a rarely-used backup.

**Always reference CSS variables (`var(--orange-500)`), never hex literals.**
OKLch values are approximate. Contrast ratios are WCAG 2.2 (AA = 4.5:1 normal
text, 3:1 large text ≥18px or ≥14px bold), computed by the official formula.

### Core role bindings (drives the live preview)

The canonical role → value mapping. These `Label: #hex` lines are the
machine-readable bindings the OD showcase parses to render the live preview in
brand; the full token reference follows in the tables below.

- Primary background: #16140f
- Secondary surface: #211e19
- Card surface: #2d2925
- Primary text: #faf3e2
- Body text: #f0e6ce
- Secondary text: #c2b39a
- Border: #3a3530
- Brand primary: #d97a2a
- Brand secondary: #d4af5a
- Display font: "Bungee", "Bowlby One", "Arial Black", sans-serif
- Body font: "Lato", "Source Sans 3", system-ui, sans-serif
- Mono font: "Special Elite", "Courier Prime", "Courier New", monospace

### Ink — dark backgrounds (warm taupe, never brown-red, never cold grey)
| Token        | Hex       | OKLch approx.          | Role / contrast                                      |
|--------------|-----------|------------------------|------------------------------------------------------|
| `--ink-1000` | `#0a0908` | `oklch(7% 0.003 60)`   | Full-bleed bg, footer, drawer/modal bg               |
| `--ink-900`  | `#16140f` | `oklch(11% 0.005 70)`  | Page background default — base of all UI             |
| `--ink-800`  | `#211e19` | `oklch(15% 0.006 70)`  | Raised surface, sticky header, alternated section    |
| `--ink-700`  | `#2d2925` | `oklch(20% 0.007 70)`  | Card surface on dark, hover                          |
| `--ink-600`  | `#3a3530` | `oklch(25% 0.008 70)`  | Hover surface, strong borders                        |
| `--ink-500`  | `#4a4540` | `oklch(31% 0.008 70)`  | Divider, muted border                               |

### Cream — light text on ink + parchment print
| Token        | Hex       | Role                                  | Contrast on ink-900 |
|--------------|-----------|---------------------------------------|---------------------|
| `--cream-50` | `#faf3e2` | Primary text, display, hero eyebrow   | 16.6:1 AAA          |
| `--cream-100`| `#f0e6ce` | Body text on ink (default `<body>`)   | 14.8:1 AAA          |
| `--warm-300` | `#c2b39a` | Secondary muted text, captions        | 9.0:1 AAA           |
| `--warm-500` | `#897a63` | **DISABLED ONLY** — WCAG-exempt       | 4.4:1 (never active text) |
| `--paper-100`| `#f5ecd6` | Primary print bg (menu, card)         | —                   |
| `--paper-200`| `#e8dcc0` | Paper aged — print variation          | —                   |
| `--paper-300`| `#d6c79e` | Paper darker / kraft — takeaway labels| —                   |

### Text on paper — 3-level hierarchy for light supports
| Token         | Hex       | Role                        | Contrast on paper-100 |
|---------------|-----------|-----------------------------|-----------------------|
| `--on-paper-1`| `#1a1108` | Primary text on cream/paper | 15.8:1 AAA            |
| `--on-paper-2`| `#4a3422` | Secondary text              | 9.9:1 AAA             |
| `--on-paper-3`| `#7a5b3f` | Tertiary / captions         | 5.3:1 AA              |

### Orange — the single brand accent (CTAs, links, eyebrows, stamps, dividers)
| Token         | Hex       | Role                                          | Contrast on ink-900 |
|---------------|-----------|-----------------------------------------------|---------------------|
| `--orange-300`| `#f5b074` | Hover soft, transient                         | —                   |
| `--orange-400`| `#ea934a` | Hover primary, eyebrows, **focus ring**       | 7.7:1 AAA           |
| `--orange-500`| `#d97a2a` | **PRIMARY** — CTAs, ribbons, stamps, dividers | 5.9:1 AA            |
| `--orange-600`| `#b35e1a` | Pressed / deep                                | —                   |
| `--orange-700`| `#7e3f10` | Darkest — orange on cream/paper               | 6.9:1 AA on paper   |

**Golden rule: max 2 orange occurrences per screen.** Hero eyebrow + primary CTA
is enough. A third orange is usually a composition bug — switch it to cream-100
or an outline.

### Gold — filigree accent (origin stamps + Le Festin du Hibou)
| Token        | Hex       | Strict use                                       | Contrast on ink-900 |
|--------------|-----------|--------------------------------------------------|---------------------|
| `--gold-400` | `#d4af5a` | Origin-stamp filigree · Festin CTAs/borders      | 8.8:1 AAA           |
| `--gold-500` | `#b88f3a` | Gold deep — Festin CTA hover                     | —                   |

⚠ Never use gold as a general UI accent. Orange-500 keeps that role on HIBOUBOX.
Gold appears only as decorative filigree (opacity ~0.72) or on Festin surfaces.

### Olive — vintage-poster ink, secondary backup (rare)
| Token         | Hex       | Role                                       |
|---------------|-----------|--------------------------------------------|
| `--olive-400` | `#a8b04a` | Hover state secondary                      |
| `--olive-500` | `#818825` | Secondary CTA `Btn.olive` (alt to primary) |
| `--olive-600` | `#5e6519` | Pressed olive                              |

### Semantic — system states (admin, forms, validation)
| Token        | Hex       | Role                          | Contrast on ink-900 |
|--------------|-----------|-------------------------------|---------------------|
| `--success`  | `#6f8a3e` | Validation, accepted          | 4.7:1 AA            |
| `--success-bg`| `#2a3318`| Success card bg               | —                   |
| `--warning`  | `#d4a13a` | Non-blocking warning          | 7.9:1 AAA           |
| `--danger`   | `#d85535` | Error, rejected, delete       | 4.6:1 AA (fixed from `#c14f2c` = 3.88:1 FAIL) |
| `--danger-bg`| `#3a1612` | Danger card bg                | —                   |
| `--info`     | `#6b8aa8` | Neutral info (muted blue)     | 5.1:1 AA            |

### Interaction aliases (derived)
`--primary` = orange-500 · `--primary-hover` = orange-400 · `--primary-pressed` =
orange-600 · `--primary-disabled` = `#6a4824` · `--primary-fg` = `#1a0e04` (text on
orange, 6.1:1 AA) · `--secondary` = olive-500 · `--secondary-fg` = `#0f1404` (4.9:1 AA).
Text on gold-400 button uses `--primary-fg` `#1a0e04` (9.1:1 AAA).

### Allowed combinations
✅ Hero: `bg ink-900` + `eyebrow orange-400` + `display cream-50` + ONE `CTA
orange-500` + `cream-100` infos. ✅ Card: `bg ink-700` + `eyebrow orange-500` +
`title cream-50` + `body cream-100` + ONE full-width `CTA orange-500`. ✅ Festin:
`bg ink-800/900` + `eyebrow gold-400` + `display cream-50` + `CTA gold-400`.

### Forbidden combinations
❌ Orange + olive on one screen. ❌ Orange + gold as two equal accents (gold is
filigree only, except on Festin). ❌ cream-50 on paper-100 (cream-on-cream). ❌
orange-500 body text on ink-700 (OK only for uppercase eyebrow ≤13px where
tracking aids legibility).

### Accessibility rules
- Critical text (CTAs, body, captions, errors): always ≥ AA. Decorative elements
  (watermark stamps, atmospheres) at opacity 0.20–0.50 may fall below AA — intentional.
- `--danger` for error text must be `#d85535`, never `#c14f2c`.
- `--warm-500` is for `disabled` only; active tertiary text uses `--warm-300`.

---

## 3. Typography

Six families loaded via Google Fonts, each with a strict exclusive role. Never
use a family outside its role.

```html
<link href="https://fonts.googleapis.com/css2?family=Bungee&family=Bowlby+One&family=Rubik+Wet+Paint&family=Cormorant+Garamond:ital,wght@0,500;0,700;1,400;1,500;1,700&family=Lato:ital,wght@0,300;0,400;0,500;0,700;1,400&family=Barlow+Condensed:wght@500;600;700&family=Special+Elite&display=swap" rel="stylesheet">
```

| Family            | Var               | EXCLUSIVE role                | Character / rules                              |
|-------------------|-------------------|-------------------------------|------------------------------------------------|
| **Bungee**        | `--font-display`  | XXL display titles            | Geometric compact signage, hyper-impact, **uppercase only**, negative letter-spacing |
| **Rubik Wet Paint**| `--font-poster`  | Concert poster XL only        | Textured grunge stencil; only on dark ink, never on paper |
| **Cormorant Garamond**| `--font-serif`| Italic taglines / quotes      | **Italic only**, never uppercase, letter-spacing 0 |
| **Lato**          | `--font-body`     | Body + UI + mobile            | Neutral, system-like, readable long-form       |
| **Barlow Condensed**| `--font-label`  | Eyebrows, labels, in-card CTAs| Uppercase, tracking ≥0.16em (canonical 0.22em), weight 600–700 |
| **Special Elite** | `--font-stamp`    | Stamps, coords, dates, Nº     | Typewriter monospace, always uppercase         |

Fallback stacks are defined in `tokens.css` (`--font-*`). The only Arial allowed
is `"Arial Black"` inside the Bungee fallback.

### Scale (desktop → mobile)
**Display (Bungee), uppercase, color cream-50:**
| Token        | Desktop | Mobile  | LS       | LH   | Use                                   |
|--------------|---------|---------|----------|------|---------------------------------------|
| `display-xl` | 92px    | 44–56px | -0.01em  | 0.9  | Page hero principal                   |
| `display-lg` | 64–72px | 36–44px | -0.005em | 0.92 | Secondary hero, major section heads   |
| `display-md` | 44–48px | 28–32px | -0.005em | 1.05 | Section heads, featured card headlines|
| `h3`         | 28px    | 22px    | 0        | 1.05 | Card titles (`text-transform: none`)  |
| `h4`         | 22px    | 18px    | 0        | 1.2  | Secondary card titles                 |

**Poster (Rubik Wet Paint):** `poster-xl` 120px+ — concert posters A3 / detail
heroes only, dark ink bg only.

**Script (Cormorant Garamond), italic mandatory, color cream-100:**
| Token       | Desktop | Mobile  | Use                                              |
|-------------|---------|---------|--------------------------------------------------|
| `script-lg` | 60px    | 38px    | Hero tagline « le voyage commence à table »      |
| `script-md` | 34px    | 17–24px | Companion phrases, inset quotes                  |
| `script-sm` | 22px    | 16–18px | Discreet section sub-titles, elegant captions    |

**Eyebrow (Barlow Condensed), uppercase, weight 600–800, color orange-400/500,
tracking 0.22em (0.18em mobile):**
| Token            | Desktop | Mobile | Use                                         |
|------------------|---------|--------|---------------------------------------------|
| `eyebrow-hero`   | 22px    | 16px   | Above page-hero display                     |
| `eyebrow-section`| 19px    | 15px   | Above section displays (standard)           |
| `eyebrow-card`   | 13–16px | 12–14px| Inside a card                               |

**Body (Lato), color cream-100 on ink / on-paper-1 on paper:**
`lead` 20px/1.55 · `body` 16px/1.55 · `small` 14px/1.55 · `micro` 12px/1.45.
Long editorial paragraphs: `text-align: justify` + `hyphens: auto` +
`text-wrap: pretty`.

**Stamp/Coord (Special Elite), uppercase, color orange-400/500:**
`stamp` 10–12px / LS 0.12em · `coord` 13–16px / LS 0.16em.

### Inviolable typography rules
1. ❌ Never Bungee in body text (illegible <22px).
2. ❌ Never Lato in display (lacks impact).
3. ❌ Never Cormorant Garamond non-italic.
4. ❌ Never an eyebrow with tracking < 0.16em (reads as shouting, not a label).
5. ❌ Never Inter/Roboto/Arial as display (AI-slop signature).
6. ❌ Never simulate Bungee with serif/Georgia in previews (glyph ~30% wider,
   breaks overflow math).

### Display accent pattern
One word of a display title goes in `<span class="accent">` colored orange-500
(gold-400 on Festin). Typically the 2nd word: `TRIO <span>MARLOWE</span>`,
`LE <span>FESTIN</span> DU HIBOU`. One accent word per display. Use
`text-wrap: balance` on serif titles and narrative leads.

### Numeric variants
`font-variant-numeric: tabular-nums` on tables, price lists, scores, coordinates,
ticket-stub dates. `proportional-nums` (default) for running body text.

### Mobile typography (always bump editorial sizes UP for legibility, never down)
Eyebrow section 19→15px (tracking 0.18em) · hero eyebrow 22→16px (0.22em kept) ·
display section 60–72→38–44px (LH 1.15 vs 1.02 to avoid cramped wraps) · body
16→14–15px (LH 1.55 kept) · in-card CTA 18→15px (weight 700 kept).

---

## 4. Visual Grammar & Motifs

Three vocabularies, picked per section by theme. Reproduce the concrete SVG
motifs below; signature SVGs ship in `assets/stamps/` and `assets/tabs/`.

### Vocabulary by world
| World        | Vocabulary                                                                                  |
|--------------|---------------------------------------------------------------------------------------------|
| Cartography  | lat/long grid · sextant cross-hairs · isohypses · spot-heights ▲ · compass rose · dashed routes · Latin placenames · `CARTE Nº X` cartouches · coord stamps |
| Passport/Postal| round obliteration cachet · rotated scotch tape · torn-ticket perforation · 4 dashed corner ticks · `PAR AVION · VIA AIR MAIL` stamps · hatched red/blue airmail bands · Roman numerals `Nº I → Nº XIV` |
| Jazz club    | 5-line music staff · treble clef `𝄞` · notes ♩♪♬♫ · vinyl grooves · boarding-pass timeline · pulsing orange featured halo · `STAGE · MMXXVI` stamp |

### Signature SVG assets (in `assets/stamps/`)
| Asset                      | Canonical use                                            |
|----------------------------|----------------------------------------------------------|
| `compass-rose.svg`         | 32-rhumb wind rose, anywhere (sections, atmospheres)     |
| `coord-stamp.svg`          | Inline coordinates badge `45°04′N · 5°33′E`              |
| `world-map.svg`            | World map filigree bg watermark                          |
| `stamp-vercors.svg`        | Round stamp `◉ VERCORS · 1050M` rotated -6°             |
| `stamp-entree-libre.svg`   | Oval banner `◉ ENTRÉE LIBRE` on concert cards           |
| `stamp-par-avion.svg`      | Hatched red/blue band `PAR AVION · VIA AIR MAIL`        |

### Origin stamps (canonical oval structure, viewBox 140×80)
56 country stamps + 4 French-region stamps (in `assets/origins/`) + 15 wine-region
stamps (in `assets/origins/vins/`) ship with this package. Every origin stamp
follows the SAME structure so a single filter chain recolors them all:
1. Outer oval ring `<ellipse>` stroke currentColor 1.4.
2. Inner dashed oval ring, opacity 0.55.
3. Dashed rectangular plate framing the name.
4. Country name `<text>` in Special Elite mono, currentColor, weight 700.
5. Centered distinctive emblem (Eiffel Tower, Fuji, kangaroo…), `scale(0.78)`.
6. Two lateral bornage dots `<circle r="1.2" opacity="0.6">`.

Name `<text>` size adapts to script: Latin short 12–13 / LS 0.4–0.6 · Latin long
8–9 / LS 0.2–0.3 · CJK 13–15 / LS 0.5–1 · Devanagari 11–13 · Arabic 11–13 ·
Hebrew 12–14 · Greek 12–14.

### Recolor — CRITICAL: filter chain, NEVER mask-image
`mask-image` + `background-color` drops the `<text>` layer of stamps/icons →
element renders invisible with no error. Always use `<img>` + a CSS `filter`
chain (variables in `tokens.css`):
```css
.icon-orange img { filter: var(--filter-orange-500); } /* → #d97a2a */
.stamp-gold  img { filter: var(--filter-gold-400);   } /* → #d4af5a */
.icon-cream  img { filter: var(--filter-cream-60);   } /* → #faf3e2 */
```
`brightness(0)` forces black regardless of stroke/fill/text, then hue recolors.

### Line-art icons (15 menu categories, in `assets/tabs/`)
Style: stroke 1.4–1.6px (never outside), linecap/linejoin round, fill none,
decorative details at opacity 0.55, bornage dots `<circle r="1.2" opacity=".6">`.
Recolor with the same filter chains (active = orange-500, inactive = cream-50 @
opacity 0.6).
- **Food (8):** `tapas` `planches` `fumaison` `currys` `pates` `woks` `salades` `desserts`
- **Drink (5):** `vins` `bieres` `cocktails` `softs` `bar`
- **Takeaway (2):** `sandwichs` `bowls`

### "Official postal stamp" border pattern (~40 uses)
The signature relief — no shadow, built from dashed borders:
```css
.stamp-officiel {
  border: 1.5px solid var(--orange-500);
  outline: 1px dashed rgba(217,122,42,.55);
  outline-offset: 4px;
  position: relative;
}
.stamp-officiel::before, .stamp-officiel::after {
  content:''; position:absolute; width:12px; height:12px;
  border:1.2px dashed var(--orange-500);
}
.stamp-officiel::before { top:6px; left:6px; border-right:none; border-bottom:none; }
.stamp-officiel::after  { bottom:6px; right:6px; border-left:none; border-top:none; }
```

### Canonical coordinates & geography
Coord HIBOUBOX `45°04′27″N · 5°33′12″E` · short `◉ 45°04′N · 5°33′E ·
VILLARD-DE-LANS` · altitude `ALT · 1050 M`. Vercors peaks (reusable): Grande
Moucherolle 2284m, Cornafion 2049m, Roc d'Arguille 1768m, HIBOUBOX 1050m.

### Latin placenames bank (use 1–2 per section)
`VIA · COQUINA` (cuisine) · `VIA · SPECIARUM` (spices) · `VIA · LITTERIS` (letters) ·
`VIA · DOMUS` (privatisation) · `TERRA · GASTRONOMICA` · `TERRA · CONVIVIA` ·
`PORTUS · DOMUS` · `MARE · APERITIVI` · `DOMUS · NOSTRA` · `AULA · MAGNA`.

### CSS textures (additive, use sparingly)
`.tex-grain` (SVG noise opacity 0.07, hero backgrounds) · `.tex-paper` (radial
cream dots, light pages) · `.tex-vinyl` (concentric grooves, music sections).

### Compass API caveat
Position the compass via explicit `top/right/bottom/left` + `size` + `opacity`.
❌ Never `position="bottom-right"` — that prop does not exist (silently ignored).
One compass per section, rolling position across sections.

---

## 5. Components & Primitives

All states are listed: default / hover / active(pressed) / disabled / featured.

### Button — levels × sizes
**Levels:**
| Level   | Background       | Text          | Border                | Hover                                  |
|---------|------------------|---------------|-----------------------|----------------------------------------|
| Primary | orange-500       | primary-fg `#1a0e04` | none           | bg orange-400 + `scale(1.02)`          |
| Outline | transparent      | orange-500    | 1.5px solid orange-500| wash `rgba(217,122,42,.10)`            |
| Ghost   | transparent      | cream-50      | 1px dashed cream-50/40| wash `rgba(250,243,226,.06)`           |
| Gold    | gold-400         | primary-fg    | none                  | bg gold-500 + `scale(1.02)` (Festin only)|

- **Pressed/active:** primary → orange-600; gold → gold-500; outline → bg wash + border orange-400.
- **Disabled:** bg `--primary-disabled` `#6a4824`, text `warm-500`, `cursor:not-allowed`, no hover transform.
- **Featured CTA:** may carry the pulsing halo, never relocated.

**Sizes:**
| Size    | Font | Padding       | Height | LS     | Use                              |
|---------|------|---------------|--------|--------|----------------------------------|
| Compact | 12px | 8×18px        | 36px   | 0.16em | header / nav                     |
| Base    | 14px | 12×22px       | 44px   | 0.14em | secondary inline CTAs            |
| Feature | 16–17px | 16–20×26–36px| 54px  | 0.12em | hero / section-end primary CTA   |
| In-card | 18–26px | 16–22×22–38px| auto  | 0.10–0.14em | CTA inside a card           |

Common: full pill (`border-radius:999px`), Barlow Condensed weight 700,
uppercase, arrow (`→` `↗`) BEFORE the label, transition transform .25s + bg .25s.

**In-card CTA rule (strict):** never compact/base inside an info card. Min 18px
desktop / 15px mobile, weight 700, padding ≥16×20, usually full-width (one CTA
per card). Hero CTAs up to 26px desktop / 18px mobile.

**Focus (WCAG 2.4.7 / 2.4.11):** `outline: 2px solid var(--orange-400);
outline-offset: 3px;` on every interactive element. Do NOT confuse the decorative
`1px dashed` postal pattern with the keyboard focus ring.

### Stamp (decorative passport badge)
Round / oval / rounded-rect (never sharp square). 1.5px solid orange-500 + inner
dashed ring offset 4px, bg ink-1000 or transparent. One mono uppercase line
(`◉ NOUVEAU · CONCERT`), optional Cormorant italic sub-line. Rotation -9°…+9°
(signature) or 0° (functional). Sizes S 28, M 56, L 92, XL 140.

### Card
On ink-900 → bg ink-800/ink-700; on ink-800 → bg ink-900. Border 1px
`rgba(217,122,42,.15)`, radius 12px, padding 24–32 desktop / 18–22 mobile.
- **Hover:** `translateY(-4px)`, border `rgba(217,122,42,.5)`, shadow
  `0 12px 40px rgba(0,0,0,.5), 0 0 30px rgba(217,122,42,.15)`.
  ⚠ Exception: Info-Pratiques cards must NOT translateY on hover
  (`transform: none !important`) — they collapse visually.
- **Featured:** border 1.5px solid orange-500 + pulsing halo (`--shadow-featured`
  + `hi-featured-halo` animation), rendered in-place — never relocated, never
  ribboned to the top.
- **Disabled:** opacity 0.5, no hover.

3 zones: head (circled dashed-orange icon + eyebrow + dashed separator) → body
(display title + Lato body + k/v list) → foot (full-width in-card CTA, `margin-top:auto`).

### Badge inline
Special Elite mono, padding 4×10, font 10–12px, 1px solid/dashed border. Variants:
orange (default), cream on dark, gold (Festin). Use: `FICHE Nº 04`, category tag.

### Chip / Pill
`border-radius:999px`, bg ink-700 or transparent + dashed border, padding
8–12×14–22, font 11–14px. For toggleable filters, classification tags, contact pills.

### Eyebrow
Label above a title, Barlow Condensed uppercase 11–22px, orange-500, LS
0.20–0.28em, weight 600, always uppercase.

### Display / Script
Display = Bungee (hero 92/48px LH 0.9 LS -0.01em; section 60–68/38–42px) with one
accent word. Script = Cormorant italic (hero 38–60/22–34px; full-width quote
26/19px), `text-wrap: balance`, always italic.

### Wave (section divider)
Soft sinusoidal SVG curve between ink-900↔ink-800, overlaid with a dashed-orange
passport-stitch (torn-ticket feel). Height 80px (up to 120px on heroes), flippable.

### Compass / Music staff / Coord badge / Section cartouche / Halo
- **Compass:** SVG wind rose, opacity 0.15–0.40, absolute position, 70–140px, one per section.
- **Music staff:** 5 dashed-orange lines + treble clef + 4–6 noted glyphs, opacity
  0.18–0.32, rotation -5…+5°, music/jazz sections only (decor, not functional).
- **Coord badge:** mono Special Elite pill, dashed-orange border, padding 4×12,
  font 11–15px. `◉ {LAT}°{MIN}′{SEC}″N · {LONG}°{MIN}′{SEC}″E`.
- **Section cartouche:** cartographer signature, `{ROLE} Nº {ROMAN} · {SUB-LATIN}`
  over `HIBOUBOX · ÉD. MMXXVI`, mono, opacity 0.62–0.78, rotation -3…+3°.
- **Featured halo:** pulsing orange glow (`box-shadow` + inset), never alters host
  position/size/alignment; on print it freezes to solid orange border + dashed offset.

### Component inventory
Button · Stamp · Card · Badge inline · Chip/Pill · Eyebrow · Display · Script ·
Wave · Compass · Music staff · Coord badge · Section cartouche · Featured halo.

---

## 6. Spacing & Layout

### Spacing — strict 4px base (all paddings/gaps/margins are multiples of 4)
`--sp-0` 0 · `--sp-1` 4 · `--sp-2` 8 · `--sp-3` 12 · `--sp-4` 16 · `--sp-5` 24 ·
`--sp-6` 32 · `--sp-7` 48 · `--sp-8` 64 · `--sp-9` 96 · `--sp-10` 128 (px).

### Section padding
`--sec-pad-y-desktop` 100px (standard) · `--sec-pad-y-lg` 128px (hero/editorial) ·
`--content-pad-x` `clamp(20px, 4vw, 64px)`. **Mobile: halved** — section 96→64,
hero 128→80, horizontal `clamp(16px, 4vw, 32px)`. Print A5+: reduce ~30%.

### Containers
`--container-max` 1280px (standard sections) · `--container-narrow` 880px
(editorial) · `--editorial-col` 720px (tight column, ~70 chars). Hero may overflow
to 1440px. **Golden rule: a long `<p>` never exceeds 720px wide.**

### Canonical grids
| Pattern            | Desktop                      | Mobile                                  |
|--------------------|------------------------------|-----------------------------------------|
| Hero split         | `1.18fr / 1fr` gap 36px      | `1fr` stack                             |
| Map + Coords       | `1fr / 1fr` gap 28–32px      | `1fr` stack                             |
| 3 feature cards    | `repeat(3,1fr)` gap 24–32px  | `1fr` stack                             |
| 4 mini-info cells  | `repeat(4,1fr)` gap 16px     | `repeat(2,1fr)` gap 12px                |
| 5 profile cards    | `repeat(5,1fr)` gap 18px     | 2×2 `calc(50%-9px)` + 5th full-width    |
| Newsletter strip   | `1.4fr / 1fr` gap 32px       | `1fr` stack                             |
| Section bascule    | `1fr / 1fr` gap 48px         | `1fr` stack                             |

### Section anatomy (order)
tone-on-tone bg → world-map filigree → compass corner → ONE signature artefact →
[eyebrow → display → lead → content] → bottom-right cartouche → Wave divider →
next section (inverse tone).

### Hero anatomy
Grid `1.18fr / 1fr`, gap 36px, max-width 1280, vertical align `start` (not center).
Main photo: outline solid orange-500 1.5px + outline dashed offset 4px + 4 corner
ticks; signature stamp integrated top-right rotated -6…-9° (never negative
overflow → mobile collapse). Meta column: eyebrow → coord badge → display (one
accent word) → script → lead (max 3 lines) → max 2 CTAs (primary + outline) →
optional full-width 4-cell mini-info band.

---

## 7. Motion & Interaction

### Durations & easings (in `tokens.css`)
fade-in 0.8s ease · hover-link 0.18s ease · hover-card 0.25s ease · featured halo
4.8s ease-in-out infinite · drawer-slide 0.32s `cubic-bezier(0.35,0,0.25,1)`.

### Elevation philosophy
HIBOUBOX avoids generic soft-UI shadows. Only three depths allowed:
1. **Functional shadow** on modals/dropdowns/popovers (`--shadow-md`).
2. **Signature orange glow** pulsing on featured items (`--glow-orange`).
3. **Inset stage glow** for "under stage light" surfaces (`--glow-stage`).

Body cards get NO shadow — relief comes from dashed-orange border + outline offset.

| Token             | Value                                  | Use                      |
|-------------------|----------------------------------------|--------------------------|
| `--shadow-sm`     | `0 1px 2px rgba(0,0,0,.4)`             | very subtle (rare)       |
| `--shadow-md`     | `0 6px 24px rgba(0,0,0,.55)`          | modal / dropdown         |
| `--shadow-lg`     | `0 24px 60px rgba(0,0,0,.7)`          | full-screen modal lift   |
| `--glow-orange`   | `0 0 40px rgba(217,122,42,.35)`       | featured halo, CTA hover |
| `--glow-stage`    | `inset 0 -30px 80px rgba(217,122,42,.25)` | stage-light surfaces |

### Featured halo (signature pattern)
```css
.item.featured { animation: hi-featured-halo 4.8s ease-in-out infinite; }
@keyframes hi-featured-halo {
  0%,100% { box-shadow: inset 0 0 0 1px rgba(217,122,42,.28); }
  50%     { box-shadow: inset 0 0 0 1px rgba(217,122,42,.42), 0 0 24px rgba(217,122,42,.18); }
}
```
The halo never changes the host's size, position, or alignment — overlay only.

### Interaction patterns
- **Hover:** primary buttons `scale(1.02)` + bg shift; cards `translateY(-4px)` +
  border brighten (except Info-Pratiques cards).
- **Marquee:** 48s linear infinite desktop / 30s mobile, items ×3, mask-image fade
  edges, pause on hover.
- **Modals/galleries:** arrow ← → nav, touch swipe, Esc, backdrop click, ✕ button;
  `backdrop-filter: blur(8px)` + `rgba(10,9,8,.94)`, z-index 9000.

### Reduced motion (non-negotiable)
`@media (prefers-reduced-motion: reduce)` disables ALL animation/transition (halos,
marquees, transitions). The package's `tokens.css` already ships a global override.

---

## 8. Do's & Don'ts

### Do's
- ✅ Use CSS variable tokens, never hex literals (`var(--orange-500)`).
- ✅ Max 2 orange accents per screen; a third → cream-100 or outline.
- ✅ One atmosphere per section; vary vocabulary; opacity ≤0.55 (cartouches ≤0.78).
- ✅ Alternate ink-900 / ink-800 between sections; footer ink-1000; join with Wave.
- ✅ Display with one inline accent word; `text-wrap: balance` on serif titles.
- ✅ Recolor SVG via `<img>` + filter chain (never mask-image).
- ✅ "Official postal stamp" relief = dashed border + outline offset 4px + 4 corner ticks.
- ✅ In-card CTA ≥18px desktop / 15px mobile, weight 700, usually full-width.
- ✅ Décor `aria-hidden`; respect `prefers-reduced-motion`; visible focus ring (orange-400, 2px).
- ✅ `tabular-nums` on tables/prices/coords; EU price format `12,00 €` (comma + nbsp + €).
- ✅ Roman numerals `Nº I → Nº XIV` for cartouches/section heads; first person in manifesto.
- ✅ Featured = derived from the clock (`UPCOMING[0]`), never a hard flag; rendered in-place.
- ✅ Generic copy (no hard dates) in section leads; "everyone is seated" (bar included).
- ✅ Forms: themed custom popovers for date/select/number, honeypot + server validation.

### Don'ts
- ❌ Purple/violet aggressive gradients; gradient on every background.
- ❌ Emoji feature icons (✨🚀🎯) or decorative emoji (⚠✓◉☕♪) in letters/manifestos/editorial.
- ❌ Rounded cards with left-border accent; an icon beside every heading.
- ❌ Inter/Roboto/Arial as display; serif/Georgia to fake Bungee in previews.
- ❌ `mask-image` + `background-color` to recolor SVG containing `<text>` (silently invisible).
- ❌ Inventing country emblems off the canonical oval stamp structure.
- ❌ Rival "Réserver" CTAs in one section; email pill rivaling the section's primary CTA.
- ❌ Two dominant signature artefacts in one section; décor hidden behind cards.
- ❌ Blurry blue soft-UI shadow (`0 4px 20px rgba(0,0,0,.1)`); colored shadow outside orange.
- ❌ `translateY(-4px)` hover on Info-Pratiques cards (override `transform:none !important`).
- ❌ "non-attablés" / "bar debout" in copy; hard dates/numbers in section leads.
- ❌ Mixing orange + gold on one CTA/section; gold as a general UI accent; olive as a CTA.
- ❌ Bungee in body; Lato in display; Cormorant non-italic; eyebrow tracking <0.16em.

### Brand voice (when generating copy)
French, sober, editorial — "independent magazine paper," never commercial/startup.
Five pillars: editorial sobriety (no superlatives), place singularity (voyage,
escale, route, fumaisons, accueil à table), assumed first person, no advertising
gesture, engagement without pose (the 10% HT to artists is factual/structural).
Master tagline: *« le voyage commence à table »*. Avoid: "unique en son genre",
"expérience inoubliable", "venez nombreux", anglicisms (foodie, hub, vibes).
Keep surface copy date-free so it works year-round; dates live on data-bound
badges/captions only.

---

## 9. Mobile Adaptations

This package is consumed by mobile-app and web-prototype skills. The source brand
is web/print-first; the rules below adapt it to native mobile (Expo / React
Native) and small-screen web while preserving the grammar.

### Touch & sizing
- **Touch targets ≥ 44px** (`--hit-target`). In-card CTAs full-width, min 48px tall.
- Buttons: never `compact`/`base` size on a primary mobile action — use `feature`
  or `in-card` (≥15px text, weight 700, padding ≥16×20).
- Increase tap spacing: min 8px (`--sp-2`) between adjacent touch targets.

### Typography on mobile (bump editorial sizes up for arm's-length legibility)
display hero 92→48px (LH 0.9→1.15) · display section 60–72→38–44px (LH 1.15) ·
eyebrow hero 22→16px (0.22em kept) · eyebrow section 19→15px (tracking 0.18em to
avoid wraps) · body 16→14–15px (LH 1.55 kept) · in-card CTA 18→15px (weight 700).
Never drop below 12px for any readable text.

### Navigation — bottom tab bar
- Use a **bottom tab bar** (not a top nav) with 3–5 items, safe-area inset bottom.
- Active tab marker: **`picto-owl-orange.png`** (in `assets/logos/`) or an orange-500
  recolored line-art icon from `assets/tabs/`; inactive icons cream-50 @ opacity 0.6
  (filter `--filter-cream-60`), active recolored orange-500 (`--filter-orange-500`).
- Tab bar bg `ink-1000`, top border `--border-faint`, labels Barlow Condensed
  uppercase 10–11px tracking 0.16em.

### Sheets instead of modals
- Replace desktop center modals with **bottom sheets** that slide up
  (`--dur-drawer` 0.32s `--ease-drawer`), rounded top corners `--r-xl` (20px),
  drag handle (cream-50 @ 0.3, 36×4px pill), backdrop `rgba(10,9,8,.94)` +
  `blur(8px)`. Full-screen galleries keep the dark modal pattern.
- Drawer/menu décor: minimal — a single music staff or compass at low opacity,
  CSS counter `upper-roman` for nav items.

### Atmosphere on small screens
Simplify rather than disable: keep ONLY world-map filigree + signature cartouche +
compass rose; drop dense grids, multiple placenames, isohypses. Décor stays
`aria-hidden`. The featured halo is fine but honor reduced-motion.

### Layout
- All multi-column grids collapse to `1fr` stack (see §6 grids) except 4 mini-info
  cells → `repeat(2,1fr)`.
- Section padding halved (96→64, hero 128→80); horizontal `clamp(16px,4vw,32px)`.
- Hero: stack meta column below the photo; stamp stays integrated top-right inside
  the photo (never negative overflow).

### Native (Expo / React Native) mapping
- Tokens → a JS theme object (mirror `tokens.css` names). Use `Platform`-safe font
  loading for the 6 families via `expo-font`; ship the same fallbacks.
- Shadows: warm only; on Android use `elevation` sparingly (modals/sheets only),
  body cards rely on dashed-border relief (use a 1px bordered `View`, no elevation).
- SVG recolor: use `react-native-svg` with `currentColor`/`fill` props rather than
  CSS `filter` (filter chains are web-only) — stamps use `currentColor` so set
  `color`/`fill` to the token hex directly.
- Respect OS "reduce motion" (`AccessibilityInfo.isReduceMotionEnabled`) → disable
  the halo and slide animations.
- Safe-area insets on hero top and tab-bar bottom (`react-native-safe-area-context`).

---

## 10. Asset References

All paths are relative to this `hiboubox-od/` package root. Black PNG/SVG assets
are recolored at use-time via the filter chains in §4 / `tokens.css` — never
re-export a recolored copy.

### Logos — `assets/logos/`
| File                        | Canonical use                                              | Min size | Recolor |
|-----------------------------|------------------------------------------------------------|----------|---------|
| `logo-full-orange.png`      | Full logo — footer, full-size print, exterior signage      | 120px w  | filter to orange-700 on cream |
| `wordmark-orange.png`       | Wordmark only — narrow banners, compact headers, watermark | 80px w   | —       |
| `picto-owl-orange.png`      | Owl picto — favicon, OG, social avatar, **mobile tab marker** | 32px   | —       |
| `hiboubox-stamp-logo.png`   | Stamp-logo — sticky header, mobile nav, document signature | 38px h mobile / 48px desktop | `--filter-stamp-sepia` default |
| `festin-du-hibou-black.png` | Le Festin du Hibou sub-brand (catering) — gold filter only | 200px w  | `--filter-gold-400` (never orange) |

Protection space = the height of the wordmark "H" around every logo. Allowed
backgrounds: ink-1000/900/800, cream-50 (recolor to orange-700 on cream).

### Signature stamps — `assets/stamps/`
`compass-rose.svg` · `coord-stamp.svg` · `world-map.svg` · `stamp-vercors.svg` ·
`stamp-entree-libre.svg` · `stamp-par-avion.svg`. All SVG monochrome with
`currentColor`, recolor via filter chain (web) or `color`/`fill` (native). Use:
see §4 table. Rule: max 1 large watermark stamp per section.

### Line-art category icons — `assets/tabs/` (15 SVG)
Food: `tapas.svg` `planches.svg` `fumaison.svg` `currys.svg` `pates.svg`
`woks.svg` `salades.svg` `desserts.svg`. Drink: `vins.svg` `bieres.svg`
`cocktails.svg` `softs.svg` `bar.svg`. Takeaway: `sandwichs.svg` `bowls.svg`.
Stroke 1.4–1.6, fill none, recolor via filter chain. Sizes: sub-tab 38px desktop
/ 28px mobile; card-head circle 56×56 / 44×44; mini-info cell 46×46 / 30×30.

### Origin stamps — `assets/origins/` (56 countries + 4 FR regions) & `assets/origins/vins/` (15 wine regions)
viewBox 140×80, monochrome `currentColor`, gold filter (`--filter-gold-400`),
watermark opacity ~0.72, max 1 large watermark per section. Canonical oval
structure in §4.
- **Countries (52):** afriquesud, algerie, allemagne, antilles, argentine,
  australie, autriche, belgique, bresil, cambodge, chili, chine, colombie, coree,
  cuba, dominicaine, egypte, espagne, etats-unis, ethiopie, france, grece, inde,
  indonesie, irlande, israel, italie, jamaique, japon, laos, liban, madagascar,
  malaisie, maroc, mexique, nouvelle-zelande, pays-bas, perou, philippines,
  portugal, reunion, senegal, singapour, sri-lanka, suisse, syrie, tahiti,
  thailande, tunisie, turquie, uk, vietnam.
- **French regions (4):** dauphine, provence, savoie, vercors-region.
- **Wine regions (15):** alsace, beaujolais, bordeaux, bourgogne, bugey,
  champagne, corse, jura, languedoc, loire, provence, rhone, roussillon, savoie,
  sud-ouest.

### Tokens & preview
- `tokens.css` — all compiled CSS custom properties (colors, type, spacing, radius,
  shadows, filter chains) + focus ring + featured-halo keyframes + reduced-motion.
- `preview/brand-showcase.html` — full interactive brand showcase (open in a browser
  to see logos, palette, type, motifs, components rendered live).

### Brand facts (for copy / signatures)
HibouJazz SARL · 41 rue des Pionniers, 38250 Villard-de-Lans · `contact@hiboubox.fr`
· coordinates `45°04′N · 5°33′E` · altitude 1050 M · edition `ÉD. MMXXVI`. Sub-brand:
Le Festin du Hibou (catering), `contact@lefestinduhibou.fr`, gold accent.
