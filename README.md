<div align="center">

# Daily Rahmat

**Al-Qur'an digital, jadwal sholat, adzan, dan arah kiblat dalam satu aplikasi Android.**

[![Release](https://img.shields.io/github/v/release/dailyrahmat/Daily-Rahmat-Android?style=for-the-badge&color=0f766e&label=release)](https://github.com/dailyrahmat/Daily-Rahmat-Android/releases/latest)
[![Build](https://img.shields.io/badge/BUILD-1793852627-0f766e?style=for-the-badge)](https://github.com/dailyrahmat/Daily-Rahmat-Android/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/dailyrahmat/Daily-Rahmat-Android/total?style=for-the-badge&color=0f766e)](https://github.com/dailyrahmat/Daily-Rahmat-Android/releases)
![Android](https://img.shields.io/badge/Android-7.0%2B-3DDC84?style=for-the-badge&logo=android&logoColor=white)
![Bahasa](https://img.shields.io/badge/bahasa-Indonesia-red?style=for-the-badge)

[⬇️ Unduh APK](https://github.com/dailyrahmat/Daily-Rahmat-Android/releases/download/v1.0.0/DailyRahmat-v1.0.0-1793536127.apk) ·
[📦 Semua Rilis](https://github.com/dailyrahmat/Daily-Rahmat-Android/releases) ·
[🔒 Kebijakan Privasi](https://dailyrahmat.ftn.host/privacy)

</div>

---

## ✨ Tentang

**Daily Rahmat** membantu menemani ibadah harianmu: membaca Al-Qur'an dengan terjemahan Indonesia, mengingatkan waktu sholat dengan adzan, dan menunjukkan arah kiblat. Konten Al-Qur'an dibundel di dalam aplikasi, sehingga bisa dibaca **tanpa internet**.

> 📌 Repositori ini berisi **rilis APK dan dokumentasi** aplikasi. Paket: `daily.rahmat.app`

## 🚀 Fitur

### 📖 Al-Qur'an
- 114 surah lengkap, teks Arab dengan font Amiri dan terjemahan Indonesia
- Navigasi per surah dan per juz, plus pencarian
- Penanda ayat (bookmark) dan "lanjutkan membaca"
- Audio murottal per ayat (qari Mishary Alafasy)
- Pengaturan tampilan dan pilihan terjemahan
- Ayat harian dan kartu ayat yang bisa dibagikan
- Bisa dibaca penuh **secara offline**

### 🕌 Sholat
- Jadwal sholat berdasarkan lokasi dengan pilihan metode hisab
- Alarm **adzan** dengan 5 pilihan suara
- Alarm tetap terjadwal ulang setelah HP dihidupkan kembali
- Arah **kiblat**

### 🌐 Konten tambahan
- Pengetahuan Islam dan kutipan inspiratif
- Berita
- Radio, video, dan siaran langsung
- Infaq, zakat, dan sedekah
- Akun opsional untuk sinkronisasi bookmark dan preferensi

> Semua fitur inti bisa dipakai **tanpa mendaftar**. Akun hanya dibutuhkan untuk sinkronisasi antar perangkat.

## 📥 Instalasi

**Persyaratan:** Android 7.0 (API 24) atau lebih baru. Ruang kosong sekitar 150 MB.

1. Unduh APK dari [halaman rilis](https://github.com/dailyrahmat/Daily-Rahmat-Android/releases/latest).
2. Buka berkas yang diunduh. Jika diminta, izinkan **"Pasang aplikasi dari sumber ini"** untuk peramban atau pengelola berkas yang kamu pakai.
3. Ketuk **Pasang**, lalu buka **Daily Rahmat**.
4. Saat diminta, izinkan **Lokasi** (untuk jadwal sholat dan kiblat) dan **Notifikasi** (untuk adzan).

### 🔐 Verifikasi keaslian berkas

Sebelum memasang, cocokkan checksum agar yakin berkasnya tidak berubah:

```bash
# Linux / macOS
sha256sum DailyRahmat-v1.0.0-1793536127.apk

# Windows (PowerShell)
Get-FileHash .\DailyRahmat-v1.0.0-1793536127.apk -Algorithm SHA256
```

Hasil yang benar untuk **v1.0.0**:

```
77da8c236ccdd04ed9d3f575202be8c17281b34d8795d9b4cdaba0fa4c52dc15
```

Pasang APK hanya dari halaman rilis resmi ini. Jangan memasang berkas dari sumber lain yang mengaku sebagai Daily Rahmat.

## 🔑 Izin aplikasi

Daily Rahmat hanya meminta izin yang dipakai fitur-fiturnya:

| Izin | Kenapa dibutuhkan |
|---|---|
| Lokasi (perkiraan/tepat) | Menghitung jadwal sholat dan arah kiblat. Bisa ditolak, lalu pilih kota manual |
| Notifikasi | Menampilkan pengingat dan adzan |
| Alarm tepat waktu | Membunyikan adzan tepat pada waktunya |
| Berjalan saat perangkat menyala | Menjadwalkan ulang alarm adzan setelah HP restart |
| Layanan latar depan (media) | Memutar adzan, radio, dan playlist |
| Abaikan optimasi baterai | Menjaga alarm tidak ditunda sistem hemat daya |
| Internet | Mengambil jadwal sholat, audio, berita, dan sinkronisasi akun |

Aplikasi **tidak** meminta akses ke kontak, SMS, kamera, mikrofon, atau foto.

## 🔒 Privasi

Kami menjaga data seminimal mungkin dan tidak menjual data pribadimu. Detail data yang dikumpulkan, tujuan, pihak ketiga, masa simpan, serta cara menghapus akun ada di:

👉 **[Kebijakan Privasi](https://dailyrahmat.ftn.host/privacy)**

## 🧩 Teknologi

Daily Rahmat adalah aplikasi **hibrida**: cangkang Android native yang menampilkan antarmuka web (HTML, CSS, JavaScript) yang dibundel di dalam aplikasi.

| Bagian | Teknologi |
|---|---|
| Platform | Android (min SDK 24, target SDK 34) |
| Antarmuka | Web app lokal di WebView (`assets/www`) |
| Data Al-Qur'an | Berkas JS per surah, dibundel offline |
| Waktu sholat | Kalkulator dan API |
| Audio Al-Qur'an | [Islamic Network CDN] |
| Notifikasi push | Firebase Cloud Messaging |
| Layanan adzan | Android Foreground Service + AlarmManager |

## 🗺️ Rencana pengembangan

- [ ] Perhitungan jadwal sholat di perangkat (tanpa kirim lokasi ke server)
- [ ] Mode pilih kota manual tanpa izin lokasi
- [ ] Tafsir ayat di dalam pembaca
- [ ] Mode hafalan dan murajaah berjadwal
- [ ] Pilihan terjemahan dan bahasa tambahan
- [ ] Ekspor dan impor bookmark
- [ ] Pengaturan adzan per waktu sholat
- [ ] Login dengan Google
- [ ] Pembaruan keamanan dan pengurangan data yang dikirim ke server

## 🙏 Penutup

Semoga aplikasi ini bermanfaat dan menjadi amal jariyah bagi kita semua. Jika ada kekurangan, mohon doa dan masukannya.

<div align="center">

**بارك الله فيكم**

[⬆ Kembali ke atas](#-daily-rahmat)

</div>
