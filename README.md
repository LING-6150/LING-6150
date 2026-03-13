🚀 Duan Ling | AI Systems & Full-Stack Engineer

MS in Information Systems @ Northeastern University

I build production-grade AI systems and full-stack platforms, focusing on LLM-powered applications, agent workflows, and scalable backend infrastructure.

My work combines AI system design, distributed backend engineering, and cloud deployment to bring intelligent applications into production.

🧠 AI Systems Expertise

Retrieval-Augmented Generation (RAG)

Autonomous Agent Systems (ReAct / Tool Calling)

Multi-Agent Workflow Orchestration

LLM Evaluation & Benchmarking

Vector Search & Hybrid Retrieval

High-Concurrency AI Systems (SSE streaming)

⚙️ Technical Stack

Languages

Java · Python · SQL · JavaScript · TypeScript

Backend

Spring Boot · FastAPI · Redis · PostgreSQL · MySQL

Frontend

Vue 3 · React

AI & LLM Systems

Spring AI · LangChain4j · LangGraph4j
RAG Pipelines · Agent Architectures · PGVector
Cross-Encoder Reranking · RAGAS Evaluation

Data Systems

Apache Kafka · RabbitMQ · Elasticsearch

Cloud & DevOps

AWS EC2 · Docker · Kubernetes
Nginx · GitHub Actions · Linux

Observability

Prometheus · Grafana · Micrometer

🌟 Featured Projects
🏥 Ling Clinic — AI-Powered Healthcare Platform

🔗 https://github.com/LING-6150/Ling-clinic-healthcare

🌐 Live Demo
http://98.93.64.174

Full-stack healthcare platform integrating a RAG-based AI health assistant with clinic management.

Tech

Spring Boot · Vue 3 · PostgreSQL · PGVector · AWS EC2 · Nginx

Features

Patient System

Secure authentication and session management

Appointment booking and cancellation

AI health assistant grounded in internal medical knowledge base

Admin System

Medical document upload pipeline

Automated semantic chunking and embedding generation

Knowledge base management

RAG Architecture

Document Pipeline

Upload PDF/TXT
↓
Text Extraction (PDFBox)
↓
SHA-256 Deduplication
↓
Semantic Chunking
↓
Embedding Generation (OpenAI)
↓
PGVector Storage (HNSW index)

Query Pipeline

User Question
↓
Embedding
↓

Hybrid Retrieval

Vector Search (PGVector)
Keyword Search (PostgreSQL FTS)

↓
Reciprocal Rank Fusion (RRF)
↓
Top-K Context
↓
LLM Prompt Construction
↓
OpenAI Chat API
↓
SSE Streaming Response

Evaluation (RAGAS)
Metric	Score
Faithfulness	0.896
Answer Relevancy	0.952
Latency	310 ms
📊 LLM Evaluation Platform

🔗 https://github.com/LING-6150/llm-eval-platform

Distributed system for benchmarking LLM reliability, latency, and output quality.

Tech

Spring Boot · Redis · Apache Kafka · CockroachDB · Prometheus · React

Key Contributions

Designed distributed evaluation pipeline using Kafka message streaming

Decoupled model inference (2–37s latency) from API responses

Implemented retry strategies and dead-letter queues

Sustained 4,800+ requests/sec with P99 latency 328ms

Optimization

Redis Lua-based atomic prompt-result caching

Cache hits reduced latency 1962ms → 0ms

Eliminated redundant LLM token usage

Observability

Elasticsearch indexing for prompt search

Prometheus + Grafana monitoring

🧠 AI Knowledge Agent Platform

🔗 https://github.com/LING-6150/ling-ai-agent

Autonomous AI agent system integrating RAG pipelines with tool-calling agents.

Key Contributions

Designed hierarchical agent architecture

BaseAgent → ReActAgent → ToolCallAgent → LingManus

Built PGVector vector search pipeline (HNSW indexing)

Integrated LangSmith tracing via OpenTelemetry

Implemented real-time SSE streaming responses

🏗 AI Web Application Generation Platform

🔗 https://github.com/LING-6150/ling-ai-generation-engine

AI system converting natural language prompts into deployable web applications.

Key Contributions

Designed multi-mode generation pipeline

Diagnosed concurrency bottleneck in SSE parsing

Enabled parallel streaming execution

Reduced generation latency by 28%

🌐 API Gateway & Integration Platform

🔗 https://github.com/LING-6150/API-Integrity-Platform

Distributed gateway handling authentication, routing, and traffic control.

Key Contributions

Managed routing across 20+ backend services

Redis-based rate limiting and circuit breaker

AK/SK signature authentication

Dubbo RPC integration

🖼 AI Image Cloud Platform

🔗 https://github.com/LING-6150/your-image-repo

AI-powered collaborative image management system.

Key Contributions

WebSocket-based real-time synchronization

Sub-200ms latency under 100+ concurrent users

Hybrid semantic + metadata search

Multi-level caching reducing DB contention

📊 GitHub Stats
<img align="center" src="https://github-readme-stats.vercel.app/api?username=LING-6150&show_icons=true&theme=tokyonight" /> <img align="center" src="https://github-readme-stats.vercel.app/api/top-langs/?username=LING-6150&layout=compact&theme=tokyonight" />
📫 Contact

LinkedIn
https://www.linkedin.com/in/duan-ling-9970ba350/

Email
duan.lin@northeastern.edu

⭐ Open to AI Application Engineering / Backend / Full-Stack roles
