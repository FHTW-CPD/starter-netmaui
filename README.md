# Cross-Platform Project Starter (.NET MAUI)

Welcome to the team project repository for the Cross-Platform Development course.

## Team Details
* **Student 1**: [Full Name] ([GitHub Handle])
* **Student 2**: [Full Name] ([GitHub Handle])
* **App Name**: [Your App Concept Name]

---

## Environment Setup Requirements

Before running the application, ensure your mobile development tools are configured.

### 1. Windows Setup
1. Install **Visual Studio 2026 Community** with the **.NET Multi-platform App UI development** workload.
2. Open Visual Studio $\rightarrow$ **Tools** $\rightarrow$ **Android** $\rightarrow$ **Android Device Manager** to create and start a virtual device (e.g., Pixel 6 with API 34).
3. Ensure `ANDROID_HOME` is set and `%ANDROID_HOME%\platform-tools` + `%ANDROID_HOME%\emulator` are added to your system `PATH`.

### 2. Mac Setup
1. Install **Xcode** from the Mac App Store (required for the iOS Simulator).
2. Install the **.NET SDK** and **Visual Studio Code** with the **.NET MAUI Extension**.

#### Managing Emulators via Terminal:
* **List installed emulators**:
  ```bash
  emulator -list-avds
  ```
* **Start an emulator from command line**:
  ```bash
  emulator -avd <YOUR_AVD_NAME>
  ```
  *(Example: `emulator -avd Pixel_6_API_34`)*

---

## How to Run the App

### Option A: Using Visual Studio 2026 (Recommended)
1. Open the `.sln` or `.csproj` file in Visual Studio 2026.
2. In the top toolbar, select your target device (e.g., **Android Emulator**, **Windows Machine**, or **iOS Simulator**).
3. Press **F5** (or click the green Play button) to build and launch the app.

### Option B: Using the Terminal / CLI
Ensure your Android Emulator or iOS Simulator is running *before* executing the build command!

* **Run on Android**:
  ```bash
  dotnet build -t:Run -f net8.0-android
  ```
* **Run on iOS (Mac only)**:
  ```bash
  dotnet build -t:Run -f net8.0-ios
  ```
* **Run on Windows Machine**:
  ```bash
  dotnet build -t:Run -f net8.0-windows10.0.19041.0
  ```

---

## Troubleshooting

* **Permission Denied / Build Locks (`bin` / `obj` errors)**
  * **Fix**: Close Visual Studio completely and run `dotnet clean` in your terminal to wipe temporary lock files.
* **`adb command not found` / Android SDK path missing**
  * **Fix**: Ensure your `ANDROID_HOME` environment variable is set correctly and points to your Android SDK location.
