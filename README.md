<div align="center">

# Hitan K

### Applied AI/ML Engineer · LLM & RAG Systems · Production ML & MLOps

<p>
  <a href="https://github.com/Hitan547">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=18&duration=2600&pause=900&color=58A6FF&center=true&vCenter=true&repeat=true&width=620&height=32&lines=Building+reliable+RAG+systems;LLM+apps+with+evaluation+guardrails;Deployed+AI+products+with+Python+and+AWS;Open+to+AI%2FML+and+GenAI+roles" alt="Building reliable RAG systems, LLM apps, and deployed AI products" />
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

## About

CS graduate with an AI specialization who builds **deployed AI systems**, not just notebooks.

- **4 deployed RAG systems** — hybrid retrieval, reranking, agentic workflows, evaluation, and hallucination guardrails
- **Research paper publishing** — Springer LNCS paper on LLM-based synthetic data augmentation for emotion classification
- **Multimodal AI products** — interview assessment using text, speech, prosody, and video signals
- **Full production stack** — FastAPI/Flask APIs, Docker, CI/CD, pytest, Hugging Face Spaces, Vercel, AWS serverless

<p>
  <strong>Open to:</strong> AI/ML Engineer · Applied AI Engineer · GenAI/LLM Engineer · NLP Engineer · MLOps Engineer roles
</p>

---

## RAG Systems — Retrieval-Augmented Generation

> **Core specialization.** Deployed RAG, agentic retrieval, validation loops, and source-grounded LLM systems.

<table>
<tr>
<td width="25%" valign="top">

### [Agentic Corrective RAG](https://github.com/Hitan547/agentic-corrective-rag)
**Self-correcting document QA**

Production-style RAG with retrieval, reranking, answer validation, and retry loops to reduce hallucination.

`BM25` `RRF` `Cross-Encoder` `LangGraph` `LLaMA` `FastAPI` `Docker` `RAGAS`

