# AutoRoomEQ Player - Beta 0.3.1

[![Version](https://img.shields.io/badge/version-0.3.1--beta-orange)](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0)

[![APK downloads](https://img.shields.io/github/downloads/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/v0.3.1-beta/total?label=APK%20downloads)](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases/download/v0.3.1-beta/AutoRoomEQPlayer-0.3.1-beta.apk)

AutoRoomEQ Player is an Android audio player focused on high-quality playback, DSP correction, USB DAC use, UPnP playback and browser-based control.

## What's new in Beta 0.3.1

### Music library: the app now matches the remote

The Android Player library now uses the same global search and browsing model as the HTML remote. Searches are performed across the complete indexed library instead of being limited to the last folder opened.

- Search by title, artist, composer, album, genre, filename and folder
- Dedicated views for Albums, Tracks, Favorites, Most played, Artists, Composers, Genres and Folders
- Album grouping and artwork in the native player library
- Playback engagement is based on actual listening time and play count

### HTML Remote Control

The browser remote has been extended into a full companion interface for the player.

- Library browsing, search and album artwork
- Player view opens after choosing a track, album or stream
- Favorites and most-played views
- Headphones section is named consistently with the Android player
- RoomEQ can import a correction WAV exported by AutoRoomEQ Web
- The current Remote and UPnP Renderer addresses are visible in the app and can be shared

### Network playback and metadata

- Improved UPnP Renderer compatibility, including high-resolution source handling
- Improved web-radio playback and stream metadata reporting
- Direct USB output remains the preferred path when the stream and DAC are supported

### Languages

Visible player and remote interface text is available in English, Italian, German and French.

## Main features

- UPnP renderer mode
- HTML remote control on the local network
- local music playback
- Bypass / Corrected playback modes
- USB DAC support with bit-perfect path detection where available
- headphone correction profiles and editing
- RoomEQ FIR correction and WAV import from AutoRoomEQ Web
- web radio and streaming search
- music-library scan, metadata and album artwork
- common audio formats including FLAC, WAV, MP3 and AAC

## Download

**[Download AutoRoomEQ Player 0.3.1 Beta APK](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases/download/v0.3.1-beta/AutoRoomEQPlayer-0.3.1-beta.apk)**

The APK is built with R8 minification, optimization and obfuscation. Its R8 mapping file is retained privately for crash analysis and is not part of the public distribution.

## Beta testing

This beta is intended for testing on real Android devices with different DACs, headphones, music files, UPnP controllers, streams and radio stations.

Feedback is especially useful for:

- USB DAC and bit-perfect routing compatibility
- UPnP Renderer compatibility, including 44.1, 96 and 176.4 kHz sources
- HTML remote behavior, library search and album artwork
- web-radio playback and metadata
- headphone correction and RoomEQ WAV import
- crashes and audio-format compatibility

The Remote works on the same local network as the player. The app displays the current Remote and Renderer URLs because local IP addresses can change. This is a beta build, not a final public release. If Android reports a signature conflict with a previous beta, uninstall the previous build before installing this APK.
