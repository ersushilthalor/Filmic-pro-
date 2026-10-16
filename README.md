# Filmic Camera (Android)

Project publication repository for the Filmic Camera Android Studio project.

## Publication status

**Source project upload is incomplete.** This repository currently contains project documentation only; the full Android source tree and APK have not been published here yet. The complete source ZIP was generated separately in the ChatGPT conversation.

## Intended stack

- Kotlin and Jetpack Compose
- Android Camera2 API with capability discovery
- Camera2 preview and photo capture
- MediaRecorder video recording and MediaStore saving
- Capability-gated camera controls and a .cube LUT parsing core

## Build

Once the complete Android Studio source tree is uploaded, open it in Android Studio with internet access and Android SDK Platform 35 installed, then run:

```bash
./gradlew testDebugUnitTest assembleDebug
```

Expected debug APK path: `app/build/outputs/apk/debug/app-debug.apk`.

## Important limitations

The Android project has not been compiled or tested on a physical device. Advanced GPU LUT rendering, true LOG/HDR profiles, HDR+ / night stacking, zebra and focus-peaking overlays, and the full LUT management UI are not complete. Do not treat this repository as a release-ready app until source publication, CI build, and device testing are complete.