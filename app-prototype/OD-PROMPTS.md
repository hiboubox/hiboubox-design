# HIBOUBOX App — prompts OD (un par écran)

> Projet OD unique, design system **HIBOUBOX** actif, skill **`mobile-app`**.
> Le projet est **auto-documenté** (`CLAUDE.md` + `memory/`, voir
> [APP-SPEC.md](APP-SPEC.md) §8). Génère un écran par session.
>
> - **Nº I (lancement)** : bootstrap du projet (CLAUDE.md + memory/) **puis** Accueil.
> - **Nº II→VII** : chaque prompt commence par lire le suivi et finit par le mettre à jour.

---

## Nº I — LANCEMENT  *(bootstrap projet + Accueil — session 1)*

```
Tu démarres le projet « HIBOUBOX App » : le PROTOTYPE mobile de l'application
HIBOUBOX (restaurant-concert-bar-galerie, Vercors), qui sera ensuite implémenté
en Expo / React Native à partir de ces maquettes, données réelles via Directus.
Le projet se construit sur PLUSIEURS sessions, un écran à la fois. AVANT de
dessiner, installe un système de suivi auto-entretenu (comme un projet de dev),
puis génère l'écran Accueil qui servira de GABARIT.

═══ ÉTAPE A — Crée le fichier CLAUDE.md à la racine du projet ═══
Il est lu au début de CHAQUE session. Mets-y EXACTEMENT ces sections :

# HIBOUBOX App — prototype mobile (OD)
## Objectif
Prototype visuel de l'app mobile HIBOUBOX, écran par écran, dans OD. Source de
vérité visuelle pour l'implémentation Expo/React Native ultérieure (Claude Code).
## Stack cible (hors proto — pour mémoire d'implémentation)
Expo / React Native (expo-router : 5 tabs + stack Détail), données Directus (SDK),
réservation = WebView CoverManager, notifs = expo-notifications + Expo Push API,
automatisations = n8n (webhook Directus « concert publié » + cron du matin).
## Design system
HIBOUBOX (actif dans OD). Version MOBILE : fond ink sombre, texte cream, accent
ORANGE unique (max 2/écran), titres Bungee (1 mot accent), citations Cormorant
italique, dates/heures/prix/coords en Special Elite mono (format FR « VEN 17 MAI
· 20H30 », « 12,00 € »), eyebrows Barlow uppercase 0.22em, cadres « tampon
postal » (orange + dashed offset + 4 corner ticks), coord badge ◉ 45°04′N ·
5°33′E, cartouche Nº romain. Cibles ≥ 44px. Copy FR sobre. Aucune image externe.
## Navigation
Tab bar 5 onglets (présente partout SAUF Détail concert) : Accueil · Programmation
· Menus · Infos · Réserver. Programmation → Détail concert (stack, sans tab bar).
Menus → Choix Sur place/À emporter → Liste menu (deep-link QR table → Sur place).
Réserver = WebView CoverManager. Onglet actif orange + picto-chouette, inactifs
cream 60 %, icônes line-art.
## Modèle de données Directus
- concerts(artiste, genre, description, date, heure_debut, heure_fin, tarif/
  prix_libre, visuel, statut=publie) → Accueil, Programmation, Détail
- expositions(artiste, titre, accroche, date_debut, date_fin, visuel) → Accueil
- infos_live(message, actif) → bandeau InfoLive Accueil
- menu_items(categorie, nom, description, prix, origine_pays, regime[], service=
  sur_place|emporter) → Menus
- etablissement(adresse, cp, ville, lat, long, altitude, horaires, happy_hour,
  tel, email, instagram, facebook) → Infos
- notification_subscriptions(expo_token, concert_id, date) → bouton « Être notifié »
## Inventaire des écrans & statut
| Nº | Écran | Archétype | Tab bar | Fichier | Statut |
|----|-------|-----------|---------|---------|--------|
| I   | Accueil        | Feed    | oui  | (à créer) | en cours |
| II  | Programmation  | Feed    | oui  | —         | à venir |
| III | Détail concert | Detail  | non  | —         | à venir |
| IV  | Menus · choix  | Focus   | oui  | —         | à venir |
| V   | Menu Sur place | Feed    | oui  | —         | à venir |
| VI  | Infos          | Profile | oui  | —         | à venir |
| VII | Réserver       | Focus   | oui  | —         | à venir |
## Conventions de cohérence (ne pas dévier)
Même cadre iPhone 15 Pro 390×844, même tab bar (icônes/positions), même échelle
typo sur tous les écrans → valeurs verrouillées dans memory/screen-conventions.md.
Cartouche Nº séquentiel (Accueil=I…). Budget accent orange = 2/écran. Affordances
notif maquettées seulement (pas de backend).
## Protocole de session
DÉBUT : lire ce CLAUDE.md + memory/INDEX.md + memory/screen-conventions.md.
FIN : mettre à jour le statut ci-dessus ; écrire memory/sessions/SESSION-XX-
<ecran>.md (produit, choix, à faire ensuite) ; ajouter la ligne dans
memory/INDEX.md ; logguer toute décision structurante dans memory/decisions.md.
## Glossaire
InfoLive = bandeau statut temps réel (repris du site). Gabarit = l'écran Accueil,
référence visuelle des suivants. Stamp = badge/cadre tampon postal.

═══ ÉTAPE B — Crée le dossier memory/ ═══
- memory/INDEX.md : titre + 1 ligne par entrée (table des matières du suivi).
- memory/decisions.md : journal append-only des décisions design/nav + pourquoi.
- memory/screen-conventions.md : à remplir en ÉTAPE E avec les valeurs RÉELLES du
  gabarit Accueil (dimensions du cadre, hauteur + icônes + ordre de la tab bar,
  tailles typo display/eyebrow/body/mono, tokens couleur utilisés) — pour que les
  prochains écrans s'y conforment au pixel.
- memory/sessions/ : un fichier log par session.

═══ ÉTAPE C — Génère l'écran ACCUEIL (gabarit) ═══
Cadré iPhone 15 Pro 390×844 (encoche, status bar, home indicator). Soigne le cadre
device et la TAB BAR (5 onglets, « Accueil » actif orange + picto-chouette, autres
cream 60 %, icônes line-art) — ils seront réutilisés tels quels.
Contenu vertical :
1. Bandeau « InfoLive » pleine largeur (ink-1000, point orange pulsant + texte
   mono) : « ◉ OUVERT · CONCERT CE SOIR 20H30 ».
2. Hero « Prochain concert » = card featured HALO orange + cadre tampon : eyebrow
   « ◉ JAZZ MANOUCHE · VERCORS », titre Bungee « TRIO MARLOWE » (MARLOWE accent),
   datetime mono « VEN 17 MAI · 20H30 », stamp « ◉ ENTRÉE LIBRE ». (Tap → détail.)
3. Card « Exposition en cours » : eyebrow « ◉ SUR NOS MURS », titre œuvre, artiste,
   placeholder visuel, petit CTA « Découvrir ».
4. Bloc citation Cormorant italique « le voyage commence à table », guillemet
   orange géant en filigrane.
5. CTA primary pleine largeur « → Réserver une table ».
Accent orange = halo + CTA (2 max). Coord badge discret. Cartouche « Nº I ».

═══ ÉTAPE D — Clôture de session ═══
Remplis memory/screen-conventions.md avec les valeurs réelles utilisées ; passe
le statut Accueil à « fait » + renseigne son nom de fichier dans CLAUDE.md ;
écris memory/sessions/SESSION-01-accueil.md ; ajoute les lignes dans INDEX.md.
Termine par un court résumé : ce qui est produit + le prochain écran (Nº II).
```

