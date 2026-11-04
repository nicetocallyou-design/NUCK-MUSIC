# Membuat APK MUSE MUSIC tanpa Android Studio

Proyek ini adalah aplikasi Android native Kotlin + Jetpack Compose. Kamu tidak perlu memasang Android Studio atau Android SDK di HP/PC. GitHub Actions akan mengompilasi APK di server cloud.

## Langkah satu kali

1. Masuk atau daftar di https://github.com.
2. Buat repository baru bernama `muse-music`. Repository boleh Public atau Private.
3. Ekstrak ZIP proyek ini di perangkat.
4. Buka repository baru tersebut di GitHub, pilih **Add file → Upload files**.
5. Unggah seluruh isi folder `MuseMusic` (termasuk folder tersembunyi `.github` yang berisi workflow), lalu tekan **Commit changes**.
6. Buka tab **Actions** di repository. Pilih workflow **Build Muse Music APK**. Jika build tidak mulai otomatis setelah commit, tekan **Run workflow**.
7. Tunggu sampai status job berwarna hijau. Buka hasil run tersebut dan unduh artifact **muse-music-debug-apk**.
8. Ekstrak ZIP artifact di HP Android, lalu ketuk `app-debug.apk` dan izinkan instalasi dari sumber tersebut bila Android memintanya.

## Informasi build

- Gradle: 9.5.0
- Android Gradle Plugin: 9.3.0
- JDK: 17
- Android compile SDK: 36
- Minimum Android: 8.0 (API 26)
- Output: `app/build/outputs/apk/debug/app-debug.apk`

## Catatan

- Workflow ini membangun APK debug untuk instalasi dan pengujian, bukan APK rilis Play Store.
- APK belum ditandatangani dengan kunci rilis pribadi.
- Aplikasi saat ini masih berupa UI/demo interaktif. Audio streaming dan pemutaran file lokal belum diimplementasikan.
- Build cloud memerlukan akun GitHub dan akses internet pada server GitHub Actions. Tidak perlu Android Studio.
