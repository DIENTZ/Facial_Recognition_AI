# Facial_Recognition_AI
# 🤖 Facial Recognition AI - Sistem Pengenalan Wajah Web

![Project Status](https://img.shields.io/badge/status-active-success.svg)
![Node.js](https://img.shields.io/badge/Node.js-v18+-green.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

**FaceGuard AI** adalah aplikasi web modern untuk sistem keamanan dan absensi berbasis pengenalan wajah (*Face Recognition*). Dibangun dengan **Node.js** di sisi backend dan **face-api.js** (TensorFlow.js) di sisi frontend, aplikasi ini mampu mendeteksi dan mengenali wajah secara *real-time* langsung dari browser tanpa memerlukan hardware khusus.

![App Screenshot](Screenshot_path_here.png)

## ✨ Fitur Utama

* **⚡ Deteksi Real-time:** Memantau video stream dan mengenali wajah yang terdaftar secara instan.
* **📸 Smart Registration:** Menggunakan teknik *multi-sampling* (mengambil 10 sampel wajah) saat registrasi untuk meningkatkan akurasi *face descriptor*.
* **📂 Database JSON Flat-file:** Menggunakan sistem penyimpanan file JSON (`fs-extra`) yang ringan dan cepat, tanpa perlu setup database SQL/NoSQL yang rumit.
* **🆔 Stabilisasi Data:** Menampilkan data statis (Nama & Umur) dari database untuk menghindari fluktuasi prediksi AI (jitter).
* **🎨 UI Modern (Dark Mode):** Antarmuka responsif dengan desain *Glassmorphism* dan indikator visual interaktif.
* **🔒 Manajemen Data:** Kemudahan menambah dan menghapus data wajah langsung dari antarmuka pengguna.

## 🛠️ Teknologi yang Digunakan

* **Backend:** Node.js, Express.js
* **Frontend:** HTML5, CSS3 (Custom Properties & Animations), Vanilla JavaScript
* **AI/ML Engine:** [face-api.js](https://github.com/justadudewhohacks/face-api.js) (TensorFlow.js core)
* **Utilities:** fs-extra (File System), Body-Parser

## 🚀 Cara Menjalankan (Installation)

Ikuti langkah berikut untuk menjalankan proyek ini di komputer lokal Anda:

1.  **Clone Repository**
    ```bash
    git clone [https://github.com/username-anda/face-recognition-web.git](https://github.com/username-anda/face-recognition-web.git)
    cd face-recognition-web
    ```

2.  **Install Dependencies**
    Pastikan Anda sudah menginstall Node.js. Lalu jalankan:
    ```bash
    npm install
    ```

3.  **Download Model AI**
    Pastikan folder `public/models` sudah berisi model-model face-api (ssd_mobilenetv1, face_landmark_68, face_recognition, dll). *Catatan: Di repo ini folder models sudah disertakan.*

4.  **Jalankan Server**
    ```bash
    npm start
    ```
    Atau:
    ```bash
    node server.js
    ```

5.  **Buka Aplikasi**
    Buka browser dan akses: `http://localhost:3000`

## ⚙️ Struktur Folder

```text
face-recognition-web/
├── public/
│   ├── models/         # Model AI (TensorFlow Weights)
│   ├── app.js          # Logika Frontend & Face API
│   ├── index.html      # Antarmuka Utama
│   └── styles.css      # Styling (Dark Theme)
├── faces_db.json       # Database Wajah (Auto-generated)
├── server.js           # Backend Server (Express)
└── package.json        # Dependencies
