# 📘 Atmos API Documentation Server

## Server Dokumentasi API Siap Production

Sebuah **server dokumentasi API modern, aman, dan scalable** yang dibangun menggunakan **NestJS v11** dan didukung oleh **Scalar API Reference**.

Project ini dirancang untuk menyediakan **infrastruktur dokumentasi API yang rapi dan production-grade**, lengkap dengan validasi terstruktur, logging terpusat, dan security hardening.

> Cocok untuk tim engineering yang ingin dokumentasi API yang bersih, profesional, dan mudah dikelola tanpa konfigurasi Swagger yang berantakan.
> Ringan, modular, dan siap digunakan di environment production.

![NestJS](https://img.shields.io/badge/NestJS-11-red?logo=nestjs\&style=flat-square)
![Scalar](https://img.shields.io/badge/API%20Docs-Scalar-yellow?style=flat-square)
![Swagger](https://img.shields.io/badge/OpenAPI-Swagger-green?logo=swagger\&style=flat-square)
![TypeScript](https://img.shields.io/badge/TypeScript-5.x-blue?logo=typescript\&style=flat-square)
![Winston](https://img.shields.io/badge/Logger-Winston-black?style=flat-square)
![Helmet](https://img.shields.io/badge/Security-Helmet-lightgrey?style=flat-square)
![Supabase](https://img.shields.io/badge/Backend-Supabase-3ECF8E?logo=supabase\&style=flat-square)

---

## 🧩 Requirements

* **Node.js ≥ 22 (LTS direkomendasikan)**
* npm ≥ 10

> Untuk production sangat disarankan menggunakan Node.js versi LTS agar stabil dan mendapat dukungan jangka panjang.

---

## 🎯 Overview

`atmos-api-documentation` adalah **server khusus untuk dokumentasi API** yang dibangun menggunakan:

* **NestJS** sebagai backend framework modular dan scalable
* **Scalar** untuk tampilan dokumentasi API yang modern dan interaktif
* **Swagger (OpenAPI)** untuk standar schema API
* **Winston** untuk structured logging
* **Helmet** untuk pengamanan HTTP header
* **Supabase** client untuk integrasi backend

Server ini membantu menjaga **konsistensi dokumentasi API**, memastikan semua endpoint terdokumentasi dengan standar yang sama dan mudah diakses oleh tim frontend, QA, maupun integrator eksternal.

---

## ✨ Fitur Utama

### 📚 Dokumentasi API Modern

* Auto-generate OpenAPI schema menggunakan `@nestjs/swagger`
* UI dokumentasi interaktif berbasis Scalar
* Dokumentasi yang cepat, ringan, dan searchable
* Dukungan DTO-driven schema
* Endpoint non-API dapat dikecualikan dari dokumentasi

---

### 🛡️ Keamanan & Hardening

* Proteksi HTTP header menggunakan **Helmet**
* Dukungan compression untuk performa
* Validasi request menggunakan `class-validator`
* Transformasi data menggunakan `class-transformer`
* Environment-based configuration

---

### 📊 Logging & Monitoring

* Logging terstruktur menggunakan **Winston**
* Dukungan `nest-winston` untuk integrasi dengan NestJS
* Pemisahan log error dan log gabungan
* Mudah diintegrasikan ke sistem observability (ELK, Grafana, dsb.)

Script monitoring log:

```bash
npm run logs:dev
npm run logs:error
```

---

### 🔗 Integrasi Backend

* Client **Supabase** tersedia untuk integrasi data
* Struktur modular sehingga mudah dikembangkan
* Cocok sebagai centralized API documentation service

---

## ⚙️ Environment Configuration

Copy file environment:

```bash
cp .env.example .env
```

### 📄 .env.example

```dotenv
PORT=3000
APP_VERSION=1.0.0
APP_NAME=ATMOS-API
NODE_ENV=development

SUPABASE_URL=your-supabase-url
SUPABASE_ANON_KEY=your-supabase-anon-key

LOG_LEVEL=debug
LOG_FORMAT=pretty
```

---

## ⚡ Quick Start

Clone repository:

```bash
git clone <repository-url>
cd atmos-api-documentation
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

---

## 🧪 Testing

```bash
npm run test
npm run test:watch
npm run test:cov
npm run test:e2e
```

---

## 🎯 Use Cases

* Dokumentasi API internal perusahaan
* Centralized API documentation gateway
* Developer portal untuk tim frontend
* Standarisasi dokumentasi microservices
* Portal dokumentasi untuk partner eksternal

---

## 📜 License

UNLICENSED
© 2026 — Atmos API Documentation Server
