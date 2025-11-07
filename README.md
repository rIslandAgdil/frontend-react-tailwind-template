# ⚛️ Frontend Template: React.js (Feature-Based Architecture)

[![React Version](https://img.shields.io/badge/React-18.x-61DAFB.svg?style=flat&logo=react)](https://reactjs.org/)
[![Router Version](https://img.shields.io/badge/React_Router-6.x-FC4661.svg)](https://reactrouter.com/en/main)
[![Axios Version](https://img.shields.io/badge/Axios-1.x-informational.svg)](https://axios-http.com/)
[![License](https://img.shields.io/badge/License-ISC-brightgreen.svg)](LICENSE)

Templat _frontend_ React modern yang menggunakan arsitektur berbasis fitur (**Feature-Based**) untuk memisahkan logika bisnis dan UI. Memastikan skalabilitas, _code reuse_, dan pemeliharaan yang mudah.

---

## 📦 Teknologi Kunci yang Digunakan

- **Framework:** React 18+ (dengan Hooks)
- **Routing:** React Router v6
- **API Client:** Axios (untuk komunikasi HTTP)
- **Styling:** CSS Modules / SCSS (tergantung pilihan Anda)
- **State Management:** React Context API (default, dapat diperluas ke Redux/Zustand)

---

## 🛠️ Persiapan dan Instalasi

### 1. Kloning Repositori

````bash
git clone <URL_REPOSITORY_ANDA>
cd frontend-app

2. Instalasi Dependensi

Bash

npm install
# atau
yarn install

3. Konfigurasi Lingkungan (.env)

Buat file .env di root proyek. Variabel di React harus diawali dengan VITE_ (jika menggunakan Vite) atau REACT_APP_ (jika menggunakan Create React App).
Cuplikan kode

# URL Backend (Pastikan menggunakan protokol yang benar: http/https)
VITE_API_BASE_URL=http://localhost:5000/api

# Pengaturan lainnya
VITE_APP_NAME="Nama Aplikasi Anda"

(Gunakan process.env.VITE_API_BASE_URL di kode Anda.)

▶️ Menjalankan Aplikasi

Mode Pengembangan (Development)

Menjalankan server pengembangan lokal:
Bash

npm run dev
# atau
yarn dev

Aplikasi akan berjalan di: http://localhost:5173 (atau port default Vite/CRA Anda).

Membangun untuk Produksi (Build)

Membuat bundle produksi ke folder /dist atau /build:

```bash
npm run build
````

## 💻 Struktur Folder Inti

Kami menggunakan struktur yang berorientasi pada fitur untuk memisahkan logika dan UI dengan jelas.

```
frontend-app/
├── node_modules/         # Library yang diinstal (diabaikan oleh Git)
├── public/               # File statis yang tidak diproses (index.html, favicon)
│   └── favicon.ico
│
├── src/                  # Semua kode sumber aplikasi
│   ├── assets/           # Media dan aset statis
│   │
│   ├── components/       # Komponen generik/UI (Shared/Presentational)
│   │
│   ├── context/          # State Management global menggunakan Context API
│   │
│   ├── hooks/            # Hooks kustom yang bersifat generik
│   │
│   ├── pages/            # Komponen utama yang di-render oleh React Router
│   │
│   ├── services/         # Logika komunikasi API (Axios instance dan fungsi API)
│   │
│   ├── App.jsx           # Komponen utama (Router utama diletakkan di sini)
│   └── main.jsx          # Entry point aplikasi (ReactDOM.createRoot)
│
├── .gitignore
├── package.json
└── README.md
```

## 🧪 Testing

Proyek ini terkonfigurasi untuk menggunakan Jest dan React Testing Library (RTL).

Menjalankan Test

```bash
npm test
```

- Fokus testing harus pada:

  - Unit Test pada fungsi helper dan hooks di src/hooks/ dan src/utils/.

  - Rendering Test pada komponen di src/components/ (memastikan elemen muncul).

## 🤝 Kontribusi

Kami menyambut kontribusi!
