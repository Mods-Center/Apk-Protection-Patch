## v4.2 (47)

Remove APK protection — v4.2 (versionCode 46).

- Fixed install failing with `OutOfMemoryError` while decompiling services.jar / framework.jar on some ROMs: APKEditor now loads one dex at a time, and retries with a bigger heap if it still runs out of memory.

Previous v4.2 notes:


- Complete APKEditor 1.4.9 engine (fixes "Decompile failed / inStream parameter is null" at install).
- Install-time integrity gate: aborts safely if the rebuilt jar's non-code resources change, instead of installing a jar that crashes at boot.

## v4.2 (46)

Remove APK protection — v4.2 (versionCode 44).

- Complete APKEditor 1.4.9 engine (fixes "Decompile failed / inStream parameter is null" at install).
- Install-time integrity gate: aborts safely if the rebuilt jar's non-code resources change, instead of installing a jar that crashes at boot.

## v4.2 (45)

### Changelog
**Nov 16, 2026**
- Added a safety check: this module and the DSV (Disable APK signature verification) module cannot be installed at the same time (they modify the same system files). Flashing the second one now shows an error.

**Nov 16, 2026**
- Fixed "Decompile failed / inStream parameter is null" on install - the bundled APKEditor 1.4.9 engine was missing its resource files; it is now complete.
- Fixed random system crashes on some devices (e.g. MediaStore/WebView `Failed to parse debian.mime.types`). The rebuilt system jar is now verified before install: if the on-device rebuild alters any non-code resource, the module aborts safely instead of installing a jar that crashes at boot.
- Updated the on-device APKEditor engine to 1.4.9 (more reliable jar rebuilds).

**Earlier**
- Added support for modifying **framework.jar** or **services.jar** directly.
- Place your JAR file inside **`/sdcard/mods_center/`** and flash the module.
- The modified JAR will be saved back in the same folder.
- **Android 15+** → use `framework.jar`
- **Android 14 and below** → use `services.jar`

