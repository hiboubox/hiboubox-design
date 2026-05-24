# HIBOUBOX — Brand Design System

Système de design officiel de **HIBOUBOX**, restaurant-concert-bar à Villard-de-Lans, Vercors.

**→ [Brand Showcase live](https://hiboubox.github.io/hiboubox-design/brand-showcase.html)**

---

## Contenu

| Fichier / Dossier | Description |
|---|---|
| `brand-showcase.html` | Showcase interactif complet du système de design |
| `DESIGN.md` | Spécification complète — tokens, typographie, couleurs, composants |
| `DESIGN-MANIFEST.json` | Manifeste machine-readable pour les outils de développement |
| `DESIGN-HANDOFF.md` | Guide d'implémentation pour les développeurs |
| `assets/` | 100+ assets SVG/PNG — logos, stamps, icônes, origines culinaires |

## Système de design

38 tokens CSS organisés en 3 rôles :

- **Palette** — ink, cream, orange, gold, olive, paper, warm
- **Typographie** — Playfair Display (titres) · Inter (corps) · JetBrains Mono (accents)
- **Composants** — boutons, cartes, badges, navigation, formulaires, états interactifs

## Usage

Ce repo est la **source de vérité visuelle** pour le site HIBOUBOX. Toute implémentation doit partir de `brand-showcase.html` et respecter les tokens définis dans `DESIGN.md`.

```css
/* Exemple : utiliser les tokens, jamais les hex en dur */
color: var(--orange-500);
background: var(--cream-100);
font-family: var(--font-display);
```

## Couverture responsive

360px → 1920px via `clamp()` fluide et container queries.
Matrice de validation : mobile compact / standard / large · tablette portrait/paysage · laptop · desktop · wide.

---

**HIBOUBOX** · 41 rue des Pionniers, 38250 Villard-de-Lans · [hiboubox.fr](https://hiboubox.fr)
