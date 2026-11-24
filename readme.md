# AutoRoomEQ Player - Beta 0.3.6

[![Version](https://img.shields.io/badge/version-0.3.6--beta-orange)](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases/tag/v0.3.6-beta)
[![Downloads 0.3.6](https://img.shields.io/github/downloads/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/v0.3.6-beta/total?label=0.3.6%20downloads)](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases/download/v0.3.6-beta/AutoRoomEQPlayer-0.3.6-beta.apk)
[![Total downloads](https://img.shields.io/github/downloads/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/total?label=total%20downloads)](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases)

AutoRoomEQ Player is an Android audio player focused on high-quality playback, DSP correction, USB DAC use, UPnP playback and browser-based control.

## Beta testers: 3 steps

> **Taking part in this beta includes anonymous usage statistics.** The beta is a testing programme: the app sends anonymous numbers once a week (see [Privacy](#privacy)) so the features can be tuned on real devices. The app asks you to confirm on first launch and you can withdraw at any time from Home, which also deletes what was sent. If you don't want to share any statistics, please wait for the stable release.

1. **Before downloading**, open the [Beta feedback form](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/issues/new?template=beta-feedback.yml) and fill in **Section 1: device model and Android version**.
2. [Download the 0.3.6 beta APK](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases/download/v0.3.6-beta/AutoRoomEQPlayer-0.3.6-beta.apk) and install it.
3. Use the app, then complete the same form: what worked, **the problems you found** (a list of typical problems is provided) and **your suggestions**.

## What's new in Beta 0.3.6

### Streamer mode
- **An old phone + a USB DAC become a hi-fi streamer**: full-screen landscape player, screen always on, AutoRoomEQ can be the phone's **Home app** so it starts by itself
- **Analogue VU meters** (blue backlit or studio cream) after 20 s without touches, following what you hear
- **Radio, Library, Network and Correction** as big-button pages inside the streamer; one volume control (DAC or Android)

### Correction for the other apps (Android 10+)
- The RoomEQ filter also corrects **other apps** (YouTube Music, Deezer, Prime Video…), with a **low-latency** mode that keeps audio and video in sync
- One-time guided setup **without a PC**; apps that forbid capture play unchanged

### Play on network devices
- **Send the track or playlist to a UPnP/DLNA renderer** (OpenHome or UPnP AV); with RoomEQ, local files arrive **already corrected**

### Android 7 and older phones
- Minimum Android **7.0**, 32-bit ARM phones too
- USB DACs on phones without direct USB transfers play through Android's USB route instead of failing
- Web radio: AAC radios no longer hang on Android 7, steadier playback on slow phones

### Web remote: the whole app from the browser
- The remote page now has **the same commands as the app**: the 8 **radio memories** (play, save, clear), **play all / shuffle** of any library view, the **queue**, your **playlists**
- **Audio settings** (ReplayGain, upsampling, crossfeed, sleep timer), **Play on UPnP device** with volume and RoomEQ correction
- Track tools (quality check, lyrics and offset, cover, download), Music ID and Flow suggestions, radio buffer and minimum bitrate, downloads, DSD DoP, library sharing, raw PCM, save DSP preset

### App colour
- **System** (Material You, Android 12+), Teal, Amber, Blue, Burgundy or Green: accent and backgrounds of player and streamer together

### Beta statistics
- The opt-in anonymous statistics now also include phone model, USB DAC, feature use, listening minutes, library formats and technical errors (never titles, files or searches); testers are asked again

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
- SHA-256: 4EAC0C37546957D5BD813A7CB923C20F2ED6221A3515D401D0A7124EA91BCFC6
- Wider device testing: please help with the [feedback form](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/issues/new?template=beta-feedback.yml)

## Download
**[Download the latest APK](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases/latest/download/AutoRoomEQPlayer-beta.apk)** (always the newest version)

[Download AutoRoomEQ Player 0.3.6 Beta APK](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases/download/v0.3.6-beta/AutoRoomEQPlayer-0.3.6-beta.apk)

The Remote works on the same local network as the player. The app displays current URLs because local IP addresses can change. If Android reports a signature conflict with a previous beta, uninstall the previous build before installing this APK.

## Trademark
© DSPxLab — AutoRoomEQ. Freeware beta for testing: all rights reserved. Redistribution and reverse engineering are not allowed. Source code is not public.
