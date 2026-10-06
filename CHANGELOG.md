# Changelog

## 0.3.3-beta - 2026-09-25

### Room correction (aligned with AutoRoomEQ Web 2.1.4)
- The RoomEQ engine now follows the web app step by step: impulse-response window (20 ms fade-in, flat, half-Hann tail) starting 2 ms before the peak, single 700 ms analysis window, 1/6-octave power smoothing on 2400 log points.
- Psychoacoustic presets with the web values: intensity blend (Natural 60 %, Balanced 75 %, Precise 85 %), boost/cut limits, three-band aggressiveness and LF/HF smoothing. Custom works like the web "Expert" mode.
- Full error loop: modal/non-modal transition, frequency-dependent boost and cut caps, up to 6 notches on room modes, coherence and spatial weighting.
- Defaults as the web "Balanced" preset: 50-16000 Hz, Flat target, 32768 taps at 48 kHz. Saved correction settings are reset once to these values.
- Group-delay correction from a loudspeaker high-pass model (one all-pass shared by L/R below 500 Hz, no longer doubled); skipped in minimum phase.
- Multi-position: positions are power-averaged with spatial weighting and the FIR is designed once.
- Gain staging like the web stereo export: common scale with -1 dB headroom, L/R balance from the measured levels, no extra pre-amp.
- Microphone calibration file applied to the measurement; time-alignment (ITC) applied in full with a 0.2 ms dead band.
- Sweep 5 s at -6 dBFS with 20 ms fades; anti-alias filtering when the FIR is resampled to a lower rate; clean switch from Bypass to Corrected.

### Headphone correction
- Loudness match now works in the main playback engine: the perceived level change of the correction is estimated with ITU-R BS.1770 K-weighting over a pink-noise spectrum, and the louder side (usually Bypass) is attenuated. Previously the switch only mirrored the manual pre-gain.
- Earbuds detected as a separate category from the AutoEQ path.

### Sources and search
- New source-independent pipeline: TrackIdentity, TrackMatcher (title, artist, duration, album, ISRC, version markers, typo tolerance) and ProviderManager (parallel search, per-provider timeout, fallback by priority).
- Internet Archive, Wikimedia Commons and Audius adapted as providers; catalogs are no longer queried during live-radio searches.
- Personal server provider using the Subsonic API with `format=raw` streams and token authentication (password not stored).
- Provider enable/disable and order are saved.
- "Identify track" hands the microphone off to Shazam or Google (whichever is installed), then searches the recognized title across the sources. No paid or unofficial recognition API is used.
- Spoken content (voice messages, interviews, audiobooks, lectures) filtered out of catalog results; optional "Verified music only" filter.

### Downloads and quality
- Shared download manager: queue, retries with backoff for network/5xx errors, HTTP Range resume, cancel, MediaStore import with title/artist/album.
- Quality check: container and format read from file bytes; spectral edge detection for lossy-sourced "lossless" files and upsampled hi-res; extension/content mismatch warning.
- Extension-less on-demand streams (Audius) are cached before playback; the HTTP stream buffer no longer overwrites unread data.

### Remote, UPnP and safety
- Pairing token required for `/remote/*` API calls; UPnP control endpoints unchanged.
- Fallback to a free port when 49152 is busy; read timeout for idle clients; artwork cache capped at 24 MB.
- RoomEQ FIR import: FFT peak-gain analysis, rejection above +24 dB, normalization to 0 dB peak.

### USB direct
- Discarded URBs are reaped regardless of their error status and kept alive until the kernel returns them; previously they could be freed while still owned by usbfs, corrupting the heap after a track change (SIGBUS in unrelated code).
- Alternate setting only via USBDEVFS_SETINTERFACE, with retries through alt 0; the raw control-transfer fallback left usbfs on the old setting (ENOENT on iso submit, seen on UMC204HD).

