# Installing AlphaNav

The macOS app is signed with an Apple Developer ID and notarised by Apple. The Windows installer is not
signed with a Microsoft certificate yet: Windows warns about it the first time. You can check a download
against the release's `SHA256SUMS.txt` first (see the [README](../README.md#verify-a-download)).

## macOS (Apple Silicon)

1. Open `AlphaNav-mac-arm64.dmg` and drag **AlphaNav** to **Applications**.
2. Open AlphaNav from Applications. macOS asks once whether to open an app downloaded from the internet:
   **Open**.
3. On the first start macOS asks whether AlphaNav may accept incoming network connections: **Allow** it
   if phones or tablets on the boat's network should open AlphaNav, otherwise **Deny**.

Versions before 1.0.7 were not notarised: if one of those will not open, install the latest instead.

Intel Macs are not supported yet.

## Windows 10 / 11

1. Run `AlphaNav-windows-x64-setup.exe`.
2. If **Windows protected your PC** appears, click **More info ▸ Run anyway**.
3. AlphaNav installs for your user and starts. A Start menu and a desktop shortcut are made.
4. Windows Firewall asks about network access: allow **Private networks** for phones and tablets on
   the boat's network.

## Linux

Debian / Ubuntu:

```sh
sudo apt install ./alphanav-linux-amd64.deb
```

Fedora / RHEL:

```sh
sudo dnf install ./alphanav-linux-x86_64.rpm
```

Start **AlphaNav** from the applications menu.

## Updating

Install the new version over the old one, as above. Settings, routes, polars and charts stay. On the
first start the new version updates its database, keeping a copy of the old one beside it
(`dev.db.before-….bak`).

## Where AlphaNav keeps its data

| System | Folder |
|---|---|
| macOS | `~/Library/Application Support/alphanav-admin-electron/server-config` |
| Windows | `C:\ProgramData\AlphaNav` |
| Linux | `~/.config/alphanav-admin-electron/server-config` |

In AlphaNav, **Help ▸ Open Data Folder** and **Help ▸ Open Logs Folder** open them.

## Phones and tablets

While AlphaNav runs, other devices on the same network open it in their browser at
`http://<this computer's address>:3002`. **AlphaNav ▸ Allow devices on the network** turns that off.
