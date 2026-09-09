# Changelog

## 0.3.2-beta - Unreleased

Implemented locally; the new obfuscated APK is not yet published. The latest downloadable release remains 0.3.1-beta.

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
