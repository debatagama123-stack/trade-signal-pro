# Trade Signal Pro — Android APK Builder

Paket ini membungkus aplikasi web Trade Signal Pro ke Android menggunakan Capacitor dan GitHub Actions.

## Cara mendapatkan APK tanpa Android Studio (pakai HP)
1. Ekstrak ZIP.
2. Buat repository baru di GitHub.
3. Upload semua isi folder ini ke repository (termasuk folder `.github/workflows`).
4. Buka tab **Actions** di repository dan pilih **Build Trade Signal Pro APK**.
5. Tekan **Run workflow** (atau tunggu workflow berjalan setelah push).
6. Jika selesai sukses, buka run tersebut → bagian **Artifacts** → unduh `TradeSignalPro-debug-apk`.
7. Ekstrak artifact ZIP, lalu instal `app-debug.apk` di Android. Android mungkin meminta izin **Install unknown apps** untuk browser/file manager yang digunakan.

## Penting
- Paket ZIP ini adalah *source/build project*, bukan APK yang sudah dikompilasi. Build memerlukan GitHub Actions atau komputer dengan Android SDK.
- APK yang dibuat workflow adalah debug APK untuk uji pribadi, bukan APK rilis Play Store.
- Aplikasi crypto mencoba mengambil data publik Binance. Koneksi mungkin gagal pada jaringan/region tertentu.
- Forex/XAUUSD/indeks memerlukan API key provider. API key di browser hanya cocok untuk pengujian pribadi; jangan distribusikan APK dengan API key rahasia.
- News Alert belum memiliki feed kalender ekonomi real-time.
- Untuk notifikasi saat aplikasi ditutup, perlu implementasi push notification server-side. Izin notifikasi browser/webview tidak menjamin push background.
- Sinyal EMA/RSI adalah indikator dasar dan bukan jaminan profit.

## Jika upload melalui browser HP
GitHub bisa digunakan dari browser, tetapi mengunggah banyak file dan folder tersembunyi mungkin lebih mudah lewat GitHub web editor atau komputer. Pastikan file `.github/workflows/build-apk.yml` ikut terunggah.
