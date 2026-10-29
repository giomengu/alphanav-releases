# AlphaNav

Sailing instruments, charts, weather and routing — for the boat and for the chart table.

AlphaNav reads the boat's instruments (NMEA 0183, NMEA 2000, NKE), shows them with charts, AIS
and GRIB weather, and computes weather routings with isochrones, uncertainty and variation sweeps.
It runs on the desktop and serves the same app to phones and tablets on the boat's network.

This repository holds the **public releases** of AlphaNav. Download the installer for your computer below.

## Download

| Computer | Installer |
|---|---|
| **macOS** (Apple Silicon: M1 and later) | [AlphaNav-mac-arm64.dmg](https://github.com/giomengu/alphanav-releases/releases/latest/download/AlphaNav-mac-arm64.dmg) |
| **Windows** 10 / 11 (64-bit) | [AlphaNav-windows-x64-setup.exe](https://github.com/giomengu/alphanav-releases/releases/latest/download/AlphaNav-windows-x64-setup.exe) |
| **Linux** Debian / Ubuntu (64-bit) | [alphanav-linux-amd64.deb](https://github.com/giomengu/alphanav-releases/releases/latest/download/alphanav-linux-amd64.deb) |
| **Linux** Fedora / RHEL (64-bit) | [alphanav-linux-x86_64.rpm](https://github.com/giomengu/alphanav-releases/releases/latest/download/alphanav-linux-x86_64.rpm) |

These links always give the latest version. Every version, its notes and its checksums are on the
[Releases](https://github.com/giomengu/alphanav-releases/releases) page; what changed is in [CHANGELOG.md](CHANGELOG.md).

## Install

The macOS app is signed and notarised by Apple: it opens like any other app. The Windows installer is
not signed with a Microsoft certificate yet, so Windows asks for one extra confirmation the first time.
[docs/INSTALL.md](docs/INSTALL.md) has the steps for each system.

Installing a new version over the old one keeps your settings, routes and charts: AlphaNav updates
its database on the first start, after making a copy of it.

## Licence and free trial

AlphaNav runs for **30 days free** on each computer, no key needed: start the trial from the
activation page. After that it needs a licence key — 1, 3, 6 or 12 months, or with no end date.
A key is issued for one computer: [ask for one](https://github.com/giomengu/alphanav-releases/issues/new?template=licence_request.yml) with the **Machine ID** shown on the activation page.

The terms are in [LICENSE](LICENSE). AlphaNav is an aid to navigation, not a replacement for official
charts, approved equipment or a proper lookout.

## Problems

Open an [issue](https://github.com/giomengu/alphanav-releases/issues/new/choose) with the version,
your system and, if you can, the log (in AlphaNav: **Help ▸ Open Logs Folder**).

## Verify a download

Each release has a `SHA256SUMS.txt`:

```sh
shasum -a 256 -c SHA256SUMS.txt --ignore-missing     # macOS / Linux
```
```powershell
Get-FileHash .\AlphaNav-windows-x64-setup.exe -Algorithm SHA256   # Windows: compare with SHA256SUMS.txt
```
