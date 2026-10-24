ORBIT TV LAUNCHER - build online (no Android Studio needed)

1. Make a free account at github.com and create a new repository (any name, public or private).
2. Upload every file and folder from this zip into the repository (Add file > Upload files).
   Make sure the hidden ".github" folder is included, because it holds the build recipe.
3. Open the Actions tab. "Build APK" starts on its own, or press Run workflow. It takes a few minutes.
4. Open the finished run, download "OrbitTV-apk" at the bottom, and unzip it to get app-debug.apk.
5. Put the APK on the TV: use the Downloader app with a link, a USB stick, or ADB.
   ADB: adb connect TV_IP:5555   then   adb install app-debug.apk
6. Open "Orbit TV" from your Apps row to try it first.
7. To make it the home screen (optional, may be blocked on some TVs):
   adb shell cmd package set-home-activity com.orbit.tv/.MainActivity
8. To go back to the normal home screen: adb uninstall com.orbit.tv
