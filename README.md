# HirePilot Releases

Official Windows companion distribution for HirePilot.

HirePilot has two separately updated components:

1. The HirePilot Chrome extension, installed through the Chrome Web Store.
2. The Windows companion published here, which provides local setup, document
   generation, tray controls, updates, and the `hirepilot://start` launcher.

The public installer does not bundle or sideload a Chrome extension. The
official Chrome Web Store listing link will be added here after Google assigns
the public item URL.

This repository is intentionally binary-only. It never contains private source
history, API keys, profiles, resumes, generated application files, or the
private closed-test extension bundle.

## Download The Windows Companion

Use the [latest stable release](https://github.com/JuanPRG/hirepilot-releases/releases/latest)
and download the exact installer named `HirePilot-Setup-v<version>.exe`.

Public release assets never use `Closed-Test` or `Validation` in their
filenames. The free-project installer is currently unsigned, so Windows may
show SmartScreen and UAC warnings. Do not install copies obtained from mirrors.

After installation, run **HirePilot Setup Console** once from the Start Menu.
The Chrome extension can then start the companion when needed.

## Verify The Installer

Each release includes a matching `.exe.sha256` file. For example:

```powershell
$version = "2.2.2"
Get-FileHash ".\HirePilot-Setup-v$version.exe" -Algorithm SHA256
Get-Content ".\HirePilot-Setup-v$version.exe.sha256"
```

The two SHA256 values must match. The HirePilot tray updater also verifies the
GitHub asset digest before opening an installer.

## Updates

Chrome updates the extension through the Chrome Web Store. Use **Check for
Updates** from the HirePilot tray menu to update the Windows companion.
Companion updates are user-confirmed and preserve `.hirepilot` configuration,
profiles, source resumes, preferences, logs, and existing Downloads.

## Privacy And Support

Read the [HirePilot Privacy Policy](PRIVACY.md) before configuring a hosted AI
provider. For support, use
[GitHub Issues](https://github.com/JuanPRG/hirepilot-releases/issues) without
posting API keys, resume contents, or other sensitive personal information.