---

## Nº II — PROGRAMMATION

```
DÉBUT : lis CLAUDE.md + memory/INDEX.md + memory/screen-conventions.md du projet.
Reprends EXACTEMENT le cadre iPhone, la tab bar et l'échelle typo de l'Accueil.
Écran « PROGRAMMATION », onglet « Programmation » actif.

Header : eyebrow « ◉ L'AGENDA À VENIR », titre Bungee « PORTÉE · NAVIGATION »
(NAVIGATION accent), décor portée musicale + clé de sol 𝄞 filigrane.
Liste de 5 concerts (cards boarding-pass → Détail) : badge date mono « VEN 17
MAI », eyebrow genre, artiste Bungee 22px (1 mot accent), meta mono « 20H30 ·
ENTRÉE LIBRE », chevron ↗.
Données : VEN 17 Trio Marlowe (manouche) · SAM 18 Quartet Ribérol (moderne) ·
DIM 19 Jam Session (scène ouverte · 19H30) · VEN 24 Duo Margaux (chanson FR) ·
SAM 25 Céline & Groupe (folk). Accent orange ≤ 2. Cartouche « Nº II ».

FIN : MAJ statut (Programmation=fait + fichier) dans CLAUDE.md ; écris
memory/sessions/SESSION-02-programmation.md ; ajoute à INDEX.md.
```

---

## Nº III — DÉTAIL CONCERT  *(SANS tab bar)*

