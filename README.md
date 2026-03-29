# Explorateur du Système Solaire

Simulation 3D interactive du système solaire et exploration de l'univers, conçue comme une expérience éducative et immersive entièrement dans un seul fichier HTML.

---

## Technologies utilisées

- **Three.js** (v0.160) — rendu 3D de la scène spatiale
- **Web Audio API** — musique d'ambiance et effets sonores générés en temps réel
- **HTML/CSS/JS vanilla** — sans framework supplémentaire
- Polices Google Fonts : *Fredoka One* (titres) + *Nunito* (texte)

---

## Démarrage

Ouvrir `index.html` dans un navigateur moderne. Aucun serveur ni installation requis.

---

## Flux de l'application

1. **Écran de chargement** — barre de progression animée pendant l'initialisation de la scène 3D
2. **Écran d'accueil** — saisie du prénom de l'astronaute, fond étoilé animé avec orbes de nébuleuse
3. **Animation de décollage** — compte à rebours 3 → 2 → 1 → Ignition → 🚀 (annulable)
4. **Exploration libre** — scène 3D interactive

---

## Vues disponibles

L'application propose trois vues accessibles via les boutons en haut à droite :

| Vue | Bouton | Description |
|-----|--------|-------------|
| **Système Solaire** | ☀️ Système Solaire | Vue par défaut — les planètes de notre système solaire |
| **Corps célestes** | 🌌 Corps célestes | Objets extrasystémiques (étoiles, galaxies, phénomènes) |
| **Notre Galaxie** | 🌌 Notre Galaxie | Mode galactique — orbite du Soleil autour de Sgr A* |

---

## Contrôles de navigation

| Touche / Action | Fonction |
|-----------------|----------|
| `↑ ↓ ← →` | Se déplacer (tangage / lacet) |
| Clic gauche + droit simultanément | Avancer |
| `Espace` | Monter |
| `Shift` | Descendre |
| Molette souris | Ajuster la vitesse de déplacement |
| Viser une planète | Afficher son panneau d'information |
| `O` | Basculer entre mode Aligné et mode Orbites |
| Clic droit | Libérer la souris (quitter le pointer lock) |

Un **curseur personnalisé** (cercle blanc) s'anime en or lorsqu'il survole un élément interactif.

---

## Modes de simulation

### Mode Aligné ↔ Mode Orbites

Basculable via le **toggle en haut au centre** de l'interface :

- **Aligné** — les planètes sont disposées sur une ligne droite depuis le Soleil, positions fixes
- **Orbites** — les planètes orbitent en temps réel autour du Soleil

Un **curseur de vitesse orbitale** (🌀 ×1 à ×20) permet d'accélérer la simulation.

---

## HUD (Interface en jeu)

| Élément | Position | Description |
|---------|----------|-------------|
| Toggle mode + vitesse orbite | Haut centre | Bascule Aligné/Orbites + slider de vitesse |
| Légende des contrôles | Bas centre | Rappel des touches clavier |
| Indicateur de vitesse | Bas droite | Vitesse de déplacement actuelle |
| Popup de vitesse | Bas centre | Apparaît lors d'un changement de vitesse |
| Minimap | Bas gauche | Carte circulaire du système solaire en temps réel |
| Label cible | Haut gauche | Nom de la planète visée avec point coloré |
| Réticule (crosshair) | Centre écran | Visible en mode pointer lock |
| Bouton Retour au Soleil | Droite bas | Téléporte vers le Soleil (ou la Nébuleuse en vue Corps célestes) |

---

## Panneau d'information des objets

Un clic ou un viser sur un objet ouvre un **panneau latéral droit** contenant :

- Icône emoji + nom + type
- Description pédagogique
- **4 faits clés** (grille 2×2)
- **Bannière "Planète du jour"** — si l'objet correspond au jour de la semaine en cours (animée avec un halo pulsant si c'est aujourd'hui)
- **"Le savais-tu ?"** — anecdote amusante
- Bouton **"S'approcher"** — déclenche une animation de vol vers l'objet

### Correspondance jours / corps célestes

| Jour | Corps |
|------|-------|
| Dimanche | Soleil ☀️ |
| Lundi | Lune 🌙 |
| Mardi | Mars ⚔️ |
| Mercredi | Mercure 💫 |
| Jeudi | Jupiter ⚡ |
| Vendredi | Vénus 💖 |
| Samedi | Saturne 💍 |

---

## Objets du Système Solaire

### Étoile
- **Soleil** ☀️ — Étoile jaune, 5 500 °C, ×109 la Terre, 4,6 milliards d'années

### Planètes rocheuses
- **Mercure** 🪨 — 4 880 km, 88 jours/an, 0 lune
- **Vénus** 🌤️ — 465 °C, 225 jours/an, rotation rétrograde, 0 lune
- **Terre** 🌍 — 12 742 km, 365 jours/an, 1 lune
- **Mars** 🔴 — 6 779 km, 687 jours/an, Olympus Mons (21 km), 2 lunes

