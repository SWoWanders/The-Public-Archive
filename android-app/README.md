# Android app (Public Archive)

Turns this web app into an installable Android APK using Capacitor.
Every push to `main` triggers `.github/workflows/android-apk.yml`, which runs
`build.sh` on GitHub's servers and posts the APK under **Releases → Latest**.

- `capacitor.config.json` — app ID, name, background colour
- `res/` — launcher icons (brass "PA" catalogue mark on green)
- `build.sh` — copies the web files, creates the Android project, builds

Signing: repo secrets `ANDROID_KEYSTORE_B64` and `ANDROID_KEYSTORE_PASSWORD`
(same key as the other apps). Without them each build uses a throwaway key.

Nothing in here affects the GitHub Pages site.
