# Flexopus Device Connect
[![GitHub Release](https://img.shields.io/github/v/release/flexopus/flexopus-device-connect)](https://github.com/flexopus/flexopus-device-connect/releases)
[![GitHub Release](https://img.shields.io/github/v/release/flexopus/flexopus-device-connect?include_prereleases&filter=preview-*&label=pre-release)](https://github.com/flexopus/flexopus-device-connect/releases?q=preview-&expanded=true)


Repository containing the releases for the Flexopus Device Connect application. The application source code is not uploaded to this repository.

## Release assets
Find the files for the latest release at https://github.com/flexopus/flexopus-device-connect/releases/latest. For all versions, see https://github.com/flexopus/flexopus-device-connect/releases.

Starting with `v1.2.6`, every release ships two APK variants:

| Variant | File name | Min. SDK | Supported Android versions |
|---|---|---|---|
| Modern (default) | `flexopus-device-connect.apk` | 29 | Android 10 and newer |
| Legacy | `flexopus-device-connect-legacy.apk` | 28 | Android 9 (and newer) |

Use the **modern** APK whenever the device runs Android 10 or newer. Only use the **legacy** APK on devices that are stuck on Android 9 (API level 28), e.g. older signage displays and wall-mounted tablets. Releases before `v1.2.6` only contain the modern APK.

## Direct download url
You can access the latest APK file at:
```
https://github.com/flexopus/flexopus-device-connect/releases/latest/download/flexopus-device-connect.apk
```
To use a specific version, use the following URL: (replace `v1.2.10` with the desired version code, with leading `v`):
```
https://github.com/flexopus/flexopus-device-connect/releases/download/v1.2.10/flexopus-device-connect.apk
```
Make sure that you enable redirect following when downloading the APK with a script:
```bash
curl -OL https://github.com/flexopus/flexopus-device-connect/releases/latest/download/flexopus-device-connect.apk
```

### Legacy APK (Android 9)
The legacy build uses the same URL scheme, with `flexopus-device-connect-legacy.apk` as the file name.

Latest version:
```
https://github.com/flexopus/flexopus-device-connect/releases/latest/download/flexopus-device-connect-legacy.apk
```
Specific version (available from `v1.2.6`):
```
https://github.com/flexopus/flexopus-device-connect/releases/download/v1.2.10/flexopus-device-connect-legacy.apk
```
With a script:
```bash
curl -OL https://github.com/flexopus/flexopus-device-connect/releases/latest/download/flexopus-device-connect-legacy.apk
```

### Fully Kiosk Browser
The provided [`fully-kiosk-config.json`](fully-kiosk-config.json) installs the modern APK via `mdmApkToInstall`. For Android 9 devices, point it at the legacy APK instead:
```json
"mdmApkToInstall": "https://github.com/flexopus/flexopus-device-connect/releases/latest/download/flexopus-device-connect-legacy.apk",
```

## Preview releases
> [!WARNING]  
> Pre-releases are intended for internal testing only and must not be used by external users. Only use these versions if you have received explicit testing instructions from the Flexopus team.

Preview releases use the release tag (`preview-[hash]`) as version code, and their APKs are named after the build variant instead of `flexopus-device-connect.apk`:

| Variant | Preview file name |
|---|---|
| Modern (minSdk 29) | `app-modern-release.apk` |
| Legacy (minSdk 28) | `app-legacy-release.apk` |

Modern:
```
https://github.com/flexopus/flexopus-device-connect/releases/download/preview-4f5f6a64/app-modern-release.apk
```
Legacy:
```
https://github.com/flexopus/flexopus-device-connect/releases/download/preview-4f5f6a64/app-legacy-release.apk
```

> [!NOTE]
> Older preview builds (before the legacy variant was introduced) used `app-release.apk`. That name is no longer published.

## Verify checksum
Every APK of a stable release has its checksum uploaded next to it (`<apk name>.sha256`), you can use them to verify file contents.
```bash
$ sha256sum --check flexopus-device-connect.apk.sha256
flexopus-device-connect.apk: OK

$ sha256sum --check flexopus-device-connect-legacy.apk.sha256
flexopus-device-connect-legacy.apk: OK
```