### Géantes gazeuses
- **Jupiter** 🟠 — 139 820 km, 12 ans/an, Grande Tache Rouge, 95 lunes
- **Saturne** 💍 — 116 460 km, 29 ans/an, anneaux de glace, 146 lunes

### Géantes de glace
- **Uranus** 🧊 — 50 724 km, 84 ans/an, inclinée à 98°, 28 lunes
- **Neptune** 🔵 — 49 244 km, 165 ans/an, vents à 2 000 km/h, 16 lunes

### Ceinture & autres
- **Ceinture d'astéroïdes** 🪨 — entre Mars et Jupiter, +1 million d'astéroïdes, Cérès (940 km)
- **La Lune** 🌙 — satellite naturel, 384 400 km, exploration Apollo 11 (1969)
- **ISS** 🛸 — station spatiale, 400 km d'altitude, tour en 90 min, 6–7 astronautes

### Planètes naines (Ceinture de Kuiper)
- **Pluton** 🪐 — 2 377 km, 248 ans/an, 5 lunes, survolé par New Horizons (2015)
- **Éris** 🔵 — 2 326 km, 559 ans/an, 1 lune (Dysnomie)

### Missions spatiales
- **Persévérance** 🤖 — rover martien (cratère Jezero, depuis 2021), production d'O₂ (MOXIE)
- **Voyager 1** 🛸 — sonde lancée en 1977, hors du système solaire, +23 Mrd km, disque d'or
- **Télescope Hubble** 🔭 — orbite à 547 km, lancé 1990, +1 million d'images
- **Télescope James Webb** 🌐 — lancé 2021, 1,5 M km, miroir 6,5 m, infrarouge

---

## Objets Corps Célestes (vue extrasystémique)

### Phénomènes stellaires
| Objet | Type | Particularité |
|-------|------|---------------|
| Nébuleuse 🌫️ | Nuage de gaz | Berceaux des étoiles |
| Géante rouge 🔴 | Étoile évoluée | 100–1 000× le Soleil |
| Supernova 💥 | Explosion stellaire | Plus brillante qu'une galaxie entière |
| Naine blanche ⚪ | Résidu stellaire | Taille Terre, ~1 t/cm³ |
| Étoile à neutrons ⭐ | Résidu ultra-dense | ~20 km, 1 milliard de t/cm³ |
| Pulsar 💫 | Étoile à neutrons | Signal radio régulier, jusqu'à 716 tours/s |
| Trou Noir 🌑 | Singularité | Rien ne s'échappe, pas même la lumière |
| Quasar 🔭 | Noyau galactique actif | Objet le plus lumineux de l'univers |

### Objets extragalactiques
| Objet | Type |
|-------|------|
| Exoplanète 🌍 | Planète hors système solaire (5 500+ connues) |
| Galaxie 🌌 | Amas de milliards d'étoiles |
| Astéroïde 🪨 | Corps rocheux mineur |
| Comète ☄️ | Corps glacé avec queue lumineuse |

### Types de galaxies (catalogue complet)
| Type | Emoji | Exemple |
|------|-------|---------|
| Galaxie spirale | 🌀 | M51 Tourbillon |
| Galaxie spirale barrée | ✨ | NGC 1300 |
| Galaxie elliptique | 🟠 | M87 |
| Galaxie lenticulaire | 💫 | NGC 5866 |
| Galaxie irrégulière | 🌌 | Grand Nuage de Magellan |
| Galaxie naine | ⭐ | Naine du Sagittaire |
| Galaxie annulaire | 💍 | Objet de Hoag |

### Galaxies et structures proches
| Objet | Distance |
|-------|---------|
| La Voie Lactée 🌌 | Notre galaxie — 200–400 milliards d'étoiles |
| Sagittarius A* 🌑 | Trou noir central — 4 millions × le Soleil |
| Andromède (M31) 🌀 | 2,5 millions a.-l., 1 000 milliards d'étoiles |
| Galaxie du Triangle (M33) 🌀 | 2,7 millions a.-l., 40 milliards d'étoiles |
| Grand Nuage de Magellan ☁️ | 160 000 a.-l., satellite irrégulier de la VL |
| Centaurus A 🟠 | 12 M a.-l., radiogalaxie avec jets plasmatiques |
| Amas de la Vierge (M87) 🌟 | 54 M a.-l., >2 000 galaxies |
| Amas de la Règle (Abell 3627) ✨ | 210 M a.-l., zone d'évitement |
| Amas de l'Hydre (Abell 1060) 💫 | 190 M a.-l., superamas Hydre-Centaure |
| Grand Attracteur 🌐 | 150–250 M a.-l., anomalie gravitationnelle massive |

