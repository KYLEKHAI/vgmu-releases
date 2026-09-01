# Installation Guide

## Android

**Verified tested:** Note: vgmu is confirmed working on Android 16 with a Google Pixel 9, whether it works on earlier/later versions is unknown.

### Requirements

- Free storage for the app plus any music you download (see the [Releases](../../releases) page for the current download size)
- Internet connection for initial setup and catalog browsing

### Steps

1. **Download the APK**
   - Visit the [Releases](../../releases) page
   - Download the latest vgmu APK file

2. **Enable Installation from Unknown Sources** (if not already enabled)
   - Open Settings > Apps
   - Tap the 3-dot menu and select "Special app access"
   - Tap "Install unknown apps"
   - Select your file manager and enable "Allow from this source"

3. **Install vgmu**
   - Open your file manager and locate the downloaded APK
   - Tap the APK file to begin installation
   - Follow the on-screen prompts

4. **Grant Permissions**
   - When prompted, grant:
     - **Storage** — to save music for offline playback
     - **Audio** — to play music
   - You can manage permissions later in Settings > Apps > vgmu > Permissions

5. **Launch vgmu**
   - Open the app from your app drawer or home screen
   - See [Getting Started](GETTING_STARTED.md) for your first steps

### Updating vgmu

Installing a new APK **does not** preserve your library, playlists, or settings — back up first.

1. Open vgmu and go to **Settings → Backup & Restore → Export backup**. Save the exported file somewhere outside the app (Files, email, cloud storage) — Auto Backup's own snapshots live inside the app itself, so they're lost along with everything else when you update, and won't help here.
2. Check the [Releases](../../releases) page for new versions
3. Download and install the new APK using the same steps above
4. Open vgmu and go to **Settings → Backup & Restore → Import backup** to restore your library, playlists, and settings from the file you exported in step 1

### Uninstalling

- Long-press the vgmu app icon and select "Uninstall"
- Or go to Settings > Apps > vgmu > Uninstall
- Your library is deleted when you uninstall — use **Settings → Backup & Restore** in the app first if you want to keep a copy (see the [Usage Guide](USAGE_GUIDE.md#backup--restore) for details)

## iOS

**Verified tested:** Note: vgmu is confirmed working on iOS 26.3 with an iPhone 16 and 17, whether it works on earlier/later versions is unknown.

### Installation via AltStore

vgmu is distributed for iOS as an IPA file installed via **AltStore**, a third-party app installer for iOS. Unlike Android's direct APK installation, iOS requires a signing step performed by your device using your own Apple ID.

#### What is AltStore?

AltStore is a free, open-source app installer that lets you sideload unsigned apps onto your iPhone or iPad without a paid Apple Developer account. It uses your own Apple ID to sign apps locally on your device, allowing them to run on iOS.

**Important:** AltStore is not affiliated with Apple, and this installation method is not officially supported by Apple. Your Apple ID and app will be subject to Apple's terms, and the app will expire after 7 days (refreshable via AltServer, see below).

Learn more: [AltStore Official Site](https://altstore.io)

#### Requirements

- **Apple ID** (free; can be a personal account, not a developer account)
- **Computer** (Mac or Windows) running AltServer software, connected to the same Wi-Fi as your device
- **Wi-Fi connection** during initial setup and refresh (every 7 days)
- **Free storage** on your device for the app (~150 MB including music you download)

#### Installation Steps

**Step 1: Install AltServer on your computer**

1. Go to [altstore.io](https://altstore.io)
2. Download AltServer for your operating system (macOS or Windows)
3. Install and launch AltServer on your computer
4. AltServer runs in the background; you'll see its icon in your menu bar (Mac) or system tray (Windows)

**Step 2: Trust AltServer on your iPhone**

1. On your iPhone, go to **Settings > General > VPN & Device Management** (or **Device Management** on iOS 16+)
2. Under "Enterprise App," tap the certificate for your Apple ID account
3. Tap **Trust** to confirm
4. Return to the VPN & Device Management screen — you should see your Apple ID now listed

**Step 3: Add vgmu IPA to AltServer**

1. Download the vgmu IPA file from [Releases](../../releases)
2. On your Mac: drag the IPA file onto the AltServer menu-bar icon
3. On Windows: open AltServer, click "Install," and select the IPA file
4. Select your device from the list
5. Enter your Apple ID and password when prompted (this is used only to sign the app locally on your device; AltServer does not store it)

**Step 4: Launch vgmu**

Once signed and installed, vgmu appears on your home screen. Tap it to launch, then follow the [Getting Started Guide](GETTING_STARTED.md).

#### 7-Day Expiry and Refresh

Apps installed via AltStore expire and stop working after 7 days. To refresh:

1. Keep AltServer running on your computer and your iPhone on the same Wi-Fi
2. Open AltServer and select your device
3. Click "Refresh" next to vgmu
4. The app will refresh in the background (or immediately if you launch it while plugged in)
5. You now have 7 more days

Alternatively, connect your iPhone to your computer via USB and launch the vgmu app — AltServer will automatically detect this and offer to refresh.

#### Updating vgmu

Installing a new IPA **does not** preserve your Library or settings — back up first.

When a new version is released:

1. Open vgmu and go to **Settings → Backup & Restore → Export backup**. Save the exported file somewhere outside the app (Files, email, cloud storage) — Auto Backup's own snapshots live inside the app itself, so they're lost along with everything else when you update, and won't help here.
2. Download the new IPA from [Releases](../../releases)
3. Follow the same AltServer installation steps (Step 3 above)
4. AltServer will replace the old version with the new one
5. Open vgmu and go to **Settings → Backup & Restore → Import backup** to restore your Library and settings from the file you exported in step 1

#### Removing vgmu

1. Your library is deleted when you remove the app — use **Settings → Backup & Restore** in the app first if you want to keep a copy (see the [Usage Guide](USAGE_GUIDE.md#backup--restore) for details)
2. Long-press the vgmu icon on your home screen
3. Tap **Remove App**
4. Choose **Delete from iPhone**
5. Optionally, return to **Settings > General > VPN & Device Management** and untrust the certificate if you no longer use AltStore for other apps

#### Troubleshooting

**"Unable to sign app"**

- Confirm your Apple ID is correct and trusted on your device (Settings > General > VPN & Device Management)
- Ensure your computer and iPhone are on the same Wi-Fi network
- Check that you're running the latest version of AltServer

**"App expired"**

- The 7-day window has passed. Use AltServer to refresh (see above)
- If refresh fails, reinstall using Step 3

**"AltServer not detecting my device"**

- Confirm your iPhone is connected to the same Wi-Fi as your computer
- Restart AltServer
- On your iPhone, go to Settings > General > AirDrop and ensure it's set to "Everyone" or "Contacts Only" (AltServer uses AirDrop to communicate)

**"Insufficient storage"**

- vgmu requires ~150 MB. Check **Settings > General > Storage** and remove apps or files if needed

For more detailed AltStore troubleshooting, see [AltStore FAQ](https://faq.altstore.io).

#### Legal & Privacy Notes

- Your Apple ID is used only to sign the app locally on your device; AltServer and vgmu do not store it
- AltStore is open-source; inspect its code at [github.com/altstoreio](https://github.com/altstoreio/AltStore)
- The 7-day expiry is an Apple limitation, not a vgmu limitation
- Your Library and settings are stored locally on your device and are not synced to Apple's servers or vgmu's servers

---

**Having trouble?** See [SUPPORT.md](../SUPPORT.md) for troubleshooting.
