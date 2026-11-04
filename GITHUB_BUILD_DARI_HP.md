# Build APK MUSE MUSIC dari HP (tanpa Android Studio)

Tujuan: membuat file APK Android menggunakan GitHub Actions. Android Studio tidak perlu dipasang di HP atau laptop.

## Yang perlu disiapkan
- Akun GitHub.
- File `MuseMusic_Android_Starter.zip` dari percakapan ini.
- Browser di HP (Chrome cukup).

## Langkah 1 — Buat repository
1. Buka https://github.com/new dan masuk ke akun GitHub.
2. Isi **Repository name** dengan `muse-music-android`.
3. Pilih **Private** agar source code tidak menjadi publik (boleh pilih Public bila memang ingin).
4. Aktifkan **Add a README file**. Ini penting agar repository memiliki branch awal.
5. Tekan **Create repository**.

## Langkah 2 — Upload ZIP proyek
1. Buka repository `muse-music-android` yang baru dibuat.
2. Pilih **Add file → Upload files**. Pada tampilan HP, mungkin perlu menu browser **Desktop site**.
3. Pilih file `MuseMusic_Android_Starter.zip` yang sudah diunduh dari percakapan.
4. Tekan **Commit changes**.

Tidak perlu mengekstrak ZIP di HP. Upload file ZIP-nya saja.

## Langkah 3 — Kirim tautan repository
Salin alamat repository GitHub dan kirim ke percakapan ini. Contoh format:

`https://github.com/USERNAME/muse-music-android`

Setelah alamat repository tersedia, workflow build akan ditambahkan ke repository tersebut. GitHub Actions akan mengekstrak source, memasang toolchain Android di server, dan membangun APK debug. Android Studio tidak digunakan.

## Langkah 4 — Unduh dan pasang APK
Jika build berhasil, hasil APK akan tersedia sebagai **artifact** pada halaman repository:
1. Buka tab **Actions**.
2. Pilih workflow **Build Muse Music APK** yang berhasil (tanda centang hijau).
3. Buka bagian **Artifacts** dan unduh `muse-music-debug-apk`.
4. Ekstrak ZIP artifact, lalu buka `app-debug.apk` di HP.
5. Izinkan pemasangan aplikasi dari sumber tersebut bila Android memintanya.

## Catatan
- Build pertama memerlukan koneksi internet di server GitHub untuk mengunduh Gradle dan Android SDK.
- APK tahap ini adalah prototipe UI dengan data demo. Audio engine, pemindaian MP3 lokal, dan streaming belum termasuk.
- Bila build gagal, log pada tab Actions akan menunjukkan tahap yang perlu diperbaiki.
