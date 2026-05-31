# NextSID

NextSID adalah Sistem Informasi Desa (SID) sumber terbuka (*open-source*) yang dirancang sebagai alternatif modern, fleksibel, dan mutakhir untuk mendukung digitalisasi administrasi serta pelayanan publik di tingkat desa.

Aplikasi ini dibangun di atas *framework* dan teknologi modern untuk memberikan pengalaman performa yang lebih cepat, efisien, aman, dan mudah dikembangkan oleh komunitas.

> ⚠️ **Status Proyek: Versi Alpha (Developer Preview)**
> Proyek ini masih dalam tahap pengembangan awal, pengujian internal, dan belum dirilis untuk versi produksi. Masih banyak fitur yang sedang dikembangkan dan kekurangan yang perlu diperbaiki. Kontribusi dan masukan dari para pengembang sangat kami harapkan.

---

## 🚀 Fitur Utama (Rencana & Pengembangan)

- **Modern Tech Stack:** Menggunakan *framework* PHP paling populer dan terbaru.
- **Dashboard Interaktif & Responsif:** Didukung oleh Filament untuk pengelolaan data yang intuitif dan cepat.
- **Ringan & Cepat:** Optimalisasi basis data dan arsitektur kode modern untuk efisiensi server desa.
- **Fleksibilitas Deployment:** Dapat dijalankan secara luring (*offline*) maupun daring (*online*) dengan mudah.

## 🛠️ Spesifikasi Teknologi

Aplikasi ini memanfaatkan ekosistem pengembangan web modern terkini:

- **Framework:** [Laravel 12.x](https://laravel.com)
- **Admin Panel / Dashboard:** [Filament v3.3.x](https://filamentphp.com)
- **Versi PHP Minimum:** PHP 8.2.12 (atau versi di atasnya yang kompatibel)

## 🖥️ Lingkungan Pengujian (Tested Environment)

NextSID telah diuji dan dikonfirmasi dapat berjalan dengan baik pada lingkungan berikut:

1. **Luring (Offline):** Menggunakan **XAMPP** standar lokal.
2. **Daring (Online):** Berhasil diuji coba online secara aman menggunakan infrastruktur **Cloudflare Zero Trust / Tunnels** tanpa membutuhkan IP publik statis.

---

## 📦 Instalasi (Tahap Pengembangan)

*Catatan: Karena masih dalam versi Alpha, langkah ini ditujukan untuk kebutuhan pengembangan (development).*

1. **Clone Repositori:**

```bash
git clone https://github.com/syabiz/NextSID.git
cd NextSID
```

2. **Install Dependensi:**

```bash
composer install
npm install
```

3. **Konfigurasi Environment:**

```bash
cp .env.example .env
php artisan key:generate
```

4. **Konfigurasi database** pada file `.env`, lalu jalankan migrasi:

```bash
php artisan migrate --seed
```

5. **Jalankan Server Lokal:**

```bash
php artisan serve
npm run dev
```

---

## 🤝 Kontribusi

Kami sangat terbuka bagi siapa saja yang ingin ikut berkontribusi membangun NextSID menjadi lebih baik—baik melalui pelaporan bug, pengajuan fitur, maupun Pull Request (PR) kode sumber.

Silakan buka bagian [Issues](https://github.com/syabiz/NextSID/issues) jika Anda menemukan kendala selama pengujian versi Alpha ini.

## 📄 Lisensi

Aplikasi dan kode sumber NextSID dirilis di bawah lisensi **GPL v3** (GNU General Public License v3). Hal ini menjamin bahwa NextSID akan selalu tetap bebas, terbuka, dan dapat diakses oleh seluruh desa tanpa batasan kode tersembunyi.

---

Dikembangkan dengan ❤️ oleh [NextSID](https://nexts.id) dan bersama Komunitas.
