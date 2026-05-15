# 🧠 HireMatch AI — HCM/HRD CV Matching Platform

> Platform cerdas untuk parsing, analisis, dan pencocokan CV/Resume dengan posisi pekerjaan menggunakan AI.

---

## 🎯 Deskripsi Proyek

HireMatch AI adalah aplikasi web berbasis AI yang membantu perusahaan/HRD dalam:
- **Memproses & mem-parsing** CV/Resume dari pelamar secara otomatis
- **Mencocokkan** kandidat dengan job description yang tersedia
- **Memberikan skor & rekomendasi** kesesuaian kandidat dengan posisi
- **Mengatur kriteria seleksi** secara fleksibel per posisi pekerjaan
- **Mempercepat proses rekrutmen** dengan shortlisting otomatis

---

## 🔍 Mengapa Kami Membangun HireMatch AI?

### 🔴 Masalah yang Kami Lihat

Proses rekrutmen di Indonesia — dan banyak negara berkembang lainnya — masih sangat manual dan tidak efisien. Setiap kali sebuah perusahaan membuka lowongan pekerjaan, tim HR langsung dibanjiri ratusan CV. Kondisi ini menciptakan masalah nyata:

- Satu lowongan bisa menerima **200–500+ lamaran** hanya dalam beberapa hari
- Tim HR menghabiskan **60–70% waktu kerja** hanya untuk membaca dan menyortir CV secara manual
- Penilaian manusia bersifat **tidak konsisten** — CV yang sama bisa dinilai berbeda oleh reviewer yang berbeda, bahkan oleh orang yang sama di waktu yang berbeda
- Kandidat berbakat sering **terlewat** karena tenggelam di tumpukan lamaran
- Perusahaan membuat **keputusan rekrutmen yang keliru** karena kriteria seleksi tidak pernah didefinisikan secara jelas
- Proses shortlisting memakan waktu **berminggu-minggu**, dan kandidat terbaik sudah diterima di tempat lain lebih dulu

### 💡 Inti Masalahnya

Masalah utamanya bukan karena terlalu banyak pelamar — melainkan karena **tidak ada sistem cerdas yang bisa menerjemahkan isi CV menjadi data terstruktur yang bisa dibandingkan secara objektif**.

CV adalah teks tidak terstruktur. Deskripsi pekerjaan juga ditulis dalam bahasa alami. Mencocokkan keduanya secara manual itu lambat, subjektif, dan rawan kesalahan.

**AI bisa menjadi jembatan di antara keduanya.** Model bahasa modern mampu membaca CV seperti seorang ahli HR senior — mengekstrak skills, level pengalaman, pendidikan, dan pencapaian — lalu menghitung secara tepat seberapa cocok seorang kandidat dengan posisi tertentu, berdasarkan kriteria yang perusahaan sendiri telah tentukan.

### ✅ Solusi yang Kami Tawarkan

HireMatch AI dibangun untuk memberikan setiap tim HR — dari startup 10 orang hingga perusahaan dengan 500+ karyawan — proses rekrutmen yang **adil, cepat, dan berbasis data**:

| Sebelum HireMatch | Dengan HireMatch |
|---|---|
| Baca 300 CV secara manual | AI memproses semua CV dalam hitungan menit |
| Penilaian tidak konsisten | Skor objektif 0–100 per kriteria yang ditentukan |
| Shortlist berdasarkan "perasaan" | Grade A/B/C/D dengan breakdown lengkap |
| Kriteria ada di kepala HR | Criteria Builder — transparan & bisa digunakan ulang |
| Kandidat terbaik bisa terlewat | Daftar ranking, tidak ada yang tenggelam |
| Butuh berminggu-minggu | Hasil shortlist di hari yang sama |

### 🚀 Visi Kami

HireMatch AI bukan sekadar pemindai CV. Ini adalah **platform intelijen rekrutmen penuh** — di mana perusahaan mendefinisikan sendiri apa arti "kandidat yang tepat" untuk setiap posisi, dan AI yang melakukan pekerjaan berat: menemukan, meranking, dan menjelaskan *mengapa* kandidat tersebut cocok atau tidak cocok.

> **Tujuan kami:** Memberikan kemampuan kepada setiap perusahaan untuk merekrut seperti tim HR terbaik di dunia — tanpa memandang ukuran atau sumber daya yang dimiliki.

---

## 🏗️ Arsitektur Proyek

```
hirematch-ai/
├── frontend/          # React/Vite - UI Web Application
├── backend/           # Node.js/Express - REST API Server
├── ai-engine/         # Python - AI/ML Services (CV Parser & Matcher)
├── docs/              # Dokumentasi, mockup, arsitektur
├── docker/            # Docker & Docker Compose configs
├── scripts/           # Utility scripts
└── .github/           # CI/CD workflows
```

---

## ✨ Fitur Utama

### 📄 CV Analyzer
- Upload CV (PDF, DOCX, JPG)
- Ekstraksi otomatis: nama, pendidikan, pengalaman, skills, sertifikasi
- Normalisasi format CV ke standar perusahaan

### 💼 Job Management
- Buat & kelola lowongan pekerjaan
- Atur kriteria wajib & opsional per posisi
- Bobot kriteria yang dapat dikustomisasi (skills, pengalaman, pendidikan)

### 🤖 AI Matching Engine
- Pencocokan kandidat ↔ posisi secara otomatis
- Skor kesesuaian (0-100) dengan breakdown per kriteria
- Rekomendasi: Sangat Direkomendasikan / Direkomendasikan / Pertimbangkan / Tidak Sesuai

### 📊 Dashboard & Analytics
- Overview pipeline rekrutmen
- Statistik kandidat per posisi
- Laporan & export data

### ⚙️ Pengaturan Kriteria
- Kriteria wajib (hard requirement)
- Kriteria preferensi (nice to have)
- Bobot nilai per kriteria
- Template kriteria yang bisa disimpan & digunakan ulang

---

## 🚀 Tech Stack

| Layer | Teknologi |
|-------|-----------|
| Frontend | React + Vite, Vanilla CSS |
| Backend | Node.js + Express |
| AI Engine | Python + LangChain / OpenAI API |
| Database | PostgreSQL + Redis (cache) |
| Storage | AWS S3 / Local Storage |
| Auth | JWT + Refresh Token |
| Deployment | Docker + Nginx |

---

## 📅 Roadmap Development

- [ ] **Phase 1**: Mockup & Design System
- [ ] **Phase 2**: Frontend (static)
- [ ] **Phase 3**: Backend API
- [ ] **Phase 4**: AI Engine integration
- [ ] **Phase 5**: Testing & QA
- [ ] **Phase 6**: Deployment & Hosting

---

## 👥 Tim
- Partner: Aswin Tresna
- AI Co-developer: Antigravity (Google DeepMind)
