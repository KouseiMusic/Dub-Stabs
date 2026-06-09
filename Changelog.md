# 𝐃𝐮𝐛 𝐒𝐭𝐚𝐛𝐬 - 𝐂𝐡𝐚𝐧𝐠𝐞𝐥𝐨𝐠

## 𝟏.𝟏.𝟎 (𝟎𝟔-𝟐𝟎𝟐𝟔)

### 𝐒𝐨𝐮𝐧𝐝 & 𝐀𝐮𝐝𝐢𝐨

- Added a master limiter at the end of the audio chain. It acts as a safety ceiling that prevents any sound from clipping or distorting at the hardware level, regardless of how the knobs are set.

- Fixed the delay effect causing loud uncontrolled feedback at high Space values. Turning Space up high could previously trigger a runaway resonance that kept growing in volume. It now stays stable at all settings.

- Fixed LFO 1 being able to push the filter into an unstable state at high Depth values, causing clicks, silence or audio glitches. The modulation range is now properly bounded.

- Improved the Noise layer. It now uses pink noise instead of white noise, which sounds warmer and less harsh, closer to the natural breath and air textures of the original hardware.

- Fixed the Grit knob causing extreme pitch beating at high values. The two oscillators could drift so far apart that the result sounded broken rather than gritty. The spread is now musically controlled.

- Fixed the Resonance knob self-oscillating at high values. Turning Resonance fully up could cause the filter to whistle and ring on its own at a very loud level. It now stays under control across the full range.

- Fixed all presets playing too quietly. The output level was being divided down too aggressively. All presets now play at a proper, usable volume straight away.

- Fixed a click sound when closing the application. The audio now fades out cleanly before the engine shuts down.

### 𝐏𝐫𝐞𝐬𝐞𝐭𝐬

- Rebalanced all eight presets. Several presets were too harsh or too loud in certain frequency areas:

  - MS-20: tamed the filter resonance which was causing sharp piercing peaks.
  - Alpha Juno-1: reduced the chorus thickness and resonance for a cleaner sound.
  - Poly6: softened the chorus slightly.
  - ESQ-1: reduced the noise layer which was overpowering the tone.
  - All presets: reverb and spatial depth brought down to more natural starting levels.

- Adjusted the number of voices per preset for a better musical balance out of the box.

- Reduced the default chorus intensity on startup.

### 𝐈𝐧𝐭𝐞𝐫𝐟𝐚𝐜𝐞

- Fixed the font not loading when there was no internet connection. The font is now bundled directly inside the application and no longer requires a network connection to appear correctly.

### 𝐑𝐞𝐥𝐢𝐚𝐛𝐢𝐥𝐢𝐭𝐲

- Fixed changing presets mid-session sometimes causing notes to play on the wrong pitch or with the wrong settings. Notes now always use the currently active preset parameters.

- Fixed rapid note triggering occasionally leaving a ghost audio connection open in the background, which could slowly increase CPU usage over a long session.

- Fixed exported WAV files leaving a small amount of memory occupied after the export completed.

### 𝐒𝐞𝐜𝐮𝐫𝐢𝐭𝐲

- The application now runs in a fully sandboxed environment. A previous configuration was allowing the interface too much access to the underlying system, which represented a security risk. This has been closed.

- The application can no longer open external websites or make network requests of any kind from within the interface.

---

## 𝟏.𝟎.𝟏 (𝟎𝟓-𝟐𝟎𝟐𝟔)

- Added multi-language keyboard layout support: French (AZERTY), Russian (ЙЦУКЕН), Japanese (JIS) and Korean (두벌식). Each layout remaps both the on-screen key labels and the computer keyboard bindings to match the physical keyboard of the selected locale.

- Added WAV recording. A one-click record button captures audio output directly from the engine and exports a timestamped WAV file named with the active preset abbreviation and the current date and time.

- Added seven colour themes selectable from the Options menu: Teal, Pink, Green, Purple, White, Juno-106 (red accent with dark panel) and DX7 (mint green accent).

- Added DX7 slider-style controls when the DX7 theme is active, replacing the standard fader style with membrane data-entry sliders matching the original hardware aesthetic.

- Added Juno-106 fader-style controls when the Juno-106 theme is active, using vertical sliders with white and red stripes matching the original hardware panel layout.

- Added DAW integration support, allowing hardware MIDI controllers and DAW piano rolls to trigger chords and automate parameters in supported DAWs.

- Extended the chord voicing engine to support 1 to 5 simultaneous voices per chord, controllable from a dedicated Voices knob.

- Added a Voices knob and a Base Note knob with a live note name display below it (e.g. A2, C#3).

- Added an output level meter in the header showing the real-time volume of the audio signal.

- Added the Options dropdown for language and theme selection.

- Added the Preset dropdown with all eight hardware presets.

- Added five modulation parameters to the control surface: LFO 1 Rate, LFO 1 Depth, LFO 2 Rate, LFO 2 Depth and Chorus.

- Added a 49-key on-screen piano keyboard (C2–C6) with mouse and computer keyboard playability, active-note highlighting and per-key note labels.

---

## 𝟏.𝟎.𝟎 (𝟏𝟕-𝟎𝟒-𝟐𝟎𝟐𝟔)

- Added ProphetVS, MS-20, Polysix, Alpha Juno-1, Blofeld and ESQ-1 presets, expanding the preset roster from two to eight.

- Added a Reverb effect with a dedicated Reverb knob for adding room and space to the sound.

- Added a delay effect with a feedback loop, a built-in tone filter on the repeats and a dedicated Delay Time knob.

- Added LFO 1 targeting the filter for rhythmic movement and LFO 2 targeting the pitch for vibrato, each with independent Rate and Depth controls.

- Added a noise layer per voice with a dedicated Noise knob for adding breath, texture and air to the sound.

- Added a filter envelope with a Filter Env knob that controls how far the filter opens on each note hit before closing back down.

- Added per-preset waveform selection: each preset automatically configures the right oscillator shapes when loaded.

- Added natural oscillator drift: each voice has a subtle random tuning variation between its two oscillators, giving a warmer, more analogue character.

- Fixed a build-up issue where playing the same note repeatedly very quickly could leave invisible audio voices running in the background.

---

## 𝟎.𝟗.𝟗 (𝟏𝟓-𝟎𝟑-𝟐𝟎𝟐𝟔)

- Dual-oscillator synthesizer engine with two oscillators per voice for rich, thick chords.

- Low-pass filter with Cutoff and Resonance controls for classic sound shaping.

- Decay knob controlling how long each chord sustains before fading out.

- Grit knob for adding subtle detuning warmth or heavier distortion-like textures.

- Space knob for adding echo and depth to the sound.

- Master Volume and Pitch controls.

- Juno-106 and DX7 presets.

- Full computer keyboard playability mapped across two and a half octaves (QWERTY English layout).

- Dark-themed interface with neon accent colours.
