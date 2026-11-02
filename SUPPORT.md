# Support and troubleshooting

## Getting help

### Frequently asked questions

**Q: Can I run vgmu on my device?**

- **Android:** Verified on Google Pixel 9
- **iOS:** Verified on iPhone 16 and 17

**Q: Where do I download vgmu?**

- See [README.md](README.md) and the [Releases](../../releases) page for download links

**Q: Is vgmu free?**

- Yes, vgmu is free to download and use for personal purposes

**Q: Will vgmu be open source?**

- No, vgmu is closed source. See [LICENSE](LICENSE.md) for details

**Q: Can I contribute to vgmu?**

- Source code contributions are not accepted at the moment, but bug reports and feedback are welcome

**Q: How do I report a bug?**

- Use the [feedback form](https://vgmu.kylekhai.workers.dev/feedback/), email [vgmu.dev@gmail.com](mailto:vgmu.dev@gmail.com), or [open a bug report](../../issues/new?template=bug_report.md) with details

**Q: My music library disappeared. Can I recover it?**

- Your library is stored locally on your device. If deleted without a backup, it cannot be recovered
- Use **Manager → Backup** to export a backup file (playlists, folders, liked and saved tracks, custom artwork, and settings) before uninstalling or switching devices, and **Import** it on the new install
- vgmu does not sync libraries across devices. Backup & Restore is a manual transfer

### Common issues

**App crashes on startup**

- Ensure you have the latest version installed
- On Android, try clearing the app cache (Settings > Apps > vgmu > Storage > Clear Cache)
- Uninstall and reinstall vgmu
- Check device storage: vgmu needs space for music and data

**Music won't play**

- Without a connection, only downloaded tracks and your Local Library play (see the [usage guide](docs/USAGE_GUIDE.md#downloads))
- Ensure the device has sufficient storage
- Try restarting the app

**Can't download music**

- Check your internet connection
- Check device storage: downloads need free space
- The music source may be temporarily unavailable; try again later

**Local Library folder won't refresh**

- Use a folder vgmu can access, and avoid importing the main Downloads folder directly
- If vgmu asks you to add a folder again, choose the same folder with **Add path** to restore access; your imported tracks stay
- On iPhone, folders added before version 1.0.7 need to be added again once

**Wi-Fi Transfer page won't load on the computer**

- Keep vgmu open on the phone: transfer stops when you leave the app
- The phone and computer need to be on the same Wi-Fi. School, office, and hotel networks often keep devices from reaching each other; try a home network or your phone's hotspot
- Or plug the phone in with a cable and use the **By cable · faster** address. If none appears, turn on Personal Hotspot (iPhone) or USB tethering (Android)
- After ten wrong codes Wi-Fi Transfer stops; tap **Start** again for a new code

**A shared link or .vgmu file doesn't open in vgmu**

- Update to vgmu 1.3 or later; earlier versions can't open shared playlists
- Update to 1.3.1 if a .vgmu file won't open from Files, iCloud Drive, or Downloads, or its name has square brackets
- For a link, tap **Open in vgmu** on the page it shows. For a file in Messages, tap it, then choose vgmu. You can also save it to Files and use **Open a shared file…** in Shared with You

**Discord Rich Presence won't connect**

- On Android, install the Discord app and sign in, then tap **Connect Discord** in vgmu. If the status says vgmu can't reach the Discord app, open Discord, check you're signed in, and play a track again
- On iPhone, finish the Discord sign-in after tapping **Connect Discord**. If the status says the sign-in expired or was cancelled, tap **Connect Discord** again
- With **Use manual token (advanced)**, a failed connection usually means the token is wrong or no longer valid; vgmu clears it, so paste a current one or switch to **Connect Discord**

**Discord Rich Presence says "Not available in this build"**

- Android versions 1.0.5 and 1.0.6 shipped without Discord Rich Presence. Update to 1.0.7 or later to use it again

**App runs slowly**

- Large libraries may impact performance; consider organizing or removing unused items
- The playback queue loads in batches of 100, so very large queues no longer cause lag or crashes
- Close other apps to free up device memory
- Restart your device

**Sync / Cloud**

- vgmu does not sync your library to the cloud
- Your library exists only on your device

## Reporting issues

### Bug reports

Use the [feedback form](https://vgmu.kylekhai.workers.dev/feedback/) or [open a bug report](../../issues/new?template=bug_report.md), and include:

- Device model and OS version
- vgmu version
- Steps to reproduce the issue
- Expected vs. actual behavior
- Relevant screenshots or logs (if safe to share)

### Feature requests and feedback

The quickest way is the [feedback form](https://vgmu.kylekhai.workers.dev/feedback/). It takes a message, and your email is optional.

You can also [open a feedback issue](../../issues/new?template=feedback.md) on GitHub.

## Documentation

- [Installation guide](docs/INSTALLATION.md): Install vgmu
- [Getting started guide](docs/GETTING_STARTED.md): Your first steps
- [Usage guide](docs/USAGE_GUIDE.md): Features and how to use them
- [Privacy Policy](PRIVACY.md): Data handling
- [Security Policy](SECURITY.md): Reporting vulnerabilities
- [License](LICENSE.md): Terms of use

## Still need help?

If your issue isn't covered above:

1. Ask in the [vgmu Discord](https://discord.gg/bFubZaxEBV), or search existing [Issues](../../issues) to see if others reported it
2. Send details through the [feedback form](https://vgmu.kylekhai.workers.dev/feedback/), email [vgmu.dev@gmail.com](mailto:vgmu.dev@gmail.com), or [open a new issue](../../issues/new?template=bug_report.md)
3. Responses may take time
