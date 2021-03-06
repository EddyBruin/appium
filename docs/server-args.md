Appium server arguments
==========

Usage: `node server.js [flags]`

### Server flags
All flags are optional, but some are required in conjunction with certain others.

|Flag|Default|Description|Example|
|----|-------|-----------|-------|
|`--app`|null|IOS: abs path to simulator-compiled .app file or the bundle_id of the desired target on device; Android: abs path to .apk file|`--app /abs/path/to/my.app`|
|`--ipa`|null|(IOS-only) abs path to compiled .ipa file|`--ipa /abs/path/to/my.ipa`|
|`-q`, `--quiet`|false|Don't use verbose logging output||
|`-U`, `--udid`|null|Unique device identifier of the connected physical device|`--udid 1adsf-sdfas-asdf-123sdf` or `auto` to auto-detect|
|`-a`, `--address`|0.0.0.0|IP Address to listen on|`--address 0.0.0.0`|
|`-p`, `--port`|4723|port to listen on|`--port 4723`|
|`-dp`, `--device-port`|4724|(Android-only) port to connect to device on|`--device-port 4724`|
|`-k`, `--keep-artifacts`|false|(IOS-only) Keep Instruments trace directories||
|`--no-session-override`|false|Disables session override||
|`--full-reset`|false|(Android-only) Reset app state by uninstalling app instead of using clean.apk||
|`--no-reset`|false|Don't reset app state between sessions (IOS: don't delete app plist files; Android: don't uninstall app before new session)||
|`-l`, `--pre-launch`|false|Pre-launch the application before allowing the first session (Requires --app and, for Android, --app-pkg and --app-activity)||
|`-g`, `--log`|null|Log output to this file instead of stdout|`--log /path/to/appium.log`|
|`-G`, `--webhook`|null|Also send log output to this HTTP listener|`--webhook localhost:9876`|
|`--native-instruments-lib`|false|(IOS-only) IOS has a weird built-in unavoidable delay. We patch this in appium. If you do not want it patched, pass in this flag.||
|`--app-pkg`|null|(Android-only) Java package of the Android app you want to run (e.g., com.example.android.myApp)|`--app-pkg com.example.android.myApp`|
|`--app-activity`|null|(Android-only) Activity name for the Android activity you want to launch from your package (e.g., MainActivity)|`--app-activity MainActivity`|
|`--app-wait-activity`|false|(Android-only) Activity name for the Android activity you want to wait for (e.g., SplashActivity)|`--app-wait-activity SplashActivity`|
|`--avd`|null|name of the avd to launch|`--avd @default`|
|`--device-ready-timeout`|5|(Android-only) Timeout in seconds while waiting for device to become ready|`--device-ready-timeout 5`|
|`--safari`|false|(IOS-Only) Use the safari app||
|`--force-iphone`|false|(IOS-only) Use the iPhone Simulator no matter what the app wants||
|`--force-ipad`|false|(IOS-only) Use the iPad Simulator no matter what the app wants||
|`--orientation`|null|(IOS-only) use LANDSCAPE or PORTRAIT to initialize all requests to this orientation|`--orientation LANDSCAPE`|
|`--tracetemplate`|null|(IOS-only) path to the .tracetemplate file instruments will use|`--tracetemplate "/Users/me/Automation.tracetemplate"`|
|`--nodeconfig`|null|Configuration JSON file to register appium with selenium grid|`--nodeconfig /abs/path/to/nodeconfig.json`|
|`-ra`, `--robot-address`|0.0.0.0|IP Address of robot|`--robot-address 0.0.0.0`|
|`-rp`, `--robot-port`|-1|port for robot|`--robot-port 4242`|
|`--selendroid-port`|8080|Local port used for communication with Selendroid|`--selendroid-port 8080`|
|`--use-keystore`|false|(Android-only) When set the keystore will be used to sign apks.||
|`--keystore-path`|/Users/rockbot/.android/debug.keystore|(Android-only) Path to keystore||
|`--keystore-password`|android|(Android-only) Password to keystore||
|`--key-alias`|androiddebugkey|(Android-only) Key alias||
|`--key-password`|android|(Android-only) Key password||
