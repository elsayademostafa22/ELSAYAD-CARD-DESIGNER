# ELSAYAD CARD DESIGNER — Android Local MVP

Flutter starter project for local voucher generation and printable voucher sheets.

## Included
- Arabic RTL interface
- Local SQLite storage using sqflite
- Generate unique random voucher codes
- Save batches and codes on the phone
- Export/print voucher sheets as PDF using the Android print/share flow
- Project structure prepared for future MikroTik integration and cloud sync

## Not included yet
- APK binary (must be built using Flutter/Android SDK)
- Live MikroTik API connection or pushing codes to a router
- Multi-company cloud accounts/subscriptions
- Visual drag-and-drop card editor

## Requirements
- Flutter stable SDK
- Android Studio (Android SDK) or VS Code with Flutter/Dart extensions
- Android phone with USB debugging enabled, or an emulator

## Open and run
1. Extract this ZIP.
2. Open the `ELSAYAD_CARD_DESIGNER_ANDROID` folder in VS Code.
3. In terminal run:
   ```bash
   flutter pub get
   flutter doctor
   flutter run
   ```
4. To create an APK:
   ```bash
   flutter build apk --release
   ```
   APK output: `build/app/outputs/flutter-apk/app-release.apk`

## Data and backup
The database is stored locally in the app's private storage. Uninstalling the app may remove local data. Add export/backup before using this for real business operations.

## Next milestones
1. Add custom card design editor and print layout settings.
2. Add router records and secure RouterOS v6/v7 connection module.
3. Add encrypted local credential storage and audit trail.
4. Add optional server synchronization, companies, and subscriptions.

## Build APK without a personal computer
This repository includes a GitHub Actions workflow at `.github/workflows/build-apk.yml`.
1. Create a GitHub repository using a mobile browser.
2. Upload the contents of this project ZIP to the repository root (including the hidden `.github` folder; if the mobile upload flow hides it, create the workflow file directly in GitHub).
3. Open the repository's Actions tab and run **Build Android APK** (or push to `main`).
4. Open the successful workflow run and download the `elsayad-card-designer-apk` artifact.
5. Extract the downloaded artifact ZIP on your phone; it contains `app-release.apk`.
