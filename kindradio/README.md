# KIND Radio v0.1 (experimental)
Android local-audio Google Cast sender for a Vizio TV connected to the phone hotspot.

## Build
GitHub Actions > Build KIND Radio APK > Run workflow. Download the KIND-Radio-debug-APK artifact and extract the APK.

## Use
Connect Vizio to Android hotspot. Install debug APK. Pick local MP3, select Vizio from Cast route button, tap Cast selected music.

## Known limitations
- Experimental, uncompiled in this environment; GitHub Actions build is the first compilation test.
- Android may not expose the hotspot interface IP in the expected order.
- HTTP server v0.1 does not implement Content-Length or Range requests. Some Cast receivers reject such streams.
- Local server runs only while the activity is alive; do not background or lock the app for initial test.
- Cast receiver may need internet to initialize.
- HTTP is deliberately unencrypted on the private hotspot; do not use on untrusted networks.
- Debug build only, not Play Store release.
