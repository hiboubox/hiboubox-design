# HIBOUBOX — App mobile · trame de projet (OD)

> Brief persistant du prototype mobile HIBOUBOX, conçu dans Open Design avec le
> design system **HIBOUBOX** actif, puis implémenté en **Expo / React Native**
> (via Claude Code) à partir des écrans OD. Données réelles : **Directus**.
>
> **But de ce fichier** : garder une source de vérité unique pour que chaque
> session (qui ajoute un écran) reste cohérente avec les précédentes. À déposer
> dans le projet OD « HIBOUBOX App ». Chaque prompt d'écran référence ce brief.

---

## 1. Périmètre & règle d'or

- OD ne produit que le **proto visuel** (maquettes iPhone, données statiques
  réalistes). Toute logique backend (Directus, notifs, n8n) est **hors proto** :
  on ne maquette que les *affordances* UI (bandeau InfoLive, bouton « Être
  notifié », état abonné…).
- **Un seul projet OD** pour toute l'app. Chaque écran = un fichier dans ce
  projet. Réutiliser le **cadre iPhone + tab bar de l'écran Accueil** comme
  gabarit pour garantir la cohérence inter-sessions.
- Cible device : **iPhone 15 Pro 390×844**. Pas d'image externe → placeholders.

## 2. Règles design mobile (résumé — détail dans le DS HIBOUBOX §9)

- Fond **ink** sombre, texte **cream**. Accent **ORANGE unique, max 2/écran**.
- Titres **Bungee** (uppercase, 1 mot accent orange). Citations **Cormorant
  italique**. Dates/heures/prix/coordonnées **Special Elite mono** (`.num`,
  tabular), format FR : « VEN 17 MAI · 20H30 », « 12,00 € ».
- Eyebrows **Barlow Condensed** uppercase, tracking 0.22em, orange.
- Grammaire cartographie/passeport/jazz en décor ≤ 0.3 : coord badge
  `◉ 45°04′N · 5°33′E`, cadres « tampon postal » (1.5px solid orange + outline
  dashed offset 4px + 4 corner ticks), rose des vents, cartouche `Nº` romain.
- Cibles tactiles ≥ 44px. Copy **FR**, sobre/éditorial, **jamais de dates dures
  dans les intros** (les dates vivent sur les badges data-bound). Jamais
  « non-attablés » (tout le monde s'assoit).
- Modales = **bottom sheets**. `prefers-reduced-motion` respecté.

## 3. Navigation

```
Tab Bar (5 onglets, bas d'écran — présente partout SAUF Détail concert)
├── Accueil
├── Programmation ──► Détail concert (stack poussé, SANS tab bar, header ‹ retour)
├── Menus ──► Choix Sur place / À emporter ──► Liste menu
│                                    └── deep-link QR table ──► Liste Sur place direct
├── Infos
└── Réserver (WebView CoverManager)
```

Onglet actif = orange + marqueur picto-chouette. Inactifs = cream 60 %. Icônes
line-art.

## 4. Modèle de données Directus (référence, pour l'impl. Expo)

| Collection | Champs clés | Écrans |
|---|---|---|
| `concerts` | artiste, genre, description, date, heure_debut, heure_fin, tarif/prix_libre (bool), visuel, statut (`publie`) | Accueil, Programmation, Détail |
| `expositions` | artiste, titre, accroche, date_debut, date_fin, visuel | Accueil |
| `infos_live` | message, actif (bool) | Accueil (bandeau InfoLive) |
| `menu_items` | categorie, nom, description, prix, origine_pays, regime[], service (`sur_place`/`emporter`) | Menus |
| `etablissement` | adresse, code_postal, ville, lat, long, altitude, horaires, happy_hour, tel, email, instagram, facebook | Infos |
| `notification_subscriptions` | expo_token, concert_id, date | Détail (bouton « Être notifié ») |

## 5. Inventaire des écrans & statut

| Nº | Écran | Archétype | Tab bar | Statut |
|----|-------|-----------|---------|--------|
| I   | Accueil            | Feed              | oui (Accueil)      | **à faire (session 1)** |
| II  | Programmation      | Feed              | oui (Programmation) | à venir |
| III | Détail concert     | Detail            | non (stack)        | à venir |
| IV  | Menus · choix      | Focus             | oui (Menus)        | à venir |
| V   | Menu Sur place     | Feed              | oui (Menus)        | à venir |
| VI  | Infos              | Profile           | oui (Infos)        | à venir |
| VII | Réserver           | Focus             | oui (Réserver)     | à venir |

> Mettre à jour la colonne **Statut** après chaque session.

## 6. Workflow inter-sessions (toujours le même projet, auto-documenté)

Le projet s'auto-entretient via `CLAUDE.md` + `memory/` (voir §8). Chaque session :

1. Ouvrir le projet OD **« HIBOUBOX App »** (design system HIBOUBOX sélectionné).
2. **Début de session** : l'agent LIT `CLAUDE.md` + `memory/INDEX.md` +
   `memory/screen-conventions.md` pour reprendre le fil.
3. Activer le skill **`mobile-app`**.
4. Coller le prompt de l'écran à faire (voir `OD-PROMPTS.md`). Chaque prompt
   (II→VII) reprend le cadre/tab bar de l'Accueil pour la cohérence.
5. **Fin de session** : l'agent met à jour le **statut** (CLAUDE.md §inventaire),
   écrit `memory/sessions/SESSION-XX-<ecran>.md`, et complète l'INDEX.

## 7. Convention de cohérence (à ne pas dévier)

- Même cadre device, même tab bar (mêmes icônes, mêmes positions), même échelle
  typo entre tous les écrans → valeurs verrouillées dans
  `memory/screen-conventions.md` après l'Accueil.
- Numérotation cartouche **séquentielle** : Accueil = `Nº I`, Programmation =
  `Nº II`, … (voir §5).
- Un seul accent orange dominant + un CTA orange par écran (budget = 2).

## 8. Suivi auto-entretenu — `CLAUDE.md` + `memory/`

Créés par l'agent à la **session 1** (prompt de lancement), maintenus ensuite.

```
HIBOUBOX App (projet OD)
├── CLAUDE.md                       ← bible du projet (lue à chaque session)
├── memory/
│   ├── INDEX.md                    ← pointeur 1 ligne par entrée
│   ├── decisions.md                ← décisions design/nav + pourquoi (append)
│   ├── screen-conventions.md       ← valeurs VERROUILLÉES du gabarit Accueil
│   │                                  (dims cadre, hauteur/icônes tab bar,
│   │                                   échelle typo, tokens) — référence pixel
│   └── sessions/
│       └── SESSION-01-accueil.md   ← log par session (produit, choix, next)
└── <Écran>.html                    ← un artefact par écran
```

**`CLAUDE.md`** contient : objectif & stack cible (Expo/RN + Directus +
CoverManager + expo-notifications + n8n), design system actif + règles mobile,
navigation complète, modèle de données Directus, inventaire écrans + statut,
conventions de cohérence, protocole de session, hors-scope proto, glossaire.

**Protocole de session** (gravé dans CLAUDE.md) — début : lire CLAUDE.md +
memory/ ; fin : MAJ statut + `memory/sessions/SESSION-XX.md` + INDEX. C'est ce
qui assure le suivi d'une session à l'autre.
