# HirePilot Releases

Official Windows installer distribution for HirePilot.

This repository is intentionally binary-only. It contains versioned Windows
installers and checksum files used by HirePilot's assisted updater; private
source history, API keys, profiles, resumes, and generated application files
are never published here.

## Download

Use the [latest stable release](https://github.com/JuanPRG/hirepilot-releases/releases/latest)
and download the exact versioned installer named
`HirePilot-Setup-v<version>.exe`.

Closed-test installers are currently unsigned. Windows may therefore show a
SmartScreen or UAC warning. Do not install files obtained from mirrors or with
a different filename.

## Verify The Installer

Each release includes a matching `.exe.sha256` file. In PowerShell:

```powershell
Get-FileHash .\HirePilot-Setup-v2.2.0.exe -Algorithm SHA256
Get-Content .\HirePilot-Setup-v2.2.0.exe.sha256
```

The two SHA256 values must match. The HirePilot tray updater also verifies the
digest reported by GitHub before opening an installer.

## Updates

After the first manual installation, use **Check for Updates** from the
HirePilot tray menu. Updates are user-confirmed and preserve the current
user's `.hirepilot` configuration and files.

## Privacy And Support

Read the [HirePilot Privacy Policy](PRIVACY.md) before configuring a hosted AI
provider. For support, use
[GitHub Issues](https://github.com/JuanPRG/hirepilot-releases/issues) without
posting API keys, resume contents, or other sensitive personal information.
