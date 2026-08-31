# vgmu Privacy Policy

**Version:** 1.0.2
**Effective date:** 2026-08-31
**Applies to:** vgmu 1.0.2 personal-use binary releases

This policy describes the current vgmu application (the “App”) in plain language. It is an owner-authored privacy notice from vgmu Developer, not legal advice. Privacy questions can be sent through [Support](SUPPORT.md) or by [opening an issue](../../issues/new?template=feedback.md).

## Summary

vgmu is local-first. It does not operate a user-account service, cloud synchronization, advertising service, or analytics service. The App stores its library and preferences on the device. When online features are used, the App makes direct requests to third-party catalog, artwork, audio, and optional Discord services from the device.

## Information stored on the device

Depending on the features you use, vgmu stores locally:

- Settings such as appearance, accent, preferred format, refresh, download-history, and playback preferences.
- Catalog and library metadata, likes, playlists, folders, playback queue, download queue, and download history.
- Cached artwork, user-selected playlist artwork, saved audio, and local-library file references or imported audio.
- A Discord account token in secure device storage if you enable Discord Rich Presence.

The App does not send this local library data to a vgmu account or vgmu-operated cloud service.

## Information sent to third-party services

When you use online catalog features, the selected third-party source may receive the search text, filters, source identifiers, requested metadata, and ordinary network information such as an IP address, timestamp, request headers, and user agent. Artwork and audio requests are made directly from the device to the relevant third-party endpoint, which can see the request and network information needed to serve it.

When Discord Rich Presence is enabled, vgmu sends the supplied token directly to Discord to connect the gateway and publish activity. The activity can include the current track title, artist, album, playback state, timing, and artwork-related information. vgmu may send a remote artwork URL to Discord’s external-asset endpoint so Discord can render the activity image. Discord’s own terms and privacy practices apply to that processing.

vgmu does not intentionally collect device identifiers for its own analytics. That does not prevent operating systems, network providers, or third-party endpoints from processing technical request information under their own policies.

## Permissions and local files

vgmu may ask for access needed for actions you choose, including selecting or saving artwork, importing local audio or folders, sharing files, and playing audio in the background. vgmu does not record or transmit microphone audio. Files selected for import or saving remain under the device’s and operating system’s storage controls.

## Retention and deletion

Local data remains on the device until you remove it through vgmu, clear the relevant history or files, disconnect Discord, uninstall the App, or otherwise manage the device storage. Download history can be configured to be removed immediately or after a selected retention period. Resolved source audio URLs are intended to be short-lived and are not durable library identifiers.

vgmu does not provide an account-based or cloud-synced backup service. It does offer a manual, on-device backup and restore feature (Settings → Backup & Restore) that exports your library metadata and settings to a file you choose where to store or share; that file stays under your control and is not sent to vgmu or a vgmu-operated service. Device operating-system backup behavior is controlled by the platform and its provider. Third-party services control their own retention of requests and content.

Disconnecting Discord clears the stored Discord token from vgmu’s secure storage. Removing local audio or artwork does not remove copies or records retained by a third-party service.

## Security

The Discord token is stored through the platform secure-storage facility. vgmu uses app-managed storage for local metadata and saved media. No storage or transmission method can guarantee absolute security, so keep the device and its operating system protected.

## Changes

vgmu may update this policy when its data practices or release behavior changes. The version and effective date identify the policy intended for a release. The policy must be reviewed against the exact binary before any broader distribution.