### Localization and UI
- Streaming results filter (All / Lossless / Compressed); video renditions, thumbnails and MIDI excluded from catalog results.
- Headphones button opens the active headphone profile.
- Automatic app language from the system language list with manual override.
- German and French resources repaired (double-encoded UTF-8) and 30 untranslated strings translated; engine error messages localized.
- Library views memoize filtering/sorting; listening statistics saved every 30 s.

### Player
- Quality check available for any track from the player (library included), with the playback chain: processing, input vs output format, resampling, bit depth, output device and bit-perfect status. The output device is read from the USB bus, so it stays correct while USB direct owns the DAC.
- Low-rate files upsampled by integer factors; MP3 files with leading tags or damaged headers recovered where possible, with a clear message for unreadable files.
- Album-art frame: rounded bottom corners.

### Playlists
- User playlists: create, rename, reorder, delete; add tracks with the + button in the library or from the player.
- M3U/M3U8 import and export (matched to the library by path, folder and file name, or artist and title).
- Automatic playlists: recently added, most played this month, favourites, not played for a while, never played; single tracks can be removed from each list and restored.

### USB direct (continued)
- Clock set before arming the streaming interface on UAC2, with a USB reset when the DAC stops answering after a clock change; in-session sample-rate change; connected DACs kept awake to avoid autosuspend.
- Known: the Behringer UMC204HD can still fall back or start silently after a rate change.

### Library
- "Parent folder" bar always visible above the folder list, with the destination folder name; the back gesture also goes up one level.

### Updates
- Automatic update check against the GitHub releases (at start-up and every 12 hours): download inside the app, SHA-256 check against the release notes, installation through the standard Android installer. "Check for updates" link in Home.

### Other
- Anonymous beta statistics as part of the testing programme (asked on first launch, can be changed or withdrawn from Home).
- Added an easter egg 🥚

### Validation
- 114 unit tests passed (matcher, provider manager, download queue, quality check, FIR safety, language, loudness, playlists and M3U, low-rate/MP3 recovery, spoken-content filter, DSP, RoomEQ engine, update parsing).
- Debug and beta builds compiled; beta APK R8-minified and obfuscated. SHA-256 14F165863214FDC645B3B8A036A205ED792974E686332F206985D51108DC0753.
- Installed and started on Motorola moto g84 5G (Android 15); wider device testing via the feedback form.

## 0.3.2-beta - 2026-09-09

### Library scanning

- Request audio-library permission when Player is first opened and start scanning after permission is granted.
- Avoid querying Android 10+ MediaStore columns on Android 8/9.
- Inspect audio entries even when Android has not marked them as music, while excluding system ringtones, alarms and notifications and validating usable audio files.
- Add scan counts and failure logging for device-specific diagnosis.

### Online headphone profiles

- Show matching AutoEQ headphone models, measurement source and category before import.
- Import or generate EQ only after the user selects a result.
- Improve model-name ranking and use the selected result path for cached-profile lookup.
- Reject searches containing no usable search terms.

### Localization

- Add English, Italian, French and German resource strings for the new search controls, results, categories, targets and AutoEQ errors.
- Verify matching string keys across the four Android resource sets. This is not a full visual translation audit of every existing screen.

### Validation and open checks

- Clean-install test on Motorola moto g84 5G, Android 15: 693 MediaStore audio entries inspected, 692 valid tracks indexed, 127 albums displayed. No AndroidRuntime errors observed during this test.
- Matching-profile search confirmed working on the test phone.
- Debug build passed. Unit tests were blocked by a local Java/Gradle loopback issue.
- Obfuscated 0.3.2-beta packaging and release verification remain pending.
- Samsung Tab A7 scanning report remains under investigation. Android version and internal-storage versus microSD details are needed; the Motorola result does not confirm a fix on this tablet.

## 0.3.1-beta

- Global library search by title, artist, composer, album, genre, filename and folder.
- Android library views aligned with HTML Remote: Albums, Tracks, Favorites, Most played, Artists, Composers, Genres and Folders.
- Remote library artwork, playback navigation, favorites, most-played views and RoomEQ WAV import.
- Visible, shareable Renderer and Remote addresses.
- UPnP, web-radio and stream-metadata improvements.
