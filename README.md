# Download Kabe

Kabe is a Wallhaven wallpaper manager for Windows 11 and Ubuntu GNOME.

Download an installer from the [latest release](https://github.com/aaronwJordan/kabe-releases/releases/latest), or browse [all releases](https://github.com/aaronwJordan/kabe-releases/releases).

## Install on Windows 11

1. Download the file named `Kabe-<version>-x64-setup.exe` from the release's **Assets**.
2. Run the installer and choose an installation folder.
3. Open Kabe from the Start menu.
4. In Windows **Settings → Personalization → Background**, select **Picture** or **Solid color** before applying a wallpaper in Kabe.
5. To start Kabe when you sign in, enable **Launch at login** in Kabe Settings.

Windows 11 x64, build 22000 or newer, is required. The installer is currently unsigned, so Windows can show an unknown-publisher warning. Download it only from this repository.

Closing Kabe's window keeps it running in the tray. Use **Quit Kabe** to exit. Kabe restores the previous wallpaper on exit while preserving wallpaper changes made outside Kabe. Slideshow and Windows spotlight are unsupported. The **None** fit requires the same original wallpaper on every monitor.

## Install on Ubuntu GNOME

Download the `.deb` package from the release's **Assets**. In the download folder, run the following command with the downloaded filename.

```bash
sudo apt install ./Kabe-<version>-amd64.deb
```

Open Kabe from the app grid. A GNOME session with `gsettings` and D-Bus is required.

The release also includes an AppImage. Make it executable before running it. The AppImage requires FUSE 2 support, so use the `.deb` package if FUSE is unavailable.

## Update Kabe

Installed copies check this public release channel at startup. In Kabe Settings, use **Check now**, select **Download** for an available version, and select **Restart & install** when the download finishes. Debian package installation requests administrator authorization.

You can also download a newer installer from the [releases page](https://github.com/aaronwJordan/kabe-releases/releases) and install it over the existing version. Use the same package type. You do not need to uninstall first.

Each release includes `SHA256SUMS.txt` for download verification. The `.yml` and `.blockmap` assets support in-app updates. You do not need to open them yourself.

This repository contains public packages and update metadata. Kabe's source repository remains private.
