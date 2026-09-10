# AutoRoomEQ Player - Beta 0.3.2

[![Version](https://img.shields.io/badge/version-0.3.2--beta-orange)](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases/tag/v0.3.2-beta)
[![APK downloads](https://img.shields.io/github/downloads/Rexxus69/AutoRoomEQ-Player-Beta-0.3.2/v0.3.2-beta/total?label=APK%20downloads)](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases/download/v0.3.2-beta/AutoRoomEQPlayer-0.3.2-beta.apk)

AutoRoomEQ Player is an Android audio player focused on high-quality playback, DSP correction, USB DAC use, UPnP playback and browser-based control.

## What's new in Beta 0.3.2

### Library scanning and search
- Reliable first-run permission flow and full MediaStore scanning on Android 8+
- Audio rows are included even when Android does not mark them as music
- Global search and browsing across the complete indexed library
- Search by title, artist, composer, album, genre, filename and folder
- Dedicated views for Albums, Tracks, Favorites, Most played, Artists, Composers, Genres and Folders
- Album grouping and artwork in the native player library
- Playback engagement based on actual listening time and play count

### Online headphone profiles
- Search results now show matching headphone candidates, model name, source and category
- The user explicitly selects the profile before importing or generating correction
- This avoids silently applying an incorrect profile when several matches exist

### HTML Remote Control
- Full companion interface with library browsing, search, album artwork and player view
- Selecting a track, album or stream opens the player screen
- Favorites and most-played views
- Headphones section named consistently with the Android player
- RoomEQ can import a correction WAV exported by AutoRoomEQ Web
- Current Remote and UPnP Renderer addresses are visible and shareable

### Network playback and metadata
- Improved UPnP Renderer compatibility, including high-resolution sources
- Improved web-radio playback and stream metadata reporting
- Direct USB output remains preferred when the stream and DAC are supported

### Languages
Visible player and remote interface text is indexed for translation in English, Italian, German and French.

## Main features
- UPnP renderer mode
- HTML remote control on the local network
- Local music playback with FLAC, WAV, MP3 and AAC
- Bypass and corrected playback modes
- USB DAC support with bit-perfect path detection where available
- Headphone correction profiles and editing
- RoomEQ FIR correction and WAV import from AutoRoomEQ Web
- Web radio and streaming search
- Music-library scan, metadata and album artwork

## Validation
- Clean-install test on Motorola moto g84 5G, Android 15: 693 MediaStore rows, 692 tracks and 127 albums; no AndroidRuntime errors
- Beta APK is minified and obfuscated with R8, with resource shrinking enabled
- APK signature verified
- SHA-256: 35900A5744C8A4BA4CBAE2D573DC37BDE21959BC3C89848B231C415F4951AD47
- Samsung Tab A7 scanning remains under investigation and is especially welcome for beta feedback

## Download
[Download AutoRoomEQ Player 0.3.2 Beta APK](https://github.com/Rexxus69/AutoRoomEQ-Player-Beta-0.3.0/releases/download/v0.3.2-beta/AutoRoomEQPlayer-0.3.2-beta.apk)

The APK is intended for beta testing on real Android devices with different DACs, headphones, music libraries, UPnP controllers, streams and radio stations. The Remote works on the same local network as the player; the app displays current URLs because local IP addresses can change. If Android reports a signature conflict with a previous beta, uninstall the previous build before installing this APK.
