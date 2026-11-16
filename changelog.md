## v4.1 (43)

### Changelog
**Nov 16, 2026**
- Fixed random system crashes on some devices (e.g. MediaStore/WebView `Failed to parse debian.mime.types`). The rebuilt system jar is now verified before install: if the on-device rebuild alters any non-code resource, the module aborts safely instead of installing a jar that crashes at boot.
- Updated the on-device APKEditor engine to 1.4.9 (more reliable jar rebuilds).

**Earlier**
- Added support for modifying **framework.jar** or **services.jar** directly.
- Place your JAR file inside **`/sdcard/mods_center/`** and flash the module.
- The modified JAR will be saved back in the same folder.
- **Android 15+** → use `framework.jar`
- **Android 14 and below** → use `services.jar`

