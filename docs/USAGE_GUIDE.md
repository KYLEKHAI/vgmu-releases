# Usage Guide

A complete reference for everything vgmu can do.

> **Tip:** You can also find a quick in-app reference anytime under **Settings → Help**.

## Contents

- [Navigation](#navigation)
- [Home](#home)
- [Browse](#browse)
- [Search](#search)
- [Library](#library)
- [Album Pages](#album-pages)
- [Playback](#playback)
- [Likes](#likes)
- [Downloads](#downloads)
- [Local Library Import](#local-library-import)
- [Backup & Restore](#backup--restore)
- [Settings](#settings)
- [Themes](#themes)
- [Discord Rich Presence](#discord-rich-presence)
- [Offline & Error Handling](#offline--error-handling)

---

## Navigation

vgmu has four tabs — **Home**, **Search**, **Library**, and **Downloads** — plus a **Settings** gear icon in the header of every screen. There is no account or sign-in; everything works locally on your device from the moment you install the app.

A **mini-player** appears above the tab bar whenever a track is loaded, showing artwork, title/artist, transport controls, and a compact progress bar. Tap it to open the full-screen **Now Playing** player.

## Home

Home shows three sections pulled live from the online catalog:

- **Latest** — recently added soundtracks
- **Top 40** — currently popular albums
- **Most Favorites** — all-time favorite albums

Each card shows the album title and a subtitle (type and year, when known). Pull down to refresh manually at any time.

**Automatic refresh** is Wi-Fi-first by default — Home only refreshes itself over cellular data if you enable **Settings → Network → Refresh Home on cellular**. If a refresh fails, Home keeps showing your last successful data along with an "Updated {time}" note so you're never left with a blank screen.

Tap **Browse** in the header to jump to more discovery options.

## Browse

Browse offers on-demand preset lists that load only when you pick one:

- **All-Time Top 100**
- **Last 6 Months Top 100**
- **Top 100 Newly Added**
- **Currently Viewed** — albums other listeners are currently browsing

There are also two quick-discovery shortcuts:

- **Random Album** — jumps straight to a random album page
- **Random Song** — jumps straight to a random track

If the online catalog's structure has changed and a preset can't be parsed, Browse tells you plainly that the preset is temporarily unavailable while your Library stays fully usable offline.

## Search

Search looks up **albums and soundtracks** (not individual track titles — track-level search results from the catalog aren't reliable enough to show). Type at least 2 characters; results load automatically about 300ms after you stop typing.

**Filters** (tap a chip to open its picker):
- **Sort**
- **Album type**
- **Year**
- **Platform**

Filter options are populated from whatever the catalog actually offers for your current search, so they may vary. Use the **Reset filters** chip to clear them all. Results load more as you scroll (with a manual "Load more" button as a fallback), and a result count is always shown.

## Library

Library is your personal collection. It's organized into a few kinds of entries:

### Built-in collections (always present)

- **Liked Tracks** — every track you've hearted
- **Offline Library** — every track that's been downloaded and verified for offline playback
- **Local Library** — audio files you've imported from your device (see [Local Library Import](#local-library-import))

These three can't be deleted, since they represent live state rather than something you created.

### Things you create

- **Playlists** — tap **Create (+) → Create Playlist**, give it a name, and optionally a description and cover photo. Add tracks from any album page, search result, or the player's queue menu. Playlist names must be unique — vgmu warns you if the name is already taken.
- **Folders** — tap **Create (+) → Create Folder** to group existing playlists and saved albums together under one name, description, and cover photo. Pick which albums and playlists belong to it using a searchable picker with A-Z section headers, artwork thumbnails, and filter chips for Albums, Playlists, and Downloaded. Deleting a folder never deletes what's inside it. Folder names must be unique — vgmu warns you if the name is already taken.
- **Saved Albums** — any album with at least one track saved to your library appears here automatically.

### Organizing your Library

- **Filter chips**: All / Playlists / Albums / Folders / Downloaded
- **Search within your library**
- **Sort**: Recently Played or Title — playing a collection inside a folder updates the timestamp for both the collection and the parent folder
- **View**: list or grid
- **Pin**: long-press a collection → **Collection options → Pin**, to keep up to 4 favorites at the top of the tab
- **Delete/Unsave**: long-press → Delete (for playlists/folders) or Unsave (for albums). Deleting a playlist or folder never deletes the underlying tracks, your likes, or any downloaded files — only the organizational grouping.
- **Hide items already in a folder**: an optional setting (**Settings → Library**) that removes albums and playlists from the main Library list once they belong to a folder, so they only show up inside that folder.

### Editing playlists and folders

Open a playlist or folder and tap **Edit** to change its name, description, and cover photo, or to delete it. Renaming to a name already used by another playlist or folder isn't allowed.

- **Playlists**: tap **Add tracks** inside the editor to search your library and select tracks to add.
- **Folders**: tap **Add items** inside the editor to open the same searchable, filterable, A-Z-sectioned picker used at creation time, and choose which albums and playlists belong to the folder.

Closing an editor with unsaved changes asks whether to keep editing or discard them — nothing is saved until you tap **Save**.

## Album Pages

Every album page offers:

- **Play album** — starts playback from the first track. Press and hold **Play** to add every track to the playback queue instead; a confirmation appears when adding 100 or more tracks. The same long-press works on playlists, folders, and Local Library pages.
- **Save album** — bookmarks it into your Library
- **Download album** — queues every track for offline saving
- Per-track rows, each with its own **play**, **like**, **add to queue**, **add to playlist**, and **download** actions
- A gallery of alternate cover art, when the catalog provides more than one image
- An "album information" panel with additional metadata

## Playback

### Mini-player and full player

The mini-player (bottom of screen) gives you play/pause, previous/next, and a compact seek bar. Tap it to open the full **Now Playing** screen, which adds:

- Large artwork with swipeable transitions between tracks
- A full seek bar
- **Like** (heart)
- **Shuffle** toggle
- **Repeat**, which cycles Off → Repeat All → Repeat One (a small "1" badge shows when repeat-one is active)
- **Queue** button, opening the full queue view
- Swipe the screen down to dismiss it back to the mini-player
- Tapping the title/artist jumps you to the album, playlist, or folder the current track is playing from

### Queue and Next Up

vgmu keeps two separate lists:

- **Queue** — tracks you've manually added; these always play first
- **Next Up** — the rest of the current context (the album, playlist, or search results you were browsing), playing automatically after the Queue is empty

Both lists load in batches of 100 tracks at a time to keep the queue responsive, even with very large collections. Section headers show the total count (e.g. "Queue (350)"), and a "+N more tracks" indicator appears when additional tracks are waiting to load. The next batch loads automatically as you play through them.

From the queue view you can reorder tracks, remove them, clear the queue, or promote an upcoming "Next Up" track into your manual queue. When tracks are still pending beyond the loaded batch, the clear button offers a choice between clearing the loaded tracks or the entire queue including all pending tracks.

**Shuffle** reshuffles the Next Up list; turning shuffle back off restores the original order.

### Background and lock-screen playback

Playback continues when you close or minimize vgmu, and when your device is locked. Your device's lock screen and notification shade show the current track's title, artist, album, and artwork, with working play/pause and next/previous controls. (Seek-forward/seek-backward buttons are intentionally not shown on the lock screen.) Bluetooth and wired headset media buttons work the same way.

Your queue, current track, and playback position are saved automatically and restored the next time you open the app.

## Likes

Tap the **heart icon** on any track row or in the full player to like it. Liking a track also saves its parent album to your Library if it isn't already saved. Liked tracks show up in **Library → Liked Tracks**; tap the heart again to remove one.

## Downloads

The **Downloads** tab tracks everything you're saving for offline playback. Its tab icon shows a live badge count of active, pending, and in-progress jobs.

### How the queue works

Only **one download runs at a time**, even if you've queued an entire album or playlist — everything else waits its turn and shows a numbered position in the "Pending" list. Bulk album/playlist downloads are grouped together with an aggregate progress indicator.

### Formats and quality

vgmu supports whatever formats the catalog offers per track: **FLAC, M4A, MP3, and OGG**. Set your preference in **Settings → Download Quality**:

- **Best Available** — automatically picks the highest-quality option actually offered for each track (FLAC → M4A → MP3 → OGG)
- **FLAC Only**, **M4A/AAC**, **MP3**, or **OGG** — force a specific format

### Failures, retries, and rate limits

Recoverable errors (network hiccups, temporary source unavailability, timeouts, and rate limits) are retried automatically up to 3 times. If the source specifically rate-limits a request, vgmu shows a **live countdown** next to the job — "Waiting to retry · Ns" — and retries exactly when the countdown reaches zero, rather than guessing.

Downloads that fail for other reasons (like a chosen format no longer being available) can be retried manually, with a prompt to pick a different format if needed. Failed jobs can be cleared individually or all at once.

### Pausing and cancelling

You can pause and resume the active download, or cancel just the current track vs. the entire remaining batch.

### Completion and history

Finished downloads appear in a "Completed" section — tap **Done** to acknowledge them, after which they move into a **Download History** you can review later. You control how long history entries stick around in **Settings → Download History**. Every file is checksum-verified before it's counted as successfully saved.

## Local Library Import

Beyond downloading from the catalog, you can import audio files already on your device. Imported tracks appear in **Library → Local Library**, separate from catalog downloads. Enable **Settings → Local Library → Scan nested folders** if your music is organized into subfolders.

## Backup & Restore

**Settings → Backup & Restore** lets you move your library to a new install or keep a personal copy.

- **Export** saves a backup file containing your playlists, folders, liked and saved tracks, custom cover art, and all settings and themes. Share or store it wherever you like (Files, AirDrop, cloud storage, and so on) — vgmu doesn't upload it anywhere on its own.
- **Import** restores a backup file onto the current install. This **replaces** everything currently in your library and settings with the backup's contents, so it asks for confirmation before proceeding.
- **What isn't included**: downloaded audio files and folders imported from your device aren't part of the backup — they stay tied to the install that made them. After importing, saved tracks re-download when opened and album covers refresh automatically; local-import tracks reappear in playlists but need to be re-imported to play.

## Settings

Reached from the gear icon (⚙️) on any screen.

| Section | What it does |
|---|---|
| **Catalog Source** | Toggle the live online catalog on/off — turn it off to restrict vgmu to your offline Library only |
| **Download Quality** | Choose Best Available, FLAC Only, M4A/AAC, MP3, or OGG |
| **Confirmations** | "Always ask before downloading" and "Always ask before saving" toggles |
| **Default App View** | Which tab opens on launch — Library, Home, Search, or Downloads |
| **Library** | "Hide items already in a folder" — remove albums and playlists from the main Library list once they belong to a folder; "Rounded artwork" — display track and album artwork as circles instead of rounded squares |
| **Themes** | See [Themes](#themes) below |
| **Marquee Scroll Speed** | How fast long titles scroll |
| **Playlist Artwork** | Use playlist art for tracks missing their own artwork, and optionally override track art with playlist art |
| **Track Metadata** | Apply playlist-level track edits globally |
| **Local Library** | Scan nested folders when importing |
| **Network** | Allow Home to auto-refresh over cellular (off = Wi-Fi only) |
| **Download History** | How long completed-download history is kept |
| **Storage** | Breakdown of space used: downloaded tracks, local imports, artwork, and total |
| **Discord Rich Presence** | See [Discord Rich Presence](#discord-rich-presence) below |
| **Backup & Restore** | See [Backup & Restore](#backup--restore) above |
| **Help** | Quick in-app usage reference |
| **About** | App version and info |
| **Legal & Safety** | Links to the Privacy Policy, EULA, and License |

## Themes

vgmu ships with dozens of built-in themes across several categories, previewed live before you apply them:

- **Baseline (Simple UI)** — follows your device's system light/dark setting, with a selectable accent color. The theme picker's preview swatch reflects your chosen accent and light/dark mode
- **Light & Classic**, **Dark & Classic**
- **Warm**, **Nature**, **Atmospheric**
- **Gaming** — including console- and platform-inspired palettes

Popular presets include Dracula, Nord, Tokyo Night, Catppuccin (Latte/Mocha), Gruvbox, Solarized (Light/Dark), Rosé Pine, Monokai, One Dark Pro, Everforest, Material, and more. Pick one, preview it, and tap **Apply theme** to confirm.

## Discord Rich Presence

An optional feature that shows what you're listening to on your Discord profile as a "Listening to" activity, including track title, artist, album, a live progress bar, and artwork.

**Important:** this connects using your own Discord account token, entered directly in Settings, over a method Discord does not officially support for this kind of use. Using it carries a real risk of account action against your Discord account, and is entirely at your own risk. It is off by default, and you must explicitly opt in.

Presence is only shown while a track is actually playing or loading — pausing, going idle, or hitting an error immediately clears it, so it never shows a stale "frozen" card. If your token becomes invalid, vgmu detects the failure and clears it from storage automatically. See [PRIVACY.md](../PRIVACY.md) for exactly what data this feature transmits.

## Offline & Error Handling

vgmu is designed to keep your Library usable even when the online catalog isn't reachable:

- **No connection**: Home, Search, and Browse show a clear "connect to Wi-Fi or cellular data and try again" message; your Library stays fully available offline.
- **Catalog temporarily disabled**: shown if you've turned off **Settings → Catalog Source**; again, your Library remains available.
- **Rate limited**: any rate-limited request shows a live retry countdown rather than a generic error.
- **Catalog structure changed**: if the online source updates its site in a way vgmu can't parse yet, you'll see a message explaining the app needs an update — your Library is unaffected.

In all of these cases, whatever you've already saved to your device keeps working normally.

### Why do I sometimes see "rate limited" messages?

vgmu doesn't run its own music servers — it reads directly from a third-party online catalog, the same way your device would if you visited it in a browser. That catalog limits how many requests it will accept from a single device in a short period of time, mainly to keep its service stable and fair for everyone using it.

If you search, browse, or download a lot in quick succession (especially downloading a large album all at once), you may occasionally hit that limit. This isn't a bug — vgmu detects it automatically and shows a live countdown ("Waiting to retry · Ns") until it's safe to try again, then resumes on its own. You don't need to do anything; just let the countdown finish.

If rate limiting happens often, spacing out large downloads (rather than queuing many albums back-to-back) can help.

---

For setup help, see the [Installation Guide](INSTALLATION.md). For problems not covered here, see [Support & Troubleshooting](../SUPPORT.md) or [open an issue](../../issues/new?template=bug_report.md).
