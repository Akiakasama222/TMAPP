# Assignment Board APK

## Option A: build in the cloud (no Android Studio)
1. Create a free GitHub repo and upload everything in this folder (keep the .github folder).
2. Open the repo's Actions tab, wait for "Build APK" to finish (about 5 minutes).
3. Open the finished run, download the "assignment-board-apk" artifact, unzip it.
4. Copy app-debug.apk to the Honor Pad and tap it. Allow "install unknown apps" when asked.

## Option B: build on your computer
Needs Node 20+, JDK 21 and Android Studio (for the SDK).
    npm install
    npx cap add android
    npx cap sync android
    cd android && ./gradlew assembleDebug
APK: android/app/build/outputs/apk/debug/app-debug.apk

## Backup and restore
Tap the gear (top-left), then "Export backup" to share a .json file (save it to Drive, Files, email...).
"Import backup" picks that file and replaces the current board. Do this before uninstalling or updating.
