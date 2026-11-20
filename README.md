# Arpeggio Trainer — GitHub Actions APK build

## Upload these files to the ROOT of your GitHub repository
- `index.html`
- `icon.png`
- `package.json`
- `capacitor.config.json`
- `build.yml` (workflow file; instructions below)

No `resources` folder is needed. The workflow creates it and copies `icon.png` into it automatically.

## Add the GitHub Actions workflow (one-time setup)
1. In your repository, open **Add file → Create new file**.
2. In the filename box, enter exactly: `.github/workflows/build.yml`
3. Open the `build.yml` file included in this package, copy all its contents, and paste them into GitHub's editor.
4. Commit the new file. GitHub creates the hidden folders automatically from that path.

## Run the build
1. Open the repository's **Actions** tab.
2. Select **Build Arpeggio Trainer APK**.
3. Choose **Run workflow**.
4. When it finishes, open the run and download the `Arpeggio-Trainer-debug-apk` artifact.
5. Extract that downloaded artifact ZIP and install `app-debug.apk` on your Android phone.

The Android project is generated during the build; you do not need to upload an `android` folder or install Android Studio.

## App identity
- Display name: Arpeggio Trainer
- Android application ID: `com.triiiga.arpeggiotrainer`

Keep the application ID unchanged for future updates.

## Playback note
The HTML includes lock-screen and keep-playing logic, but Android may still suspend WebView audio when the screen is off. Test this on the target phone.
