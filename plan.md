# Plan: Prototipe Mobile HTML dari Mockup

## Tujuan
Membuat prototipe mobile berbasis HTML dari 13 file mockup PNG dengan navigasi fungsional (tanpa logic backend).

## Daftar Mockup & Halaman yang Akan Dibuat

| No | File Mockup | Nama Halaman HTML | Keterangan |
|----|-------------|-------------------|-------------|
| 1 | visily-login-karyawan.png | login-karyawan.html | Login untuk karyawan |
| 2 | visily-login-pemasok.png | login-pemasok.html | Login untuk pemasok |
| 3 | visily-login-berhasil.png | login-berhasil.html | Halaman setelah login berhasil |
| 4 | visily-login-berhasil-1.png | login-berhasil-1.html | Variant halaman sukses |
| 5 | visily-otp.html | otp.html | Verifikasi OTP |
| 6 | visily-super-admin-pov.html | super-admin.html | Tampilan Super Admin |
| 7 | visily-supplier-list-(admin).html | supplier-list-admin.html | Daftar supplier (view Admin) |
| 8 | visily-supplier-approval-(owner).html | supplier-approval-owner.html | Approval supplier (view Owner) |
| 9 | visily-pov-profil-pemasok.html | profil-pemasok.html | Profil pemasok |
| 10 | visily-pov-pemasok.html | dashboard-pemasok.html | Dashboard pemasok |
| 11 | visily-notifikasi-pemasok.html | notifikasi.html | Notifikasi |
| 12 | visily-notifikasi-pemasok-1.html | notifikasi-1.html | Notifikasi variant |
| 13 | visily-multicomponents (1).png | components.html | Komponen UI |

## Arsitektur Navigasi

```
                    ┌─────────────────┐
                    │   login-karyawan │
                    └────────┬────────┘
                             │ (submit)
                    ┌────────▼────────┐
                    │   login-pemasok  │
                    └────────┬────────┘
                             │ (submit)
                    ┌────────▼────────┐
                    │   login-berhasil │
                    └────────┬────────┘
                             │ (klik button)
                    ┌────────▼────────┐
                    │      otp        │
                    └────────┬────────┘
                             │ (verify)
              ┌──────────────┼──────────────┐
              │              │              │
    ┌─────────▼────┐ ┌──────▼──────┐ ┌─────▼──────┐
    │ super-admin  │ │  dashboard  │ │   profil    │
    │              │ │  -pemasok  │ │  -pemasok  │
    └──────┬───────┘ └──────┬──────┘ └──────┬─────┘
           │                │               │
    ┌──────▼──────┐  ┌──────▼──────┐ ┌─────▼──────┐
    │ supplier-   │  │ notifikasi  │ │ notifikasi │
    │ list-admin │  │             │ │     -1     │
    └─────────────┘  └─────────────┘ └────────────┘
```

## Struktur Folder

```
D:\zahra1428.github.io\
├── plan.md
├── login-karyawan.html
├── login-pemasok.html
├── login-berhasil.html
├── login-berhasil-1.html
├── otp.html
├── super-admin.html
├── supplier-list-admin.html
├── supplier-approval-owner.html
├── profil-pemasok.html
├── dashboard-pemasok.html
├── notifikasi.html
├── notifikasi-1.html
├── components.html
└── style.css (shared styles)
```

## Spesifikasi Teknis

- **Viewport**: Mobile-first (max-width: 480px)
- **CSS**: Internal CSS atau file terpisah
- **Navigasi**: Link/button mengarahkan ke halaman lain
- **Font**: System font atau Google Fonts (Opsional)
- **Responsif**: Center layout pada layar lebih besar

## Tahap Pelaksanaan

### Tahap 1: Setup & Styling Dasar
- Buat style.css dengan reset CSS dan styling mobile
- Definisikan variabel warna dan typography

### Tahap 2: Halaman Login
- login-karyawan.html
- login-pemasok.html

### Tahap 3: Halaman OTP & Sukses Login
- otp.html
- login-berhasil.html
- login-berhasil-1.html

### Tahap 4: Dashboard & Profil Pemasok
- dashboard-pemasok.html
- profil-pemasok.html

### Tahap 5: Halaman Admin/Owner
- super-admin.html
- supplier-list-admin.html
- supplier-approval-owner.html

### Tahap 6: Notifikasi
- notifikasi.html
- notifikasi-1.html

### Tahap 7: Components
- components.html

### Tahap 8: Verifikasi & Linking
- Pastikan semua navigasi terhubung dengan benar

## Catatan
- Setiap halaman HTML akan meniru tampilan mockup PNG
- Interaksi hanya berupa navigasi antar halaman (prototype)
- Tidak ada logic fungsional seperti autentikasi, validasi, dll