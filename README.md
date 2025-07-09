![cover](https://github.com/user-attachments/assets/98851f94-1600-4187-b167-5bb4412c572a)

# Flutter Installation Guide (Windows)

This guide provides a step-by-step process to install Flutter on your Windows system, set up Android Studio, create an Android emulator, and run your first Flutter app. Follow the instructions below in the specified sequence.

---

## Table of Contents

1. [System Requirements](#system-requirements)
2. [Install Flutter](#install-flutter)
3. [Install Java JDK](#install-java-jdk)
4. [Configure Java](#configure-java)
5. [Install Android Studio](#install-android-studio)
6. [Set Up Android Emulator](#set-up-android-emulator)
7. [Set up IDE (Optional)](#set-up-ide-optional)
   - [Visual Studio Code](#visual-studio-code)
   - [Configure Android Emulator in VS Code](#configure-android-emulator-in-vs-code)
8. [Final Configuration Check](#final-configuration-check)
9. [Run Your First App](#run-your-first-app)
10. [Additional Resources](#additional-resources)
11. [Troubleshooting Installation Issues](#troubleshooting-installation-issues)

---

## System Requirements

Before you install Flutter, ensure your system meets the following requirements:

- **Operating System**: Windows 10 or later.
- **Disk Space**: `2.8 GB` (does not include disk space for IDE/tools).
- **Tools**: `Git` and `PowerShell`.

---

## Install Flutter

1. **Download the Flutter SDK**:
   - Visit the [Flutter SDK download page](https://docs.flutter.dev/get-started/install/windows) and download the latest stable release for Windows.
   - Direct download link (latest stable version):
     ```bash
     https://storage.googleapis.com/flutter_infra_release/releases/stable/windows/flutter_windows_3.32.4-stable.zip
     ```

2. **Extract the Flutter SDK**:
   - Extract the downloaded zip file to a desired location (e.g., `C:\src\flutter`).

3. **Update Environment Variables**:
   - Open **System Properties** → **Advanced** → **Environment Variables**.
   - Under **User variables**, select `Path` and click **Edit**.
   - Add the `flutter\bin` directory to your system path (e.g., `C:\src\flutter\bin`).

4. **Verify Installation**:
   - Open a new terminal (Command Prompt or PowerShell) and run:
     ```bash
     flutter doctor
     ```
   - This command checks your environment and displays a report of the status of your Flutter installation.

---

## Install Java JDK

1. **Download the Java JDK**:
   - Visit the [Oracle JDK download page](https://www.oracle.com/java/technologies/downloads/#java17-windows) for Java 17 (or the latest version).
   - Direct download link (latest stable version):
     ```bash
     https://download.oracle.com/java/17/archive/jdk-17.0.12_windows-x64_bin.exe
     ```
   - Accept the license agreement and download the Windows installer.

2. **Install the JDK**:
   - Run the installer and follow the instructions to complete the installation.

---

## Configure Java

1. **Set the `JAVA_HOME` Environment Variable**:
   - Open **System Properties** → **Advanced** → **Environment Variables**.
   - Under **System variables**, click **New** and add:
     - Variable name: `JAVA_HOME`
     - Variable value: `C:\Program Files\Java\jdk-17` (replace `17` with the actual version number if different).

2. **Update the `Path` Variable**:
   - In the **System variables** section, find the `Path` variable and click **Edit**.
   - Click **New** and add the following entry:
     ```
     %JAVA_HOME%\bin
     ```
   - Click **OK** to save the changes.

3. **Verify Java Installation**:
   - Open a new Command Prompt or PowerShell window.
   - Run the following command to verify Java is correctly configured:
     ```bash
     java -version
     ```
   - You should see the installed Java version displayed.

---

## Install Android Studio

1. **Download Android Studio**:
   - Visit the [Android Studio download page](https://developer.android.com/studio) and download the latest version for Windows.

2. **Install Android Studio**:
   - Run the downloaded installer and follow the installation wizard.
   - During installation, ensure the following components are selected:
     - Android SDK
     - Android SDK Platform
     - Android Virtual Device (AVD)

3. **Launch Android Studio**:
   - After installation, launch Android Studio and complete the setup wizard to install the latest SDK tools.

---

## Set Up Android Emulator

1. **Open AVD Manager**:
   - In Android Studio, go to **Tools** > **Device Manager**.

2. **Create a New Virtual Device**:
   - Click **Create Device**.
   - Select a device definition (e.g., `Pixel 6 pro`) and click **Next**.

3. **Select System Image**:
   - Choose a system image with **Android 14 (API Level 35)**.
   - If the image is not installed, click the **Download** link next to the release name and follow the prompts to install it.

4. **Configure AVD**:
   - After selecting the system image, click **Next**.
   - Configure the AVD settings (e.g., RAM, storage) and click **Finish**.

5. **Launch the Emulator**:
   - In the Device Manager, select the newly created AVD and click **Start**.

---

## Set up IDE (Optional)

### **Visual Studio Code**

1. **Install Visual Studio Code**:
   - Download and install [Visual Studio Code](https://code.visualstudio.com/).

2. **Install Flutter and Dart Extensions**:
   - Open VS Code, go to the **Extensions** view (`Ctrl+Shift+X`), and search for "Flutter" and "Dart".
   - Install both extensions.

3. **Verify Setup**:
   - Open a terminal in VS Code and run:
     ```bash
     flutter doctor
     ```

---

## Configure Android Emulator in VS Code

1. **Install Android Emulator Extension**:
   - Open VS Code, go to the **Extensions** view (`Ctrl+Shift+X`), and search for "Android Emulator".
   - Install the extension.

2. **Set Emulator Path**:
   - Open VS Code settings (`Ctrl+,`).
   - Search for "emulator path".
   - Add the following path to the emulator settings:
     ```
     C:\Users\<YourUsername>\AppData\Local\Android\Sdk\emulator
     ```
     Replace `<YourUsername>` with your actual Windows username.

3. **Launch Emulator**:
   - Open the Command Palette (`Ctrl+Shift+P`) and search for "Android Emulator: Start".
   - Select the emulator you want to launch.

---

## Final Configuration Check

After completing the installation and setup, it’s important to verify that everything is configured correctly. Use the following command to check your Flutter environment:

```bash
flutter doctor
```

This command scans your system and identifies any missing dependencies or tools required for Flutter development. It provides a summary of your setup and highlights any issues that need to be resolved.

### Example Output:
```
Doctor summary (to see all details, run flutter doctor -v):
[✓] Flutter (Channel stable, 3.27.3, on Windows 11)
[✓] Android toolchain - develop for Android devices
[✓] Chrome - develop for the web
[✓] Android Studio (version 2022.1)
[✓] VS Code (version 1.80.0)
```

### What to Look For:
- **Green checkmarks (✓)**: Indicate that the component is properly installed and configured.
- **Red crosses (✗)**: Highlight missing dependencies or tools that need to be addressed.

If any issues are reported, follow the suggestions provided by `flutter doctor` to resolve them. Once all checks pass, your Flutter environment is ready for development!

---

## Run Your First App

1. **Create a New Flutter Project**: 
   - Open a terminal and run:
     ```bash
     flutter create my_first_app
     ```

2. **Navigate to Your Project Directory**:
   - Run:
     ```bash
     cd my_first_app
     ```

3. **Run the App**:
   - Start the Android emulator or connect a physical device.
   - Run the app using:
     ```bash
     flutter run
     ```

---

## Additional Resources
``visit the official:``
- [Dart website](https://dart.dev/guides).
- [Flutter website](https://docs.flutter.dev/get-started/install).
- [Oracle website](https://www.oracle.com/java/).

Happy learning! 🚀

---

## Troubleshooting Installation Issues

Stuck with an error? Don’t worry even superheroes trip over their capes sometimes! Installation hiccups are normal, and we’ve all been there. Here’s how to tackle common issues and keep your spirits high:

### Common Fixes:
1. **Restart Your Terminal/IDE**:  
   Sometimes a simple restart works wonders. Think of it as a “turn it off and on again” for your sanity.

2. **Check Environment Variables**:  
   Ensure `JAVA_HOME`, and Flutter’s `bin` directory are correctly added to your system `Path`.

3. **Update Flutter**:  
   Run `flutter upgrade` to ensure you’re using the latest version. Bugs love outdated software!

4. **Check Dependencies**:  
   Run `flutter doctor -v` for detailed diagnostics. It’s like asking a doctor for a second opinion (but for code).

---

### Still Stuck? Contact Us!
<img src="https://github.com/user-attachments/assets/de21f4b6-6707-44f6-9f03-1effecb0910e" width="20%" />

If you’re still facing issues, we’re here to help! Reach out to us through the form below, and we’ll get back to you as soon as possible:  
👉 **[Contact Us Form](https://forms.gle/SGBfMHqyVdxJGDbg7)**  

Remember: Every error is a step closer to mastery. You’ve got this!

--- 
