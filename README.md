# Flexopus Device Connect
[![GitHub Release](https://img.shields.io/github/v/release/flexopus/flexopus-device-connect)](https://github.com/flexopus/flexopus-device-connect/releases)
[![GitHub Release](https://img.shields.io/github/v/release/flexopus/flexopus-device-connect?include_prereleases&filter=preview-*&label=pre-release)](https://github.com/flexopus/flexopus-device-connect/releases?q=preview-&expanded=true)


Repository containing the releases for the Flexopus Device Connect application. The application source code is not uploaded to this repository.

## Release assets
Find the files for the latest release at https://github.com/flexopus/flexopus-device-connect/releases/latest. For all versions, see https://github.com/flexopus/flexopus-device-connect/releases.


## Direct download url
You can access the latest APK file at:
```
https://github.com/flexopus/flexopus-device-connect/releases/latest/download/flexopus-device-connect.apk
```
To use a specific version, use the following URL: (replace `v1.0.15` with the desired version code, with leading `v`):
```
https://github.com/flexopus/flexopus-device-connect/releases/download/v1.0.15/flexopus-device-connect.apk
```
Make sure that you enable redirect following when downloading the APK with a script:
```bash
curl -OL https://github.com/flexopus/flexopus-device-connect/releases/latest/download/flexopus-device-connect.apk
```

## Preview releases
> [!WARNING]  
> Pre-releases are intended for internal testing only and must not be used by external users. Only use these versions if you have received explicit testing instructions from the Flexopus team.

To use a specific preview release, use the release tag (`preview-[hash]`) as version code, and replace `flexopus-device-connect.apk` with `app-release.apk`:
```
https://github.com/flexopus/flexopus-device-connect/releases/download/preview-5769f8df/app-release.apk
```

## Verifiy checksum
All release files have their checksum uploaded, you can use them to verify file contents.
```bash
$ sha256sum --check flexopus-device-connect.apk.sha256
flexopus-device-connect.apk: OK
```
