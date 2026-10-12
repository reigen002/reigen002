<div align="center">

# Panshul Pratik Sarma

**AI Engineer · Backend / Software Engineer · B.Tech CSE (AI & ML)**

I build **backend services and AI applications**, focusing on API contracts, transactional consistency, retrieval, concurrency, testing, and predictable failure handling.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/panshul-sarma-746462287/)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:pans83372@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/reigen002)

</div>

## About

I'm a B.Tech Computer Science student specializing in AI & ML at Jain University, Bengaluru. I work at the intersection of **backend engineering, LLM applications, and reliable systems**—moving from prototypes to tested services with explicit contracts and operational boundaries.

Current interests: AI agent tools and evaluation, retrieval-augmented generation, distributed-system fundamentals, transactional backend services, and efficient local inference.

## Selected Projects

### [FleetSignal — Fleet Telemetry & Rental Operations](https://github.com/reigen002/FleetSignal)

**Reliability-focused FastAPI and React system for rental-fleet telemetry, alerts, and asset-allocation decisions.**

- Built **retry-safe/idempotent telemetry ingestion** with transactional alert reconciliation and stable alert episodes.
- Added database migrations, documented API/reliability contracts, integration tests, CI validation, and Docker persistence checks.
- The reliability work was verified with **262 backend tests**, alongside frontend build and local Docker checks.
- Added locally validated **AWS EC2 demo deployment configuration**; this is not a claim of a production-scale hosted service.
- Supports asset rental lifecycle, explainable rules, utilization analysis, and a synthetic seven-asset demo.

**Stack:** Python · FastAPI · SQLAlchemy · SQLite · React · Docker · GitHub Actions · AWS EC2

[Implementation](https://github.com/reigen002/FleetSignal/tree/main/caterpillar-smart-rental) · [Reliability notes](https://github.com/reigen002/FleetSignal/blob/main/caterpillar-smart-rental/docs/RELIABILITY.md)

### [PolyglotTalk](https://github.com/reigen002/polyglot-talk)

**Offline multilingual speech-to-speech translation for eight Indian languages.**

```text
Microphone → faster-whisper ASR → Argos Translate → Facebook MMS-TTS → WAV output
```

- Four concurrently executing pipeline stages with queues and backpressure.
- Overlapping audio windows, transcription deduplication, and sentence buffering improve continuity across chunks.
- Fully local inference after downloading models; ASR and translation use CPU, while TTS can use CUDA or CPU.
- Includes silence detection, configurable languages, tests, and benchmarking support.

**Stack:** Python · faster-whisper · Argos Translate · PyTorch · Hugging Face · MMS-TTS · pytest

### [Skylark AI Agent](https://github.com/reigen002/skylark_aiagent)

**Conversational business-intelligence agent over Monday.com Deals and Work Orders boards.**

- LangGraph ReAct workflow calls dedicated tools for pipeline, operational, cross-board, and leadership analysis.
- Fetches live board data using Monday.com GraphQL with cursor pagination.
- FastAPI backend and independently deployed static frontend; handles missing fields and inconsistent business records.

**Stack:** Python · LangGraph · FastAPI · GraphQL · httpx · Groq

[Frontend demo](https://skylark-aiagent.vercel.app)

### [Lore-X](https://github.com/reigen002/Lore-X)

**Gaming assistant using retrieval-first answers, web fallback, and persistent conversations.**

- Queries **ChromaDB** cached snippets before falling back to Serper and DuckDuckGo search; web results can be indexed for reuse.
- FastAPI API with validated user input, a resizable browser sidebar, and per-game **SQLite** conversation history.
- Recent fixes improve API error handling and SQLite connection lifecycle.
- If provider formatting fails, the application can return raw retrieved snippets.
- **Known limitations:** a failed request may leave a partial conversation turn; retries are not idempotent; some handled failures return HTTP 200 with a failure string. The main-branch HTTP request path is not an MCP server.

**Stack:** Python · FastAPI · ChromaDB · SQLite · Groq · Serper · DuckDuckGo

[Main-branch reliability contract](https://github.com/reigen002/Lore-X/blob/main/docs/MAIN_BACKEND_RELIABILITY.md)

### [Gmail Automation with CrewAI](https://github.com/reigen002/gmail_automation-crewai)

**Multi-agent inbox triage and email-management workflow.**

- Specialized agents for message classification, organization, draft replies, notifications, and cleanup.
- Configurable LLM providers; Gmail IMAP integration and Slack notifications.
- Includes thread-aware processing and configurable message-retention policies.

**Stack:** Python · CrewAI · Gmail IMAP · Slack · LLM APIs

## Other Work

**[Real-Time Chat Application](https://github.com/reigen002/EazyByts)** — Multi-room messaging with Java, Spring Boot, WebSockets, React, and Maven.

## Technology

| Area | Tools and technologies |
| --- | --- |
| Languages | Python, Java, SQL, JavaScript |
| Backend | FastAPI, Spring Boot, REST APIs, WebSockets, SQLAlchemy |
| AI & Retrieval | LangGraph, CrewAI, RAG, ChromaDB, PyTorch, Hugging Face, NLP |
| Data | SQLite, SQL databases, vector search |
| Engineering & Cloud | Docker, Git, GitHub Actions, pytest, AWS EC2 |
| Frontend | React, Vite, Tailwind CSS, HTML/CSS/JavaScript |

## Experience

**Java Developer Intern — EazBytz** — Worked on Java/Spring Boot development and application components.

**Tech Co-Lead — Cognito Club** — Contributed to technical activities and delivered an agentic-AI workshop using Lyzr AI.

## Engineering Focus

I am especially interested in systems where the model is only one part of the product: **tool boundaries, retrieval quality, durable state, tests, observability, evaluation, cost, and failure behavior** all determine whether the system is dependable.

## GitHub Activity

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=reigen002&theme=dark&hide_border=false&include_all_commits=false&count_private=false)

![GitHub Streak](https://nirzak-streak-stats.vercel.app/?user=reigen002&theme=dark&hide_border=false)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=reigen002&theme=dark&hide_border=false&include_all_commits=false&count_private=false&layout=compact)

</div>

<div align="center">

[LinkedIn](https://www.linkedin.com/in/panshul-sarma-746462287/) · [GitHub](https://github.com/reigen002) · [Email](mailto:pans83372@gmail.com)

</div>
