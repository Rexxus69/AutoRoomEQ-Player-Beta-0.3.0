# AutoRoomEQ Player - Beta 0.3.3

[![Version](https://img.shields.io/badge/version-0.3.3--beta-orange)](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases/tag/v0.3.3-beta)
[![APK downloads](https://img.shields.io/github/downloads/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/v0.3.3-beta/total?label=APK%20downloads)](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases/download/v0.3.3-beta/AutoRoomEQPlayer-0.3.3-beta.apk)

AutoRoomEQ Player is an Android audio player focused on high-quality playback, DSP correction, USB DAC use, UPnP playback and browser-based control.

## Beta testers: 3 steps

> **Taking part in this beta includes anonymous usage statistics.** The beta is a testing programme: the app sends anonymous numbers once a week (see [Privacy](#privacy)) so the features can be tuned on real devices. The app asks you to confirm on first launch and you can withdraw at any time from Home, which also deletes what was sent. If you don't want to share any statistics, please wait for the stable release.

1. **Before downloading**, open the [Beta feedback form](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/issues/new?template=beta-feedback.yml) and fill in **Section 1: device model and Android version**.
2. [Download the 0.3.3 beta APK](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases/download/v0.3.3-beta/AutoRoomEQPlayer-0.3.3-beta.apk) and install it.
3. Use the app, then complete the same form: what worked, **the problems you found** (a list of typical problems is provided) and **your suggestions**.

## What's new in Beta 0.3.3

### Player
- **Quality check on any track**, library included: real format, sample rate and bit depth read from the file, spectral check for fake lossless and upsampled files, plus the **full playback chain** (processing, input vs output rate and bit depth, resampling, output device, bit-perfect or not)
- **Playlists**: create, reorder, rename; add tracks with the + button from the library or the player; **M3U/M3U8 import and export**
- **Automatic playlists**: recently added, most played this month, favourites, not played for a while, never played (tracks can be removed from each list)
- **Identify track**: hands off to Shazam or Google, then searches the recognized title across the sources
- Spoken content (voice messages, interviews, audiobooks) filtered out of catalog results; optional "Verified music only" filter
- "Parent folder" bar always visible in the folder view (back gesture goes up too)
- **Automatic updates**: the app finds new releases here, downloads them, checks the SHA-256 and opens the Android installer
- Added an easter egg 🥚

### Room correction
- Engine aligned with **AutoRoomEQ Web 2.1.4**: same impulse-response window, smoothing, psychoacoustic presets (Natural / Balanced / Precise, Custom = Expert), modal error loop, group-delay and time-alignment correction, multi-position averaging and -1 dB headroom
- Microphone calibration file applied; default settings = web "Balanced" (saved correction settings are reset once)

### Headphone correction
- Real loudness matching for Bypass/Corrected A/B (K-weighted level estimate, louder side turned down)
- Earbuds recognized as their own category

### Streaming search and sources
- Parallel multi-source search with relevance ranking; unrequested live/remix/cover versions ranked lower
- Personal server support (Subsonic API: Navidrome, Airsonic, Gonic…), original files without transcoding
- Sources window to enable, disable and reorder sources

### Downloads
- Download manager with queue, retries, resume and cancel
- Quality check: real format/sample rate/bit depth and detection of fake lossless or upsampled files

### Web Remote and safety
- Pairing code required by the Remote (link shown in the app)
- Safe RoomEQ FIR import (gain check and normalization)
- Automatic fallback port for the Remote/UPnP server

### Other
- Lossless / Compressed filter for streaming results
- USB direct stability fixes (track changes, clock and sample-rate changes); UMC204HD may still fall back, see known limitations in the release notes
- Automatic app language with manual override
- German and French texts repaired and completed
- Faster library on large collections; fixed large on-demand streams

## Main features
- UPnP renderer mode
- HTML remote control on the local network
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
- 114 unit tests passed; APK minified and obfuscated with R8, resource shrinking enabled
- SHA-256: 14F165863214FDC645B3B8A036A205ED792974E686332F206985D51108DC0753
- Installed and started on Motorola moto g84 5G (Android 15); wider device testing: please help with the feedback form

## Download
[Download AutoRoomEQ Player 0.3.3 Beta APK](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases/download/v0.3.3-beta/AutoRoomEQPlayer-0.3.3-beta.apk)

The Remote works on the same local network as the player. The app displays current URLs because local IP addresses can change. If Android reports a signature conflict with a previous beta, uninstall the previous build before installing this APK.
