<p align="center"><img width="320" height="71" alt="dubstabsbanner" src="https://github.com/user-attachments/assets/b7f90e93-898a-4a42-98ae-8ec98a1e8178" /></p>

 _<p align="center">Dub Techno Stabs & Chords Synthesizer.</p>_

---

![Version](https://img.shields.io/badge/Version-1.1.0-brightgreen?style=flat-square)
![macOS Support](https://img.shields.io/badge/macOS-Sonoma%20%7C%20Sequoia%20%7C%20Tahoe-000000?style=flat-square&logo=apple&logoColor=white)
![Architecture](https://img.shields.io/badge/Architecture-Intel%20%7C%20Arm64%20%7C%20Universal-black?labelColor=606060&style=flat-square&logo=apple&logoColor=white)
![Format](https://img.shields.io/badge/Format-Standalone%20%7C%20AU%20%7C%20VST3-00CED1?style=flat-square)
![DAW](https://img.shields.io/badge/DAW-Ableton%20Live%2012%2B-000000?style=flat-square&logo=abletonlive&logoColor=white)

---

<img width="1195" height="792" alt="dubstabspreview" src="https://github.com/user-attachments/assets/44b8f37c-b921-4d63-9c8a-c231f68a91eb" />

---

## 𝐅𝐞𝐚𝐭𝐮𝐫𝐞𝐬

- **Virtual Analog Engine**: Dual-oscillator voices with per-voice low-pass filtering, amplitude envelopes and natural oscillator drift for analogue warmth. Chord voicing spans 1 to 5 simultaneous notes per trigger.
- **Eight Hardware Presets**: Juno-106, Prophet VS, DX7, MS-20, Polysix, Alpha Juno-1, Blofeld and ESQ-1. Each preset configures waveform types and a curated set of starting parameters matched to the character of the original hardware.
- **Dual LFO Modulation**: LFO 1 targets filter cutoff; LFO 2 targets oscillator pitch. Each has an independent Rate and Depth control. Both run per-voice and are started and stopped with the note, preventing accumulation artefacts.
- **Global Delay**: Feedback delay with a pre-feedback low-pass filter to darken repeats. Feedback depth and wet level are both adjustable. Maximum feedback is capped to prevent runaway self-oscillation.
- **Global Reverb**: Parallel comb filter network (four delay lines) for spatial depth. Wet level is controllable from the Reverb knob.
- **Brickwall Limiter**: A Dynamics Compressor sits at the end of the master chain before the hardware output, protecting against clipping at any parameter combination.
- **WAV Recording**: One-click recording to a WAV file named with the active preset and a date-time stamp. Captured post-limiter for a clean, ready-to-use bounce.
- **Multi-Language Keyboard Support**: Interface and keyboard bindings adapt to English (QWERTY), French (AZERTY), Russian (ЙЦУКЕН), Japanese (JIS) and Korean (두벌식) layouts. On-screen key labels update to match the selected locale.
- **Seven Colour Themes**: Teal, Pink, Green, Purple, White, Juno-106 (dark panel with red accent) and DX7 (dark panel with mint teal accent). The Juno-106 and DX7 themes also switch the control style to hardware-matched fader and slider designs respectively.
- **Zero Dependencies at Runtime**: No internet connection required. Fully self-contained once installed.

---

## 𝐒𝐲𝐬𝐭𝐞𝐦 𝐑𝐞𝐪𝐮𝐢𝐫𝐞𝐦𝐞𝐧𝐭𝐬

- **macOS**: 14.0 (Sonoma), 15.0 (Sequoia) or 16.0 (Tahoe)
- **Architecture**: Intel (x64), Apple Silicon (Arm64) or Universal (U2B)
- **DAW (plugin mode)**: Ableton Live 12 or 11, Logic Pro, Reason with the [BlackHole](https://github.com/ExistentialAudio/BlackHole) virtual audio driver for DAW routing in standalone mode.
> Audio Unit (AU) & VST3 plugins formats are currently under development.

---

## 𝐈𝐧𝐬𝐭𝐚𝐥𝐥𝐚𝐭𝐢𝐨𝐧

### 𝐒𝐭𝐚𝐧𝐝𝐚𝐥𝐨𝐧𝐞

1. Download the latest [`Dub Stabs`](https://github.com/KouseiMusic/Dub-Stabs/releases/tag/Dub-Stabs-1.1.0).
2. Extract & Drag `Dub Stabs` to your `Applications` folder.
3. If macOS shows a Gatekeeper warning on first launch, right-click the application and choose `Open`, then confirm.

### 𝐀𝐮𝐝𝐢𝐨 𝐔𝐧𝐢𝐭 (𝐀𝐔)

> 𝐔𝐧𝐝𝐞𝐫 𝐃𝐞𝐯𝐞𝐥𝐨𝐩𝐦𝐞𝐧𝐭

### 𝐕𝐒𝐓𝟑

> 𝐔𝐧𝐝𝐞𝐫 𝐃𝐞𝐯𝐞𝐥𝐨𝐩𝐦𝐞𝐧𝐭

---

## 𝐏𝐫𝐞𝐬𝐞𝐭𝐬

Each preset configures the oscillator waveform pair, filter starting point, resonance, noise level, decay, modulation depth and spatial effects to match the character of the hardware it is modelled after. Parameters can be adjusted freely after loading a preset.

| Preset | Oscillators | Character |
| :--- | :--- | :--- |
| **Juno-106** | Sawtooth + Square | Warm DCO-based stabs with lush chorus. The reference dub techno sound. |
| **Prophet VS** | Sawtooth + Triangle | Digital vector synthesis edge. Sharp attack, evolving mid texture. |
| **DX7** | Sine + Sine | Precision FM tones. Clean, metallic, crystalline. Low noise floor. |
| **MS-20** | Square + Sawtooth | Aggressive semi-modular character. High resonance, raw filter sweeps. |
| **Polysix** | Sawtooth + Sawtooth | Detuned oscillator stacks. Deep, warm vintage pads and chords. |
| **Alpha Juno-1** | Sawtooth + Square | Multi-waveform Roland DCO. Plucky stabs, resonant basses, flexible envelopes. |
| **Blofeld** | Triangle + Sawtooth | Wavetable-influenced textures. Granular movement, complex harmonic content. |
| **ESQ-1** | Square + Sawtooth | Hybrid digital/analog. Gritty 8-bit oscillators through a warm filter. |

---

## 𝐂𝐨𝐧𝐭𝐫𝐨𝐥𝐬

### 𝐒𝐲𝐧𝐭𝐡 𝐏𝐚𝐫𝐚𝐦𝐞𝐭𝐞𝐫𝐬

| Parameter | Range | Description |
| :--- | :--- | :--- |
| **Pitch** | -24 to +24 st | Master semitone transpose applied to all oscillators. |
| **Cutoff** | 20 Hz – 10 kHz | Low-pass filter cutoff frequency. |
| **Reso** | 0 – 100% | Filter resonance (Q). Higher values accentuate the cutoff frequency. Self-oscillation is prevented by an internal Q ceiling. |
| **Grit** | 0 – 100 | Oscillator frequency spread between the two oscillators. Low values add warmth; high values produce beating and distortion-like textures. |
| **Decay** | 10 – 5000 ms | Length of both the amplitude and filter envelopes. Controls how long a triggered chord sustains. |
| **Env** | 0 – 100% | Filter envelope depth. Controls how far above the Cutoff setting the filter opens at the moment of each trigger before decaying back. |
| **Noise** | 0 – 100 | Level of a pink noise layer blended into each voice. Adds breath and air, or textural roughness at higher values. |
| **Space** | 0 – 1 | Delay wet level and feedback depth together. Increasing Space adds echo repeats and widening. |
| **Reverb** | 0 – 1 | Wet level of the parallel comb reverb. |
| **Delay Time** | 0.01 – 2 s | Time between delay repeats. Set to rhythmic subdivisions of your tempo for musical results. |
| **Chorus** | 0 – 1 | Chorus depth, affecting the width and movement of the stereo image. |
| **Voices** | 1 – 5 | Number of notes in each triggered chord. The intervals are fixed (minor seventh, dominant ninth shape) and transpose with the Base Note and Pitch settings. |

### 𝐌𝐨𝐝𝐮𝐥𝐚𝐭𝐢𝐨𝐧 (𝐋𝐅𝐎𝐬)

| Parameter | Range | Description |
| :--- | :--- | :--- |
| **LFO 1 Rate** | 0.1 – 20 Hz | Speed of LFO 1. Below ~1 Hz produces slow filter sweeps; above 10 Hz enters audio-rate FM territory. |
| **LFO 1 Depth** | 0 – 1 | Amount of filter cutoff modulation from LFO 1. At full depth the filter sweeps across a wide range of the frequency spectrum on each cycle. |
| **LFO 2 Rate** | 0.1 – 20 Hz | Speed of LFO 2. |
| **LFO 2 Depth** | 0 – 1 | Amount of pitch modulation from LFO 2. At low depths this produces vibrato; at higher depths, wide pitch sweeps. |

### 𝐁𝐚𝐬𝐞 𝐍𝐨𝐭𝐞 & 𝐕𝐨𝐢𝐜𝐢𝐧𝐠

The **Base Note** knob (C through B, displayed as a note name below the knob) sets the root of the chord relative to each key pressed. The chord shape is always built upward from the played note using a fixed interval set. Combining Base Note with the Pitch transpose lets you voice chords in any key without remapping the keyboard.

### 𝐌𝐚𝐬𝐭𝐞𝐫 𝐕𝐨𝐥𝐮𝐦𝐞 & 𝐋𝐞𝐯𝐞𝐥 𝐌𝐞𝐭𝐞𝐫

The **Vol** knob in the header sets the master output level. The adjacent bar meter shows real-time peak amplitude drawn from the output analyser. The master chain includes a brickwall limiter that engages before the hardware output regardless of the Vol setting.

---

## 𝐐𝐖𝐄𝐑𝐓𝐘 (𝐄𝐧𝐠𝐥𝐢𝐬𝐡) 𝐊𝐞𝐲𝐛𝐢𝐧𝐝𝐢𝐧𝐠𝐬

Keyboard bindings adapt automatically when a language is selected from the Options menu. The tables below show the default English (QWERTY) layout.

**White keys**

| Key | Note | Key | Note | Key | Note | Key | Note |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| **Q** | C2 | **W** | D2 | **E** | E2 | **R** | F2 |
| **T** | G2 | **Y** | A2 | **U** | B2 | **I** | C3 |
| **O** | D3 | **P** | E3 | **A** | F3 | **S** | G3 |
| **D** | A3 | **F** | B3 | **G** | C4 | **H** | D4 |
| **J** | E4 | **K** | F4 | **L** | G4 | **Z** | A4 |
| **X** | B4 | **C** | C5 | **V** | D5 | **B** | E5 |
| **N** | F5 | **M** | G5 | **,** | A5 | **.** | B5 |
| **/** | C6 | | | | | | |

**Black keys**

| Key | Note | Key | Note | Key | Note | Key | Note |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| **1** | C#2 | **2** | D#2 | **3** | F#2 | **4** | G#2 |
| **5** | A#2 | **6** | C#3 | **7** | D#3 | **8** | F#3 |
| **9** | G#3 | **0** | A#3 | **-** | C#4 | **=** | D#4 |
| **[** | F#4 | **]** | G#4 | **;** | A#4 | **'** | C#5 |
| **\\** | D#5 | **⇧** | F#5 | G#5 | **⌥** | A#5 |

French (AZERTY), Russian (ЙЦУКЕН), Japanese (JIS) and Korean (두벌식) layouts are available from **Options > Language**. Selecting a language remaps both the on-screen key labels and the computer keyboard bindings to match the physical layout of that locale.

---

## 𝐑𝐞𝐜𝐨𝐫𝐝𝐢𝐧𝐠

Press the `Rec` button in the header to begin capturing audio. Press it again to stop. A `.wav` file is exported automatically and named using the active preset abbreviation and the current date and time (e.g. `dubstabs_juno106_260609143022.wav`). Recording captures the full processed signal including delay, reverb and the master limiter.

---

## 𝐃𝐀𝐖 𝐔𝐬𝐚𝐠𝐞

**Standalone + BlackHole**: Install the [`BlackHole`](https://github.com/ExistentialAudio/BlackHole) virtual audio driver, set `Dub Stabs` output to `BlackHole` in macOS `Audio MIDI Setup`, and route `BlackHole` as an input track in your DAW. This allows you to record the output in real time or resample it.

**MIDI input**: Connect a MIDI controller before launching. `Dub Stabs` responds to note-on and note-off messages on any channel. Each MIDI note triggers a full chord built on that note using the current Voices and Base Note settings.

> **Audio Unit (AU) & VST3**: Plugins formats are under development. When available they will support full parameter automation and direct DAW audio routing without BlackHole.

---

_This software is free. If you liked the synthesizer, don't forget to give it a ⭐️ on GitHub._

---

<p align="center"><code>𝒦𝑜𝓊𝓈𝑒𝒾</code></p>
<p align="center"><code>2026</code></p>
