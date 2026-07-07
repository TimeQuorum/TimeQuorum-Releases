# TimeQuorum Releases

This repository is the **public artifact mirror** for [TimeQuorum](https://timequorum.com) desktop app releases. It exists so that installers and auto-update packages can be downloaded by anyone without requiring access to the private source repositories.

## Downloading

The easiest way to get the latest version is from the downloads page:

**[timequorum.com/downloads](https://timequorum.com/downloads.html)**

Direct platform links (always redirect to the latest production release):

- **Windows** — [releases.timequorum.com/download/windows](https://releases.timequorum.com/download/windows) (`.msi`, x64)
- **macOS** — [releases.timequorum.com/download/mac](https://releases.timequorum.com/download/mac) (`.dmg`, universal — Intel & Apple Silicon)
- **Linux (Debian/Ubuntu)** — [releases.timequorum.com/download/linux-deb](https://releases.timequorum.com/download/linux-deb) (`.deb`, amd64)
- **Linux (Fedora/RHEL)** — [releases.timequorum.com/download/linux-rpm](https://releases.timequorum.com/download/linux-rpm) (`.rpm`, x86_64)

A self-contained downloads page is also served at [releases.timequorum.com/downloads](https://releases.timequorum.com/downloads).

## System Requirements

| Platform | Minimum |
|---|---|
| Windows | Windows 10 64-bit (build 1903+), x64 |
| macOS | macOS 12 Monterey (Intel or Apple Silicon) |
| Linux | Ubuntu 22.04 / Debian 12 / Fedora 38 or equivalent, x86_64 |

## Releases

Each platform is published under its **own release tag** — a single app version produces up to four releases:

| Tag | Contents |
|---|---|
| `desktop-win-v<version>` | `TimeQuorum_<version>_x64_en-US.msi` — Windows installer |
| `desktop-macos-v<version>` | `TimeQuorum_<version>_universal.dmg` — macOS installer (universal) |
| `desktop-linux-deb-v<version>` | `timequorum-desktop_<version>_amd64.deb` — Debian/Ubuntu package |
| `desktop-linux-rpm-v<version>` | `timequorum-desktop-<version>-1.x86_64.rpm` — Fedora/RHEL package |

When auto-updater artifacts are built, the Windows release also carries the update payload (`.msi.zip` + `.msi.zip.sig`) and the macOS release its signature file (`.dmg.sig`).

### Dev builds

Releases marked **Pre-release** (tags like `desktop-macos-dev-<build>`) are internal development builds. They are unsigned or ad-hoc signed, not production-ready, and excluded from the downloads page and the download/update endpoints. Use them only if you have been given a specific build number to test.

## Auto-updates

On Windows and macOS, the desktop app checks for updates on launch via `https://releases.timequorum.com/desktop/<target>/latest.json`. Update packages are signed with a minisign (Ed25519) key, and the signature is verified by the app before installation.

On Linux there is no in-app updater — install new versions through your package manager using the latest `.deb` or `.rpm`.

If you want to stay on a specific version, auto-updates can be disabled in the app settings.

## Source Code

TimeQuorum is a commercial product. Source code is maintained in private repositories. If you have questions about licensing or security disclosures, contact [hello@timequorum.com](mailto:hello@timequorum.com).

## Mobile Apps

iOS and Android apps are distributed through their respective stores and are not hosted here.

- **App Store** — coming soon
- **Google Play** — coming soon
