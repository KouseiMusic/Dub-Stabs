Dub Stabs — Changelog
─────────────────────────────────────────────────────────────────────────────

Version 1.1.0 (06-2026)
─────────────────────────────────────────────────────────────────────────────

Audio Engine

  - Added a DynamicsCompressorNode (Brickwall Limiter) in the master output
    chain. All audio passes through it before reaching the hardware output,
    preventing clipping and protecting hearing at any parameter combination.

  - Fixed a feedback runaway instability in the global delay. The previous
    feedback formula (0.65 + space * 0.20) could reach 0.85 at high Space
    values, causing self-oscillation and unbounded volume growth. The formula
    is now (0.45 + space * 0.20) and is hard-capped at 0.75.

  - Fixed an LFO depth overflow. LFO 1 was modulating the filter Cutoff
    frequency with a multiplier of 3000, which at depth = 1 could push the
    filter to NaN or negative frequency values, causing audio glitches. The
    multiplier is now 1200 with clamping on both LFOs.

  - Replaced raw white noise with a pink noise approximation (Paul Kellet
    method). Pink noise rolls off at -3 dB/octave and is spectrally closer to
    natural acoustic sources, reducing harshness at high Noise values.

  - Fixed oscillator grit detuning. The secondary oscillator frequency ratio
    had no upper bound, which at Grit = 100 produced extreme beating artifacts.
    The maximum effective spread is now capped at +40 cents.

  - Fixed filter resonance scaling. Q was previously (resonance / 5), reaching
    Q = 20 at maximum resonance, causing self-oscillation of the filter. Q is
    now clamped to 12 with a non-linear curve that preserves the musically
    useful range.

  - Fixed a voice gain stacking issue. With 5 voices all routed to the master
    bus simultaneously, the summed gain could approach 0.75 before limiting.
    Voice peak gain is now divided by the active voice count.

  - Added engine destroy() method. The AudioContext is now properly ramped to
    silence and closed on application quit, eliminating an AudioContext leak
    and preventing an audible click on exit.

  - Noise buffer creation is now wrapped in a try/catch. In some Safari/WebKit
    states, sampleRate can read as 0 on context construction; this previously
    caused a silent crash with no audio output.

Presets

  - Rebalanced all eight presets for safe output levels. Specific changes:
      · MS-20:       resonance reduced from 65 to 52 (was causing harsh peaks)
      · AlphaJuno-1: chorus reduced from 0.70 to 0.55; resonance from 55 to 48
      · Poly6:       chorus reduced from 0.60 to 0.50
      · ESQ-1:       noise reduced from 20 to 14
      · All presets: reverb maximum reduced from 0.35 to 0.28;
                     space maximum reduced from 0.25 to 0.20
  - Default voice count adjusted per preset for musical balance.
  - Default chorus on startup reduced from 0.70 to 0.45.
  - Default master volume reduced from 0.50 to 0.42 as a safer initial level.

Stability

  - Fixed a stale closure bug in the keyboard event handler. The handler was
    capturing an outdated reference to params, so changing presets mid-session
    could cause notes to trigger on the wrong base note or with incorrect
    parameters. A paramsRef is now used to always read the current state.

  - Fixed initEngine recreating a new function reference on every render, which
    caused the keyboard and audio-init effects to re-register on every state
    change. initEngine is now stable via useCallback.

  - Fixed a recording AudioContext leak. The temporary decode context used for
    WAV export was not being closed after use. It is now explicitly closed after
    decodeAudioData returns.

  - Fixed a recording destination leak. The MediaStream destination node was
    staying connected to the analyser after recording stopped. It is now
    disconnected in the onstop handler.

  - Fixed the anchor element created for WAV download not being removed from
    the DOM after click.

