<p align="center"><img width="320" height="71" alt="dubstabsbanner" src="https://github.com/user-attachments/assets/b7f90e93-898a-4a42-98ae-8ec98a1e8178" /></p>

 **_<p align="center">Synthétiseur pour Dub Techno Stabs et Chords.</p>_**

---

![Version](https://img.shields.io/badge/Version-1.1.0-brightgreen?style=flat-square)
![macOS Support](https://img.shields.io/badge/macOS-Sonoma%20%7C%20Sequoia%20%7C%20Tahoe-000000?style=flat-square&logo=apple&logoColor=white)
![Architecture](https://img.shields.io/badge/Architecture-Universal-black?labelColor=606060&style=flat-square&logo=apple&logoColor=white)
![Format](https://img.shields.io/badge/Format-Standalone%20%7C%20AU%20%7C%20VST3-00CED1?style=flat-square)
![DAW](https://img.shields.io/badge/DAW-Ableton%20Live%2012%2B-000000?style=flat-square&logo=abletonlive&logoColor=white)

---

<img width="1195" height="792" alt="dubstabspreview" src="https://github.com/user-attachments/assets/44b8f37c-b921-4d63-9c8a-c231f68a91eb" />

---

## 𝐅𝐞𝐚𝐭𝐮𝐫𝐞𝐬

- **Moteur Virtual Analog** : Voix à double oscillateur avec filtrage passe-bas par voix, enveloppes d'amplitude et dérive naturelle des oscillateurs pour une chaleur analogique. Le voicing des accords s'étend de 1 à 5 notes simultanées par déclenchement.
- **Huit Presets Matériels** : Juno-106, Prophet VS, DX7, MS-20, Polysix, Alpha Juno-1, Blofeld et ESQ-1. Chaque preset configure les types de formes d'onde et un ensemble de paramètres initiaux sélectionnés pour correspondre au caractère du matériel original.
- **Double Modulation LFO** : Le LFO 1 cible le Cutoff du filtre; le LFO 2 cible le Pitch de l'oscillateur. Chacun possède un contrôle Rate et Depth indépendant. Les deux fonctionnent par voix et démarrent/s'arrêtent avec la note pour éviter les artefacts d'accumulation.
- **Delay Global** : Feedback delay avec un filtre passe-bas pré-feedback pour assombrir les répétitions. La profondeur du feedback et le niveau wet sont tous deux ajustables. Le feedback maximum est limité pour empêcher toute auto-oscillation incontrôlée.
- **Reverb Globale** : Réseau de filtres en peigne parallèles (quatre lignes de delay) pour la profondeur spatiale. Le niveau wet est contrôlable via le bouton Reverb.
- **Limiteur Brickwall** : Un compresseur de dynamique est placé à la fin de la chaîne master avant la sortie matérielle, protégeant contre l'écrêtage quel que soit le réglage des paramètres.
- **Enregistrement WAV** : Enregistrement en un clic vers un fichier WAV nommé selon le preset actif et horodaté. Capture effectuée post-limiteur pour un bounce propre et prêt à l'emploi.
- **Support Clavier Multilingue** : L'interface et les raccourcis clavier s'adaptent aux dispositions anglaise (QWERTY), française (AZERTY), russe (ЙЦУКЕН), japonaise (JIS) et coréenne (두벌식). Les étiquettes des touches à l'écran se mettent à jour selon la langue choisie.
- **Sept Thèmes de Couleur** : Teal, Pink, Green, Purple, White, Juno-106 (panneau sombre avec accents rouges) et DX7 (panneau sombre avec accents menthe). Les thèmes Juno-106 et DX7 modifient également le style des contrôles pour correspondre aux faders et curseurs du matériel original.
- **Zéro Dépendance au Runtime** : Aucune connexion internet requise. Entièrement autonome une fois installé.

---

## 𝐒𝐲𝐬𝐭𝐞𝐦 𝐑𝐞𝐪𝐮𝐢𝐫𝐞𝐦𝐞𝐧𝐭𝐬

- **macOS** : 14.0 (Sonoma), 15.0 (Sequoia) ou 16.0 (Tahoe)
- **Architecture** : Intel (x64), Apple Silicon (Arm64) ou Universal (U2B)
- **DAW (Mode Plugin)** : Ableton Live 12 ou 11, Logic Pro, Reason avec le pilote audio virtuel [BlackHole](https://github.com/ExistentialAudio/BlackHole) pour le routage DAW en mode standalone.
> Les formats de plugins Audio Unit (AU) & VST3 sont actuellement en cours de développement.

---

## 𝐈𝐧𝐬𝐭𝐚𝐥𝐥𝐚𝐭𝐢𝐨𝐧

### 𝐒𝐭𝐚𝐧𝐝𝐚𝐥𝐨𝐧𝐞

1. Téléchargez le dernier [`Dub Stabs`](https://github.com/KouseiMusic/Dub-Stabs/releases/download/Dub_Stabs_1.1.0/Dub.Stabs.macOS.Universal.zip).
2. Extrayez et glissez `Dub Stabs` vers votre dossier `Applications`.
3. Si macOS affiche un avertissement Gatekeeper au premier lancement, faites un clic droit sur l'application, choisissez `Ouvrir`, puis confirmez.

### 𝐀𝐮𝐝𝐢𝐨 𝐔𝐧𝐢𝐭 (𝐀𝐔)

> 𝐄𝐧 𝐜𝐨𝐮𝐫𝐬 𝐝𝐞 𝐝é𝐯𝐞𝐥𝐨𝐩𝐩𝐞𝐦𝐞𝐧𝐭

### 𝐕𝐒𝐓𝟑

> 𝐄𝐧 𝐜𝐨𝐮𝐫𝐬 𝐝𝐞 𝐝é𝐯𝐞𝐥𝐨𝐩𝐩𝐞𝐦𝐞𝐧𝐭

## 𝐃𝐀𝐖 𝐔𝐬𝐚𝐠𝐞

1. Installez [`BlackHole`](https://github.com/ExistentialAudio/BlackHole), un pilote audio virtuel gratuit pour macOS.
2. Ouvrez `Configuration audio et MIDI` (situé dans `/Applications/Utilitaires/`).
3. Créez un `Appareil à sorties multiples` incluant votre `Interface Audio` et `BlackHole`.
4. Définissez cet `Appareil à sorties multiples` comme sortie système dans `Réglages Système` > `Son`.
5. Dans votre `DAW`, créez une piste d'entrée audio et réglez sa source d'entrée sur `BlackHole`.
6. Vous pouvez maintenant enregistrer ou monitorer la sortie de `Dub Stabs` en temps réel.

---

## 𝐏𝐫𝐞𝐬𝐞𝐭𝐬

Chaque preset configure la paire de formes d'onde des oscillateurs, le point de départ du filtre, la résonance, le niveau de bruit, le decay, la profondeur de modulation et les effets spatiaux pour correspondre au caractère du matériel modélisé. Les paramètres peuvent être ajustés librement après le chargement d'un preset.

| Preset | Oscillateurs | Caractère |
| :--- | :--- | :--- |
| **Juno-106** | Sawtooth + Square | Stabs chauds basés sur DCO avec un chorus riche. Le son de référence dub techno. |
| **Prophet VS** | Sawtooth + Triangle | Tranchant de synthèse vectorielle numérique. Attaque nette, texture de médiums évolutive. |
| **DX7** | Sine + Sine | Tons FM de précision. Propre, métallique et cristallin. Faible niveau de bruit. |
| **MS-20** | Square + Sawtooth | Caractère semi-modulaire agressif. Résonance élevée, balayages de filtre bruts. |
| **Polysix** | Sawtooth + Sawtooth | Stacks d'oscillateurs désaccordés. Pads et accords vintage profonds et chauds. |
| **Alpha Juno-1** | Sawtooth + Square | Roland DCO multi-formes d'onde. Stabs percutants, basses résonantes et enveloppes flexibles. |
| **Blofeld** | Triangle + Sawtooth | Textures influencées par la synthèse à table d'ondes. Mouvement granulaire, contenu harmonique complexe. |
| **ESQ-1** | Square + Sawtooth | Hybride numérique/analogique. Oscillateurs 8-bit granuleux à travers un filtre chaud. |

---

## 𝐂𝐨𝐧𝐭𝐫𝐨𝐥𝐬

### 𝐒𝐲𝐧𝐭𝐡 𝐏𝐚𝐫𝐚𝐦𝐞𝐭𝐞𝐫𝐬

| Paramètre | Plage | Description |
| :--- | :--- | :--- |
| **Pitch** | -24 à +24 st | Transposition master en demi-tons appliquée à tous les oscillateurs. |
| **Cutoff** | 20 Hz - 10 kHz | Fréquence de coupure du filtre passe-bas. |
| **Reso** | 0 - 100% | Résonance du filtre (Q). Les valeurs élevées accentuent la fréquence de coupure. L'auto-oscillation est empêchée par un plafond interne. |
| **Grit** | 0 - 100 | Écart de fréquence entre les deux oscillateurs. Les valeurs basses ajoutent de la chaleur; les valeurs hautes produisent des battements et des textures de type distorsion. |
| **Decay** | 10 - 5000 ms | Longueur des enveloppes d'amplitude et de filtre. Contrôle la durée de maintien d'un accord déclenché. |
| **Env** | 0 - 100% | Profondeur de l'enveloppe de filtre. Contrôle l'ouverture du filtre au-dessus du réglage Cutoff au moment du déclenchement avant de redescendre. |
| **Noise** | 0 - 100 | Niveau d'une couche de bruit rose mélangée à chaque voix. Ajoute du souffle ou une rugosité texturale aux valeurs élevées. |
| **Space** | 0 - 1 | Contrôle simultané du niveau wet et du feedback du delay. Augmenter Space ajoute des répétitions d'écho et de l'élargissement. |
| **Reverb** | 0 - 1 | Niveau wet de la réverbération à peigne parallèle. |
| **Delay Time** | 0.01 - 2 s | Temps entre les répétitions du delay. Réglez sur des subdivisions rythmiques de votre tempo pour des résultats musicaux. |
| **Chorus** | 0 - 1 | Profondeur du chorus, affectant la largeur et le mouvement de l'image stéréo. |
| **Voices** | 1 - 5 | Nombre de notes dans chaque accord déclenché. Les intervalles sont fixes (forme septième mineure, neuvième de dominante) et se transposent avec les réglages Base Note et Pitch. |

### 𝐌𝐨𝐝𝐮𝐥𝐚𝐭𝐢𝐨𝐧 (𝐋𝐅𝐎𝐬)

| Paramètre | Plage | Description |
| :--- | :--- | :--- |
| **LFO 1 Rate** | 0.1 - 20 Hz | Vitesse du LFO 1. Sous ~1 Hz, produit des balayages de filtre lents; au-dessus de 10 Hz, entre dans le territoire de la FM à taux audio. |
| **LFO 1 Depth** | 0 - 1 | Quantité de modulation du Cutoff du filtre par le LFO 1. À pleine profondeur, le filtre balaie une large partie du spectre à chaque cycle. |
| **LFO 2 Rate** | 0.1 - 20 Hz | Vitesse du LFO 2. |
| **LFO 2 Depth** | 0 - 1 | Quantité de modulation du Pitch par le LFO 2. À faible profondeur, cela produit un vibrato; à des profondeurs plus élevées, des balayages de pitch larges. |

### 𝐁𝐚𝐬𝐞 𝐍𝐨𝐭𝐞 & 𝐕𝐨𝐢𝐜𝐢𝐧𝐠

Le bouton **Base Note** (de C à B, affiché sous forme de note sous le bouton) définit la fondamentale de l'accord par rapport à chaque touche pressée. La forme de l'accord est toujours construite vers le haut à partir de la note jouée en utilisant un ensemble d'intervalles fixes. Combiner Base Note avec la transposition Pitch permet de jouer des accords dans n'importe quelle tonalité sans remapper le clavier.

### 𝐌𝐚𝐬𝐭𝐞𝐫 𝐕𝐨𝐥𝐮𝐦𝐞 & 𝐋𝐞𝐯𝐞𝐥 𝐌𝐞𝐭𝐞𝐫

Le bouton **Vol** dans l'en-tête règle le niveau de sortie master. Le vumètre adjacent affiche l'amplitude de crête en temps réel via l'analyseur de sortie. La chaîne master inclut un limiteur brickwall qui s'active avant la sortie matérielle quel que soit le réglage Vol.

---

## 𝐐𝐖𝐄𝐑𝐓𝐘 (𝐄𝐧𝐠𝐥𝐢𝐬𝐡) 𝐊𝐞𝐲𝐛𝐢𝐧𝐝𝐢𝐧𝐠𝐬

Les raccourcis clavier s'adaptent automatiquement lorsqu'une langue est sélectionnée dans le menu Options. Les tableaux ci-dessous montrent la disposition par défaut English (QWERTY).

**Touches blanches**

| Touche | Note | Touche | Note | Touche | Note | Touche | Note |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| **Q** | C2 | **W** | D2 | **E** | E2 | **R** | F2 |
| **T** | G2 | **Y** | A2 | **U** | B2 | **I** | C3 |
| **O** | D3 | **P** | E3 | **A** | F3 | **S** | G3 |
| **D** | A3 | **F** | B3 | **G** | C4 | **H** | D4 |
| **J** | E4 | **K** | F4 | **L** | G4 | **Z** | A4 |
| **X** | B4 | **C** | C5 | **V** | D5 | **B** | E5 |
| **N** | F5 | **M** | G5 | **,** | A5 | **.** | B5 |
| **/** | C6 | | | | | | |

**Touches noires**

| Touche | Note | Touche | Note | Touche | Note | Touche | Note |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| **1** | C#2 | **2** | D#2 | **3** | F#2 | **4** | G#2 |
| **5** | A#2 | **6** | C#3 | **7** | D#3 | **8** | F#3 |
| **9** | G#3 | **0** | A#3 | **-** | C#4 | **=** | D#4 |
| **[** | F#4 | **]** | G#4 | **;** | A#4 | **'** | C#5 |
| **\\** | D#5 | **⇧** | F#5 | G#5 | **⌥** | A#5 |

Les dispositions French (AZERTY), Russian (ЙЦУКЕН), Japanese (JIS) et Korean (두벌식) sont disponibles via **Options > Language**. Sélectionner une langue remplace à la fois les étiquettes de touches à l'écran et les raccourcis du clavier informatique pour correspondre à la disposition physique locale.

---

## 𝐑𝐞𝐜𝐨𝐫𝐝𝐢𝐧𝐠

Appuyez sur le bouton `Rec` dans l'en-tête pour commencer la capture audio. Appuyez à nouveau pour arrêter. Un fichier `.wav` est exporté automatiquement et nommé selon l'abréviation du preset actif et la date/heure actuelle (ex: `dubstabs_juno106_260609143022.wav`). L'enregistrement capture le signal complet traité, incluant le delay, la reverb et le limiteur master.

---

_Ce logiciel est gratuit. Si vous avez aimé le synthétiseur, n'oubliez pas de lui donner une ⭐️ sur GitHub._

---

<p align="center"><code>𝒦𝑜𝓊𝓈𝑒𝒾</code></p>
<p align="center"><code>2026</code></p>