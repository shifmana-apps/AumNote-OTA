# AumNote OTA

Public distribution repository for **web-runtime OTA bundles only**. The Android application and source of truth live in the private [`shifmana-apps/AumNote`](https://github.com/shifmana-apps/AumNote) repository.

Canonical rules:

- This repository must never become a second AumNote source tree.
- It must not contain APK files, signing keys, passwords, tokens, or source secrets.
- The installed native shell family is selected by `latest.json.nativeVersionCode`.
- Web-only updates are stored under `bundles/` and verified by SHA-256 before activation.
- A native Android change requires a new signed base APK from the main AumNote repository; it is **not** shipped as OTA.
- Keep `latest.json.enabled=false` until a bundle has passed the canonical device acceptance gate.

The current publication state is in [`latest.json`](latest.json). The historical personal-account URL continues to serve installed clients, while new AumNote builds should use this organization-owned URL. The source repository's publication workflow controls future bundles; device acceptance remains a separate release gate.
