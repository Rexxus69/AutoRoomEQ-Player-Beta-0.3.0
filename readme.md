# AutoRoomEQ Player - Beta 0.3.5

[![Version](https://img.shields.io/badge/version-0.3.5--beta-orange)](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases/tag/v0.3.5-beta)
[![Downloads 0.3.5](https://img.shields.io/github/downloads/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/v0.3.5-beta/total?label=0.3.5%20downloads)](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases/download/v0.3.5-beta/AutoRoomEQPlayer-0.3.5-beta.apk)
[![Total downloads](https://img.shields.io/github/downloads/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/total?label=total%20downloads)](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases)

AutoRoomEQ Player is an Android audio player focused on high-quality playback, DSP correction, USB DAC use, UPnP playback and browser-based control.

## Beta testers: 3 steps

> **Taking part in this beta includes anonymous usage statistics.** The beta is a testing programme: the app sends anonymous numbers once a week (see [Privacy](#privacy)) so the features can be tuned on real devices. The app asks you to confirm on first launch and you can withdraw at any time from Home, which also deletes what was sent. If you don't want to share any statistics, please wait for the stable release.

1. **Before downloading**, open the [Beta feedback form](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/issues/new?template=beta-feedback.yml) and fill in **Section 1: device model and Android version**.
2. [Download the 0.3.5 beta APK](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases/download/v0.3.5-beta/AutoRoomEQPlayer-0.3.5-beta.apk) and install it.
3. Use the app, then complete the same form: what worked, **the problems you found** (a list of typical problems is provided) and **your suggestions**.

## What's new in Beta 0.3.5

### DSD
- **DSF / DFF playback**: DSD64, DSD128 and higher
- **DSD → PCM** by default (any DAC, correction and volume available) or **DoP** to a DoP-capable USB DAC (experimental, automatic fallback to PCM)

### CUE sheets
- **One-file albums + CUE** split into tracks: external `.cue`, FLAC CUESHEET tag and block
- **Add a music folder** in the library: finds external `.cue` and DSD files that Android 13+ hides

### Output
- **DAC volume** with USB direct: hardware volume (stays bit-perfect) or software volume with TPDF dither
- **Correction per output**: remembered for each USB DAC, wired headphones, Bluetooth device and speaker, restored on switch

### Library
- **Empty or incomplete library**: list shown in seconds, deeper search of storage and microSD, **Add a music folder** reads what Android does not list, and a **library report** to paste in your issue

### Network
- **Share the library**: the phone becomes a UPnP/DLNA media server for AutoRoomEQ Desktop, foobar2000, JRiver, BubbleUPnP and network streamers (opt-in)

### Audio settings
- **ReplayGain** Off / Track / Album with preamp, never clips; tracks without tags are measured (EBU R128); **stays bit-perfect on DACs with their own volume control**
- **Upsampling** on USB direct: ×2, ×4, 96 or 192 kHz, linear or minimum phase
- **Sleep timer**: 15 / 30 / 60 min or end of track

### Widget and lock screen
- **Home screen widget** with artwork and controls; artwork on the lock screen

### Headphones
- **Crossfeed** Off / Light / Medium / Strong (bs2b model)

### Streaming
- **FLAC radios in Ogg** (e.g. Radio Paradise FLAC) now play; **steadier radio** buffering

### Artwork and metadata
- **Faster and more accurate artwork**, **PDF booklet covers**, composer and genre from the tags filled in progressively

### Player
- **Quality check with spectrum chart**, faster seek in MP3/AAC/Ogg, library remembers where you were

### Other
- The bit-perfect badge says **why** playback is not bit-perfect; tap it for the quality check
- Messages and notifications follow the app language everywhere

## Main features
- UPnP renderer mode
- HTML remote control on the local network
- Pairing with AutoRoomEQ Desktop (Windows): remote control and exchange of presets, playlists, favourites and mic calibration
- Local music playback with FLAC, WAV, MP3 and AAC
- Bypass and corrected playback modes
- USB DAC support with bit-perfect path detection where available
- Headphone correction profiles and editing
- RoomEQ FIR correction and WAV import from AutoRoomEQ Web
- Web radio, catalog streaming, personal server and downloads with quality check
- Music-library scan, metadata and album artwork
- In-player quality check with the full playback chain (input/output rate and bit depth, resampling, output device)
- Track recognition via Shazam or Google
- Playlists with M3U import/export and automatic playlists

## Privacy
- Some features learn from how you listen. Learning happens locally: listening data stays on the device, is never uploaded, and can be switched off and deleted at any time.
- Beta only: on first launch the app asks whether to send anonymous usage statistics once a week (counts and accuracy figures, app and Android version, a random install code). No titles, files, searches or IP addresses are stored. You can change your choice from the Home screen; withdrawing consent also deletes the reports already sent.

## Validation
- APK minified and obfuscated with R8, resource shrinking enabled
- SHA-256: CD6326E3709C8C870E13294C6EE8A7118AE558883D21BA1CDE81396961BCF3DB
- Wider device testing: please help with the [feedback form](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/issues/new?template=beta-feedback.yml)

## Download
**[Download the latest APK](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases/latest/download/AutoRoomEQPlayer-beta.apk)** (always the newest version)

[Download AutoRoomEQ Player 0.3.5 Beta APK](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases/download/v0.3.5-beta/AutoRoomEQPlayer-0.3.5-beta.apk)

The Remote works on the same local network as the player. The app displays current URLs because local IP addresses can change. If Android reports a signature conflict with a previous beta, uninstall the previous build before installing this APK.
