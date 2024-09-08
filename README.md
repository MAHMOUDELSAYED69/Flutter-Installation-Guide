# Flutter Installation Guide

This guide provides a step-by-step process to install Flutter on your system. Follow the instructions based on your operating system.

## Table of Contents

1. [System Requirements](#system-requirements)
2. [Install Flutter](#install-flutter)
   - [Windows](#windows)
   - [macOS](#macos)
3. [Set up IDE](#set-up-ide)
   - [Visual Studio Code](#visual-studio-code)
   - [Android Studio](#android-studio)
4. [Configure Flutter](#configure-flutter)
5. [Run Your First App](#run-your-first-app)

---

## System Requirements

Before you install Flutter, ensure your system meets the following requirements:

- **Operating System**: Windows 10 or later, macOS 10.14 or later, or a 64-bit Linux distribution.
- **Disk Space**: 2.8 GB (does not include disk space for IDE/tools).
- **Tools**: Git, bash (for macOS/Linux), PowerShell (for Windows).

---

## Install Flutter

### Windows

1. Download the Flutter SDK from the [Flutter Windows Installation](https://docs.flutter.dev/get-started/install/windows) page.

   ```bash
   https://storage.googleapis.com/flutter_infra_release/releases/stable/windows/flutter_windows_3.24.2-stable.zip
   ```
2. Extract the downloaded zip file to a desired location.

3. Update your environment variables:

- Open System Properties → Advanced → Environment Variables.
- Under User variables, select Path and click Edit.
- Add the `flutter/bin` directory to your system path.
  
4. Run the following command in your terminal to verify the installation:

```bash
flutter doctor
```
### macOS
1. Download the Flutter SDK from the Flutter macOS Installation page.
```bash
https://storage.googleapis.com/flutter_infra_release/releases/stable/macos/flutter_macos_3.24.2-stable.zip
```
2. Extract the zip file to a desired location.

3. Update your `PATH` environment variable by adding the following to your `.bashrc` or `.zshrc` file:
```bash
export PATH="$PATH:`pwd`/flutter/bin"
```
4. Run the following command to verify the installation:
```bash
flutter doctor
```
## Install Java JDK
### Windows
1. Visit the Oracle JDK download page (or the latest version).

2. Accept the license agreement and download the Windows installer.

3. Run the installer and follow the instructions to complete the installation.

4. Set the `JAVA_HOME` environment variable:

- Open System Properties → Advanced → Environment Variables.
- Under System variables, click New and add:
   - Variable name: JAVA_HOME
   - Variable value: `C:\Program Files\Java\jdk-<version>` (replace <version> with the actual version number).
5. Update the Path variable to include `%JAVA_HOME%\bin`.
### macOS
1. Visit the Oracle JDK download page (or the latest version).

2. Accept the license agreement and download the macOS installer.

3. Run the installer and follow the instructions to complete the installation.

4. Set the JAVA_HOME environment variable by adding the following line to your .bash_profile or .zshrc file:

```bash
export JAVA_HOME=$(/usr/libexec/java_home)
```
5. Run source ~/.bash_profile or source ~/.zshrc to apply the changes.
## Set up IDE
### Visual Studio Code
1. Install Visual Studio Code.
2. Open VS Code, go to Extensions, and install the Flutter and Dart extensions.
3. Open a terminal in VS Code and run

```bash
flutter doctor
```
### Android Studio
1. Download Android Studio.
2. Open Android Studio and install the Flutter and Dart plugins:
- Go to File > Settings > Plugins > Marketplace.
- Search for "Flutter" and "Dart" and install them.
3. Configure the Android SDK and set up an emulator or physical device to test your apps.
## Configure Flutter
After installing the SDK, run the following command to ensure everything is configured properly:
```bash
flutter doctor
```
It will show if there are any missing dependencies or tools required to complete the setup.

Example output:
```bash
Doctor summary (to see all details, run flutter doctor -v):
[✓] Flutter (Channel stable, 3.24.2, on macOS 12.6)
[✓] Android toolchain - develop for Android devices
[✓] Xcode - develop for iOS and macOS
[✓] Chrome - develop for the web
[✓] Android Studio (version 2022.1)
[✓] VS Code (version 1.80.0)
```
## Run Your First App
1. Create a new Flutter project:
```bash
flutter create my_first_app
```
2. Navigate into your project directory:

```bash
cd my_first_app
```
3. Run the app on an emulator or a connected device:

```bash
flutter run
```
## Conclusion
Congratulations! You have successfully installed Flutter and set up your development environment. You're now ready to start building beautiful and powerful applications across multiple platforms. Don't forget to explore the vast resources available in the Flutter community, and always keep learning and experimenting.

Happy coding! If you encounter any issues or have questions, feel free to reach out or check the Flutter community for support.