---

## Visite guidée

Le bouton **🚀 Visite guidée** lance un tour automatique avec :
- Barre de progression avec **points de navigation** cliquables (précédent/suivant/quitter)
- Animation de vol vers chaque objet avec son panneau d'information
- Disponible dans les deux vues (Système Solaire et Corps Célestes)

### Ordre de la visite (Système Solaire)
Voie Lactée → Soleil → Mercure → Vénus → Terre → Lune → ISS → Mars → Persévérance → Ceinture d'astéroïdes → Jupiter → Saturne → Uranus → Neptune

### Ordre de la visite (Corps Célestes)
Nébuleuse → Galaxie annulaire → Galaxie naine → Galaxie irrégulière → Galaxie lenticulaire → Galaxie elliptique → Galaxie spirale barrée → Galaxie spirale → James Webb → Hubble → Voyager 1 → Comète → Astéroïde → Exoplanète → Quasar → Trou Noir → Pulsar → Étoile à neutrons → Supernova → Naine blanche → Géante rouge

---

## Quiz

Le bouton **🧠 Quiz** lance un quiz à choix multiples :
- Questions tirées aléatoirement depuis une banque de 10+ questions
- 4 réponses proposées par question
- Retour visuel immédiat (bonne réponse en vert, mauvaise en rouge, + révélation de la bonne réponse)
- Explication pédagogique après chaque réponse
- Score final avec message de félicitations
- Entièrement disponible en français et en anglais

Exemples de thèmes couverts : planète la plus proche du Soleil, plus grande planète, couleur de Mars, nombre de planètes, la Lune, planète la plus froide, plus haute montagne du système solaire, nature du Soleil, etc.

---

## Mode Notre Galaxie (Galactique)

Activé via le bouton **🌌 Notre Galaxie**, ce mode affiche :

- La simulation de l'**orbite du Soleil** autour de Sagittarius A* (rayon de 300 unités)
- Un **panneau d'information** (haut gauche) avec :
  - Vitesse du Soleil dans la Galaxie : 828 000 km/h
  - Distance à Sgr A* : 26 000 années-lumière
  - Durée d'une année galactique : 225 millions d'années
  - **Barre de progression** de l'orbite galactique en temps réel
  - **Dérive vers le Grand Attracteur** avec un slider de vitesse (×1 à ×20)
- Les galaxies proches (Andromède, Centaurus A, amas) sont disposées à l'échelle dans la scène
- Des labels flottants identifient la **Voie Lactée** et le **Système Solaire** lorsqu'on zoome dehors

---

## Fonctionnalités supplémentaires

### Internationalisation
- Bouton **🇫🇷 FR / EN** (bas droite) — bascule toute l'interface entre français et anglais
- Toutes les descriptions, faits, anecdotes et questions du quiz sont traduits

### Mode daltonien
- Bouton **👁️ Daltonien** (bas droite) — applique un filtre SVG de simulation du daltonisme (deutéranopie) à toute la page

### Audio
- **Musique d'ambiance spatiale** générée via Web Audio API (oscillateurs)
- **Sons de déplacement** (whoosh) lors des téléportations vers les planètes

### Effets visuels
- **Lens flare** dynamique sur le Soleil (canvas overlay)
- **Vignette warp** lors des déplacements rapides
- **Overlay atmosphérique** lors de l'animation de décollage
- **Labels 3D** au-dessus des planètes avec ligne et point coloré
- Labels **Voie Lactée** / **Système Solaire** apparaissant selon le zoom
- **Minimap** circulaire en temps réel

### Nom du joueur
- Le prénom saisi à l'accueil s'affiche au-dessus de l'astronaute pendant l'exploration

---

## Structure du code

Tout le code est contenu dans un seul fichier `index.html` organisé en sections commentées :

- **CSS** — styles complets intégrés dans `<style>`
- **HTML** — structure de tous les overlays, panneaux et éléments HUD
- **`PLANETS_DATA`** — base de données de tous les objets célestes (nom, type, emoji, couleur, rayon, distance, vitesse orbitale, description FR/EN, faits FR/EN, anecdote FR/EN, lunes, anneaux)
- **`CELESTIAL_CATALOGUE`** — catalogue de référence des objets Corps Célestes
- **Scène Three.js** — création des meshes, lumières, étoiles, anneaux, etc.
- **Boucle de rendu** — `requestAnimationFrame`, déplacements, minimap, labels
- **Système audio** — Web Audio API, musique ambiante, sons
- **Tour guidé** — logique de navigation entre objets
- **Quiz** — banque de questions, logique de scoring
- **Mode galactique** — orbite galactique, Grand Attracteur, galaxies voisines
- **Internationalisation** — fonction `T()` de traduction