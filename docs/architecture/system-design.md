# System Design — HireMatch AI

## Alur Utama Aplikasi

```
[User/HR]
   │
   ▼
[Upload CV] ──────────────────────────────────────────┐
   │                                                   │
   ▼                                                   ▼
[CV Parser Service]                         [Job Management]
   │  - Extract text (PDF/DOCX)                 - Buat lowongan
   │  - Parse sections                           - Set kriteria
   │  - Normalize data                           - Bobot nilai
   │
   ▼
[Candidate Profile]
   │
   ▼
[AI Matching Engine] ◄──────────── [Job Requirements]
   │  - Semantic similarity
   │  - Skill gap analysis
   │  - Score calculation
   │
   ▼
[Scoring & Recommendation]
   │  - Skor 0-100
   │  - Grade: A/B/C/D
   │  - Breakdown per kriteria
   │  - Rekomendasi AI
   │
   ▼
[HR Dashboard]
   - Shortlist kandidat
   - Filter & sort
   - Export laporan
   - Interview scheduling
```

## Data Flow

### Input CV
1. User upload file (PDF/DOCX/Image)
2. File disimpan ke storage
3. AI Engine mem-parse konten
4. Data tersimpan sebagai Candidate Profile

### Proses Matching
1. HR pilih job position
2. System ambil semua kandidat
3. AI Engine hitung skor per kandidat
4. Result diurutkan berdasarkan skor
5. HR lihat shortlist dengan rekomendasi

## Entitas Data Utama

- **Company** — Data perusahaan
- **Job Position** — Lowongan pekerjaan + kriteria
- **Criteria Template** — Template kriteria yang bisa dipakai ulang
- **Candidate** — Data pelamar
- **CV Document** — File CV + parsed data
- **Match Result** — Hasil pencocokan kandidat ↔ posisi
- **Score Breakdown** — Detail skor per kriteria
