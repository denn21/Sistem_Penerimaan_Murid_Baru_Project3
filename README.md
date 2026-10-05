# 🎓 Sistem Penerimaan Siswa Otomatis

Alur kerja penerimaan siswa otomatis yang dibangun dengan **n8n** untuk menyederhanakan dan mengoptimalkan proses pendaftaran dan seleksi siswa.

Sistem secara otomatis memproses data pelamar dari Google Sheets, mengevaluasi pelamar berdasarkan kriteria yang telah ditentukan, mengirimkan notifikasi email yang dipersonalisasi, memberikan rekomendasi sekolah alternatif bertenaga AI, dan menghasilkan ringkasan penerimaan mingguan.

---

## 🚀 Fitur

- 📥 **Pemrosesan Pendaftaran Otomatis**
  - Menerima data pendaftaran siswa baru dari Google Sheets.
  - Memeriksa apakah informasi pelamar yang diperlukan sudah lengkap.

- 🔎 **Penyaringan Pelamar Otomatis**
  - Mengevaluasi pelamar berdasarkan kriteria yang telah ditentukan seperti:
    - Usia pelamar
    - Kisaran penghasilan orang tua
    - Informasi pendaftaran yang diperlukan

- ✅ **Klasifikasi Penerimaan Otomatis**
  - Secara otomatis mengkategorikan pelamar ke dalam:
    - Diterima
    - Ditolak
    - Rekomendasi alternatif

- 📧 **Notifikasi Email Otomatis**
  - Mengirimkan email yang dipersonalisasi kepada orang tua berdasarkan hasil penerimaan.
  - Memberikan informasi tentang kegiatan Open House dan Trial Class.

- 🤖 **Rekomendasi Sekolah Bertenaga AI**
  - Menggunakan LLM untuk menghasilkan rekomendasi untuk tiga sekolah dasar terdekat ketika pelamar tidak memenuhi syarat karena usia.

- 📊 **Ringkasan Eksekutif Mingguan**
  - Secara otomatis meringkas pelamar yang diterima dan ditolak dari tujuh hari sebelumnya.
  - Mengirimkan ringkasan melalui email setiap Senin pukul 08:00 WIB.

---
<img width="591" height="358" alt="image" src="https://github.com/user-attachments/assets/d8cb4353-fcb4-40b2-84ad-f6745bf2b412" />


Google Sheets
      │
      ▼
Pendaftaran Siswa Baru
      │
      ▼
Periksa Data yang Diperlukan
      │
      ▼
Periksa Usia Siswa
      │
      ├─────────────── Usia > 6
      │                    │
      │                    ▼
      │              Rekomendasi Sekolah AI
      │                    │
      │                    ▼
      │               Hasil Email
      │
      ▼
Evaluasi Penghasilan Orang Tua
      │
      ├─────────────── Ditolak
      │                    │
      │                    ▼
      │               Simpan ke Sheet
      │                    │
      │                    ▼
      │               Hasil Email
      │
      └─────────────── Diterima
                           │
                           ▼
                      Simpan ke Sheet
                           │
                           ▼
                      Hasil Email


