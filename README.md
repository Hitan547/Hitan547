<div align="center">

# Hey, I'm Hitan K 👋

**Final-year CS undergrad (AI specialisation) · Bengaluru, India**

I build production AI systems — not just notebooks. Multimodal pipelines, RAG backends, full-stack AI apps with real users.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/hitan-k)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat&logo=huggingface&logoColor=black)](https://huggingface.co/Hitan2004)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:hitank2004@gmail.com)

</div>

---

## About me

- 🏗️ Currently building **PsySense** — a multimodal AI interview platform deployed live at a Bengaluru startup
- 📄 Co-authored a **Springer-published paper** (WCSC 2026) on LLM-based emotion data augmentation
- 🤗 Published a production model on HuggingFace: [`Hitan2004/psysense-emotion-ai`](https://huggingface.co/Hitan2004/psysense-emotion-ai) — 28-label DistilBERT emotion classifier actively serving a REST API
- 🎯 Strongest in: **GenAI / LLM integration · NLP / HuggingFace · FastAPI backend engineering · end-to-end deployment**
- 🎓 B.E. Computer Science — AI Specialisation · CGPA 7.9 · Dayananda Sagar Academy of Technology and Management

---

## Projects

### 🧠 PsySense — Multimodal AI Behavioral Interview Assessment Platform
> *FastAPI · Groq · LLaMA 3.1 · DistilBERT · Whisper · WebRTC · librosa · Docker · AWS ECS*

A **5-microservice production backend** deployed live at a startup. Evaluates candidates through voice, video, and language — all in real time.

- **Whisper ASR + WebRTC video + librosa prosody** → unified weighted score (cognitive 50%, speech 30%, visual 20%)
- Fine-tuned DistilBERT for 28-label emotion classification, serving predictions via REST API
- Discriminative gap validated: weak candidates ~48/100 · strong candidates ~76/100 **(28-point gap)**
- Auto-generates PDF assessment reports · SQLite + SQLAlchemy persistence · containerised with Docker · migrating to AWS ECS

---

### 📚 Brain Buddy — AI-Powered PDF Learning Platform
> *TypeScript · React · Vite · Node.js · Express · MongoDB · Gemini API · Firebase · Vercel*

**Live at [brainbuddy.vercel.app](https://brainbuddy.vercel.app)** — real users, real deployments.

Transforms static PDFs into interactive learning experiences via:
- Context-aware conversational Q&A (RAG over chunked PDF content using Gemini API)
- Podcast-style audio summaries
- Auto-generated quizzes

Node.js/Express REST backend · MongoDB persistence · Firebase auth · ImageKit + Cloudinary CDN · **GitHub Actions CI/CD — zero-downtime on every push**

---

### 🛡️ SentinelNet — Real-Time AI Network Intrusion Detection System
> *Python · Flask · scikit-learn · Docker · Vanilla JS · HuggingFace Spaces*

**Live on [HuggingFace Spaces](https://huggingface.co/Hitan2004)**

- Flask REST API serving a **Random Forest classifier for 5-class threat detection** (DoS, Probe, R2L, U2R, normal) on NSL-KDD 41-feature data
- Full preprocessing pipeline serialised with joblib (OHE · frequency encoding · log transforms · standard scaling)
- Real-time JS dashboard: live threat timeline · activity heatmap · confidence panels · batch CSV analysis
- Reports exportable as CSV / PDF / JSON · **Dockerised**

---

## Research

### 📑 Multi-Dataset Conditional Text Generation for Emotion Augmentation
> *Published · WCSC 2026 · Springer*

- Designed an **LLM-based synthetic data augmentation pipeline** generating **100K+ training samples**
- Improved minority emotion-class representation by **2×–40×** across multiple NLP benchmarks
- **RoBERTa fine-tuning with Bayesian hyperparameter search:**

| Dataset | Before | After |
|---|---|---|
| GoEmotions | macro-F1 0.51 | **0.83** |
| TweetEval | macro-F1 0.71 | **0.79** |
| DAIR | macro-F1 0.90 | **0.97** |

---

## Tech stack

```text
GenAI & LLMs     LangChain · LangGraph · RAG · Corrective RAG · Prompt Engineering
                 Groq · Gemini API · OpenAI · LLaMA · Fine-tuning

NLP              HuggingFace Transformers · DistilBERT · RoBERTa · Whisper
                 Sentence Transformers · Text Classification · NER · Summarisation

Vector DBs       ChromaDB · FAISS  (familiar: Pinecone · Weaviate)

Computer Vision  OpenCV · WebRTC video · PIL  (familiar: CLIP · YOLOv8 · ViT)

Backend          FastAPI · Flask · Node.js · Express · REST APIs · Uvicorn · Async

Frontend         React · Vite · Streamlit · Vanilla JS · TypeScript

MLOps            Docker · GitHub Actions CI/CD · Git · Linux · HuggingFace Hub

Cloud            AWS ECS (active) · Vercel · Firebase

Databases        MongoDB · SQLite · SQL · SQLAlchemy

ML/DL            PyTorch · scikit-learn · librosa · pandas · NumPy
```

---

## Certifications

- 🎓 Natural Language Processing in TensorFlow — **DeepLearning.AI**
- 🎓 Artificial Intelligence Fundamentals — **IBM SkillsBuild**
- 🎓 Machine Learning for All — **University of London**

---

<div align="center">

*"Ship first, iterate always."*

![Profile views](https://komarev.com/ghpvc/?username=Hitan547&color=185FA5&style=flat)

</div>
