# fileadeX Mobile for Android

This public repository contains Android APK releases and update manifests, not application source code or signing credentials.

## Download

[Download fileadeX Android v1.0.4](https://github.com/Fardin7864/fileadex-mobile-releases/releases/download/v1.0.4/fileadeX-1.0.4-android.apk)

Production releases use the same certificate as v1.0.2. Android may ask you to allow installation from your browser, file manager, or fileadeX. Installation always requires your approval.

The app checks `version.json` on launch and periodically on resume. From v1.0.4, it checks build numbers, downloads updates in the app, verifies SHA-256, and opens Android's installer. Older releases may open the download in a browser.

## QA builds

[Download QA v1.0.4 build 10](https://github.com/Fardin7864/fileadex-mobile-releases/releases/download/v1.0.4-qa/fileadeX-1.0.4-build10-android-QA.apk)

Recent 1.0.3 QA APKs use a different signing certificate. Install this QA build manually once to keep that certificate and enter the separate `qa-version.json` update channel. Do not install production APKs over QA APKs, or vice versa. Switching signing certificates cannot preserve an installation through an ordinary Android update.

## Requirements

- Android 8.0 (API 26) or newer
- ARM64 or ARMv7 Android device

## Integrity

The SHA-256 checksum for the current release is published in `version.json` and in the matching GitHub release notes.
