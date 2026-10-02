# 🩺 Health Connect Test Data Writer

A small Android developer tool for writing labeled synthetic step records to Health Connect. Use it to test apps that read step data through the Health Connect API.

> **Testing use** — Enter a step count, write records, then read today's aggregate to check how a test app handles Health Connect data.

---

## ✨ Features

- **Write Step Records** — Enter a step count and write it to Health Connect as time-bounded sessions across the current day
- **Labeled Test Records** — Every record uses a `hc-testdata-` client record ID prefix and `RECORDING_METHOD_MANUAL_ENTRY`
- **Read & Verify Steps** — Read today's aggregate step count in the app
- **Persistent Data Label** — The app displays **Synthetic test data** so the testing context stays visible
- **No Root Required** — Runs on a supported Android device with Health Connect

## 📥 Download APK

Download the debug build from the [v1.0.0 release](https://github.com/Heer12354/health-connect-test-data-writer/releases/tag/v1.0.0), or browse the [Releases page](https://github.com/Heer12354/health-connect-test-data-writer/releases).

## 🚀 Using the App

1. Install Health Connect on an Android 14 or newer device if it is not already available.
2. Install and open **Health Connect Test Data Writer**.
3. Grant the requested Health Connect read and write access for step records.
4. Enter a step count and tap **Write Steps to Health Connect**.
5. Tap **Read Today's Steps** to view the current day's aggregate.
6. Use the device's Health Connect settings to review or revoke the app's access.

## 🛠️ Requirements

- Android 14 or higher (API 34+)
- Health Connect available and set up on the device
- Health Connect read and write access for step records

## 🏗️ Building from Source

### Prerequisites

- JDK 17
- Android SDK Platform 35

### Build

```bash
./gradlew assembleDebug
```

The APK is generated at:

```text
app/build/outputs/apk/debug/app-debug.apk
```

## 📦 Tech Stack

- **Language**: Kotlin
- **UI**: Android XML Views
- **Health API**: [AndroidX Health Connect Client](https://developer.android.com/health-and-fitness/guides/health-connect)
- **Minimum Android version**: Android 14 (API 34)
- **Target SDK**: 35

## 📄 Permissions

The app requests the following Health Connect permissions:

- `android.permission.health.READ_STEPS`
- `android.permission.health.WRITE_STEPS`

Access is requested through Health Connect's permission flow and can be changed in Health Connect settings.

## ⚠️ Disclaimer

For testing on your own device only. Records created by the app are synthetic test data.

## 📜 License

This project is available under the [MIT License](LICENSE).
