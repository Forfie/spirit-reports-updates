# Spirit Reports updates

This repository only hosts automatic updates for **Spirit Reports**, Spirit Radio's internal reporting app. There is no source code here.

Each [release](../../releases) contains:

- `SpiritReports-<version>.zip`: the app, signed with Spirit Radio's Apple Developer ID and notarized by Apple.
- `appcast.json`: the update feed (version, download link, SHA-256, notes).

These files never contain the Bloomerang API key or any donor data. Installed copies of the app keep those locally, and only install an update whose signature matches Spirit Radio's Developer ID and whose checksum matches the feed.

Releases are published with `PUBLISH=1 ./scripts/release.sh <version> "<notes>"` from the private source repository.
