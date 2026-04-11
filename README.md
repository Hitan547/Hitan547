# 🧠 Hitan K — AI Systems Engineer

<div align="center">

**Building production-grade AI systems with LLMs, ML pipelines, and full-stack architecture**

*Final-year CS undergrad (AI Specialization) · Bengaluru, India*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Hitan%20K-blue?style=for-the-badge&logo=linkedin)](https://linkedin.com/in/hitan-k)
[![GitHub](https://img.shields.io/badge/GitHub-Hitan547-black?style=for-the-badge&logo=github)](https://github.com/Hitan547)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-Hitan2004-yellow?style=for-the-badge&logo=huggingface)](https://huggingface.co/Hitan2004)
[![Email](https://img.shields.io/badge/Email-Contact-red?style=for-the-badge)](mailto:hitan.k@outlook.com)

*"Ship first, iterate always. Real systems, real users, real impact."*

</div>

---

## 🎯 Who I Am

I'm a final-year CS undergraduate specializing in AI who builds **production systems, not notebooks**. My focus is on:

- **GenAI & LLM Integration** — Building agent-based systems that actually work
- **Full-Stack ML** — From training to inference to real-time dashboards
- **Systems Engineering** — Docker, CI/CD, distributed architectures
- **Research** — Published work on LLM-based synthetic data augmentation

**Current:** Graduating May 2025 | **CGPA:** 7.9/10 | **Education:** DSATM, Bengaluru

---

## 🚀 Featured Projects

### 1. 🧠 Agentic Corrective RAG — Document Q&A with Self-Correction

**Live Demo:** [Frontend](https://hitan2004-agentic-corrective-rag-ui.hf.space) | [API](https://hitan2004-agentic-corrective-rag.hf.space) | [Docs](https://hitan2004-agentic-corrective-rag.hf.space/docs)

#### What It Does
A production-grade document Q&A system that answers questions **only from your uploaded documents**. Unlike naive RAG systems that hallucinate, this uses a self-correcting agent that:

- **Retrieves** with hybrid search (FAISS semantic + BM25 keyword)
- **Reranks** with cross-encoder for higher precision
- **Generates** answers using LLaMA 3.3 70B
- **Validates** every claim against source material
- **Retries** up to 3 times if validation fails
- **Returns** grounded answers with source chunks

#### Technical Highlights

**Architecture:**
- **Ingestion Pipeline** → PDF/TXT → PyMuPDF → Chunking (512 tokens, 20 overlap) → Embeddings
- **Hybrid Retrieval** → FAISS (dense) + BM25 (sparse) → RRF Fusion → Cross-Encoder Reranking
- **Corrective Agent** → LangGraph StateGraph with generate → validate → retry loop
- **Backend** → FastAPI with session memory + endpoint security
- **Frontend** → Static HTML/JS (separate HuggingFace Space)

**Retrieval Models:**
| Component | Model | Dimension | Purpose |
|-----------|-------|-----------|---------|
| Dense Embeddings | all-MiniLM-L6-v2 | 384 | Semantic similarity |
| Sparse Search | BM25 | inverted index | Keyword matching |
| Reranker | cross-encoder/ms-marco-MiniLM-L-6-v2 | score | Query-chunk interaction |

**Reasoning Engine:**
| Role | Model | API |
|------|-------|-----|
| Generation | LLaMA 3.3 70B | Groq |
| Validation | LLaMA 3.3 70B | Groq |

**Testing & CI/CD:**
✅ Unit tests (RRF fusion, reranking, config validation)  
✅ Integration tests (full pipeline, API, hallucination detection)  
✅ GitHub Actions CI with test separation (unit in CI, integration local-only)  
✅ Multi-service deployment (backend API + frontend UI on separate Spaces)  

**Advanced Features:**
- Hallucination detection with second validation LLM call
- Session memory (last 5 conversation turns per user)
- Reciprocal Rank Fusion (RRF) combining dense + sparse signals
- Synchronous indexing for consistency
- Proper error handling for external APIs
- Retry feedback loop (agent knows why it failed)

**Stack:** Python · FastAPI · LangGraph · FAISS · BM25 · Groq API · pytest · Docker · GitHub Actions · HuggingFace Spaces

**Repo:** [github.com/Hitan547/agentic-corrective-rag](https://github.com/Hitan547/agentic-corrective-rag)

---

### 2. 🛡️ SentinelNet — Real-Time Network Intrusion Detection System

**Live Demo:** [HuggingFace Spaces](https://huggingface.co/spaces/Hitan2004/sentinelnet)

#### What It Does
A full-stack ML system that detects network threats in real-time:

- **Live Monitor Tab** → Auto-generates NSL-KDD packets, runs inference, displays live threat timeline, attack distribution, activity heatmaps, confidence panels
- **CSV Analysis Tab** → Upload NSL-KDD CSVs, stream predictions with progress bar, auto-generate threat reports (risk gauge, distribution charts, attack patterns)
- **Multi-Format Export** → CSV, PDF report, JSON

#### Technical Highlights

**ML Pipeline:**
- **Dataset** → NSL-KDD (125K training, 22K test records, 41 features)
- **Model** → Random Forest (100 trees, 5-class classification)
- **Classes** → normal, DoS, Probe, R2L, U2R
- **Preprocessing** → One-hot encoding (protocol, flag) + frequency encoding (service) + log transforms (bytes/duration) + feature engineering (total_bytes, ratios, error flags) + standard scaling

**Feature Engineering Pipeline:**
```
Raw 41 features
    ↓
One-hot: protocol_type (tcp/udp/icmp) → 3 columns
One-hot: flag (11 variants) → 11 columns
Frequency: service → service rank
Log transforms: log(1 + src_bytes), log(1 + dst_bytes), log(1 + duration)
Engineering: total_bytes, src_bytes_ratio, is_error_flag
Standard scaling: (x - μ) / σ
    ↓
41 standardized features → Random Forest inference
```

**Serialization:**
- `sentinel_brain.joblib` (trained RF model)
- `ohe_encoder.joblib` (one-hot encoder)
- `freq_map.joblib` (service frequency dict)
- `scaler.joblib` (standard scaler)
- `label_encoder.joblib` + `selected_features.joblib`

**Backend:**
- Flask REST API with `/health` and `/predict` endpoints
- Batch inference with streaming predictions
- CORS handling for frontend communication
- Error handling and input validation

**Frontend:**
- Vanilla HTML/CSS/JavaScript (no frameworks)
- Canvas API for high-performance charting
- Real-time updates with WebSocket-style polling
- Responsive grid layout (desktop/tablet)
- 3-file architecture: index.html, style.css, app.js

**CI/CD:**
✅ GitHub Actions workflow  
✅ Python setup + dependency install  
✅ Syntax validation  
✅ Flask health check (with `SKIP_MODEL=true` to avoid model loading timeout)  
✅ Docker build test  
✅ Auto-deployment to HuggingFace Spaces  

**Advanced Engineering:**
- Handled CI failure due to model loading (introduced `SKIP_MODEL` env var)
- Health-check retry system
- Dockerized for cloud deployment
- Production-ready error boundaries

**Stack:** Python · Flask · scikit-learn · pandas · joblib · Vanilla JS · Canvas API · Docker · GitHub Actions · HuggingFace Spaces

**Repo:** [github.com/Hitan547/sentinelnet](https://github.com/Hitan547/sentinelnet)

---

## 🧪 Testing & Quality

### SentinelNet
- ✅ Model serialization validation
- ✅ Flask endpoint health checks
- ✅ Docker build verification
- ✅ CI integration with GitHub Actions

### Agentic Corrective RAG
- ✅ Unit tests: RRF fusion, reranking, config validation, chunk processing
- ✅ Integration tests: full pipeline, Groq API, hallucination detection
- ✅ CI/CD smart separation (unit in CI, expensive integration tests locally)
- ✅ pytest with `@pytest.mark.integration` decorator

**Philosophy:** Tests validate assumptions, prevent regressions, and enable confident refactoring. Cost-aware CI/CD prevents wasting API credits.

---

## 📚 Other Projects

### 🎓 Brain Buddy — AI-Powered PDF Learning Platform

**Live at:** [brainbuddy.vercel.app](https://brainbuddy.vercel.app)

Interactive learning experience for static PDFs:
- Context-aware conversational Q&A (RAG with Gemini API)
- Podcast-style audio summaries
- Auto-generated quizzes

**Stack:** TypeScript · React · Vite · Node.js · Express · MongoDB · Gemini API · Firebase · Vercel

---

### 🎤 PsySense — Multimodal AI Behavioral Interview Assessment Platform

Evaluates candidates through voice, video, and language (deployed live at startup):
- Whisper ASR + WebRTC video + librosa prosody
- Fine-tuned DistilBERT (28-label emotion classification)
- Weighted scoring: cognitive 50% + speech 30% + visual 20%
- Auto-generates PDF assessment reports
- SQLite + SQLAlchemy persistence

**Metrics:**
- Weak candidates: ~48/100
- Strong candidates: ~76/100
- **Discriminative gap:** 28 points

**Stack:** FastAPI · Groq · LLaMA 3.1 · DistilBERT · Whisper · WebRTC · librosa · Docker · AWS ECS

---

## 📖 Research

### Multi-Dataset Conditional Text Generation for Emotion Augmentation

**Published:** WCSC 2026 (Springer)

Designed an LLM-based synthetic data augmentation pipeline generating 100K+ training samples:
- Improved minority emotion-class representation by 2×–40×
- RoBERTa fine-tuning with Bayesian hyperparameter search

**Results:**
| Dataset | Before | After | Improvement |
|---------|--------|-------|-------------|
| GoEmotions | macro-F1 0.51 | 0.83 | +62% |
| TweetEval | macro-F1 0.71 | 0.79 | +11% |
| DAIR | macro-F1 0.90 | 0.97 | +8% |

Repo: [ github.com/Hitan547/sentinelnet](https://github.com/Hitan547/-project-conditional-text-generation-and-augmentation-for-sentiment-classification)
---

## 💻 Tech Stack

### GenAI & LLMs
**Production:** LangChain · LangGraph · RAG · Corrective RAG · Prompt Engineering  
**Platforms:** Groq · Gemini API · OpenAI · LLaMA · Fine-tuning

### NLP
**Transformers:** HuggingFace Transformers · DistilBERT · RoBERTa · Whisper  
**Tasks:** Text Classification · NER · Summarization · Sentence Embeddings

### Retrieval & Vector Databases
**Dense:** FAISS · all-MiniLM-L6-v2  
**Sparse:** BM25 · rank-bm25  
**Familiar:** Pinecone · Weaviate · ChromaDB

### Computer Vision
**Active:** OpenCV · WebRTC · PIL  
**Familiar:** CLIP · YOLOv8 · ViT

### Backend & APIs
**Frameworks:** FastAPI · Flask · Node.js/Express  
**Servers:** Uvicorn · Gunicorn  
**Patterns:** REST APIs · Async/await · Dependency injection

### Frontend
**Frameworks:** React · Vite · Vanilla JS/TypeScript  
**Styling:** Tailwind · CSS Grid/Flexbox  
**Visualization:** Canvas API · Recharts · D3

### MLOps & DevOps
**Containerization:** Docker · Docker Compose  
**CI/CD:** GitHub Actions · Automated testing  
**Version Control:** Git · GitHub  
**Deployment:** HuggingFace Spaces · Vercel · AWS ECS

### Cloud & Infrastructure
**Platforms:** AWS ECS · HuggingFace Spaces · Vercel · Firebase  
**Databases:** MongoDB · SQLite · SQL · SQLAlchemy  
**ML/DL:** PyTorch · scikit-learn · librosa · pandas · NumPy

---

## 📊 Career Metrics

| Metric | Value |
|--------|-------|
| **Published Papers** | 1 (WCSC 2026) |
| **Live Systems** | 4+ deployed projects |
| **Real Users** | 100+ beta testers |
| **Model Downloads** | 28-label DistilBERT publicly on HuggingFace |
| **GitHub Stars** | 50+ (SentinelNet) |
| **Production Deployments** | HuggingFace Spaces, AWS ECS, Vercel |

---

## 🎓 Education

**Bachelor of Engineering — Computer Science (AI Specialization)**  
Dayananda Sagar Academy of Technology and Management (DAYTM)  
**CGPA:** 7.9/10 | **Graduation:** May 2025

**Certifications:**
- 🎓 Natural Language Processing in TensorFlow (DeepLearning.AI)
- 🎓 Artificial Intelligence Fundamentals (IBM SkillsBuild)
- 🎓 Machine Learning for All (University of London)

---

## 🎯 Core Competencies

### AI/ML Systems Architecture
✅ Training ML models end-to-end  
✅ Feature engineering & preprocessing pipelines  
✅ Model serialization & serving  
✅ Real-time inference optimization  
✅ Batch processing with streaming updates  

### LLM-Based Systems
✅ Prompt engineering for diverse tasks  
✅ RAG (retrieval-augmented generation)  
✅ Agent-based reasoning loops  
✅ Hallucination detection & correction  
✅ Multi-turn conversation management  

### Full-Stack Development
✅ Backend: FastAPI, Flask, Node.js  
✅ Frontend: React, Vanilla JS, responsive design  
✅ Real-time dashboards: Canvas API, charting libraries  
✅ Database design: MongoDB, SQLite, SQL  

### DevOps & Production
✅ Docker containerization  
✅ GitHub Actions CI/CD  
✅ Cloud deployment (AWS, HuggingFace, Vercel)  
✅ Monitoring & logging  
✅ Cost-aware infrastructure decisions  

### Research & Innovation
✅ Literature review & experimental design  
✅ Hyperparameter tuning (Bayesian search, grid search)  
✅ Synthetic data generation  
✅ Publishing peer-reviewed work  

---

## 🔥 Key Achievements

**🏆 Technical Excellence**
- Built 4 production systems with real users
- Achieved 94% hallucination detection rate in RAG system
- Trained models with 28-point discriminative gap in emotion classification
- Optimized batch CSV processing to handle 100K+ records

**📖 Research Impact**
- Published paper on LLM-based synthetic data augmentation (Springer, WCSC 2026)
- Improved minority emotion classes by 2×–40× across 3 datasets
- Contributed to emotion AI field with novel augmentation approach

**🚀 Deployment & Scale**
- Live systems serving real users on HuggingFace, AWS, Vercel
- 100+ beta testers across projects
- Dogfooding my own systems (PsySense deployed at startup)

**💡 System Design**
- Designed multi-service architecture (backend + frontend separation)
- Implemented smart CI/CD test separation (cost optimization)
- Built self-correcting agent with validation loop (production reliability)

---

## 📝 Philosophy

> **"Ship first, iterate always."**

I believe in:
- **Real systems over toy projects** — Every project has real users or solves a real problem
- **Production-first mindset** — Code should be deployable, testable, maintainable
- **Continuous learning** — Ship → measure → learn → iterate
- **Depth over breadth** — Master core concepts rather than collect tools
- **Open-source contribution** — Build in public, help others learn

---

## 🤝 Let's Connect

I'm actively looking for opportunities to:
- Build AI systems at scale
- Contribute to open-source ML projects
- Collaborate on research
- Mentor other engineers

**Get in touch:**
- 💼 [LinkedIn](https://linkedin.com/in/hitan-k)
- 💻 [GitHub](https://github.com/Hitan547)
- 🤗 [HuggingFace](https://huggingface.co/Hitan2004)
- 📧 [Email](mailto:hitan.k@outlook.com)

---

<div align="center">

## 📌 Featured Repositories

| Project | Stars | Type | Live Demo |
|---------|-------|------|-----------|
| [Agentic Corrective RAG](https://github.com/Hitan547/agentic-corrective-rag) | ⭐⭐⭐ | RAG Agent | [API](https://hitan2004-agentic-corrective-rag.hf.space) |
| [SentinelNet](https://github.com/Hitan547/sentinelnet) | ⭐⭐⭐ | ML System | [Live](https://huggingface.co/spaces/Hitan2004/sentinelnet) |
| [Brain Buddy](https://github.com/Hitan547/brain-buddy) | ⭐⭐ | Full-Stack | [App](https://brainbuddy.vercel.app) |
| [PsySense](https://github.com/Hitan547/psysense) | ⭐⭐⭐ | Multimodal AI | Deployed |

---

**"Build systems that matter. Learn every day. Ship confidently."**

*Last updated: April 2026*

</div>
