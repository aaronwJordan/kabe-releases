# Download Kabe

Kabe is a Wallhaven wallpaper manager for Windows 11 and Ubuntu GNOME.

Download an installer from the [latest release](https://github.com/aaronwJordan/kabe-releases/releases/latest), or browse [all releases](https://github.com/aaronwJordan/kabe-releases/releases). New releases are published automatically when Kabe changes, and installed copies update from Settings.

## Install on Windows 11

1. From the release's **Assets**, download `Kabe-Native-<version>-windows-x64-setup.exe`.
2. Run the installer. It installs Kabe for the current user.
3. Open Kabe from the Start menu.
4. In Windows **Settings → Personalization → Background**, select **Picture** or **Solid color** before you apply a wallpaper in Kabe. Kabe does not support Slideshow or Windows spotlight.
5. To start Kabe when you sign in, turn on **Launch at login** in Kabe Settings.

Windows 11 x64 is required. The installer is unsigned, so Windows SmartScreen can show an unknown-publisher warning. Download it only from this repository.

Each release also includes `Kabe-Native-<version>-windows-x64.exe`, a standalone executable that runs without installation. Keep `Kabe-Native-<version>-NOTICES.html` with it, because that file lists the licenses of the code Kabe includes. A standalone copy can check for updates, but Restart and install updates the installed copy.

Closing Kabe's window keeps it running in the tray. Choose **Quit Kabe** from the tray menu to exit. When Kabe exits or crashes, it restores the wallpaper it replaced and keeps wallpaper changes made outside Kabe.

## Install on Ubuntu GNOME

Ubuntu 24.04 or later on amd64 is required. Download `Kabe-Native-<version>-amd64.deb` from the release's **Assets**. In the download folder, run the following command with the downloaded filename.

```bash
sudo apt install ./Kabe-Native-<version>-amd64.deb
```

Open Kabe from the app grid. A GNOME session is required. The tray icon needs the AppIndicator extension, and the Wallhaven API key is stored in the GNOME keyring.

## Update Kabe

Open **Settings**, choose **Check for updates**, then choose **Download &lt;version&gt;**. When the download finishes, choose **Restart and install**. Kabe checks the package's SHA-256 digest before it installs, then starts again. On Ubuntu, GNOME asks for your password so apt can install the package.

You can also install a newer setup file or `.deb` over the existing version yourself. On Windows, quit Kabe from the tray first. Your profile, API key, and wallpaper library are kept.

## Verify a download

Each release includes `SHA256SUMS.txt`. Compare it with the checksum of the downloaded file. On Windows, run the following command in PowerShell.

```powershell
Get-FileHash .\Kabe-Native-<version>-windows-x64-setup.exe
```

On Ubuntu, run `sha256sum --check --ignore-missing SHA256SUMS.txt` in the download folder.

Releases 0.1.x are an earlier, retired version of Kabe. Current releases do not upgrade them or import their profiles.

This repository contains public packages. Kabe's source repository is private.
