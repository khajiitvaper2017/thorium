# Thorium for Android with microG

[Download APKs from Releases](https://github.com/khajiitvaper2017/thorium/releases).

Fork of [gz83/thorium](https://github.com/gz83/thorium), based on the original
[Thorium](https://github.com/Alex313031/thorium). Adds Google account sign-in and
sync integration through ReVanced microG, using patches from
[microg-ungoogled-chromium](https://github.com/bearinmindcat/microg-ungoogled-chromium).

## Differences

- Targets Android ARM64 on Chromium **156.0.8078.28**.
- Preserves microG sign-in and sync settings across restarts.
- Includes Android extension-menu and toolbar crash fixes.
- Offers an optional [faster ARM64 release build](./arm/android/arm64_fast_release_args.gn).
- Hides Discover cards when their renderer is unavailable.

## Setup

1. Install ReVanced microG (`app.revanced.android.gms`).
2. Add your Google account in microG.
3. Select that account in Thorium's sign-in settings.

## Build

See the [Android build and installation guide](./arm/android/README.md).
You need a separate Chromium checkout, `depot_tools`, and Android build dependencies.
This repository contains the [patch series](./patch_scripts/series/series) and build scripts.

## Limitations

Trusted Vault key retrieval and recovery are unsupported, so affected encrypted
data cannot sync. Android extensions are experimental,
and intermittent freezes remain under investigation.
