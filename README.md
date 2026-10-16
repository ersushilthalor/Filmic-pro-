# Filmic Camera (Android)

A Kotlin + Jetpack Compose Android camera project built around the Android Camera2 API.

## Project status

This repository is the publication home for the Filmic Camera source project. The current implementation is an early development baseline, **not a release-ready camera app**. It has not been built with Android Gradle Plugin or validated on a physical device yet.

## Included architecture

- Camera2 camera inventory and capability inspection
- Camera2 preview/capture engine
- Photo capture and MediaStore integration
- Video recording path using MediaRecorder
- Device-capability-gated camera controls
- Cube LUT parsing/interpolation core and unit test
- GitHub Actions workflow for Android debug builds

## Known limitations

The advanced GPU LUT rendering pipeline, full cinema color management, real LOG/HDR profile support, HDR+ / night stacking, zebra and focus-peaking overlays, and full LUT management UI are not complete. Unsupported hardware features must remain unavailable rather than being simulated.

## Build

Open the project in Android Studio with internet access and Android SDK Platform 35 installed, then run:

```bash
./gradlew testDebugUnitTest assembleDebug
```

The expected APK path is `app/build/outputs/apk/debug/app-debug.apk`.

**Build status:** not yet verified. Do not treat this repository as a tested release until CI passes and the app is exercised on target hardware.

See [FEATURE_MATRIX.md](FEATURE_MATRIX.md) for implementation status and outstanding work.