Security

  - Removed nodeIntegration: true and contextIsolation: false from the
    BrowserWindow configuration. These settings exposed the Node.js runtime to
    renderer-process JavaScript, which is a critical Electron security
    vulnerability. The renderer now runs fully sandboxed.

  - Added sandbox: true and webSecurity: true to webPreferences.

  - Added a Content-Security-Policy header blocking all external network
    connections from the renderer (connect-src: none).

  - Added a will-navigate handler that prevents the renderer from navigating
    to any non-file URL.

  - Blocked webview element creation and window.open calls to external origins.

─────────────────────────────────────────────────────────────────────────────

Version 1.0.2  (2026)
─────────────────────────────────────────────────────────────────────────────

  - Added multi-language keyboard layout support: French (AZERTY), Russian
    (ЙЦУКЕН), Japanese (JIS) and Korean (두벌식). Each layout remaps
    both the on-screen key labels and the computer keyboard bindings to match
    the physical keyboard of the selected locale.

  - Added WAV recording. A one-click record button captures audio output
    directly from the engine and exports a timestamped WAV file named with the
    active preset abbreviation and the current date and time.

  - Added seven colour themes selectable from the Options menu: Teal, Pink,
    Green, Purple, White, Juno-106 (red accent with dark panel), and DX7
    (mint green accent).

  - Added DX7 slider-style controls when the DX7 theme is active, replacing
    the standard fader style with membrane data-entry sliders matching the
    original hardware aesthetic.

  - Added Juno-106 fader-style controls when the Juno-106 theme is active,
    using vertical sliders with white and red stripes matching the original
    hardware panel layout.

  - Added iPlug2 / AU / VST3 parameter bridge. The renderer now communicates
    with the plugin host via the iPlug2 messaging protocol, enabling parameter
    automation and MIDI input in supported DAWs.

  - Added MIDI note-on and note-off handling via the iPlug2 message bridge,
    allowing hardware MIDI controllers and DAW piano rolls to trigger chords.

  - Extended the chord voicing engine to support 1 to 5 simultaneous voices
    per chord, controllable from a dedicated Voices knob.

  - Added a Voices knob and a Base Note knob with a live note name display
    below it (e.g. A2, C#3).

  - Added a LevelMeter component in the header displaying real-time output
    amplitude drawn from the AnalyserNode.

  - Added the Options dropdown for language and theme selection.

  - Added the Preset dropdown with all eight hardware presets.

  - Added five LFO parameters to the control surface: LFO 1 Rate, LFO 1 Depth,
    LFO 2 Rate, LFO 2 Depth and Chorus.

  - Added a 49-key on-screen piano keyboard (C2–C6) with mouse and computer
    keyboard playability, active-note highlighting and per-key note labels.


─────────────────────────────────────────────────────────────────────────────

Version 1.0.1  (2026)
─────────────────────────────────────────────────────────────────────────────

  - Added ProphetVS, MS-20, Polysix, Alpha Juno-1, Blofeld and ESQ-1 presets,
    expanding the preset roster from two to eight.

  - Added global reverb with a Schroeder-style parallel comb filter network
    (four delay lines) and a dedicated Reverb knob.

  - Added global delay with a feedback loop, a pre-feedback low-pass filter
    and a dedicated Delay Time knob.

  - Added LFO 1 targeting filter cutoff and LFO 2 targeting oscillator pitch,
    each with independent Rate and Depth controls.

  - Added a noise oscillator layer per voice with a dedicated Noise knob.

  - Added a filter envelope with a Filter Env knob controlling the initial
    cutoff peak.

  - Added an Electron main process (main.cjs) for standalone macOS packaging
    via electron-builder with DMG, PKG and ZIP targets.

  - Added per-preset waveform selection: oscillator types are now set
    automatically when a preset is loaded.

  - Added natural oscillator drift: each voice applies a small random detune
    to osc1 and osc2 in opposite directions for subtle analogue warmth.

  - Fixed a voice accumulation issue where rapidly triggering the same MIDI
    note without a note-off would leave previous voice nodes connected to the
    output graph indefinitely.