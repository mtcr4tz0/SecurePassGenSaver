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
