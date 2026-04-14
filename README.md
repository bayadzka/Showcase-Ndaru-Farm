# 🌾 Ndaru Farm Backend API

## Core API Server untuk Ekosistem Agritech

Sebuah **backend API modern, aman, dan scalable** yang dibangun menggunakan **NestJS**. Sistem ini bertindak sebagai tulang punggung (core engine) untuk platform agritech Ndaru Farm.

Project ini dirancang untuk mengelola alur data e-commerce secara komprehensif, mulai dari manajemen produk pertanian, pemesanan jasa, hingga integrasi pembayaran otomatis menggunakan payment gateway.

> Cocok untuk mendukung ekosistem aplikasi pertanian digital yang membutuhkan pemrosesan transaksi yang cepat, aman, dan pencatatan data yang terstruktur.
> Dirancang secara modular agar mudah dikembangkan (*scalable*) untuk kebutuhan bisnis di masa depan.

-----

## 🧩 Requirements

  * **Node.js ≥ 20 (LTS direkomendasikan)**
  * npm ≥ 10

> Untuk *production*, sangat disarankan menggunakan Node.js versi LTS agar stabil dalam menangani proses transaksi *payment gateway*.

-----

## 🎯 Overview

`NDARU-FARM-BACKEND` adalah **server utama** yang melayani aplikasi *frontend* Ndaru Farm. Arsitektur ini dibangun menggunakan:

  * **NestJS** sebagai framework *backend* modular berbasis TypeScript.
  * **Midtrans SDK** untuk menangani *webhook* dan otomatisasi sistem pembayaran klien.
  * **Swagger (OpenAPI)** untuk menghasilkan dokumentasi API (*endpoint*) secara otomatis bagi tim *frontend*.
  * **Class-Validator & Class-Transformer** untuk memastikan validitas data *payload* transaksi.

Server ini memastikan semua logika bisnis dari operasional Ndaru Farm berjalan dengan presisi dan aman dari sisi *server-side*.

-----

## ✨ Fitur Utama

### 🌱 Manajemen Data Agritech Terpusat

  * Endpoint lengkap untuk pengelolaan katalog jual beli sayuran segar.
  * Sistem manajemen *booking* untuk layanan jasa pertanian dan pelatihan masyarakat umum.
  * Inventarisasi penyediaan sarana pertanian.

### 💳 Integrasi Payment Gateway (Midtrans)

  * *Generate* Virtual Account (VA), QRIS, dan metode pembayaran lainnya secara instan.
  * Penanganan *Callback/Webhook* yang aman untuk *auto-update* status transaksi.
  * Sistem rekonsiliasi data pembayaran.

### 🛡️ Keamanan & Validasi

  * Proteksi rute menggunakan sistem autentikasi (JWT/Session).
  * Validasi *input request* menggunakan `class-validator` untuk mencegah manipulasi data.
  * Environment-based configuration untuk memisahkan *key* Midtrans mode *Sandbox* dan *Production*.

-----

## ⚙️ Environment Configuration

Copy file environment:

```bash
cp .env.example .env
```

### 📄 .env.example

```dotenv
PORT=8080
APP_VERSION=1.0.0
APP_NAME=NDARU-FARM-API
NODE_ENV=development

# Database Configuration
DATABASE_URL=your-database-connection-url

# Midtrans Configuration
MIDTRANS_IS_PRODUCTION=false
MIDTRANS_SERVER_KEY=your-midtrans-server-key
MIDTRANS_CLIENT_KEY=your-midtrans-client-key

# JWT / Security
JWT_SECRET=your-super-secret-key
```

-----

## ⚡ Quick Start

Clone repository:

```bash
git clone <repository-url>
cd NDARU-FARM-BACKEND
npm install
```

Jalankan development server:

```bash
npm run start:dev
```

Build untuk production:

```bash
npm run build
npm run start:prod
```

-----

## 🧪 Testing

```bash
npm run test
npm run test:watch
npm run test:cov
npm run test:e2e
```

-----

## 🎯 Use Cases

  * Sistem *backend* untuk aplikasi e-commerce produk pertanian.
  * Platform manajemen penjadwalan *training* atau penyuluhan petani.
  * Integrasi *headless commerce* yang membutuhkan pemrosesan pembayaran otomatis.

-----

## 📜 License

UNLICENSED
© 2026 — Ndaru Farm Development Team
