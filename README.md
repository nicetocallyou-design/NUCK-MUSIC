# MUSE MUSIC — Android Starter

Aplikasi Android native dengan Kotlin dan Jetpack Compose. Visualnya mengambil inspirasi dari pengalaman Apple Music, namun menggunakan identitas MUSE MUSIC sendiri.

## Isi prototipe
- Listen, Browse, Radio, Library, dan Search.
- Mini-player dan layar Now Playing.
- Data contoh untuk lagu, playlist, stasiun, dan favorit.
- Navigasi dan interaksi demo.

## Build APK tanpa Android Studio
Gunakan panduan [`GITHUB_BUILD_DARI_HP.md`](GITHUB_BUILD_DARI_HP.md). Proyek sudah memiliki workflow GitHub Actions untuk build langsung dari folder proyek. Tidak perlu memasang Android Studio.

Konfigurasi saat ini:
- Kotlin + Jetpack Compose + Material 3
- Minimum Android: API 26 (Android 8.0)
- Compile / target SDK: API 36
- AGP 9.3.0, Gradle 9.5.0, JDK 17

## Status
Ini adalah starter UI, belum merupakan layanan streaming musik. Tombol pemutar masih menggunakan state demo; audio engine, akses koleksi file audio lokal, metadata/cover album, playback background, dan notifikasi media akan dikembangkan pada tahap berikutnya.