[![Demo](https://img.shields.io/badge/Live-HF_Space-FF9D00?style=flat-square&logo=huggingface)](https://huggingface.co/spaces/Hitan2004/agentic-corrective-rag)

</td>
<td width="25%" valign="top">

### [BIS Standards RAG](https://github.com/Hitan547/BIS-Standards-RAG)
**Standards code recommendation**

Maps building material queries to BIS/IS codes using hybrid retrieval, query expansion, reranking, and confidence filtering.

`FAISS` `BGE` `BM25` `RRF` `Cross-Encoder` `LangGraph` `Streamlit`

**100% Hit Rate @3 · 0.95 MRR @5**

</td>
<td width="25%" valign="top">

### [Local Pilot](https://github.com/Hitan547/local-pilot)
**Local-first AI assistant**

Local RAG/assistant prototype focused on private document workflows, local execution, and practical AI automation.

`Python` `RAG` `Local AI` `Document QA` `Automation`

</td>
<td width="25%" valign="top">

### [Proanalyst RAG Bot](https://github.com/Hitan547/Proanalyst_Hitan_k_rag)
**API documentation support bot**

Source-grounded API assistant with guardrails, fallback behavior, and traceable answers.

`ChromaDB` `MiniLM` `Streamlit` `Guardrails` `Traceability`

[![Demo](https://img.shields.io/badge/Live-Streamlit-FF4B4B?style=flat-square&logo=streamlit)](https://proanalysthitank-p9xvkrnqrj9ahyey5xmh3a.streamlit.app/)

</td>
</tr>
</table>

<details>
<summary><b>RAG Architecture Comparison</b></summary>
<br/>

| Capability | Agentic Corrective RAG | BIS Standards RAG | Local Pilot | Proanalyst RAG |
|:---|:---:|:---:|:---:|:---:|
| **Retrieval** | BM25 + RRF | FAISS + BM25 + RRF | Local document retrieval | ChromaDB semantic |
| **Reranking** | Cross-Encoder | Cross-Encoder | Project-specific | Lexical rerank |
| **Agent Workflow** | LangGraph retry loop | LangGraph corrective agent | Local assistant flow | Guardrail fallback |
| **Evaluation** | RAGAS + pytest | Hit Rate + MRR | Local validation | 36-question eval set |
| **Deployment** | HF Space + Docker | Streamlit | Local-first | Streamlit Cloud |

</details>

---

## NLP, NLU & Research

<table>
<tr>
<td width="50%" valign="top">

### [Conditional Text Generation for Emotion Classification](https://github.com/Hitan547/-project-conditional-text-generation-and-augmentation-for-sentiment-classification)
**Research paper publishing — Springer LNCS, WCSC 2026**

LLM-based conditional text generation pipeline for synthesizing minority-class emotion samples and improving class balance across emotion datasets.

Generated **100K+ synthetic training samples** and evaluated across GoEmotions, TweetEval, and DAIR.

`PyTorch` `RoBERTa` `SmolLM` `Optuna` `GoEmotions` `TweetEval` `DAIR`

</td>
<td width="50%" valign="top">

### [PsySense Emotion AI](https://github.com/Hitan547/psysense-emotion-ai)
DistilBERT emotion classifier with production assets: FastAPI, Streamlit UI, Docker/K8s manifests, monitoring, and Hugging Face model hosting.

`DistilBERT` `Transformers` `FastAPI` `Streamlit` `Docker` `Kubernetes`

### GoEmotions Emotion Classifier
Transformer-based multi-label emotion classification using DistilBERT trained on GoEmotions to detect overlapping human emotions in text.

`DistilBERT` `Multi-Label Classification` `Jupyter`

</td>
</tr>
</table>

---

## Applied ML & Multimodal AI

<table>
<tr>
<td width="50%" valign="top">

### [Talentryx AI — Interview Platform](https://github.com/Hitan547/ai-behavioral-interviewer-proctoring)
Full SaaS-style AI hiring platform with recruiter and candidate flows, AI scoring, browser proctoring signals, and serverless AWS architecture.

`Python` `TypeScript` `React` `AWS Lambda` `DynamoDB` `Cognito` `S3` `Step Functions`

Also: [Streamlit prototype](https://github.com/Hitan547/talentryx-streamlit-prototype)  
[![Demo](https://img.shields.io/badge/Live-Streamlit-FF4B4B?style=flat-square&logo=streamlit)](https://talentryx-app-prototype-39r2voisbo3erml4erxqtr.streamlit.app/)

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
End-to-end data analysis of trader performance vs market sentiment on Hyperliquid: feature engineering, behavioral segmentation, statistical testing, and actionable strategy insights.

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

## Technical Stack

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

## Research & Achievements

| Achievement | Detail |
|:---|:---|
| **Research Paper Publishing** | *Multi-Dataset Conditional Text Generation for Emotion Augmentation* — WCSC 2026, Springer LNCS |
| **100K+ Synthetic Samples** | Generated minority-class training data improving macro-F1 across GoEmotions, TweetEval, and DAIR |
| **4 Deployed RAG Systems** | Agentic Corrective RAG, BIS Standards RAG, Local Pilot, Proanalyst RAG |
| **BIS Hackathon Results** | 100% Hit Rate @3, 0.95 MRR @5, 3.46s average latency |
| **5+ Deployed AI Systems** | Live on Hugging Face Spaces, Streamlit Cloud, Vercel, and AWS |
| **Production Engineering** | CI/CD workflows, Docker builds, pytest suites, API health checks, SSE streaming |

---

## Certifications

<p>
  <img src="https://img.shields.io/badge/DeepLearning.AI-NLP_in_TensorFlow-0056D2?style=for-the-badge" alt="DeepLearning.AI" />
  <img src="https://img.shields.io/badge/IBM-AI_Fundamentals-052FAD?style=for-the-badge&logo=ibm&logoColor=white" alt="IBM" />
  <img src="https://img.shields.io/badge/University_of_London-Machine_Learning_for_All-A51C30?style=for-the-badge" alt="UoL" />
</p>

---

<div align="center">

### Let's Connect

<p>
  <a href="https://linkedin.com/in/hitan-k"><img src="https://skillicons.dev/icons?i=linkedin" alt="LinkedIn" /></a>
  &nbsp;&nbsp;
  <a href="mailto:hitan.k@outlook.com"><img src="https://skillicons.dev/icons?i=gmail" alt="Email" /></a>
  &nbsp;&nbsp;
  <a href="https://github.com/Hitan547"><img src="https://skillicons.dev/icons?i=github" alt="GitHub" /></a>
</p>

**Build systems that matter. Learn every day. Ship confidently.**

</div>
