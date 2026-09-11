<div align="center">

# Panshul Sarma

**AI/ML Engineer · Backend Developer · B.Tech CSE (AI & ML)**

I build AI systems that connect **models, retrieval, agents, APIs, and real-world data** — with most of my recent work focused on local inference, RAG, agentic workflows, and Python backends.

[Portfolio](https://www.panshul.tech) · [LinkedIn](https://www.linkedin.com/in/panshul-sarma-746462287/) · [Email](mailto:pans83372@gmail.com)

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

`Python` `PyTorch` `Whisper` `Transformers` `NLP` `CUDA` `pytest`

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

`Python` `LangGraph` `FastAPI` `GraphQL` `Groq` `httpx`

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

`Python` `CrewAI` `RAG` `ChromaDB` `FastAPI` `SQLite` `Groq`

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

`Python` `FastAPI` `SQLAlchemy` `React` `Forecasting` `Docker`

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

`Python` `CrewAI` `Gmail` `LLMs` `Slack`

## Other Work

### [Real-Time Chat Application](https://github.com/reigen002/EazyByts)

Full-stack multi-room chat application with a React frontend and Java Spring Boot backend, using WebSockets for real-time messaging.

`Java` `Spring Boot` `WebSocket` `React` `Maven`

## Tech

| Area            | Technologies                                                 |
| --------------- | ------------------------------------------------------------ |
| **Languages**   | Python, Java, SQL, JavaScript                                |
| **AI / ML**     | PyTorch, Hugging Face, NLP, RAG, CrewAI, LangGraph, ChromaDB |
| **Backend**     | FastAPI, Spring Boot, REST APIs, WebSockets, SQLAlchemy      |
| **Data**        | SQLite, SQL, vector databases                                |
| **Engineering** | Docker, Git, GitHub Actions, pytest                          |
| **Frontend**    | React, Vite, Tailwind CSS                                    |

## Experience

**Java Developer Intern — EazBytz**
Worked on Java/Spring Boot backend development and reusable application components.

**Tech Co-Lead — Cognito Club**
Contributed to technical development and helped conduct an Agentic AI workshop using Lyzr AI.

## What I'm Exploring

I'm particularly interested in systems where AI is only one component of the architecture — retrieval, state, tools, APIs, concurrency, evaluation and failure handling matter just as much as the model itself.

I'm currently looking to deepen my work in **AI engineering, backend systems, agent infrastructure, and production-oriented ML**.

<div align="center">

### Let's connect

[LinkedIn](https://www.linkedin.com/in/panshul-sarma-746462287/) · [Portfolio](https://www.panshul.tech) · [GitHub](https://github.com/reigen002)

</div>