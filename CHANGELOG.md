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
