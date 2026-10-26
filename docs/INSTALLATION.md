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

You sideload VGMU yourself with one of two self-signing stores. Both use your own Apple ID, and install the same IPA from the [latest release](https://github.com/KYLEKHAI/vgmu-releases/releases/latest). If one stops working after an iOS or store update, switch to the other (see [Switching stores](#switching-between-altstore-and-sidestore)).

| | AltStore Classic | SideStore |
|---|---|---|
| Computer needed | For setup **and** every refresh (AltServer) | For setup only (iloader) |
| Refresh | On the same network as AltServer | On the phone, with LocalDevVPN connected |
| Setup guide | [AltStore FAQ](https://faq.altstore.io/altstore-classic/how-to-install-altstore-macos) | [SideStore docs](https://docs.sidestore.io/docs/installation/prerequisites) |

### Common requirements

- An iPhone with a passcode, your own Apple ID, and storage for the app and saved audio.
- A Mac, Windows, or Linux computer for setup (AltServer runs on Mac and Windows only).
- A plan to refresh before expiry: a free Apple ID normally gives seven days. A free account can have three sideloaded apps active at once, and the store itself uses one.
- Developer Mode turned on (iOS 16 and later), when the setup guide asks for it.

Never send your Apple ID or credentials to VGMU support or enter them into the landing website. VGMU does not handle your Apple ID; review each store's policies for its signing and account processing.

### Option A: AltStore Classic

1. Follow AltStore's current [macOS setup](https://faq.altstore.io/altstore-classic/how-to-install-altstore-macos) or [Windows setup](https://faq.altstore.io/altstore-classic/how-to-install-altstore-windows). Install AltServer and AltStore Classic, connect and trust the device, and enable Developer Mode where required.
2. Download the `.ipa` from the [latest VGMU release](https://github.com/KYLEKHAI/vgmu-releases/releases/latest) and [verify its checksum](#verify-your-download).
3. With AltServer running and reachable, open **AltStore → My Apps → +**, choose the downloaded IPA, and complete signing with your Apple ID.
4. Open VGMU and follow [Getting Started](GETTING_STARTED.md).

**Refresh:** In **My Apps**, use **Refresh All** while AltServer is reachable, before the seven-day window ends. Background refresh depends on your setup and is not guaranteed. See [AltStore's refresh guidance](https://faq.altstore.io/altstore-classic/your-altstore) and [troubleshooting](https://faq.altstore.io/altstore-classic/troubleshooting-guide).

This route uses AltStore Classic. AltStore PAL is a different distribution route and does not apply here.

### Option B: SideStore with iloader

[iloader](https://github.com/nab138/iloader) is a desktop app that installs SideStore and its pairing file over USB. After that, SideStore refreshes on the phone without a computer.

1. Follow SideStore's current [prerequisites](https://docs.sidestore.io/docs/installation/prerequisites) and [install guide](https://docs.sidestore.io/docs/installation/install). In short:
   - Install [LocalDevVPN](https://apps.apple.com/app/localdevvpn/id6755608044) from the App Store on the iPhone.
   - On the computer, install iloader from its [official releases](https://github.com/nab138/iloader/releases) only. Windows also needs iTunes (for its device driver); macOS includes it.
   - Connect the iPhone by USB, trust the computer, open iloader, sign in with your Apple ID, select the device, and choose **Install SideStore (Stable)**.
   - On the iPhone, trust the developer profile in **Settings → General → VPN & Device Management**, turn on Developer Mode if asked, connect LocalDevVPN, and sign in to SideStore with the same Apple ID.
2. Download the `.ipa` from the [latest VGMU release](https://github.com/KYLEKHAI/vgmu-releases/releases/latest) and [verify its checksum](#verify-your-download).
3. With LocalDevVPN connected, open **SideStore → My Apps → +**, choose the downloaded IPA, and complete signing with your Apple ID.
4. Open VGMU and follow [Getting Started](GETTING_STARTED.md).

**Refresh:** Connect LocalDevVPN, then tap the days counter or **Refresh All** in SideStore's **My Apps**. LocalDevVPN must be on any time SideStore installs, updates, or refreshes an app, and it needs Wi-Fi. If refresh fails after an iOS update or reset, the pairing file may need replacing: run iloader again. iloader problems are handled by its developers, not SideStore or VGMU support.

### Switching between AltStore and SideStore

Store updates often fix whatever broke in the other one, so switching is a normal fix.

1. In VGMU, **Manager → Backup → Export backup**, and save the file outside the app.
2. Set up the other store using its option above. To stay within the three-app limit, remove the store you are leaving if needed.
3. Install the VGMU IPA from the new store, signed with the same Apple ID.
4. Open VGMU. If your library is missing, use **Import backup**.

Only one store manages refreshes for an installed copy of VGMU, so refresh from the store you installed it with most recently.

## Verify your download

Check the repository owner and version, then compare your downloaded file's SHA-256 value with the release's `SHA256SUMS.txt` asset:

- macOS: `shasum -a 256 filename`
- Windows PowerShell: `Get-FileHash filename -Algorithm SHA256`

Replace `filename` with the downloaded APK or IPA. If values differ, do not install; retrieve the file again from the canonical release. A matching hash checks integrity against the published checksum, not a guarantee of safety.

## Updating or uninstalling

Back up before changing your installation. Do not rely on an update or reinstall preserving all local data.

1. In VGMU, open **Manager → Backup → Export backup** (before version 1.3, **Settings → Backup & Restore**).
2. Save the exported file **outside the app**. Auto Backup snapshots inside the app can be lost when the app is removed.
3. Install the new APK or IPA using the steps above.
4. Use **Import backup** as needed. Review the [usage guide](USAGE_GUIDE.md#backup--restore) for backup contents and limitations; do not assume saved audio is included.

Uninstalling removes the app's local data. There is no VGMU account-based cloud recovery.

## Help and policies

[Support](../SUPPORT.md) · [Privacy](../PRIVACY.md) · [Security](../SECURITY.md) · [License](../LICENSE.md)

The official Discord community invite is not yet published. Until it is available, use the existing GitHub support and feedback channels.
