# NextSID — Sistem Informasi Desa Modern

**NextSID** adalah Sistem Informasi Desa (SID) *open-source* yang dirancang untuk mendukung digitalisasi administrasi dan pelayanan publik di tingkat desa. Dibangun dengan teknologi modern, modular, dan mudah dikustomisasi untuk kebutuhan spesifik setiap desa.

> 📌 **Status:** v1.0.0 — Developer Preview (Alpha)  
> Masih dalam tahap pengembangan. Kontribusi dan masukan sangat diharapkan!

---

## ✨ Fitur Utama

### 📊 Portal Admin (Dashboard)
- **Panel Pengelolaan Terpadu** powered by [Filament](https://filamentphp.com) v3.3.x
- **RBAC (Role-Based Access Control)** dengan Spatie Permission
- **User & Role Management** untuk kontrol akses granular
- **Real-time Statistics** data kependudukan, layanan, dan transparansi

### 🏛️ Portal Publik
- **Responsive Website** untuk akses warga dari desktop, tablet, mobile
- **Tema Nusantara** — desain modern dengan sentuhan Indonesia
- **Carousel Hero** dengan galeri foto desa (desa-1.jpg, desa-2.jpg, desa-3.jpg)
- **Layanan Online:**
  - 📝 Ajukan Surat (Surat Pengantar, Keterangan, dll)
  - 📊 Data Penduduk Transparan
  - 💰 Transparansi APBDes
  - 📢 Sistem Pengaduan Warga
  - 🏪 Lapak UMKM Desa

### 🔧 Modular Architecture
- **Sistem Modul** — Fitur terpisah yang dapat diaktifkan/nonaktifkan
- **Plugin System** — Ekstensi fungsionalitas tanpa modifikasi core
- **Theme System** — Multiple tema yang dapat dipilih
- **Custom Hooks** — HookSystem untuk integrasi custom logic

### 🔌 Integrasi
- **REST API Publik** untuk integrasi dengan sistem lain
- **Multi-Database Support** (MySQL, PostgreSQL, SQLite)
- **Offline-Ready** (PWA roadmap untuk mode offline)

---

## 🛠️ Tech Stack

| Komponen | Teknologi | Versi |
|----------|-----------|-------|
| **Backend** | [Laravel](https://laravel.com) | 12.x |
| **Admin Panel** | [Filament](https://filamentphp.com) | 3.3.x |
| **Frontend** | [Tailwind CSS](https://tailwindcss.com), [Vite](https://vitejs.dev) | 4.0, 7.x |
| **PHP** | PHP | 8.2.12+ |
| **Database** | MySQL/MariaDB, PostgreSQL, SQLite | - |
| **Auth** | Laravel Sanctum, Spatie Permission | - |

---

## 📁 Struktur Project

```
nextsid/
├── app/                          # Aplikasi Core
│   ├── Core/                      # Hook System, Module Loader, Plugin Manager, Theme Manager
│   ├── Filament/                  # Admin Panel Resources & Pages
│   ├── Http/                      # Controllers, Requests, Middleware
│   ├── Models/                    # Eloquent Models
│   └── Providers/                 # Service Providers
├── bootstrap/                    # Bootstrap Framework
├── config/                       # Konfigurasi Aplikasi
│   └── nextsid.php              # NextSID Configuration
├── database/
│   ├── migrations/               # Database Schema
│   ├── factories/                # Model Factories
│   └── seeders/                  # Database Seeders
├── modules/                      # Modular Features
│   ├── Penduduk/                 # Kependudukan
│   ├── InfoDesa/                 # Profil Desa
│   ├── Statistik/                # Dashboard Statistik
│   ├── LayananSurat/             # Layanan Surat Online
│   ├── Keuangan/                 # APBDes & Transparansi
│   ├── Pembangunan/              # Proyek Pembangunan
│   ├── Kesehatan/                # Data Kesehatan
│   ├── Kehadiran/                # Absensi Aparatur
│   └── [15+ modules lainnya]/   # Custom modules
├── plugins/                      # Plugin Extensions
│   └── whatsapp-notif/          # Notifikasi WhatsApp
├── public/                       # Web Root
│   ├── index.php
│   ├── themes/                   # Published Theme Assets
│   └── build/                    # Vite Build Output
├── resources/
│   ├── css/                      # Global Styles (Tailwind)
│   ├── js/                       # App.js
│   └── views/                    # Blade Views
├── routes/
│   ├── web.php                   # Web Routes
│   ├── api.php                   # API Routes
│   ├── console.php               # Console Routes
│   └── _theme_route_snippet.php # Theme Dynamic Routes
├── storage/                      # File Storage (logs, cache, uploads)
├── tests/                        # Test Suite
├── themes/                       # Theme Source Files
│   └── default/                  # Tema Nusantara (default)
│       ├── assets/               # CSS, JS theme
│       ├── images/               # Gambar desa (desa-1.jpg, desa-2.jpg, desa-3.jpg)
│       ├── views/                # Blade templates
│       └── theme.json            # Theme metadata
└── vendor/                       # Composer Dependencies
```

---

## 📋 Modul Standar

NextSID dilengkapi modul-modul berikut (dapat diaktifkan/dinonaktifkan):

| Modul | Deskripsi | Status |
|-------|-----------|--------|
| **Penduduk** | Manajemen data penduduk & keluarga | ✅ Active |
| **InfoDesa** | Profil desa, struktur pemerintah | ✅ Active |
| **Statistik** | Dashboard statistik penduduk | ✅ Active |
| **LayananSurat** | Sistem ajuan surat online | ✅ Active |
| **SuratDinas** | Manajemen surat dinas | ✅ Active |
| **Keuangan** | APBDes, transparansi anggaran | ✅ Active |
| **Pembangunan** | Proyek infrastruktur desa | ✅ Active |
| **Inventaris** | Aset dan inventori desa | ✅ Active |
| **Kesehatan** | Data kesehatan warga | ✅ Active |
| **Kehadiran** | Absensi aparatur desa | ✅ Active |
| **Ekspedisi** | Manajemen pengiriman dokumen | ✅ Active |
| **AdminWeb** | Manajemen website & SEO | ✅ Active |
| **LayananMandiri** | Portal self-service warga | ✅ Active |
| **Pengaturan** | Konfigurasi sistem | ✅ Active |

---

## 🎨 Tema

### Tema Nusantara (Default)
Tema utama NextSID dengan desain modern dan responsif:

- **Hero Section** dengan carousel galeri desa
- **Responsive Grid** untuk semua ukuran layar
- **Accessible Components** sesuai WCAG 2.1
- **Dark Mode Support** (via Tailwind)
- **Custom Fonts** (Space Grotesk, Open Sans)

**Menambahkan Gambar Desa:**
1. Letakkan foto-foto desa ke `themes/default/images/`:
   - `desa-1.jpg` (utama)
   - `desa-2.jpg` (sekunder)
   - `desa-3.jpg` (opsional)
2. Carousel akan otomatis mendeteksi dan menampilkan slide

---

## 🚀 Instalasi & Setup

### Prerequisites
- **PHP 8.2.12+**
- **Composer** (dependency manager)
- **Node.js 16+** & NPM (untuk build assets)
- **MySQL 5.7+** atau **PostgreSQL 10+**

### 1. Clone Repository

```bash
git clone https://github.com/syabiz/NextSID.git
cd NextSID
```

### 2. Install PHP Dependencies

```bash
composer install
```

### 3. Install Frontend Dependencies

```bash
npm install
```

### 4. Setup Environment

```bash
cp .env.example .env
php artisan key:generate
```

Edit `.env` dan sesuaikan konfigurasi database Anda:

```env
APP_NAME=NextSID
APP_ENV=local
APP_DEBUG=true

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=nextsid
DB_USERNAME=root
DB_PASSWORD=

# NextSID Specific
NEXTSID_NAMA_DESA="Desa Contoh"
NEXTSID_KECAMATAN="Kecamatan Contoh"
NEXTSID_KABUPATEN="Kabupaten Contoh"
NEXTSID_THEME=default
```

### 5. Buat Database & Run Migrations

```bash
# Buat database MySQL terlebih dahulu
mysql -u root -e "CREATE DATABASE nextsid CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;"

# Run migrations dan seeders
php artisan migrate --seed
```

### 6. Build Frontend Assets

```bash
npm run build       # Production build
npm run dev         # Development (watch mode)
```

### 7. Jalankan Server

```bash
# Development server (dengan auto-reload)
php artisan serve
```

Server akan berjalan di `http://localhost:8000`

---

## 📖 Development

### File Structure untuk Development

```bash
# Untuk Laravel development
php artisan make:model NamaModel -m    # Buat Model + Migration
php artisan make:controller NamaController
php artisan make:migration create_table_name --create=table_name

# Untuk Filament Resource
php artisan make:filament-resource NamaResource

# Untuk Custom Module
php artisan make:module NamaModule

# Database
php artisan migrate                    # Run migrations
php artisan migrate:refresh --seed     # Reset & seed data
php artisan tinker                     # Interactive shell
```

### Testing

```bash
# Run test suite
php artisan test

# Run dengan coverage report
php artisan test --coverage
```

### Asset Development

```bash
# Watch CSS/JS changes secara real-time
npm run dev

# Build untuk production
npm run build
```

### Cache Management

```bash
# Clear semua cache
php artisan cache:clear
php artisan config:cache
php artisan route:cache
php artisan view:clear
php artisan optimize:clear
```

---

## 🔐 Security

- ✅ **CSRF Protection** di semua forms
- ✅ **SQL Injection Prevention** via Eloquent ORM & Query Builder
- ✅ **Password Hashing** dengan bcrypt
- ✅ **RBAC & Permission** via Spatie Permission
- ✅ **API Authentication** via Sanctum tokens
- ✅ **HTTPS** recommended untuk production
- ✅ **Environment Variables** untuk sensitive data

**Untuk Production:**
```bash
# Disable debug mode
APP_DEBUG=false

# Cache config untuk performa
php artisan config:cache

# Use HTTPS & HSTS headers
FORCE_HTTPS=true
```

---

## 📡 API Publik

NextSID menyediakan REST API untuk integrasi dengan sistem lain:

```bash
GET    /api/v1/penduduk              # List penduduk
GET    /api/v1/statistik             # Statistik desa
GET    /api/v1/layanan-surat         # Daftar tipe surat
POST   /api/v1/pengaduan             # Submit pengaduan
```

Dokumentasi API lebih lengkap di: `docs/API.md` (akan datang)

---

## 🐛 Troubleshooting

### Database Connection Error
```bash
# Verify .env configuration
php artisan config:cache

# Test database connection
php artisan db:show
```

### Permission Denied on storage/
```bash
chmod -R 775 storage bootstrap/cache
```

### Modules/Plugins tidak terdeteksi
```bash
php artisan cache:clear
php artisan view:clear
```

### CSS/JS tidak ter-update
```bash
npm run build
php artisan view:clear
```

---

## 🤝 Kontribusi

Kami sangat menghargai kontribusi dari komunitas! Bagaimana Anda dapat membantu:

### Pelaporan Bug
- Gunakan [Issues](https://github.com/syabiz/NextSID/issues)
- Sertakan:
  - Deskripsi jelas tentang bug
  - Steps untuk reproduce
  - Screenshot/error logs
  - Environment info (OS, PHP, MySQL versi)

### Feature Request
- Buka [Discussion](https://github.com/syabiz/NextSID/discussions)
- Jelaskan use case dan benefit
- Hubungi maintainer untuk diskusi

### Pull Request
1. Fork repository
2. Buat branch feature (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push ke branch (`git push origin feature/AmazingFeature`)
5. Buat Pull Request dengan deskripsi jelas

**Coding Standards:**
- Follow [PSR-12](https://www.php-fig.org/psr/psr-12/) untuk PHP
- Use Tailwind CSS untuk styling
- Test coverage minimal 80%

---

## 📚 Dokumentasi

- [Panduan Instalasi Lengkap](docs/INSTALLATION.md)
- [Panduan Development Module](docs/MODULE_DEVELOPMENT.md)
- [Panduan Theme Development](docs/THEME_DEVELOPMENT.md)
- [API Reference](docs/API.md)
- [Database Schema](docs/DATABASE_SCHEMA.md)

---

## 📦 Dependencies

### Laravel Ecosystem
- `laravel/framework` — Core framework
- `filament/filament` — Admin panel
- `spatie/laravel-permission` — RBAC
- `spatie/laravel-query-builder` — Query helpers

### Frontend
- `tailwindcss` — Utility-first CSS
- `vite` — Modern build tool
- `axios` — HTTP client

### Utilities
- `nesbot/carbon` — Date/time handling
- `symfony/var-dumper` — Debugging
- `phpunit/phpunit` — Testing

*Lihat `composer.json` dan `package.json` untuk daftar lengkap*

---

## 📄 Lisensi

NextSID dirilis di bawah lisensi **GNU General Public License v3 (GPLv3)**.

Lisensi ini menjamin bahwa:
- ✅ NextSID akan selalu **bebas** dan **open-source**
- ✅ Setiap desa dapat menggunakan tanpa biaya lisensi
- ✅ Source code dapat dipelajari, dimodifikasi, dan didistribusikan
- ✅ Tidak ada kode tersembunyi atau proprietary

Lihat [LICENSE](LICENSE) untuk detail lengkap.

---

## 👨‍💻 Authors & Credits

**NextSID** dikembangkan oleh [Syabiz](https://github.com/syabiz) dan berkontribusi dari komunitas open-source Indonesia.

Terima kasih kepada:
- [Laravel Community](https://laravel.com)
- [Filament Community](https://filamentphp.com)
- [Indonesian Open Source Community](https://id-opensourcecommunity.org)

---

## 📞 Support & Community

- 💬 **GitHub Discussions** — Ask questions & discuss features
- 🐛 **GitHub Issues** — Report bugs
- 📧 **Email** — [contact@nextsid.id](mailto:contact@nextsid.id)
- 🌐 **Website** — https://nextsid.id

---

## 🎯 Roadmap

- [ ] v1.1.0 — PWA & Offline Mode
- [ ] v1.2.0 — Mobile App (Flutter)
- [ ] v1.3.0 — Advanced Analytics & Reporting
- [ ] v1.4.0 — Multi-language Support (Regional)
- [ ] v2.0.0 — AI-Powered Features & Automation

---

**Dikembangkan dengan ❤️ oleh komunitas untuk digitalisasi desa Indonesia**
