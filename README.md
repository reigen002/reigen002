<div align="center">

# Panshul Sarma

**AI/ML Engineer · Backend Developer · B.Tech CSE (AI & ML)**

I build AI systems that connect **models, retrieval, agents, APIs, and real-world data** — with most of my recent work focused on local inference, RAG, agentic workflows, and Python backends.

<br/>

[![Portfolio](https://img.shields.io/badge/Portfolio-panshul.tech-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://www.panshul.tech)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/panshul-sarma-746462287/)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:pans83372@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/reigen002)

</div>

## About

I'm a Computer Science student specializing in Artificial Intelligence and Machine Learning at Jain University, Bengaluru.

My work generally sits between **AI engineering and backend development**: taking models or LLM workflows beyond notebooks and turning them into usable systems with APIs, persistence, retrieval, concurrency, testing, and deployment.

Currently interested in:

* Agentic AI and tool-using systems
* Retrieval-Augmented Generation and semantic search
* Speech and multilingual NLP systems
* Backend/API architecture with Python and Java
* Local and resource-efficient AI inference

## Selected Projects

### [PolyglotTalk](https://github.com/reigen002/polyglot-talk)

**Offline multilingual speech-to-speech translation for 8 Indian languages.**

```text
Microphone → Whisper ASR → Argos Translate → MMS-TTS → Speech
```

Built as a concurrent four-stage inference pipeline rather than a sequential model demo.

* Runs completely locally after model setup; no cloud inference APIs
* Uses `faster-whisper`, Argos Translate and Facebook MMS-TTS
* Separate worker threads for audio capture, ASR, translation and synthesis
* Overlapping audio windows prevent words from being lost at chunk boundaries
* Sentence buffering preserves translation context across ASR fragments
* Bounded queues and drop-oldest backpressure keep the pipeline responsive
* Automatic CUDA/CPU selection for TTS
* Includes automated tests and ASR benchmarking infrastructure

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Whisper](https://img.shields.io/badge/Whisper-412991?style=flat-square&logo=openai&logoColor=white)
![Transformers](https://img.shields.io/badge/Transformers-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![NLP](https://img.shields.io/badge/NLP-00A67E?style=flat-square)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=flat-square&logo=nvidia&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)

---

### [Skylark AI Agent](https://github.com/reigen002/skylark_aiagent)

**Conversational business-intelligence agent over live Monday.com operational data.**

Built an AI agent that can reason over Deals and Work Orders boards and answer questions such as pipeline health, overdue work, sector performance and leadership-level KPIs.

```text
User
  → FastAPI
  → LangGraph ReAct Agent
  → Business Intelligence Tools
  → Monday.com GraphQL API
```

* LangGraph ReAct agent with tool-based reasoning
* Queries live Monday.com data through its GraphQL API
* Cursor-paginated board ingestion
* Cross-board analysis across sales and operational data
* Dedicated tools for pipeline, work-order and leadership analysis
* Handles inconsistent dates, currencies, missing values and dynamic schemas
* FastAPI backend with a separately deployed web frontend

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![GraphQL](https://img.shields.io/badge/GraphQL-E10098?style=flat-square&logo=graphql&logoColor=white)
![Groq](https://img.shields.io/badge/Groq-F55036?style=flat-square)
![httpx](https://img.shields.io/badge/httpx-000000?style=flat-square)
[![Live Demo](https://img.shields.io/badge/Live-Demo-000000?style=flat-square&logo=vercel&logoColor=white)](https://skylark-aiagent.vercel.app)

---

### [RPG Gaming Assistant](https://github.com/reigen002/ai_gaming_assistant)

**RAG-powered gaming assistant with local retrieval, web fallback and persistent conversations.**

Rather than sending every question directly to an LLM, the assistant uses progressively more expensive information sources:

```text
Question
   → ChromaDB semantic retrieval
   → Web search when local knowledge is insufficient
   → Cache new knowledge
   → LLM synthesis
```

* ChromaDB-backed semantic retrieval
* Automatic web-search fallback using Serper and DuckDuckGo
* Successful web results are indexed for future retrieval
* CrewAI-based agent orchestration
* FastAPI backend
* Per-game conversation persistence using SQLite
* Graceful fallback when LLM rate limits are reached
* Embeddable browser sidebar interface

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![CrewAI](https://img.shields.io/badge/CrewAI-1C1C1C?style=flat-square&logo=openai&logoColor=white)
![RAG](https://img.shields.io/badge/RAG-5C2D91?style=flat-square)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6B6B?style=flat-square)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)
![Groq](https://img.shields.io/badge/Groq-F55036?style=flat-square)

---

### [Smart Rental Tracking System](https://github.com/reigen002/Edgerunners-SRTS)

**Team-built rental fleet intelligence system for tracking equipment, telemetry and utilization.**

Developed as a hackathon project around rental-fleet operations and decision support.

* Asset check-in/check-out lifecycle tracking
* Telemetry ingestion and deterministic simulation scenarios
* Rule-based anomaly detection and alert generation
* Utilization analysis from engine and idle hours
* Demand forecasting and asset-allocation recommendations
* FastAPI + SQLAlchemy backend
* React frontend connected to the real backend API
* Reproducible seeded demo environment with automated backend tests

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat-square)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Forecasting](https://img.shields.io/badge/Forecasting-FF6F00?style=flat-square)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

---

### [Gmail Automation with CrewAI](https://github.com/reigen002/gmail_automation-crewai)

**Multi-agent email triage and inbox automation system.**

Uses specialized agents to process an inbox as a workflow rather than treating email automation as a single LLM prompt.

* Email categorization and priority classification
* Gmail organization and labeling
* Draft response generation
* Slack alerts for high-priority messages
* Rule-based cleanup and preservation policies
* Multiple configurable LLM providers

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![CrewAI](https://img.shields.io/badge/CrewAI-1C1C1C?style=flat-square&logo=openai&logoColor=white)
![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=flat-square&logo=gmail&logoColor=white)
![LLMs](https://img.shields.io/badge/LLMs-412991?style=flat-square&logo=openai&logoColor=white)
![Slack](https://img.shields.io/badge/Slack-4A154B?style=flat-square&logo=slack&logoColor=white)

## Other Work

### [Real-Time Chat Application](https://github.com/reigen002/EazyByts)

Full-stack multi-room chat application with a React frontend and Java Spring Boot backend, using WebSockets for real-time messaging.

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![WebSocket](https://img.shields.io/badge/WebSocket-010101?style=flat-square)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Maven](https://img.shields.io/badge/Maven-C71A36?style=flat-square&logo=apachemaven&logoColor=white)

## Tech

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

**AI / ML**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![NLP](https://img.shields.io/badge/NLP-00A67E?style=flat-square)
![RAG](https://img.shields.io/badge/RAG-5C2D91?style=flat-square)
![CrewAI](https://img.shields.io/badge/CrewAI-1C1C1C?style=flat-square&logo=openai&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6B6B?style=flat-square)

**Backend**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![REST APIs](https://img.shields.io/badge/REST%20APIs-02569B?style=flat-square)
![WebSockets](https://img.shields.io/badge/WebSockets-010101?style=flat-square)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat-square)

**Data**

![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![Vector DBs](https://img.shields.io/badge/Vector%20DBs-FF6B6B?style=flat-square)

**Engineering**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)

**Frontend**

![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)

## Experience

**Java Developer Intern — EazBytz**
Worked on Java/Spring Boot backend development and reusable application components.

**Tech Co-Lead — Cognito Club**
Contributed to technical development and helped conduct an Agentic AI workshop using Lyzr AI.

## What I'm Exploring

I'm particularly interested in systems where AI is only one component of the architecture — retrieval, state, tools, APIs, concurrency, evaluation and failure handling matter just as much as the model itself.

I'm currently looking to deepen my work in **AI engineering, backend systems, agent infrastructure, and production-oriented ML**.

## GitHub Stats

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=reigen002&theme=dark&hide_border=false&include_all_commits=false&count_private=false)

![GitHub Streak](https://nirzak-streak-stats.vercel.app/?user=reigen002&theme=dark&hide_border=false)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=reigen002&theme=dark&hide_border=false&include_all_commits=false&count_private=false&layout=compact)

</div>

---

<div align="center">

### Let's connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/panshul-sarma-746462287/)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://www.panshul.tech)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/reigen002)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:pans83372@gmail.com)

<br/>

[![Profile views](https://visitcount.itsvg.in/api?id=reigen002&icon=0&color=0)](https://visitcount.itsvg.in)

</div>