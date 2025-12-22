---
layout: default
title: Instalasi
parent: Dokumentasi
nav_order: 1
---

# Instalasi

Panduan instalasi dan setup untuk menggunakan layanan QoutaID.

{: .fs-6 .fw-300 }

---

## Persyaratan

Sebelum memulai, pastikan kamu memiliki:

- Node.js versi 18 atau lebih baru
- npm atau yarn package manager
- Akun QoutaID yang sudah terverifikasi

## Langkah Instalasi

### 1. Clone Repository

```bash
git clone https://github.com/QoutaID/your-project.git
cd your-project
```

### 2. Install Dependencies

```bash
npm install
# atau
yarn install
```

### 3. Konfigurasi Environment

Buat file `.env` dengan konfigurasi berikut:

```env
QOUTA_API_KEY=your_api_key_here
QOUTA_SECRET=your_secret_here
```

### 4. Jalankan Aplikasi

```bash
npm run dev
# atau
yarn dev
```

---

## Troubleshooting

Jika mengalami masalah saat instalasi, cek halaman [FAQ](faq) atau hubungi tim support.
