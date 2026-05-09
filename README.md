# TimeQuorum Releases

This repository is the **public artifact mirror** for [TimeQuorum](https://timequorum.com) desktop app releases. It exists so that installers and auto-update packages can be downloaded by anyone without requiring access to the private source repository.

## Downloading

The easiest way to get the latest version is from the downloads page:

**[timequorum.com/downloads](https://timequorum.com/downloads.html)**

Direct platform links:
- **Windows** — [releases.timequorum.com/download/windows](https://releases.timequorum.com/download/windows) (`.msi`)
- **macOS** — [releases.timequorum.com/download/mac](https://releases.timequorum.com/download/mac) (`.dmg`)
- **Linux** — [releases.timequorum.com/download/linux](https://releases.timequorum.com/download/linux) (`.AppImage`)

## System Requirements

| Platform | Minimum |
|---|---|
| Windows | Windows 10 64-bit (build 1903+) |
| macOS | macOS 12 Monterey |
| Linux | Ubuntu 22.04 / Debian 12 / Fedora 38 or equivalent |

## Releases

Each [release](https://github.com/TimeQuorum/TimeQuorum-Releases/releases) is tagged `desktop/v<version>` and contains:

| File | Purpose |
|---|---|
| `timequorum-desktop_<ver>_x64_en-US.msi` | Windows installer |
| `timequorum-desktop_<ver>_x64_en-US.msi.zip` | Windows auto-updater payload |
| `timequorum-desktop_<ver>_x64_en-US.msi.zip.sig` | Auto-updater signature |
| `timequorum-desktop_<ver>_aarch64.dmg` | macOS installer (Apple Silicon) |
| `timequorum-desktop_<ver>_aarch64.dmg.sig` | Auto-updater signature |
| `timequorum-desktop_<ver>_amd64.AppImage` | Linux portable binary |
| `timequorum-desktop_<ver>_amd64.AppImage.tar.gz` | Linux auto-updater payload |
| `timequorum-desktop_<ver>_amd64.AppImage.tar.gz.sig` | Auto-updater signature |

### Pre-release tags

Tags ending in `-test.<number>` (e.g. `desktop/v0.2.0-test.17`) are **internal test builds**. They are not production-ready and are excluded from the downloads page. Use them only if you have been given a specific build number to test.

## Auto-updates

The desktop app checks for updates automatically on launch via [releases.timequorum.com](https://releases.timequorum.com). Updates are signed with an Ed25519 key — the `.sig` files in each release are the per-file signatures verified by the app before installation.

If you want to stay on a specific version, auto-updates can be disabled in the app settings.

## Source Code

TimeQuorum is a commercial product. Source code is maintained in a private repository. If you have questions about licensing or security disclosures, contact [hello@timequorum.com](mailto:hello@timequorum.com).

## Mobile Apps

iOS and Android apps are distributed through their respective stores and are not hosted here.

- **App Store** — coming soon
- **Google Play** — coming soon
