# K-Reader

A personal reader for light novels and manga, on Android and Windows, that keeps your place in step
across all your devices.

## Downloads

- **Android:** the latest `K-Reader-v….apk` from [Releases](../../releases/latest). Once installed, the
  app checks this page for updates itself.
- **Windows:** `K-Reader-Desktop-Setup-….exe` from the
  [K-Reader Desktop release](../../releases/tag/desktop-latest). Run it to install; installed copies
  update themselves.

## What it does

**Light novels** come from your own EPUB and PDF files, one folder per series.

- Series with their own covers, a volume order you set, and a description.
- A reader with themes, fonts and text size, and page or scroll layouts. PDFs keep pictures in their own
  colours in the dark and sepia themes.
- Bookmarks, highlights and notes, a dictionary, and reading stats.
- Import volumes from your phone or Google Drive, or point the desktop app at a folder (Google Drive for
  Desktop works well).
- Arrange series into your own order by dragging them.

**Manga** comes from online sources through Mihon-compatible extensions. No extension repositories are
included; add your own.

- On Android, it's the full Mihon manga reader.
- On Windows, K-Reader sets up [Suwayomi](https://github.com/Suwayomi/Suwayomi-Server) for you the first
  time you open the Manga tab, and shows it in the app's own colours. It runs the same extensions.

**Reading sync** keeps your devices in step through a sync server you run yourself (a
[KOReader-compatible](https://github.com/koreader/koreader-sync-server) server with a few K-Reader
additions). There are no sessions, so you stay signed in until you sign out. It syncs:

- where you are in each volume, on every device
- bookmarks, highlights and notes
- which volumes and manga chapters you've read
- series covers and the order you've arranged your series in
- reading stats, combined across devices

Accounts on a server need an invite code from whoever runs it.

**Backups:** the Windows app backs up your reading data and manga library once a day to a folder you
choose (one on Google Drive keeps it in the cloud), and can restore it on a new PC. On Android, use the
backup in More → Settings → Data and storage.

## Credits and licence

K-Reader is a modified version of [Mihon](https://github.com/mihonapp/mihon), used under the Apache
License 2.0. Changes from Mihon include:

- a Novels library and reader for EPUB and PDF files, built on the
  [Readium Kotlin Toolkit](https://github.com/readium/kotlin-toolkit) (BSD 3-Clause)
- reading sync, shared series covers and order, and read status for novels and manga
- new name, icon and app ID
- the Library tab renamed Manga, and Updates moved into More
- updates delivered from this repository

K-Reader Desktop is built with [Electron](https://www.electronjs.org) (MIT). It shows EPUBs with
[foliate-js](https://github.com/johnfactotum/foliate-js) (MIT) and PDFs with
[pdf.js](https://github.com/mozilla/pdf.js) (Apache 2.0). Suwayomi (MPL 2.0) is downloaded from its own
releases when you set up manga, not bundled.

The full list of open-source libraries and their licences in the Android app is under
**More → About → Open source licenses**.

Licensed under the [Apache License 2.0](LICENSE).
