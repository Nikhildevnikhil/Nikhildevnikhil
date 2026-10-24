# Nikhil Deo

**AI Engineer** • Generative AI, Hybrid RAG Architectures & Agentic Systems  
Kolkata, India • [nikhildeonikhil@gmail.com](mailto:nikhildeonikhil@gmail.com) • [LinkedIn](https://www.linkedin.com/in/nikhildeo1610) • [GitHub](https://github.com/nikhildevnikhil)

---

## 🎯 About & Engineering Focus

AI Engineer with 3+ years of software and GenAI engineering experience architecting enterprise RAG pipelines, multi-agent systems, and low-latency inference microservices. 

At **Tata Consultancy Services (Client: KPMG)**, I architected an enterprise hybrid RAG aggregator indexing 300,000+ monthly documents with `<180ms` p95 retrieval latency using Azure AI Search, dense vectors, BM25, and semantic reranking. Previously, engineered a ServiceNow ticket triage agent using LangChain, LangGraph, and Azure OpenAI that routed ~30,000 tickets monthly, cutting triage time from 2.5 hours to under 4 minutes.

My technical focus centers on **empirical retrieval quality, multi-agent orchestration, and production inference economics**:
- **Information Retrieval & Hybrid RAG:** Dense + sparse (BM25) fusion, Reciprocal Rank Fusion (RRF), cross-encoder reranking, and semantic chunking.
- **Agentic Workflows & Multi-Agent Systems:** Stateful LangGraph execution graphs, human-in-the-loop validation, dynamic tool routing, and deterministic guardrails.
- **Empirical Evaluation & LLMOps:** Automated evaluation gates using RAGAS, continuous benchmarking (MRR, nDCG@K, Precision@K, Context Recall), and LLM-as-a-Judge rubrics.
- **Cost & Latency Reduction:** Vector semantic caching with Redis, context-window budgeting, and prompt compression techniques.

---

## 🚀 Featured AI Engineering Projects

### 🧠 [RAG Studio — Configurable RAG & LLM-as-a-Judge Evaluation Workbench](https://github.com/Nikhildevnikhil/RAG-Studio)
> *An enterprise AI workbench for end-to-end RAG experimentation, inline citation verification, and automated evaluation across 10 retrieval metrics and 11 LLM-as-a-Judge criteria.*

- **Multi-Format Ingestion Engine:** Parses PDF, DOCX, TXT, Markdown, CSV, and XLSX preserving document hierarchy, breadcrumbs, and tables with SHA-256 deduplication.
- **6 Chunking Strategies:** Recursive character, fixed-window, token-budgeted, sentence-level, paragraph, and markdown header-aware splitting.
- **Top 10 Mathematical IR Metrics:** Calculates exact mathematical scores against gold-standard passage labels: Precision@K, Recall@K, F1@K, Hit Rate@K, MRR, MAP@K, nDCG@K, R-Precision, Context Precision, and Context Recall.
- **LLM-as-a-Judge Engine:** Standardized 11-criteria rubric (Faithfulness, Answer Relevance, Citation Correctness, Groundedness) with root-cause failure tagging (`low_retrieval_recall`, `noisy_retrieval`, `hallucination_unfaithful`, `failed_abstention`).
- **Interactive Evidence Inspector:** 3-panel chat playground with bracketed citations (`[1]`, `[2]`), latency breakdown tracing, and chunk inspection.
- **Tech Stack:** `Python` • `FastAPI` • `ChromaDB` • `NumPy` • `PostgreSQL / pgvector` • `React` • `TypeScript` • `Docker`

---

### 🤖 [Autonomous Multi-Agent Research Assistant & Self-Corrective RAG](https://github.com/Nikhildevnikhil/autonomous-agent-rag) `[Repository Draft]`
> *Stateful multi-agent research workflow featuring autonomous web search tool calling, persistent scratchpad memory, and a self-corrective hallucination grader.*

- **Self-Corrective Loop:** Implemented a LangGraph cyclical state machine where an LLM-as-a-Judge grader evaluates retrieval confidence and answer faithfulness. Low confidence triggers automatic query reformulation and re-retrieval.
- **Empirical Impact:** Cut ungrounded claims from **22% down to 8%** across a 50-document evaluation benchmark.
- **Stateful Memory:** Checkpointed graph state enabling deterministic resumption, conversational context tracking, and tool execution rollback.
- **Tech Stack:** `Python` • `LangGraph` • `LangChain` • `FastAPI` • `ChromaDB` • `Tavily Search API` • `Docker`

---

### ⚡ [High-Throughput Async AI Inference Gateway](https://github.com/Nikhildevnikhil/async-ai-inference-gateway) `[Repository Draft]`
> *Event-driven LLM inference gateway engineered for high-concurrency workloads, semantic vector caching, and end-to-end Prometheus observability.*

- **Redis Vector Semantic Caching:** Achieved a **34% cache-hit ratio** on recurring user query distributions, bypassing LLM API calls and reducing token costs.
- **Asynchronous Kafka Workers:** Decoupled client request ingress from long-running LLM generation pipelines, maintaining service availability under traffic spikes.
- **Latency Optimization:** Reduced p95 end-to-end workflow execution time from **3.5s to 2.1s**.
- **Tech Stack:** `FastAPI` • `LangChain` • `Redis` • `Apache Kafka` • `PostgreSQL` • `Prometheus` • `Grafana`

---

### 🛡️ [Universal Android Debloater & System Automation Suite](https://github.com/Nikhildevnikhil/debloat-your-device)
> *Zero-dependency, evidence-based package audit and device debloating engine with automated rollback safety for 8+ Android OEM ecosystems.*

- **5-Tier Safety Classification:** Isolates carrier and vendor telemetry/adware while strictly preserving OEM critical framework dependencies (Tier 0).
- **Atomic Safety Verification:** Creates machine-readable hardware and package snapshots before any mutation, generating one-click recovery scripts.
- **Tech Stack:** `Python 3 (Standard Library)` • `ADB` • `PowerShell` • `Bash` • `Cross-Platform Systems`

---

## 🛠️ Technical Capabilities

| Domain | Technologies & Methodologies |
| :--- | :--- |
| **LLM & Agentic Engineering** | Hybrid RAG, Multi-Agent Orchestration (LangGraph, LangChain), Tool Calling, Self-Correction, Semantic Chunking, Context-Window Budgeting, Prompt-Injection Guardrails |
| **Retrieval & Vector Search** | Azure AI Search, ChromaDB, PostgreSQL (pgvector), Redis Semantic Cache, BM25 Hybrid Fusion, Cross-Encoder Reranking, MMR |
| **Evaluation & Quality Assurance** | RAGAS (Faithfulness, Context Precision, Answer Relevancy), LLM-as-a-Judge Rubrics, Precision@K, Recall@K, MRR, nDCG@K |
| **Backend & Microservices** | FastAPI, Python (Asyncio), Spring Boot, Java, RESTful APIs, Apache Kafka, RabbitMQ, Redis, PostgreSQL, MongoDB |
| **Cloud, Models & LLMOps** | Azure OpenAI (GPT-4o, text-embedding-3), Azure AI Foundry, AWS Bedrock (Claude 3.5, Llama 3), Docker, Kubernetes (AKS), GitHub Actions CI/CD, Prometheus, Grafana, Linux |

---

## 💼 Professional Experience

- **System Engineer (GenAI / RAG Engineering)** — **Tata Consultancy Services** *(Client: KPMG)*  
  *Mar 2026 – Present • Kolkata, India*  
  - Architected enterprise RAG knowledge aggregator on FastAPI and Azure AI Search (`text-embedding-3-large` + BM25 hybrid search with semantic reranking), indexing 300,000+ monthly documents with `<180ms` p95 retrieval latency.  
  - Deployed multi-agent workflows on Azure AI Foundry, Azure OpenAI (GPT-4o), Docker, and AKS; instrumented Prometheus latency and token telemetry with prompt-injection guardrails.

- **Assistant System Engineer (AI Engineering)** — **Tata Consultancy Services**  
  *Mar 2024 – Mar 2026 • Kolkata, India*  
  - Engineered Python ServiceNow triage and routing agent using LangChain, LangGraph, and Azure OpenAI, routing 1,000+ daily tickets (~30,000/month); slashed triage time from 2.5 hours to under 4 minutes, saving 42+ engineer-hours weekly.  
  - Built low-latency LLM inference microservices with FastAPI, LlamaIndex, and ChromaDB; reduced p95 response latency from 4.2s to 2.9s (31%) via semantic chunking and prompt compression.  
  - Automated CI/CD pipelines with GitHub Actions and Docker embedding automated RAGAS evaluation gates across 3 production pipelines; reduced monthly token spend by 18% using Redis semantic caching.

- **Software Engineer Intern (Backend & Full-Stack)** — **Learnship & Apric**  
  *Sep 2022 – Jul 2023 • India*  
  - Developed containerized Java Spring Boot microservices on Docker/K8s, scaling throughput from 120 to 165 req/sec; integrated Kafka/RabbitMQ streaming pipelines.

---

## 📜 Certifications & Education

### Certifications
- **Microsoft Certified:** Azure AI Apps and Agents Developer Associate (`AI-103`)
- **Microsoft Certified:** Azure AI Fundamentals (`AI-900`) • Azure Fundamentals (`AZ-900`)
- **LangChain:** RAG, Agents & Production LLM Integration
- **Microsoft:** LangChain Foundations

### Education
- **Master of Computer Applications (MCA)** — Vellore Institute of Technology (VIT) | *CGPA: 8.58/10 (Graduated Jul 2023)*
- **Bachelor of Computer Applications (BCA)** — Aryabhatta Knowledge University | *(Graduated 2020)*

---

## 📬 Contact & Collaboration

I am actively open to discussing **AI Engineer, LLM Engineer, Generative AI Engineer, and Applied AI Engineer** opportunities.

- 📧 **Email:** [nikhildeonikhil@gmail.com](mailto:nikhildeonikhil@gmail.com)
- 💼 **LinkedIn:** [linkedin.com/in/nikhildeo1610](https://www.linkedin.com/in/nikhildeo1610)
- 🐙 **GitHub:** [github.com/nikhildevnikhil](https://github.com/nikhildevnikhil)
