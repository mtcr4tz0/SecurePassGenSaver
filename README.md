# SecurePassGenSaver

SecurePassGenSaver is an open-source C# Windows password generator with a compact utility-style interface. It can generate strong passwords locally, save entries securely, and protect saved files with PIN-based encryption.

## Download and Install

For normal users, the easiest way to install SecurePassGenSaver is through the **GitHub Releases** page.

### Recommended Installation

1. Open the repository on GitHub.
2. Go to the **Releases** section.
3. Download the latest setup file:

```text
SecurePassGenSaver-1.5.0-Setup.exe
```

4. Run the setup file.
5. Follow the installer steps.
6. After installation, open SecurePassGenSaver from:

   * Desktop shortcut
   * Start Menu
   * Windows Search

The installer places the app in:

```text
C:\Program Files\SecurePassGenSaver
```

It also supports desktop shortcuts, Start Menu shortcuts, Windows Search, and manual taskbar pinning.

## Portable Version

A portable EXE may also be included in the release assets:

```text
SecurePassGenSaver.exe
```

This version can be run without using the installer. However, the setup installer is recommended for most users because it creates shortcuts and installs the app properly.

## Main Features

* Local password generation
* Uses `.NET RandomNumberGenerator`
* Password length and character customization
* Entropy estimation
* Saved password list
* Copy, edit, and delete saved entries
* Custom save folder support
* Optional app PIN
* PIN-based encrypted `.spgs` files
* Dark and light theme support
* Custom application icon
* Windows installer support

## Security

When a PIN is enabled, saved `.spgs` files use PIN-based encryption.

SecurePassGenSaver 1.5.0 uses:

* PBKDF2-SHA256
* 250,000 iterations
* AES-GCM encryption
* Random salt per file
* Random nonce per file

This means deleting the app settings file does not unlock PIN-encrypted saved passwords.

Important: if you forget the PIN, PIN-encrypted saved passwords cannot be recovered. That is the tradeoff of real encryption.

## Build from Source

This repository also includes the open-source project files for developers who want to inspect, modify, or build the app themselves.

### Requirements

To build from source, install:

* Windows 10 or Windows 11
* .NET 8 SDK or newer
* Inno Setup

### Build the App and Installer

After cloning or downloading the source code, open the project folder and run:

```text
BUILD_SETUP.bat
```

This will build the app and create the installer.

The portable EXE will be created here:

```text
Publish\SecurePassGenSaver.exe
```

The setup installer will be created here:

```text
InstallerOutput\SecurePassGenSaver-1.5.0-Setup.exe
```

## Inno Setup

Inno Setup is required only if you want to build the installer from the source code.

You do not need Inno Setup if you only want to install the app from GitHub Releases.

Normal users should download:

```text
SecurePassGenSaver-1.5.0-Setup.exe
```

Developers who want to build the setup file themselves need Inno Setup installed.

## Project Purpose

SecurePassGenSaver was created as a cybersecurity and programming portfolio project.

It demonstrates:

* C# programming
* Windows Forms UI design
* Password generation
* Local encrypted storage
* PIN-based encryption
* Windows installer creation
* GitHub release management
* Open-source project structure

## Disclaimer

SecurePassGenSaver is an educational and portfolio project. For critical real-world accounts, a trusted professional password manager is still recommended.
# SecurePassGenSaver Version Downloads

| Version | Release Name | Recommended Download | Source Code ZIP | Main Change | Status |
|---|---|---|---|---|---|
| v1.5.0 | PIN-Based Encryption Release | `SecurePassGenSaver-1.5.0-Setup.exe` | `SecurePassGenSaver_1.5.0_PinBasedEncryption_Source.zip` | PIN is now used for file encryption with PBKDF2-SHA256 and AES-GCM | **Recommended / Current** |
| v1.4.2 | PIN Fix Release | `SecurePassGenSaver-1.4.2-Setup.exe` | `SecurePassGenSaver_1.4.2_PinFix_Source.zip` | Fixed Save PIN behavior so saving a PIN enables it properly | Old |
| v1.4.1 | Final UI Polish | `SecurePassGenSaver-1.4.1-Setup.exe` | `SecurePassGenSaver_1.4.1_FinalUIPolish_Source.zip` | Improved the Information/About tab layout and readability | Old |
| v1.4.0 | Portable OpenRGB-Style Release | `SecurePassGenSaver-1.4.0-Setup.exe` | `SecurePassGenSaver_1.4.0_Portable_OpenRGBStyle_Source.zip` | Added portable self-contained EXE and OpenRGB/Rufus-style UI polish | Old |
| v1.3.0 | Encrypted Storage Release | `SecurePassGenSaver-1.3.0-Setup.exe` | `SecurePassGenSaver_1.3.0_EncryptedStorage_ThemePolish_Source.zip` | Added Windows DPAPI encrypted `.spgs` storage | Old |
| v1.2.0 | Installer and Icon Release | `SecurePassGenSaver-1.2.0-Setup.exe` | `SecurePassGenSaver_Final_1.2.0_IconShortcutReady_Source.zip` | Added installer, icon, desktop shortcut, and Start Menu shortcut support | Old |
| v1.1.0 | Windows UI Release | No setup installer | `SecurePassGenSaver_DarkUI_Source.zip` | First Windows Forms GUI version | Archive |
| v1.0.0 | Console Prototype | No setup installer | `SecurePassGen_Source.zip` | First console password generator prototype | Archive |
