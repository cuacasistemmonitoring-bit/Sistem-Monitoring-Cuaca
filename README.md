# Dashboard Monitoring (Terhubung ke Firebase Realtime Database)

Dashboard berbasis Web (*Single Page Application*) ini telah diintegrasikan dengan Firebase Realtime Database menggunakan Firebase JavaScript SDK (Modular versi 10+).

## Perubahan Utama:
1. **Koneksi Firebase:** Menambahkan script `firebase-app.js` dan `firebase-database.js` beserta kredensial `firebaseConfig` sesuai data pengguna.
2. **Path Database:** Sistem kini "mendengarkan" (*listen*) perubahan pada node `/HistoriCuaca` yang dikirimkan oleh mikrokontroler (ESP32).
3. **Pembaruan Dinamis:** 
   - **Halaman Realtime:** Mengambil data anak (child) terakhir dari list `HistoriCuaca`.
   - **Halaman Grafik & Histori:** Mengambil 15 data terakhir untuk divisualisasikan dalam *chart* dan diurutkan dalam tabel.
4. **Indikator Koneksi:** Menggunakan node referensi khusus Firebase (`.info/connected`) untuk mengetahui status *online/offline* koneksi web ke server Firebase.

## Cara Menjalankan:
**Sangat Penting:** Karena *browser* modern memblokir impor *module* JavaScript secara lokal (aturan CORS), Anda tidak bisa membukanya langsung dengan *double-click* (file `file://...`).

Untuk melihat data masuk:
1. Ekstrak file HTML ini.
2. Anda **HARUS** menjalankannya menggunakan Local Web Server. 
   - *Pilihan 1 (VS Code):* Gunakan ekstensi **Live Server** (Klik kanan pada file -> *Open with Live Server*).
   - *Pilihan 2 (Python):* Buka terminal/CMD di folder ekstrak, ketik `python -m http.server`, lalu buka `http://localhost:8000` di *browser*.
   - *Pilihan 3:* Hosting ke GitHub Pages atau Firebase Hosting.
