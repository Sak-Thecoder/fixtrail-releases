# FixTrail

**Understand your device. Extend its life.**

FixTrail is a free desktop app that shows how healthy your computer is. It reads your processor, memory, storage, battery, temperatures and network directly from the hardware. It runs diagnostic scans that explain what it finds, and it keeps a history so you can see how your device changes over time.

It works completely offline. You don't need an account, and nothing leaves your computer unless you set up sync yourself.

> **FixTrail 0.1.1 is a beta.** It has been tested on Linux, Windows and an Apple Silicon Mac. Please try it and tell us what works and what doesn't in [Issues](../../issues).

**[⬇ Download FixTrail](#download)**

---

## Contents

- [What FixTrail does](#what-fixtrail-does)
- [Download](#download)
- [Install](#install)
- [What FixTrail can read on each system](#what-fixtrail-can-read-on-each-system)
- [Where your data is stored](#where-your-data-is-stored)
- [Uninstall](#uninstall)
- [Check your download](#check-your-download)
- [Privacy](#privacy)
- [Troubleshooting](#troubleshooting)
- [Known limitations](#known-limitations)
- [Reporting problems](#reporting-problems)

---

## What FixTrail does

| Screen | What you get |
| --- | --- |
| **Overview** | Your device's health at a glance: the last scan result, warnings, and live CPU, memory, battery and temperature readings. |
| **Components** | One page per part (processor, memory, storage, battery, graphics, network) with specifications, current readings and a history chart. |
| **Diagnostics** | **Quick Scan** checks your hardware in a few seconds and is completely read-only. **Full Scan** also asks your disks for their SMART health status (Linux). Neither scan runs a disk self-test or changes any settings. |
| **History** | Every past scan and its results, filterable by outcome. |
| **Device Passport** | A lifecycle record for your computer: specifications, warranty and repair or maintenance notes you add yourself. Exportable. |
| **Reports** | A full diagnostic report (device summary, hardware inventory, findings and timestamps) that you can save as a PDF. |
| **Settings** | Light, dark or system theme, how often readings refresh, how long history is kept, export or delete your history, and optional sync. |

---

## Download

Click a file name to download it.

| Your computer | Download | Requirements |
| --- | --- | --- |
| **Mac with Apple chip** (M1, M2, M3, M4 and later) | [**`FixTrail_0.1.1_aarch64.dmg`**](https://github.com/Sak-Thecoder/fixtrail-releases/releases/latest/download/FixTrail_0.1.1_aarch64.dmg) | macOS 11 Big Sur or later |
| **Mac with Intel chip** | [**`FixTrail_0.1.1_x64.dmg`**](https://github.com/Sak-Thecoder/fixtrail-releases/releases/latest/download/FixTrail_0.1.1_x64.dmg) | macOS 11 Big Sur or later |
| **Windows PC** (recommended) | [**`FixTrail_0.1.1_x64-setup.exe`**](https://github.com/Sak-Thecoder/fixtrail-releases/releases/latest/download/FixTrail_0.1.1_x64-setup.exe) | Windows 10 or 11, 64-bit (x64) |
| **Windows PC** (MSI package, for IT-managed PCs) | [**`FixTrail_0.1.1_x64_en-US.msi`**](https://github.com/Sak-Thecoder/fixtrail-releases/releases/latest/download/FixTrail_0.1.1_x64_en-US.msi) | Windows 10 or 11, 64-bit (x64) |
| **Ubuntu, Debian, Linux Mint, Pop!_OS** | [**`FixTrail_0.1.1_amd64.deb`**](https://github.com/Sak-Thecoder/fixtrail-releases/releases/latest/download/FixTrail_0.1.1_amd64.deb) | 64-bit (x86_64) |
| **Fedora, openSUSE** | [**`FixTrail-0.1.1-1.x86_64.rpm`**](https://github.com/Sak-Thecoder/fixtrail-releases/releases/latest/download/FixTrail-0.1.1-1.x86_64.rpm) | 64-bit (x86_64) |
| **Arch Linux, Manjaro, EndeavourOS** | [**`fixtrail-0.1.1-1-x86_64.pkg.tar.zst`**](https://github.com/Sak-Thecoder/fixtrail-releases/releases/latest/download/fixtrail-0.1.1-1-x86_64.pkg.tar.zst) | 64-bit (x86_64) |
| **Any other Linux** | [**`FixTrail_0.1.1_amd64.AppImage`**](https://github.com/Sak-Thecoder/fixtrail-releases/releases/latest/download/FixTrail_0.1.1_amd64.AppImage) | 64-bit (x86_64) |
| Checksums for all files | [`SHA256SUMS`](https://github.com/Sak-Thecoder/fixtrail-releases/releases/latest/download/SHA256SUMS) | See [Check your download](#check-your-download) |

Windows on ARM isn't supported yet. All versions and release notes are on the [releases page](../../releases).

**Not sure which Mac you have?** Click the Apple menu → **About This Mac**. If it says "Chip: Apple M…", use the Apple chip file. If it says "Processor: Intel", use the Intel file.

**Linux requirements:** glibc 2.34 or newer, GTK 3 and WebKitGTK 4.1. Ubuntu 22.04 and later, Fedora and current Arch already meet these. The `.deb`, `.rpm` and Arch packages install the missing libraries for you.

---

## Install

The beta builds aren't signed with an Apple or Microsoft developer certificate yet. Your system will warn you the first time you open FixTrail. This is expected for beta software from an independent developer. Only open files downloaded from this repository's [releases page](../../releases).

### macOS

1. Double-click the `.dmg` file you downloaded.
2. Drag **FixTrail** onto the **Applications** folder in the window that opens.
3. Open **Applications** and double-click **FixTrail**.
4. macOS says it can't verify that FixTrail is free of malware. Click **Done** (or **OK**).
5. Open **System Settings → Privacy & Security**. Scroll down to the message about FixTrail and click **Open Anyway**.
6. Click **Open Anyway** again and enter your Mac password if asked.

You only need to do this once. After that, FixTrail opens normally. You don't need to turn off Gatekeeper or change any other security settings.

**Optional:** to show your Wi-Fi network name, open the Network component and click **Allow Wi-Fi name access**. macOS asks for Location Services permission because it treats Wi-Fi names as location data. FixTrail never reads your actual location.

### Windows

1. Double-click `FixTrail_0.1.1_x64-setup.exe`.
2. If you see **"Windows protected your PC"**, click **More info**, then **Run anyway**.
3. Follow the installer. It installs for your user account only, so you don't need administrator rights.
4. Open FixTrail from the Start menu.

Don't turn off SmartScreen or Microsoft Defender to install FixTrail.

FixTrail uses Microsoft Edge WebView2, which is built into Windows 11 and most up-to-date Windows 10 PCs. If it's missing, the installer downloads it automatically, so stay connected to the internet during installation.

Use the `.msi` instead if you manage several PCs or your organization deploys software with MSI packages.

### Linux

Open a terminal in the folder where you saved the file and run the command for your distribution:

```bash
# Ubuntu, Debian, Linux Mint, Pop!_OS
sudo apt install ./FixTrail_0.1.1_amd64.deb

# Fedora, openSUSE
sudo dnf install ./FixTrail-0.1.1-1.x86_64.rpm

# Arch Linux, Manjaro, EndeavourOS
sudo pacman -U fixtrail-0.1.1-1-x86_64.pkg.tar.zst

# Any distribution (no install needed)
chmod +x FixTrail_0.1.1_amd64.AppImage
./FixTrail_0.1.1_amd64.AppImage
```

Then open **FixTrail** from your applications menu. The `.rpm` isn't GPG-signed, so `dnf` mentions that it skipped OpenPGP checks. That's expected for this beta.

**Optional tools** that unlock more readings. FixTrail works without them and never installs them for you:

| Tool | Package | Adds |
| --- | --- | --- |
| `smartctl` | `smartmontools` | Disk health (SMART) during Full Scan |
| `nvidia-smi` | NVIDIA driver | NVIDIA graphics usage |
| `iw` or `nmcli` | `iw` or `NetworkManager` | Wi-Fi network name |
| `pci.ids` | `hwdata` | Readable graphics card names |

---

## What FixTrail can read on each system

FixTrail only shows a reading when your system actually provides it. If a value isn't available, it says so instead of guessing.

| Reading | Linux | Windows | macOS |
| --- | :---: | :---: | :---: |
| Operating system, version, uptime | ✅ | ✅ | ✅ |
| Processor model, cores, usage | ✅ | ✅ | ✅ |
| Memory use | ✅ | ✅ | ✅ |
| Storage space per drive | ✅ | ✅ | ✅ |
| Disk read and write speed | ✅ | ✅ | ✅ |
| Network upload and download speed | ✅ | ✅ | ✅ |
| Battery charge, health and cycle count | ✅ | ✅ | ✅ |
| Charger connected and charging status | ✅ | ✅ | ✅ live updates |
| CPU temperature | ✅ Intel and AMD | ⚠️ only when the PC's firmware reports it (works on many ASUS laptops) | ✅ |
| Graphics card name | ✅ | ✅ | ✅ |
| Graphics temperature | ⚠️ when the driver reports it | ⚠️ when the driver reports it | ⚠️ confirmed on M1 and M2 |
| Graphics usage | ⚠️ NVIDIA with `nvidia-smi` | ❌ | ❌ |
| Disk health (SMART) | ⚠️ with `smartctl` | ❌ | ❌ |
| Computer manufacturer and model | ✅ | ❌ | ❌ |
| Wi-Fi network name | ⚠️ with `iw` or `nmcli` | ❌ | ⚠️ after you allow it |

✅ supported · ⚠️ depends on your hardware or an optional tool · ❌ not available yet

---

## Where your data is stored

All your history stays in one database file on your computer:

| System | Folder |
| --- | --- |
| macOS | `~/Library/Application Support/org.fixtrail.desktop` |
| Windows | `%APPDATA%\org.fixtrail.desktop` |
| Linux | `~/.local/share/org.fixtrail.desktop` |

You can export your history as a JSON file or delete it from **Settings** at any time. The **Local data retention** setting controls how long old scans are kept.

---

## Uninstall

| System | How |
| --- | --- |
| macOS | Quit FixTrail, then drag it from **Applications** to the Trash. |
| Windows | **Settings → Apps → Installed apps**, find **FixTrail**, click **⋯ → Uninstall**. |
| Ubuntu, Debian | `sudo apt remove fix-trail` |
| Fedora | `sudo dnf remove fix-trail` |
| Arch | `sudo pacman -R fixtrail` |
| AppImage | Delete the `.AppImage` file. |

Uninstalling keeps your history so a reinstall picks up where you left off. To remove it too, delete the folder listed in [Where your data is stored](#where-your-data-is-stored).

---

## Check your download

Each release includes a `SHA256SUMS` file with a fingerprint for every installer. Checking it confirms your download is complete and hasn't been changed. Run the command for your system, then compare the result with the matching line in `SHA256SUMS`:

```bash
# macOS
shasum -a 256 FixTrail_0.1.1_aarch64.dmg

# Linux (checks every file in the folder at once)
sha256sum -c SHA256SUMS --ignore-missing
```

```powershell
# Windows PowerShell
Get-FileHash .\FixTrail_0.1.1_x64-setup.exe
```

---

## Privacy

- **Offline by default.** No account, no ads, no analytics, no tracking.
- **No connection unless you ask.** While sync is off, which is the default, FixTrail doesn't open any network connection.
- **Sync is optional.** To use it, you run your own server, enter its address in Settings, and sign in. Nothing is sent before that.
- **Never uploaded, even with sync on:** your serial number, MAC addresses, Wi-Fi name, files, passwords, private keys and system logs.
- **Your serial number isn't saved.** It's shown on screen only, and exports leave it out unless you turn on "Include serial in exports".
- **Read-only.** Scans never change your hardware, firmware or settings, and FixTrail never asks for administrator access to monitor your device.

---

## Troubleshooting

**macOS says FixTrail "can't be opened" and there's no Open Anyway button.**
Try opening FixTrail once first (step 3 of the macOS install). The **Open Anyway** button only appears in Privacy & Security for about an hour after a blocked attempt.

**Windows says "Windows protected your PC" and there's no Run anyway button.**
Click the small **More info** link first. If your PC is managed by work or school, the administrator may block unsigned apps.

**Linux: the window is blank or doesn't open.**
Make sure WebKitGTK 4.1 is installed (`libwebkit2gtk-4.1-0` on Ubuntu and Debian, `webkit2gtk4.1` on Fedora, `webkit2gtk-4.1` on Arch). On some systems with NVIDIA graphics, starting FixTrail with `WEBKIT_DISABLE_DMABUF_RENDERER=1 fixtrail` helps.

**Linux: the `.deb` or `.rpm` refuses to install because of glibc.**
Your distribution is older than Ubuntu 22.04. Use a newer release, or try the AppImage.

**Temperatures show as unavailable.**
Your system doesn't report a sensor that FixTrail can read. This is common on Windows desktops and some laptops. Everything else still works.

**CPU temperature is unavailable inside a virtual machine (VMware, VirtualBox, Hyper-V, QEMU/KVM).**
This is expected. Virtual machines don't give the guest system access to the processor's temperature sensor, so there's no reading for any app to show (`sensors` reports "No sensors found!" too). FixTrail detects the virtual machine and explains this in the CPU temperature check. Run FixTrail on the host computer to see the real temperature.

**Disk health shows as unavailable.**
SMART data is currently Linux-only and needs `smartctl` (from `smartmontools`). Run a **Full Scan** after installing it.

**Readings look out of date.**
FixTrail refreshes on the interval set in **Settings → Monitoring interval** (5 to 60 seconds), and again whenever you switch back to its window.

---

## Known limitations

This is the first beta, so some things aren't finished yet:

- Installers aren't signed with Apple or Microsoft developer certificates, so first launch shows a warning.
- There are no automatic updates. Check this page for new versions.
- Intel Macs have only been tested in a virtual environment, not on real hardware.
- CPU temperature isn't available inside virtual machines, because they don't expose the processor's sensor.
- Disk health (SMART) and computer model detection are Linux-only for now.
- Graphics usage isn't available on Windows or macOS.
- Linux packages are for 64-bit Intel and AMD (x86_64) only. There's no ARM or Flatpak build yet.

---

## Reporting problems

Your feedback makes FixTrail better. [Open an issue](../../issues/new) and include:

1. **Your system**: operating system and version (for example "macOS 15.2" or "Windows 11 23H2"), and your computer model.
2. **Which file** you installed (for example `FixTrail_0.1.1_aarch64.dmg`).
3. **What happened**, and what you expected to happen.
4. **A screenshot**, if it helps.

Please don't include serial numbers, passwords or personal files.

---

## License

FixTrail is released under the MIT License. See [LICENSE](LICENSE).
