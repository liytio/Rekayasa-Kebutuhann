# Alumni Tracker OSINT System - Daily Project 3

Sistem ini adalah purwarupa berbasis web untuk melacak rekam jejak pekerjaan dan studi lanjut alumni menggunakan pengumpulan data publik (Open-Source Intelligence/OSINT) dari platform seperti LinkedIn, Google Scholar, dan situs web publik.

## Tautan Proyek
* **Source Code GitHub:** `[Masukkan URL Repositori GitHub Anda di sini]`
* **Live Demo (Web Terpublikasi):** `[Masukkan URL Web Publish Anda di sini, misal: Github Pages/Vercel]`

## Fitur Utama (Berdasarkan Daily Project 2)
1. **Dasbor Statistik:** Melihat jumlah alumni yang teridentifikasi dan yang perlu verifikasi.
2. **Job Pelacakan (Scheduler Simulasi):** Tombol yang menyimulasikan *query* pencarian dan ekstraksi sinyal identitas dari sumber publik.
3. **Sistem Status & Disambiguasi:** Pengkategorian otomatis menjadi "Teridentifikasi Kuat" atau "Perlu Verifikasi Manual" berdasarkan skor kecocokan *timeline* dan afiliasi.

---

## Tabel Pengujian Kualitas Aplikasi (Quality Assurance)

Berikut adalah pengujian aplikasi berdasarkan aspek kualitas yang telah dirancang:

| ID Uji | Aspek Kualitas | Skenario Pengujian (Test Case) | Hasil yang Diharapkan (Expected Result) | Status | Keterangan |
|---|---|---|---|---|---|
| TC-01 | **Fungsionalitas** | Menekan tombol "Jalankan Job Pelacakan" | Sistem memproses data (tombol berubah status) dan memperbarui tabel dari "Belum Dilacak" menjadi status baru beserta info pekerjaan. | **LULUS** | Simulasi JavaScript berjalan sesuai alur *pseudocode*. |
| TC-02 | **Usability (UI/UX)** | Mengakses web menggunakan *browser* seluler (Mobile) | Layout web, statistik, dan tabel menyesuaikan ukuran layar tanpa *layout* yang pecah (Responsif). | **LULUS** | Menggunakan sistem *grid* dan kelas responsif Tailwind CSS. |
| TC-03 | **Reliability** | Memastikan *Disambiguasi* memberikan status yang berbeda | Sistem memberikan status "Teridentifikasi Kuat" untuk data dengan skor tinggi, dan "Perlu Verifikasi" untuk data ambigu. | **LULUS** | Tercermin dari perubahan *badge* warna hijau dan oranye pada baris tabel yang berbeda. |
| TC-04 | **Performance** | Memuat halaman awal dasbor (Initial Load) | Halaman termuat sempurna dalam waktu kurang dari 2 detik. | **LULUS** | Dioptimalkan dengan CDN untuk pemuatan aset yang cepat. |
