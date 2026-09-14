# Installation Guide

VGMU is distributed through [KYLEKHAI/vgmu-releases](https://github.com/KYLEKHAI/vgmu-releases/releases/latest). There is no App Store or Google Play listing. Pick the APK for Android or the IPA for iOS; GitHub's automatic source archives contain public repository files, not the application or an installer.

## Android

Published device testing covers Android 16 on Google Pixel 9. Compatibility with other configurations has not been established by that check.

You need enough storage for the app and saved audio, and an internet connection for the download and online catalog features.

1. Open the [latest release](https://github.com/KYLEKHAI/vgmu-releases/releases/latest), read the notes, and download its `.apk` asset.
2. [Verify the SHA-256 checksum](#verify-your-download).
3. Open the APK using your browser or file manager. If prompted, allow that specific app to **Install unknown apps** in Android Settings. Labels differ by device; keep Play Protect enabled.
4. Follow the install prompts and open VGMU. Grant access only for the features you choose to use. You can disable the installer permission afterward.
5. Follow [Getting Started](GETTING_STARTED.md). For offline listening, finish downloads and check the Offline Library before disconnecting.

## iOS

Published device testing covers iOS 26.3 on iPhone 16 and 17. Other configurations are not verified.

### Requirements

- AltStore **Classic**, installed with AltServer on a Mac or Windows computer.
- Your own Apple ID for self-signing, an iPhone, and storage for the app and saved audio.
- A connection to download the IPA, and AltServer reachable during installation and refresh.
- A plan to refresh before expiry: a free Apple ID normally gives seven days. Apple's active sideloaded-app limits also apply, with AltStore itself using a slot.

### Setup and installation

1. Follow AltStore's current [macOS setup](https://faq.altstore.io/altstore-classic/how-to-install-altstore-macos) or [Windows setup](https://faq.altstore.io/altstore-classic/how-to-install-altstore-windows). Install AltServer and AltStore Classic, connect and trust the device, and enable Developer Mode where required. Platform prerequisites are maintained in those official guides.
2. Download the `.ipa` from the [latest VGMU release](https://github.com/KYLEKHAI/vgmu-releases/releases/latest) and [verify its checksum](#verify-your-download).
3. With AltServer running and reachable, open **AltStore → My Apps → +** on your iPhone. Choose the downloaded IPA and complete signing in AltStore with your Apple ID. Never send credentials to VGMU support or enter them into the landing website.
4. Open VGMU and follow [Getting Started](GETTING_STARTED.md).

### Expiry and refresh

In AltStore's **My Apps** tab, use **Refresh All** while AltServer is reachable, before the seven-day free-account window ends. Automatic background refresh depends on your setup and is not guaranteed. See [AltStore's current refresh guidance](https://faq.altstore.io/altstore-classic/your-altstore) and [troubleshooting](https://faq.altstore.io/altstore-classic/troubleshooting-guide).

This guide describes the AltServer-based Classic route. AltStore PAL is a different distribution route. VGMU does not handle your Apple ID; review AltStore's policies for its signing and account processing.

## Verify your download

Check the repository owner and version, then compare your downloaded file's SHA-256 value with the release's `SHA256SUMS.txt` asset:

- macOS: `shasum -a 256 filename`
- Windows PowerShell: `Get-FileHash filename -Algorithm SHA256`

Replace `filename` with the downloaded APK or IPA. If values differ, do not install; retrieve the file again from the canonical release. A matching hash checks integrity against the published checksum, not a guarantee of safety.

## Updating or uninstalling

Back up before changing your installation. Do not rely on an update or reinstall preserving all local data.

1. In VGMU, open **Settings → Backup & Restore → Export backup**.
2. Save the exported file **outside the app**. Auto Backup snapshots inside the app can be lost when the app is removed.
3. Install the new APK or IPA using the steps above.
4. Use **Import backup** as needed. Review the [usage guide](USAGE_GUIDE.md#backup--restore) for backup contents and limitations; do not assume saved audio is included.

Uninstalling removes the app's local data. There is no VGMU account-based cloud recovery.

## Help and policies

[Support](../SUPPORT.md) · [Privacy](../PRIVACY.md) · [Security](../SECURITY.md) · [License](../LICENSE.md)

The official Discord community invite is not yet published. Until it is available, use the existing GitHub support and feedback channels.
