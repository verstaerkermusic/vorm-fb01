# vørm fb01 0.29.3 beta

- **True stereo input.** Select Stereo in the input menu, then Main Stereo or Out1 Stereo. The left and right channels have independent filters, saturation and Envelope Followers. LFO, ADSR and AR triggers are linked. Stereo external sidechains follow the matching channels. Mono sidechains feed both.
- **Faster processing.** The internal oversampling filters use the symmetry of their existing coefficients to reduce work. The current mono modes and automation assignments remain available. Existing sessions keep their saved routing.
- **Eco mode.** Available under Settings > Processing Quality. At 44.1 and 48 kHz it uses shorter sample-rate filters and can slightly change the highest frequencies. At other host rates it behaves like Low.
- Updated English and German guides.

Select Mono for a single processing path. Stereo runs both channels through the model and requires more CPU.

- **macOS 12+ (universal):** AU, VST3, CLAP.
- **Windows 10/11 (x64):** VST3, CLAP.
- **Linux (x86_64 beta):** VST3, LV2, CLAP. Ubuntu 22.04 baseline with X11 editor.

See the README inside your download for installation instructions. The public downloads contain the plug-in binaries and documentation.

# vørm fb01 0.29.1 beta

- Revised Input knob and nonlinear glow across Bright, Dark and Flat, with the knob and lighting rendered together and LED lighting adapted to the new panels.
- A bounded background cache loads the Input animation at full resolution with premultiplied interpolation, instead of keeping the entire decoded animation atlas in memory.
- Universal macOS bundles share artwork between Apple Silicon and Intel, reducing duplicated resources. Artwork stays inside each plug-in bundle.
- macOS installer now offers User or System-wide installation, followed by All / VST3 / AU / CLAP. Single-format installation backs up and removes other formats only in the selected location; installation failures restore replacements and removed formats.
- Updated English/German Quick Start and PDF guides. No developer tools required on the destination Mac.
- No DSP changes from 0.29.0. Existing projects and presets remain compatible.

macOS 12+: universal Apple Silicon/Intel AU, VST3 and CLAP. Windows 10/11 x64: VST3 and CLAP. Linux x86_64 beta: VST3, LV2 and CLAP, Ubuntu 22.04 baseline with X11 editor.

Use the README in your platform package for installation. Automated checks do not replace hands-on DAW, controller and sidechain testing.

# vørm fb01 0.29.0 beta

- **LFO Tempo Sync:** click the wave icon below/between Speed and Depth. Green means enabled. Speed selects 4 bars, 2 bars, 1 bar, 1/2, 1/4, 1/8, 1/16, 1/32, 1/64 and 1/128 over the lower 70% of the knob range.
- Above that range, Speed moves continuously into audio rate, starting at the last synced frequency without a backward jump (64 Hz at 120 BPM in 4/4), up to 3823.6 Hz.
- Sync follows host tempo and time signature, with musical phase alignment during playback. ADSR > Speed can still modulate the selected base rate; strict phase locking is suspended during that intentional modulation. Without host tempo, the starting fallback is 120 BPM.
- **LFO Bleed:** a new Hardware Character control mixes the existing raw LFO into the wet input stage independently of Depth. A fixed 40 Hz, 24 dB/octave high-pass suppresses subsonic content. All character presets start with Bleed at 0; manual bleed edits select Custom.
- **Wet Pre-EQ (introduced in the macOS 0.28.0 test build):** Low, Mid and High gain controls (-24 to +12 dB), adjustable low/high shelf frequencies and an independent EQ switch. Processes only the wet program signal before input drive, saturation and internal envelope detection; external sidechains and added character signals are unaffected.
- EQ controls support MIDI Learn and are stored in projects, sound presets, Init and A/B. Changes are smoothed; no extra latency.
- New controls default off/neutral in existing projects. Dry and full bypass remain unchanged. Existing parameter IDs/order are retained; new parameters are appended.
- Updated English and German guides.

macOS 12+: universal Apple Silicon/Intel AU, VST3 and CLAP. Windows 10/11 x64: VST3 and CLAP. Linux x86_64 beta: VST3, LV2 and CLAP, Ubuntu 22.04 baseline with X11 editor.

Use the README in your platform package for installation. Automated checks do not replace hands-on DAW, controller and sidechain testing.

# 0.27.6 beta

