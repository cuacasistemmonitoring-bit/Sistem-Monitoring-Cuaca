# Dashboard Monitoring 3 Halaman (Termasuk Curah Hujan)

Dashboard berbasis Web (*Single Page Application*) dengan 3 menu navigasi tab interaktif dan 5 parameter sensor.

## Fitur dan Struktur:
1. **Page 1: Realtime Monitoring**
   - Menampilkan kotak indikator Status Sistem (Online/Offline) berserta penunjuk Waktu dan Tanggal *realtime*.
   - 5 Kartu parameter sensor: Suhu Udara, Kelembapan, Kecepatan Udara, Intensitas Cahaya, dan **Curah Hujan**. Grid otomatis menyesuaikan ukuran layar.
2. **Page 2: Grafik Parameter**
   - Menampilkan 5 grafik interaktif menggunakan `Chart.js` (Grafik garis untuk Suhu, Kelembapan, Angin, Cahaya, dan Grafik Batang/Bar untuk Curah Hujan).
3. **Page 3: Histori Pembacaan**
   - Menampilkan tabel *log* riwayat pembacaan 5 parameter sensor lengkap dengan stempel waktu.

## Cara Penggunaan:
1. Ekstrak file zip ini.
2. Buka `index.html` di browser internet (diperlukan koneksi internet agar *library* grafik Chart.js dapat dimuat).
3. Gunakan menu *sidebar* di sebelah kiri untuk berpindah halaman secara dinamis.
