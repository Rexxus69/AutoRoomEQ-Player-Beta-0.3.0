# AutoRoomEQ Player - Beta 0.3.4

[![Version](https://img.shields.io/badge/version-0.3.4--beta-orange)](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases/tag/v0.3.4-beta)
[![Downloads 0.3.4](https://img.shields.io/github/downloads/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/v0.3.4-beta/total?label=0.3.4%20downloads)](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases/download/v0.3.4-beta/AutoRoomEQPlayer-0.3.4-beta.apk)
[![Total downloads](https://img.shields.io/github/downloads/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/total?label=total%20downloads)](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases)

AutoRoomEQ Player is an Android audio player focused on high-quality playback, DSP correction, USB DAC use, UPnP playback and browser-based control.

## Beta testers: 3 steps

> **Taking part in this beta includes anonymous usage statistics.** The beta is a testing programme: the app sends anonymous numbers once a week (see [Privacy](#privacy)) so the features can be tuned on real devices. The app asks you to confirm on first launch and you can withdraw at any time from Home, which also deletes what was sent. If you don't want to share any statistics, please wait for the stable release.

1. **Before downloading**, open the [Beta feedback form](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/issues/new?template=beta-feedback.yml) and fill in **Section 1: device model and Android version**.
2. [Download the 0.3.4 beta APK](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases/download/v0.3.4-beta/AutoRoomEQPlayer-0.3.4-beta.apk) and install it.
3. Use the app, then complete the same form: what worked, **the problems you found** (a list of typical problems is provided) and **your suggestions**.

## What's new in Beta 0.3.4

### AutoRoomEQ Desktop (Windows)
- **Pair the phone with the PC**: scan with the built-in QR reader the QR code shown by [AutoRoomEQ Desktop](https://github.com/Rexxus69/AutoRoomEQ-Desktop-Beta/releases/latest) or type the 6-digit code
- **Remote for the PC player**, on the home Wi-Fi and away on mobile data
- **Two-way exchange with the PC**: RoomEQ presets, playlists, favourites and microphone calibration
- No PC app yet? *Send the link to your PC* shares the download link by e-mail, chat or Nearby Share

### Library
- **Library on microSD fixed**: on some phones (e.g. Realme, Huawei) the library was empty or incomplete
- The saved library is shown at once and **refreshed automatically in the background** at every start
- Much faster first scan: composer and genre are read afterwards, in the background
- Music not indexed by Android (storage or microSD) is found and indexed; DSF/DFF, APE, WavPack, MKA and TAK files are listed too
- If music access was denied, the *Allow music access* button asks again or opens the app settings

### Quality check
- **Direct playback check for DAPs**: what Android reports for unmixed PCM at 44.1 / 96 / 192 kHz on the output in use; on Android 14+ also whether the bit-perfect mixer is offered for the connected USB DAC
- Clearer playback chain: *Android output (no USB DAC)* with the phone speaker or wired headphones; technical detail no longer cut off

### Other
- New app icon
- The whole interface follows the language chosen in the app
- RoomEQ texts updated for the 2.1 engine, scenario names translated
- Synced lyrics: the offset buttons now sit right above the lyric line

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
- SHA-256: 438A339856F8A27CAD3DDBBC0D7518538C5768704098E77D7362825218BD32A2
- Wider device testing: please help with the [feedback form](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/issues/new?template=beta-feedback.yml)

## Download
[Download AutoRoomEQ Player 0.3.4 Beta APK](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases/download/v0.3.4-beta/AutoRoomEQPlayer-0.3.4-beta.apk)

The Remote works on the same local network as the player. The app displays current URLs because local IP addresses can change. If Android reports a signature conflict with a previous beta, uninstall the previous build before installing this APK.
