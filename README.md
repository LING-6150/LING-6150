# Ling Duan — AI Systems & Backend Engineer

**MS Information Systems · Northeastern University**

I build production-grade AI systems — RAG pipelines, autonomous agent frameworks, and scalable backend infrastructure. Focused on making LLM applications reliable and deployable in the real world.

> Open to **Open to AI Infra / LLMOps / AI Backend Engineering roles** roles

---

## Technical Stack

**AI & LLM Systems**

![Spring AI](https://img.shields.io/badge/Spring_AI-6DB33F?style=flat&logoColor=white)
![RAG](https://img.shields.io/badge/RAG_Pipelines-7F77DD?style=flat&logoColor=white)
![ReAct Agents](https://img.shields.io/badge/ReAct_Agents-7F77DD?style=flat&logoColor=white)
![PGVector](https://img.shields.io/badge/PGVector-7F77DD?style=flat&logoColor=white)
![LangSmith](https://img.shields.io/badge/LangSmith-7F77DD?style=flat&logoColor=white)
![MCP](https://img.shields.io/badge/MCP_Protocol-7F77DD?style=flat&logoColor=white)

**Backend**

![Java](https://img.shields.io/badge/Java-1D9E75?style=flat&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-1D9E75?style=flat&logoColor=white)
![Python](https://img.shields.io/badge/Python-1D9E75?style=flat&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-1D9E75?style=flat&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-1D9E75?style=flat&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-1D9E75?style=flat&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-1D9E75?style=flat&logoColor=white)

**Frontend**

![Vue 3](https://img.shields.io/badge/Vue_3-378ADD?style=flat&logoColor=white)
![React](https://img.shields.io/badge/React-378ADD?style=flat&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-378ADD?style=flat&logoColor=white)

**Cloud & DevOps**

![AWS EC2](https://img.shields.io/badge/AWS_EC2-BA7517?style=flat&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-BA7517?style=flat&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-BA7517?style=flat&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-BA7517?style=flat&logoColor=white)

---

## Performance Highlights

| Metric | Result |
|--------|--------|
| Embedding API cost reduction | **93%** (30 → 2 calls/doc via batching + SHA-256 dedup) |
| RAG throughput | **~41 req/min**, P95 6.1s, **0% error** (JMeter) |
| RAGAS answer relevancy | **0.952** |
| LLM eval platform throughput | **4,800+ req/sec**, P99 328ms |
| Redis cache latency | **1,962ms → 0ms** on cache hits |

---

## Featured Projects

### [AI Knowledge Agent Platform](https://github.com/LING-6150/ling-ai-agent)

Autonomous AI agent system integrating RAG pipelines with tool-calling agents.

- Hybrid retrieval: vector search (PGVector HNSW) + BM25 via RRF fusion, cross-encoder reranking (ms-marco-MiniLM-L-6-v2) via Python FastAPI
- ReAct hierarchical agent: `BaseAgent → ReActAgent → ToolCallAgent → LingManus` with stuck-state detection and human-in-the-loop escalation
- 8 tool callbacks + custom MCP Server (Pexels image search, Stdio/SSE transport) + Amap location MCP integration
- LangSmith tracing via OpenTelemetry · SSE streaming · CI/CD with Docker Buildx ARM→amd64

`Spring Boot` `Spring AI` `PGVector` `Python FastAPI` `Vue 3` `AWS EC2` `LangSmith`

---

### [Ling Clinic — AI Healthcare Platform](https://github.com/LING-6150/Ling-clinic-healthcare) · [Live Demo](http://98.93.64.174)

Full-stack clinic platform with a RAG-based AI health assistant grounded in an internal medical knowledge base.

- RAG pipeline: PDF ingestion → SHA-256 dedup → chunking → OpenAI embedding → PGVector (HNSW) → hybrid retrieval → RRF → SSE streaming
- RAGAS evaluation: Faithfulness **0.896** · Answer Relevancy **0.952** · Latency **310ms**
- Patient booking system + admin document upload pipeline + knowledge base management

`Spring Boot` `Vue 3` `PostgreSQL` `PGVector` `OpenAI` `AWS EC2` `Nginx`

---

### [LLM Evaluation Platform](https://github.com/LING-6150/llm-eval-platform)

Distributed system for benchmarking LLM reliability, latency, and output quality.

- Kafka-based async pipeline decoupling model inference (2–37s) from API responses
- Redis Lua atomic caching: latency **1,962ms → 0ms** on cache hits
- Sustained **4,800+ req/sec**, P99 **328ms** · retry strategies + dead-letter queues
- Elasticsearch prompt search · Prometheus + Grafana observability

`Spring Boot` `Apache Kafka` `Redis` `CockroachDB` `Prometheus` `Grafana` `React`

---

### [API Gateway & Integration Platform](https://github.com/LING-6150/API-Integrity-Platform)

Distributed gateway handling authentication, routing, and traffic control across 20+ backend services.

- Redis-based rate limiting and circuit breaker · AK/SK signature authentication · Dubbo RPC integration

`Spring Boot` `Redis` `Dubbo`

---

### [AI Web Generation Engine](https://github.com/LING-6150/ling-ai-generation-engine)

Natural language prompts → deployable web applications.

- Diagnosed concurrency bottleneck in SSE parsing · parallel streaming execution reduced latency by **28%**

`Spring Boot` `SSE`

---

## Contact

- LinkedIn: [duan-ling-9970ba350](https://www.linkedin.com/in/duan-ling-9970ba350/)
- Email: duan.lin@northeastern.edu
