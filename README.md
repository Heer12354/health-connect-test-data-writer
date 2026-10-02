# 🩺 Health Connect Test Data Writer

**A developer utility for testing apps that read step data from Health Connect.** This Android app writes labeled synthetic step records and lets you read today's aggregate step count from Health Connect.

> **TL;DR** — Open the app → grant Health Connect access → enter a step count → write the records → read today's total to verify your integration.

---

## 🧪 What is Health Connect Test Data Writer?

This app helps Android developers exercise Health Connect step-data integrations on a device they control. Enter a step count and the app writes time-bounded records across the current day. Records are marked with the manual-entry recording method and use client record IDs beginning with `hc-testdata-`.

The app keeps a **Synthetic test data** label visible in its interface so the test-data context is clear.

---

## ✨ Features

- **Step Record Writing** — Enter a step count and write it to Health Connect
- **Labeled Records** — Every record uses the `hc-testdata-` client record ID prefix and `RECORDING_METHOD_MANUAL_ENTRY`
- **Read & Verify Steps** — Read today's aggregate step count in the app
- **Time Handling** — Writes time-bounded sessions across the current day
- **No Root Required** — Runs on a supported Android device with Health Connect

## 📥 Download APK

[![GitHub Release](https://img.shields.io/github/v/release/Heer12354/health-connect-test-data-writer?style=for-the-badge&logo=android&color=3DDC84)](https://github.com/Heer12354/health-connect-test-data-writer/releases/latest)

👉 **[Download Latest APK](https://github.com/Heer12354/health-connect-test-data-writer/releases/latest/download/app-debug.apk)** (Android only)

Or browse all versions on the [Releases page](https://github.com/Heer12354/health-connect-test-data-writer/releases).

## 🚀 How to Use

1. Install **[Health Connect](https://play.google.com/store/apps/details?id=com.google.android.apps.healthdata)** if it is not already available on your device.
2. Install and open **Health Connect Test Data Writer**.
3. Grant read and write access to step records in the Health Connect permission flow.
4. Enter a step count and tap **Write Steps to Health Connect**.
5. Tap **Read Today's Steps** to check the current day's aggregate.
6. Review or revoke access at any time in Health Connect settings.

## 📱 App Interface

The app has a dark interface with a step-count input, write and read actions, status feedback, and a persistent **Synthetic test data** label.

## 🛠️ Requirements

- Android 14 or higher (API 34+)
- [Health Connect](https://developer.android.com/health-and-fitness/guides/health-connect) available and set up on the device
- Health Connect read and write permissions for step records

## 💡 Developer Use Cases

- Testing apps that read step data from Health Connect
- Verifying Health Connect permission and data-reading flows
- Debugging AndroidX Health Connect API integrations

## 🏗️ Building from Source

### Prerequisites

- JDK 17
- Android SDK Platform 35

### Build

```bash
./gradlew assembleDebug
```

The APK will be generated at:

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

Permissions are granted through Health Connect and can be reviewed or revoked in its settings.

## ⚠️ Disclaimer

For testing on your own device only. Records created by this app are synthetic test data.

## 📜 License

This project is available under the [MIT License](LICENSE).
