# Folder Structure — HireMatch AI

## Overview Lengkap

```
hirematch-ai/
│
├── 📁 frontend/                          # Web Application (React + Vite)
│   ├── 📁 public/                        # Static assets
│   ├── 📁 mockups/                       # Mockup HTML files (phase 1)
│   └── 📁 src/
│       ├── 📁 assets/
│       │   ├── icons/                    # SVG icons
│       │   ├── images/                   # Images & illustrations
│       │   └── fonts/                    # Custom fonts
│       │
│       ├── 📁 components/
│       │   ├── ui/                       # Reusable UI components
│       │   │   ├── Button.jsx
│       │   │   ├── Card.jsx
│       │   │   ├── Modal.jsx
│       │   │   ├── Badge.jsx
│       │   │   ├── ScoreRing.jsx         # Skor visualizer (donut)
│       │   │   ├── ProgressBar.jsx
│       │   │   └── FileUploader.jsx
│       │   │
│       │   ├── layout/                   # Layout components
│       │   │   ├── Navbar.jsx
│       │   │   ├── Sidebar.jsx
│       │   │   └── PageWrapper.jsx
│       │   │
│       │   ├── cv/                       # CV-related components
│       │   │   ├── CVUploader.jsx        # Upload zone
│       │   │   ├── CVPreview.jsx         # Preview parsed CV
│       │   │   ├── CVSection.jsx         # Tampilkan section CV
│       │   │   └── ExtractedData.jsx     # Data hasil ekstraksi
│       │   │
│       │   ├── jobs/                     # Job management components
│       │   │   ├── JobCard.jsx
│       │   │   ├── JobForm.jsx
│       │   │   ├── CriteriaBuilder.jsx   # Builder kriteria seleksi
│       │   │   └── CriteriaWeight.jsx    # Pengatur bobot kriteria
│       │   │
│       │   └── analytics/               # Dashboard & charts
│       │       ├── ScoreCard.jsx
│       │       ├── FunnelChart.jsx
│       │       └── CandidateTable.jsx
│       │
│       ├── 📁 pages/
│       │   ├── auth/
│       │   │   ├── Login.jsx
│       │   │   └── Register.jsx
│       │   │
│       │   ├── dashboard/
│       │   │   └── Dashboard.jsx         # Overview rekrutmen
│       │   │
│       │   ├── cv-analyzer/
│       │   │   ├── Upload.jsx            # Upload CV page
│       │   │   ├── Analysis.jsx          # Hasil analisis CV
│       │   │   └── BatchUpload.jsx       # Upload massal
│       │   │
│       │   ├── jobs/
│       │   │   ├── JobList.jsx           # Daftar lowongan
│       │   │   ├── JobDetail.jsx         # Detail + kandidat list
│       │   │   └── JobCreate.jsx         # Buat lowongan baru
│       │   │
│       │   ├── candidates/
│       │   │   ├── CandidateList.jsx     # Semua kandidat
│       │   │   └── CandidateProfile.jsx  # Profil + skor kandidat
│       │   │
│       │   ├── reports/
│       │   │   └── Reports.jsx           # Laporan & export
│       │   │
│       │   └── settings/
│       │       ├── Company.jsx           # Pengaturan perusahaan
│       │       ├── Criteria.jsx          # Template kriteria
│       │       └── Users.jsx             # Manajemen user HR
│       │
│       ├── 📁 hooks/                     # Custom React hooks
│       │   ├── useCV.js
│       │   ├── useJobs.js
│       │   └── useAuth.js
│       │
│       ├── 📁 services/                  # API calls
│       │   ├── api.js                    # Axios instance
│       │   ├── cv.service.js
│       │   ├── jobs.service.js
│       │   └── auth.service.js
│       │
│       ├── 📁 store/                     # State management
│       │   ├── authStore.js
│       │   ├── cvStore.js
│       │   └── jobStore.js
│       │
│       ├── 📁 utils/                     # Helper functions
│       │   ├── scoreHelper.js
│       │   ├── formatters.js
│       │   └── validators.js
│       │
│       ├── 📁 types/                     # TypeScript types / JSDoc
│       │   ├── candidate.types.js
│       │   ├── job.types.js
│       │   └── criteria.types.js
│       │
│       ├── App.jsx
│       ├── main.jsx
│       └── index.css                     # Global styles & design tokens
│
├── 📁 backend/                           # REST API Server (Node.js)
│   ├── 📁 src/
│   │   ├── 📁 api/
│   │   │   ├── routes/
│   │   │   │   ├── auth.routes.js
│   │   │   │   ├── cv.routes.js
│   │   │   │   ├── jobs.routes.js
│   │   │   │   ├── candidates.routes.js
│   │   │   │   └── reports.routes.js
│   │   │   │
│   │   │   ├── middlewares/
│   │   │   │   ├── auth.middleware.js    # JWT verification
│   │   │   │   ├── upload.middleware.js  # Multer file upload
│   │   │   │   └── rateLimiter.js
│   │   │   │
│   │   │   └── validators/              # Request validation
│   │   │       ├── cv.validator.js
│   │   │       └── jobs.validator.js
│   │   │
│   │   ├── 📁 services/
│   │   │   ├── cv-parser/
│   │   │   │   ├── pdfParser.js         # Parse PDF files
│   │   │   │   ├── docxParser.js        # Parse DOCX files
│   │   │   │   └── imageOCR.js          # OCR untuk gambar
│   │   │   │
│   │   │   ├── ai-matcher/
│   │   │   │   ├── matcher.service.js   # Koordinator matching
│   │   │   │   └── aiClient.js          # Client ke AI Engine
│   │   │   │
│   │   │   ├── scoring/
│   │   │   │   ├── scorer.js            # Kalkulasi skor
│   │   │   │   └── grader.js            # A/B/C/D grading
│   │   │   │
│   │   │   └── notifications/
│   │   │       └── email.service.js
│   │   │
│   │   ├── 📁 models/                   # Database models (ORM)
│   │   │   ├── Company.model.js
│   │   │   ├── User.model.js
│   │   │   ├── JobPosition.model.js
│   │   │   ├── Criteria.model.js
│   │   │   ├── Candidate.model.js
│   │   │   ├── CVDocument.model.js
│   │   │   └── MatchResult.model.js
│   │   │
│   │   ├── 📁 config/
│   │   │   ├── database.js
│   │   │   ├── redis.js
│   │   │   └── storage.js
│   │   │
│   │   ├── 📁 utils/
│   │   │   ├── logger.js
│   │   │   └── response.js
│   │   │
│   │   └── app.js                       # Express app entry
│   │
│   ├── 📁 tests/
│   │   ├── unit/
│   │   └── integration/
│   │
│   └── package.json
│
├── 📁 ai-engine/                         # AI/ML Service (Python)
│   ├── 📁 models/                        # AI model configs
│   ├── 📁 prompts/                       # LLM prompt templates
│   │   ├── cv_extractor.txt             # Prompt untuk ekstrak CV
│   │   ├── job_matcher.txt              # Prompt untuk matching
│   │   └── score_explainer.txt          # Prompt untuk penjelasan skor
│   │
│   ├── 📁 utils/
│   │   ├── text_cleaner.py
│   │   └── similarity.py
│   │
│   ├── main.py                          # FastAPI server
│   ├── cv_parser.py                     # CV parsing logic
│   ├── job_matcher.py                   # Matching logic
│   └── requirements.txt
│
├── 📁 docs/
│   ├── 📁 mockups/                      # Design mockup files
│   ├── 📁 api/                          # API documentation
│   └── 📁 architecture/                 # Arsitektur & diagram
│
├── 📁 docker/
│   ├── Dockerfile.frontend
│   ├── Dockerfile.backend
│   ├── Dockerfile.ai-engine
│   └── nginx.conf
│
├── 📁 scripts/
│   ├── setup.sh                         # Setup development env
│   └── seed.js                          # Seed data dummy
│
├── 📁 .github/
│   └── workflows/
│       └── ci.yml                       # CI/CD pipeline
│
├── docker-compose.yml
├── .env.example
├── .gitignore
└── README.md
```

## Urutan Development

### Phase 1 — Mockup (Sekarang)
1. `frontend/mockups/` — HTML mockup statis semua halaman
2. `docs/mockups/` — Screenshot & catatan desain

### Phase 2 — Frontend
1. Setup Vite + React
2. Design system di `index.css`
3. Komponen UI
4. Halaman-halaman

### Phase 3 — Backend
1. Setup Express
2. Database schema & models
3. API routes
4. File upload & CV parsing

### Phase 4 — AI Engine
1. Setup FastAPI Python
2. Integrasi LLM (OpenAI/local)
3. Prompt engineering
4. Scoring algorithm

### Phase 5 — Integration & Deploy
1. Sambungkan frontend ↔ backend ↔ AI
2. Docker setup
3. Deployment ke VPS/Cloud
