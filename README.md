# Health Connect Test Data Writer

An Android developer utility for writing labeled synthetic step records to Health Connect and reading the current day's aggregated step total. Use it to exercise app integrations that consume Health Connect step data.

## What it does

- Accepts a step count and divides it among time-bounded sessions across the current day.
- Writes each session with a `hc-testdata-` client record ID prefix and the manual-entry recording method.
- Reads today's aggregate step count for verification.
- Keeps a visible **Synthetic test data** label in the app.

## Requirements

- Android 14 (API 34) or newer.
- Health Connect available and set up on the device.
- JDK 17 and Android SDK Platform 35 to build from source.

## Permissions

The app requests Health Connect access to read and write step records:

- `android.permission.health.READ_STEPS`
- `android.permission.health.WRITE_STEPS`

Grant these permissions in the Health Connect permission flow when prompted. You can revoke them from Health Connect settings.

## Build

```sh
./gradlew assembleDebug
```

The debug APK is generated at `app/build/outputs/apk/debug/app-debug.apk`.

## Disclaimer

For testing on your own device only. The records created by this app are synthetic test data.
