# FixTrail

Understand your device. Extend its life.

FixTrail is an offline desktop app that shows your computer's health: CPU, memory, storage, battery, temperatures and network. It runs quick and full diagnostic scans and keeps a local history of your device. No account is needed and nothing leaves your computer unless you turn on sync yourself.

This repository only hosts the installers. **FixTrail 0.1.0 is a beta.** Please try it and report what works and what doesn't in [Issues](../../issues).

## Download

Get the file for your system from the [latest release](../../releases/latest).

| System | File |
| --- | --- |
| macOS, Apple Silicon (M1 and later) | `FixTrail_0.1.0_aarch64.dmg` |
| macOS, Intel | `FixTrail_0.1.0_x64.dmg` |
| Windows 10/11, 64-bit | `FixTrail_0.1.0_x64-setup.exe` (or the `.msi`) |
| Ubuntu, Debian, Linux Mint | `FixTrail_0.1.0_amd64.deb` |
| Fedora, openSUSE | `FixTrail-0.1.0-1.x86_64.rpm` |
| Arch Linux | `fixtrail-0.1.0-1-x86_64.pkg.tar.zst` |
| Other Linux | `FixTrail_0.1.0_amd64.AppImage` |

Linux packages need an x86_64 system with glibc 2.34 or newer, GTK 3 and WebKitGTK 4.1. Tested on Ubuntu 22.04 and 24.04, Fedora 44 and Arch Linux.

## Install

The beta builds are not signed with an Apple or Microsoft developer certificate yet, so your system will warn you the first time. Only open files downloaded from this repository's releases.

### macOS

1. Open the `.dmg` and drag FixTrail into Applications.
2. Open FixTrail. macOS will say it can't verify the developer. Click **Done**.
3. Open **System Settings → Privacy & Security**, scroll down to the FixTrail message and click **Open Anyway**, then confirm.

You only need to do this once. You don't need to turn off Gatekeeper.

### Windows

1. Run `FixTrail_0.1.0_x64-setup.exe`.
2. If SmartScreen says "Windows protected your PC", click **More info**, then **Run anyway**.

Don't turn off SmartScreen or Defender.

### Linux

```bash
sudo apt install ./FixTrail_0.1.0_amd64.deb            # Ubuntu, Debian
sudo dnf install ./FixTrail-0.1.0-1.x86_64.rpm         # Fedora
sudo pacman -U fixtrail-0.1.0-1-x86_64.pkg.tar.zst     # Arch
chmod +x FixTrail_0.1.0_amd64.AppImage && ./FixTrail_0.1.0_amd64.AppImage   # any distro
```

Disk health (SMART) data appears when `smartctl` is installed.

## Check your download

Each release includes a `SHA256SUMS` file. Compare it with:

```bash
shasum -a 256 FixTrail_0.1.0_aarch64.dmg          # macOS
sha256sum FixTrail_0.1.0_amd64.deb                 # Linux
```

```powershell
Get-FileHash .\FixTrail_0.1.0_x64-setup.exe        # Windows PowerShell
```

## Privacy

- Works offline. No account, no analytics.
- Sync is off until you turn it on in Settings and point it at a server.
- Your device serial number, MAC addresses, files and passwords are never uploaded.
- History stays on your computer and can be exported or deleted in Settings.

## Reporting problems

Open an [issue](../../issues) with your operating system and version, your computer model, and what you saw. A screenshot helps. Please don't include serial numbers or personal files.

## License

MIT. See [LICENSE](LICENSE).