- Added Flat alongside revised Bright/Dark graphics with corrected knob edges.
- Added Gain/Gamma appearance controls (0.80-1.30, neutral 1.00) with reset, project recall and defaults for new instances. Sound presets/A-B retain appearance settings.
- Corrected LED glow exports and intermediate-frame blending to preserve soft falloff and the bright core.
- Fixed editor shrinking after Gain/Gamma changes on Retina/HiDPI displays; regression checks cover 1x to 3x.
- All three themes support full/compact view. Updated English/German guides.
- No audio processing changes.

macOS: universal AU/VST3/CLAP. Windows x64: VST3/CLAP. Linux x86_64: VST3/LV2/CLAP, Ubuntu 22.04 baseline and X11 editor.

# 0.27.3 beta

- Optional Compact interface in Settings: approximately 15% less window height at unchanged control size.
- View persists in projects, can be remembered for new instances, and is retained across sound preset and A/B changes. Full view remains the factory default.
- Revised Bright/Dark PAR/SER and Dry/Wet knob graphics.
- Updated English/German guides.
- No audio processing changes.

Available for macOS (AU/VST3/CLAP), Windows x64 (VST3/CLAP) and Linux x86_64 (VST3/LV2/CLAP).

# VØRM FB01 0.27.2 beta

Analog filtering, powerful saturation and hands-on modulation for macOS, Windows and Linux.

## Included formats

- macOS 12+: universal Apple Silicon / Intel, AU / VST3 / CLAP.
- Windows 10/11 x64: VST3 / CLAP.
- Linux x86_64 r2: VST3 / LV2 / CLAP, built on Ubuntu 22.04 with an X11 editor. First Linux beta; real DAW testing is still needed.

## Linux package revision r2

- Adds Linux CLAP with audio, state, MIDI and X11 editor checks at 44.1/48/96 kHz.
- Sound processing and the approved V23 interface are unchanged. macOS and Windows packages are unchanged.
- Install the CLAP file in ~/.clap/ or a host-configured CLAP folder.

## Changes and features

- Revised Bright and Dark interfaces, complete switch geometry and soft LED falloff.
- Input, Wet Level and Output remain visible across every expanded controls page.
- Processing quality is now in Settings: Low 96 kHz / Mid 176.4 kHz / High 384 kHz.
- Equal Power is the factory Dry/Wet default; stored projects, presets and custom Init settings retain their saved curves.
- Recent MIDI smoothing, endpoint and project-save fixes are included.
- Cmd-drag on macOS or Ctrl-drag on Windows/Linux links matching F1/F2 knobs while preserving their offset. Shift gives finer movement; frequency and envelope-depth links require FREE mode.
- Internal/external FM and AM, independent sidechain routing, ADSR/AR audio and MIDI triggers, Envelope Follower, LFO and Harmonics sync.
- Preset browser, MIDI Learn/controller profiles, A/B comparison, optional character controls, Gain Match and output controls.
- Existing plug-in IDs, parameter IDs, presets and user-data locations are retained. Gain Match routing and the core sound model are unchanged in this update.

## Installation

Use the README inside the package for your operating system. Quit your DAW first and keep one copy of each plug-in ID in its scan folders. When updating, back up/remove older plug-in copies from those folders to avoid duplicate IDs.

macOS: extract the complete ZIP and run Install-VORM-fb01.command. This beta is ad-hoc signed and not notarized. If blocked, attempt to open it, then use System Settings > Privacy & Security > Open Anyway. No developer tools are required.

Windows: copy the entire VST3 bundle and/or CLAP file to the corresponding plug-in folder. Rescan the DAW.

Linux: extract the tar.gz archive and copy the complete VST3 bundle to ~/.vst3/ and/or the complete LV2 bundle to ~/.lv2/. Copy the CLAP file to ~/.clap/. The graphical editor uses X11; Wayland sessions may use XWayland. Other distributions need testing.

English/German control guides are included; their Quick Start installation section describes macOS. Use the package README for Windows/Linux installation.

## Validation and feedback

Automated DSP, MIDI, state and GUI checks passed on all three platforms. Linux also passed actual VST3 factory loading and LV2 metadata/instantiation/MIDI-event/audio checks at 44.1, 48 and 96 kHz. The added CLAP format also passed factory/parameter/state/MIDI/audio and X11 GUI checks at those rates. These checks do not replace hands-on DAW, controller and sidechain validation.

Project and feedback: https://github.com/verstaerkermusic/vorm-fb01
Support: https://buymeacoffee.com/verstaerker
