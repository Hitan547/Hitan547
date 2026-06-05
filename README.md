<div align="center">

# Hitan K

### Applied AI/ML Engineer · LLM & RAG Systems · Production ML & MLOps

<p>
  <a href="https://github.com/Hitan547">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=18&duration=2800&pause=1000&color=58A6FF&center=true&vCenter=true&multiline=true&repeat=true&width=700&height=70&lines=Building+production+RAG+systems+with+self-correction+%26+hallucination+control;3+deployed+RAG+pipelines+%C2%B7+Published+NLP+research+%C2%B7+Multimodal+AI+systems" alt="Typing SVG" />
  </a>
</p>

<p>
  <a href="https://linkedin.com/in/hitan-k"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="https://huggingface.co/Hitan2004"><img src="https://img.shields.io/badge/Hugging_Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" alt="Hugging Face" /></a>
  <a href="mailto:hitan.k@outlook.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
</p>

<img src="https://komarev.com/ghpvc/?username=Hitan547&style=flat-square&color=58A6FF&label=Profile+Views" alt="Profile Views" />

</div>

---

## 🧑‍💻 About

CS graduate with an AI specialization who builds **deployed AI systems**, not just notebooks.

- **3 production RAG pipelines** — hybrid retrieval, cross-encoder reranking, LangGraph self-correction, hallucination guardrails
- **Published NLP research** — Springer LNCS on LLM-based synthetic data augmentation for emotion classification
- **Multimodal AI products** — interview assessment using text, speech, prosody, and video signals
- **Full production stack** — FastAPI/Flask APIs, Docker, CI/CD, pytest, Hugging Face Spaces, Vercel, AWS serverless

<p>
  <strong>Open to:</strong> AI/ML Engineer · Applied AI Engineer · GenAI/LLM Engineer · NLP Engineer · MLOps Engineer roles
</p>

---

## 🔍 RAG Systems — Retrieval-Augmented Generation

> **Core specialization.** Each project demonstrates a progressively more advanced retrieval + generation + validation architecture.

<table>
<tr>
<td width="33%" valign="top">

### [Agentic Corrective RAG](https://github.com/Hitan547/agentic-corrective-rag)
**Self-correcting document QA**

Production RAG with agentic self-correction loop that detects hallucinations and retries with refined retrieval.

`ChromaDB` `BM25` `RRF Fusion` `Cross-Encoder` `LangGraph` `LLaMA 3.3 70B` `Groq` `FastAPI` `MCP Tools` `RAGAS Eval` `Docker` `CI/CD`

