# Download Kabe

Kabe is a Wallhaven wallpaper manager for Windows 11 and Ubuntu GNOME.

Download an installer from the [latest release](https://github.com/aaronwJordan/kabe-releases/releases/latest), or browse [all releases](https://github.com/aaronwJordan/kabe-releases/releases).

Kabe 0.2.0 and later is a native application. Releases 0.1.x are the earlier Electron version. Each section below names the files for both.

## Install on Windows 11

1. From the release's **Assets**, download the setup file:
   - 0.2.0 and later: `Kabe-Native-<version>-windows-x64-setup.exe`
   - 0.1.x: `Kabe-<version>-x64-setup.exe`
2. Run the installer. It installs Kabe for the current user.
3. Open Kabe from the Start menu.
4. In Windows **Settings → Personalization → Background**, select **Picture** or **Solid color** before you apply a wallpaper in Kabe. Kabe does not support Slideshow or Windows spotlight.
5. To start Kabe when you sign in, turn on **Launch at login** in Kabe Settings.

Windows 11 x64 is required. The installer is unsigned, so Windows SmartScreen can show an unknown-publisher warning. Download it only from this repository.

Native releases also include `Kabe-Native-<version>-windows-x64.exe`, a standalone executable that runs without installation. Keep `Kabe-Native-<version>-NOTICES.html` with it, because that file lists the licenses of the code Kabe includes.

Closing Kabe's window keeps it running in the tray. Choose **Quit Kabe** from the tray menu to exit. When Kabe exits or crashes, it restores the wallpaper it replaced and keeps wallpaper changes made outside Kabe.

## Install on Ubuntu GNOME

Native releases currently contain Windows files only. Ubuntu packages are available in the 0.1.x releases.

Download the `.deb` package from a 0.1.x release's **Assets**. In the download folder, run the following command with the downloaded filename.

```bash
sudo apt install ./Kabe-<version>-amd64.deb
```

Open Kabe from the app grid. A GNOME session with `gsettings` and D-Bus is required.

The 0.1.x releases also include an AppImage. Make it executable before you run it. The AppImage requires FUSE 2 support, so use the `.deb` package if FUSE is not available.

## Update Kabe

In Kabe 0.2.0 and later, open **Settings**, choose **Check for updates**, then choose **Download &lt;version&gt;**. When the download finishes, choose **Restart and install**. Kabe checks the installer's SHA-256 digest before it installs.

Kabe 0.1.x cannot update itself to a native release. To upgrade, quit Kabe from the tray, then download and run the native setup file. The installer keeps your profile and wallpaper library. You do not need to uninstall first.

You can also install any newer setup file over the existing version. Quit Kabe from the tray first.

## Verify a download

Each release includes `SHA256SUMS.txt`. Compare it with the checksum of the downloaded file. On Windows, run the following command in PowerShell.

```powershell
Get-FileHash .\Kabe-Native-<version>-windows-x64-setup.exe
```

The `.yml` and `.blockmap` files in 0.1.x releases support in-app updates for that version. You do not need to open them.

This repository contains public packages and update metadata. Kabe's source repository is private.
