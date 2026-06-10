# SecurePassGenSaver

SecurePassGenSaver is an open-source C# Windows password generator with a compact dark utility-style interface. It generates passwords locally using `.NET RandomNumberGenerator`, supports custom password options, estimates entropy, saves entries as Markdown files, and includes installer support.

## Features

* Local password generation
* Uses `.NET RandomNumberGenerator`
* Dark Windows Forms UI
* Custom themed tab bar
* Floating password length indicator
* Password length selection from 8 to 32 characters
* Options for lowercase letters, uppercase letters, numbers, and special characters
* Option to avoid ambiguous characters such as `I`, `l`, `1`, `O`, and `0`
* Entropy and strength estimation
* Save passwords as Markdown files
* Choose a save folder or USB drive
* View saved password entries
* Copy, edit, and delete saved entries
* Optional 4-digit app PIN with hint
* Dark, light, and system theme options
* Accessibility text-to-speech option
* Installer support with desktop and Start Menu shortcuts

## Important Security Note

Saved password files are stored as readable Markdown plain text.

The optional 4-digit PIN only protects access to the app. It does **not** encrypt saved password files.

For real passwords and important accounts, use a trusted password manager and enable multi-factor authentication when possible.

## Requirements

To build or run the project from source, you need:

* Windows 10 or Windows 11
* .NET 8 SDK
* Visual Studio 2022 or Visual Studio Code

To build the installer, you also need:

* Inno Setup

## How to Run from Source

Clone or download this repository.

Open PowerShell or Terminal inside the project folder, where `SecurePassGenSaver.csproj` is located.

Run:

```powershell
dotnet run
```

The app should open normally.

## How to Build the EXE

Open PowerShell inside the project folder and run:

```powershell
dotnet publish -c Release -r win-x64 --self-contained false /p:PublishSingleFile=true
```

After building, the executable will be located in:

```text
bin\Release\net8.0-windows\win-x64\publish\
```

The main file will be:

```text
SecurePassGenSaver.exe
```

## How to Build the Installer

This project includes installer files.

First, build the published app by running:

```powershell
.\Scripts\build-publish.ps1
```

Then open this file in Inno Setup:

```text
Installer\SecurePassGenSaver.iss
```

Press:

```text
Compile
```

The final installer will be created in:

```text
InstallerOutput\
```

The installer will:

* Install SecurePassGenSaver into `C:\Program Files\SecurePassGenSaver`
* Create a desktop shortcut
* Create a Start Menu shortcut
* Make the app searchable from Windows Search
* Add an uninstall option in Windows settings

## How to Use

1. Open SecurePassGenSaver.
2. Go to the Generate tab.
3. Enter a save file name and username if needed.
4. Choose password length.
5. Select character options.
6. Click Generate.
7. Copy or save the password.
8. Saved entries can be managed from the Password List tab.
9. Saved Markdown files can be viewed from the Saved Files tab.

## Version History

### 1.0.0 — Console Prototype

Initial C# console password generator.

Features:

* Local password generation
* Character type options
* Password length selection
* Entropy estimation

### 1.1.0 — Windows UI Version

Added a Windows Forms graphical interface.

Features:

* Dark UI
* Password generation tab
* Password list tab
* Saved files tab
* Options and settings
* Markdown saving
* Optional app PIN
* Text-to-speech option

### 1.2.0 — Installer-Ready Release

Improved the app for release and installation.

Features:

* Installer support
* Program Files installation
* Desktop shortcut
* Start Menu shortcut
* Windows Search support
* Custom themed tab bar
* Floating password length indicator
* Improved dark theme consistency

## Project Purpose

This project was created as a beginner cybersecurity and programming portfolio project.

It demonstrates:

* C# programming
* Windows Forms UI design
* Password generation
* Random number generation
* Entropy estimation
* Local file storage
* Basic privacy awareness
* Installer setup for Windows apps

## Disclaimer

This project is for educational and portfolio purposes.

It is not a replacement for a professional password manager.

## License

This project is licensed under the MIT License.
