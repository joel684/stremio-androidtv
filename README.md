# Stremio (Android TV) 1.9.10, armeabi-v7a

Stremio's Android TV app for sideloading on 32-bit ARM TV boxes running Android 11. The APK is unmodified.

## Download

Get `Stremio-TV-1.9.10-armeabi-v7a.apk` from the **Releases** section of this repository.

## About this build

- Package `com.stremio.one`, version 1.9.10 (versionCode 11049225).
- Android TV only. It requires the Leanback feature.
- Minimum Android 6.0 (API 23). Android 11 is fine.
- Native code is armeabi-v7a (32-bit ARM) only. It runs on 32-bit ARM TVs and most 64-bit ARM TVs, but not on Intel (x86) boxes.
- APK SHA-256: `5478ea5d40a86d93e150b3e9d316af13c05e1336b7a7648f40d01a83796564f9`
- Signing certificate SHA-256: `7e6a979c968f771e3fbcf2c2e8718ce61e708d87caf91fc13e2d4c19a8022c6b`

## Install

**Downloader app:** install Downloader from the TV's app store and allow it to install unknown apps. On Android 11 this is usually under Settings > Apps > Special app access > Install unknown apps (menu names vary by TV maker). Open Downloader, enter the APK's download link, and install.

**USB stick:** copy the APK to a USB stick formatted as FAT32 or exFAT, plug it into the TV, open the file manager, select the APK, and install.

## Before using it on 500 MB of RAM

- The streaming server runs as a foreground service (`ServerService`), which is heavy for 500 MB.
- Expect slow playback or crashes. Reboot the TV, close other apps, and use lower-quality streams.
- This build has not been tested on a real 500 MB TV.

## Permissions

The app asks for the microphone (`RECORD_AUDIO`), the advertising ID, and the ability to receive boot events, among others. It includes Firebase analytics and crash-reporting components. You can review or revoke permissions in the TV's app settings.

## Verify the download

Linux or macOS, using `SHA256SUMS.txt` from the release:

    sha256sum -c SHA256SUMS.txt

Windows:

    certutil -hashfile Stremio-TV-1.9.10-armeabi-v7a.apk SHA256

Compare the result with the APK SHA-256 above.

## Troubleshooting

- **App not installed:** uninstall any existing Stremio first, then install again.
- **Parse error:** check the checksum, and make sure the TV's CPU is ARM, not Intel (x86).
- **Crashes or freezes during playback:** see the RAM notes above.

## Source and terms

This repository redistributes Stremio's Android TV build 1.9.10 (armeabi-v7a, nodpi variant) from APKMirror, without changes to the APK. Stremio's terms apply to the app. This project is not affiliated with Stremio.