```
DÉBUT : lis CLAUDE.md + memory/. Reprends le cadre iPhone et l'échelle typo de
l'Accueil, mais SANS tab bar (stack). Header chevron retour « ‹ ».
1. Visuel affiche plein cadre (placeholder) + cadre tampon + stamp top-right
   rotated -6° « ◉ DANS 3 JOURS ».
2. Eyebrow « ◉ JAZZ MANOUCHE · VERCORS ». 3. Titre Bungee « TRIO MARLOWE ».
4. Script italique « guitare · contrebasse · violon ».
5. Datetime stamp : « VEN 17 MAI » / « 20H30 → 22H30 » / mono « ◉ DEUX SETS ·
   ENTRÉE LIBRE · PRIX LIBRE ». 6. Description 2-3 phrases sobres.
7. Bouton orange « → Être notifié » (au tap : « ◉ Vous serez prévenu le jour J »).
8. Bouton outline « → Ajouter à l'agenda ». Accent = stamp + bouton (2).
Cartouche « Nº III ».
FIN : MAJ statut + memory/sessions/SESSION-03-detail.md + INDEX.md.
```

---

## Nº IV — MENUS · CHOIX

```
DÉBUT : lis CLAUDE.md + memory/. Reprends cadre/tab bar/typo de l'Accueil. Onglet
« Menus » actif. Archétype Focus.
Header : eyebrow « ◉ NOTRE CARTE », titre Bungee « SUR PLACE OU EMPORTER ? ».
2 grandes cartes de choix (≥ 88px) : « SUR PLACE » (icône assiette line-art,
« cuisine du monde, servie à table ») / « À EMPORTER » (icône sac kraft,
« sandwichs, bowls, à récupérer »), cadres tampon. Note mono « ◉ Scannez le QR
sur votre table pour ouvrir le menu directement ». Accent ≤ 2. Cartouche « Nº IV ».
FIN : MAJ statut + memory/sessions/SESSION-04-menus-choix.md + INDEX.md.
```

---

## Nº V — MENU SUR PLACE (liste)

```
DÉBUT : lis CLAUDE.md + memory/. Reprends cadre/tab bar/typo de l'Accueil. Onglet
« Menus » actif (atterrissage deep-link QR).
Sous-onglets catégories line-art scrollables : Tapas · Woks · Currys · Salades ·
Desserts · Vins · Bières (« Woks » actif orange). Chips filtres Végé · Sans gluten.
Liste items : « nom …… (dot-leaders) 16,00 € » (prix mono tabular) + courte desc.
Stamp origine gold filigrane « ◉ THAÏLANDE ». Ex. Woks : Wok bœuf basilic thaï
16,00 € · Pad thaï crevettes 17,50 € · Wok légumes & tofu fumé 14,00 €.
Accent ≤ 2. Cartouche « Nº V ».
FIN : MAJ statut + memory/sessions/SESSION-05-menu-surplace.md + INDEX.md.
```

---

## Nº VI — INFOS

```
DÉBUT : lis CLAUDE.md + memory/. Reprends cadre/tab bar/typo de l'Accueil. Onglet
« Infos » actif. Archétype Profile.
Section « VENIR » (eyebrow « ◉ SE RENDRE À HIBOUBOX ») : bloc adresse dashed
« 41 rue des Pionniers / 38250 · Villard-de-Lans / ◉ 45°04′N · 5°33′E · ALT 1050
M » ; widget carte (grille + pin orange) → « Ouvrir dans Google Maps » ; k/v mono
Horaires « Mar → Dim · 18-22h » · Concerts « 20h30 · entrée libre » · Happy hour
« 16h → 18h · -20% ».
Section « NOUS CONTACTER » (eyebrow « ◉ VIA · LITTERIS ») : pill ☎ « 04 56 00 09
56 » · pill « contact@hiboubox.fr » · Instagram · Facebook line-art · CTA « → Nous
écrire ». Accent ≤ 2. Cartouche « Nº VI ».
FIN : MAJ statut + memory/sessions/SESSION-06-infos.md + INDEX.md.
```

---

## Nº VII — RÉSERVER

```
DÉBUT : lis CLAUDE.md + memory/. Reprends cadre/tab bar/typo de l'Accueil. Onglet
« Réserver » actif. Archétype Focus.
WebView CoverManager habillée « cadre passport » : topstrip orange « ◉ RÉSERVATION
· COVERMANAGER » ; grand cadre tampon (fond ink-1000) avec MOCK de formulaire
(date · couverts · créneau · nom) ; état « chargement de la réservation… » mono ;
foot note italique « réservation sécurisée via CoverManager · widget tiers habillé
en prod ». Accent ≤ 2. Cartouche « Nº VII ».
FIN : MAJ statut (toutes pages = fait) + memory/sessions/SESSION-07-reserver.md +
INDEX.md + note de clôture « proto complet, prêt pour handoff Expo ».
```