[![Demo](https://img.shields.io/badge/Live-HF_Space-FF9D00?style=flat-square&logo=huggingface)](https://huggingface.co/spaces/Hitan2004/agentic-corrective-rag)

</td>
<td width="33%" valign="top">

### [BIS Standards RAG](https://github.com/Hitan547/BIS-Standards-RAG)
**Standards code recommendation engine**

Maps building material descriptions to BIS/IS codes. Built for the BIS × SS Hackathon 2026.

`FAISS` `BGE Embeddings` `BM25` `RRF Fusion` `Query Expansion` `Cross-Encoder` `LangGraph` `LLaMA 3.3 70B` `Streamlit`

**100% Hit Rate @3 · 0.95 MRR @5 · 3.46s latency**

</td>
<td width="33%" valign="top">

### [Proanalyst RAG Bot](https://github.com/Hitan547/Proanalyst_Hitan_k_rag)
**API documentation support bot**

Source-grounded Upwork API assistant with deterministic guardrails and hallucination fallback.

`ChromaDB` `MiniLM` `DeepInfra Meta-LLaMA` `Streamlit` `Guardrails` `Chunk Traceability`

[![Demo](https://img.shields.io/badge/Live-Streamlit-FF4B4B?style=flat-square&logo=streamlit)](https://proanalysthitank-p9xvkrnqrj9ahyey5xmh3a.streamlit.app/)
**36/36 eval pass · Source traceability**

</td>
</tr>
</table>

<details>
<summary><b>📊 RAG Architecture Comparison</b></summary>
<br/>

| Capability | Agentic Corrective RAG | BIS Standards RAG | Proanalyst RAG |
|:---|:---:|:---:|:---:|
| **Retrieval** | ChromaDB + BM25 + RRF | FAISS + BM25 + RRF | ChromaDB semantic |
| **Reranking** | Cross-Encoder | Cross-Encoder | Lexical rerank |
| **LLM** | LLaMA 3.3 70B (Groq) | LLaMA 3.3 70B (Groq) | Meta-LLaMA (DeepInfra) |
| **Self-Correction** | ✅ LangGraph retry loop | ✅ LangGraph corrective agent | ✅ Hallucination guardrails |
| **Evaluation** | RAGAS + pytest | Hit Rate + MRR | 36-question eval set |
| **Deployment** | HF Space + Docker + CI | Streamlit | Streamlit Cloud |
| **API** | FastAPI + SSE streaming | — | — |
| **Sessions** | SQLite memory | — | — |
| **MCP Tools** | ✅ | — | — |

</details>

---

## 🧠 NLP, NLU & Research

<table>
<tr>
<td width="50%" valign="top">

### [Conditional Text Generation for Emotion Classification](https://github.com/Hitan547/-project-conditional-text-generation-and-augmentation-for-sentiment-classification)
📄 **Published — Springer LNCS, WCSC 2026**

Novel approach using LLM-based conditional text generation to synthesize minority-class samples, solving class imbalance in emotion datasets. Generated **100K+ synthetic training samples**.

`PyTorch` `RoBERTa` `SmolLM` `Optuna` `GoEmotions` `TweetEval` `DAIR`

</td>
<td width="50%" valign="top">

### [GoEmotions Emotion Classifier](https://github.com/Hitan547/GoEmotions_Emotion_Classifier)
Transformer-based multi-label emotion classification using DistilBERT trained on GoEmotions to detect **overlapping human emotions** in text.

`DistilBERT` `Transformers` `Multi-Label Classification` `Jupyter`

### [PsySense Emotion AI](https://github.com/Hitan547/psysense-emotion-ai)
DistilBERT emotion classifier with production assets — FastAPI, Streamlit UI, Docker/K8s manifests, monitoring, and HF model hosting.

`DistilBERT` `FastAPI` `Streamlit` `Docker` `Kubernetes`

</td>
</tr>
</table>

---

## 🛡️ Applied ML & Multimodal AI

<table>
<tr>
<td width="50%" valign="top">

### [Talentryx AI — Interview Platform](https://github.com/Hitan547/ai-behavioral-interviewer-proctoring)
Full SaaS-style AI hiring platform with recruiter and candidate flows, AI scoring, browser proctoring signals, and serverless AWS architecture.

`Python` `TypeScript` `React` `AWS Lambda` `DynamoDB` `Cognito` `S3` `Step Functions`

Also: [Streamlit prototype](https://github.com/Hitan547/talentryx-streamlit-prototype) [![Demo](https://img.shields.io/badge/Live-Streamlit-FF4B4B?style=flat-square&logo=streamlit)](https://talentryx-app-prototype-39r2voisbo3erml4erxqtr.streamlit.app/)

</td>
<td width="50%" valign="top">

### [SentinelNet — Intrusion Detection](https://github.com/Hitan547/sentinelnet)
Real-time network intrusion detection with Random Forest, NSL-KDD preprocessing, live Flask dashboard, CSV analysis, Docker, and CI/CD.

`scikit-learn` `Flask` `pandas` `Canvas API` `Docker` `CI/CD`

[![Demo](https://img.shields.io/badge/Live-HF_Space-FF9D00?style=flat-square&logo=huggingface)](https://huggingface.co/spaces/Hitan2004/sentinelnet)

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [Trader Sentiment Analysis](https://github.com/Hitan547/trader-sentiment-analysis)
End-to-end data analysis of trader performance vs market sentiment on Hyperliquid — feature engineering, behavioral segmentation, statistical testing, and actionable strategy insights.

`Python` `pandas` `scipy` `Jupyter` `Visualization`

</td>
<td width="50%" valign="top">

### [Brain Buddy AI — Learning Assistant](https://github.com/Hitan547/brain-buddy-ai)
AI-powered PDF learning assistant with conversational Q&A, audio summaries, and auto-generated quizzes using Gemini API.

`TypeScript` `React` `Vite` `Node.js` `Express` `MongoDB` `Gemini API`

</td>
</tr>
</table>

---

## ⚙️ Technical Stack

### Languages
<p>
  <img src="https://skillicons.dev/icons?i=python,java,js,ts,c,cpp,r" alt="Languages" />
</p>

### AI/ML & LLMs
<p>
  <img src="https://skillicons.dev/icons?i=pytorch,tensorflow,sklearn,opencv" alt="AI ML" />
  <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" alt="LangChain" />
  <img src="https://img.shields.io/badge/LangGraph-FF6B35?style=for-the-badge" alt="LangGraph" />
  <img src="https://img.shields.io/badge/Hugging_Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" alt="HuggingFace" />
  <img src="https://img.shields.io/badge/RAG-00A67E?style=for-the-badge" alt="RAG" />
  <img src="https://img.shields.io/badge/FAISS-276DC3?style=for-the-badge" alt="FAISS" />
  <img src="https://img.shields.io/badge/ChromaDB-5B61FF?style=for-the-badge" alt="ChromaDB" />
  <img src="https://img.shields.io/badge/BM25-4B5563?style=for-the-badge" alt="BM25" />
</p>

### Backend & Frontend
<p>
  <img src="https://skillicons.dev/icons?i=fastapi,flask,nodejs,express,react,vite,html,css,tailwind" alt="Backend Frontend" />
</p>

### Infrastructure & DevOps
<p>
  <img src="https://skillicons.dev/icons?i=docker,aws,firebase,vercel,mongodb,sqlite,git,github,githubactions" alt="Infra DevOps" />
</p>

---

## 📈 GitHub Activity

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Hitan547&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=58A6FF&icon_color=58A6FF&text_color=c9d1d9&ring_color=58A6FF" height="170" alt="GitHub Stats" />
  <img src="https://github-readme-streak-stats.herokuapp.com?user=Hitan547&theme=github-dark-blue&hide_border=true&background=0d1117&stroke=30363d&ring=58A6FF&fire=58A6FF&currStreakLabel=58A6FF" height="170" alt="Streak Stats" />
</div>

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Hitan547&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=58A6FF&text_color=c9d1d9&langs_count=8" height="170" alt="Top Languages" />
</div>

---

## 🏆 Research & Achievements

| Achievement | Detail |
|:---|:---|
| 📄 **Published Research** | *Multi-Dataset Conditional Text Generation for Emotion Augmentation* — WCSC 2026, Springer LNCS |
| 🧪 **100K+ Synthetic Samples** | Generated minority-class training data improving macro-F1 across GoEmotions, TweetEval, and DAIR |
| 🔍 **3 Production RAG Systems** | Agentic Corrective RAG, BIS Standards RAG, Proanalyst RAG — all with retrieval + validation + deployment |
| 🏗️ **BIS Hackathon Results** | 100% Hit Rate @3, 0.95 MRR @5, 3.46s avg latency |
| 🚀 **5+ Deployed AI Systems** | Live on Hugging Face Spaces, Streamlit Cloud, Vercel, and AWS |
| 🧪 **Production Engineering** | CI/CD workflows, Docker builds, pytest suites, API health checks, SSE streaming |

---

## 📜 Certifications

<p>
  <img src="https://img.shields.io/badge/DeepLearning.AI-NLP_in_TensorFlow-0056D2?style=for-the-badge" alt="DeepLearning.AI" />
  <img src="https://img.shields.io/badge/IBM-AI_Fundamentals-052FAD?style=for-the-badge&logo=ibm&logoColor=white" alt="IBM" />
  <img src="https://img.shields.io/badge/University_of_London-Machine_Learning_for_All-A51C30?style=for-the-badge" alt="UoL" />
</p>

---

<div align="center">

### 💬 Let's Connect

<p>
  <a href="https://linkedin.com/in/hitan-k"><img src="https://skillicons.dev/icons?i=linkedin" alt="LinkedIn" /></a>
  &nbsp;&nbsp;
  <a href="mailto:hitan.k@outlook.com"><img src="https://skillicons.dev/icons?i=gmail" alt="Email" /></a>
  &nbsp;&nbsp;
  <a href="https://github.com/Hitan547"><img src="https://skillicons.dev/icons?i=github" alt="GitHub" /></a>
</p>

**Build systems that matter. Learn every day. Ship confidently.**

</div>
