# Ling Duan — Agent Systems & Backend Engineer

**M.S. Information Systems · Northeastern University · Graduating Dec 2026**

I build reliable AI agent systems and backend infrastructure — from multi-agent runtimes, tool execution, and context engineering to evaluation, observability, state management, and production delivery.

> Open to **Agent Infrastructure / AI Backend / LLM Platform / Software Engineering** roles · Available full-time **January 2027**

---

## What I Work On

* **Agent runtimes & orchestration** — multi-agent workflows, tool-result loops, bounded execution, HITL, cancellation, replay, and failure semantics
* **Evaluation & observability** — frozen-input benchmarks, replay, LangSmith, RAGAS, OpenTelemetry, pass@k, fault injection, and cost/latency analysis
* **Stateful AI backends** — PostgreSQL, Redis/Lua, Kafka, async workflows, concurrency control, SSE/WebSocket, and cross-session memory
* **Production delivery** — Docker, Kubernetes/ACK, Helm, GitHub Actions, AWS EC2, rollout validation, and regression testing

---

## Open Source & Production Agent Systems

### [OpenMAIC](https://github.com/THU-MAIC/OpenMAIC) — Internship

Open-source AI education platform where I work on agent runtime, tool execution, grounding, evaluation, and reliability.

* Evolved the in-class agent runtime from a **Pi-based POC** into a bounded native execution layer, separating Director-led orchestration, child reasoning loops, and host execution with explicit budgets, cancellation/timeouts, terminal-state handling, and late-event isolation.
* Architected a closed-loop **Tool Harness** across **13 native tools and 4 execution paths**, standardizing idempotency, replay, cancellation, exception propagation, and authoritative tool-result continuation.
* Designed authoritative state coordination around **RuntimeStore + CAS optimistic concurrency + idempotent replay**, with browser E2E coverage for duplicate delivery, delayed results, cancellation, and races.
* Built a **100-case frozen-input benchmark and replay harness** informed by **141,102 production calls**, compared 10+ model/provider configurations, and validated a selected route at **106-way concurrency for 10 minutes with 755/755 usable outputs**.

Also contributed rendering/reliability work upstream to [HyperFrames](https://github.com/heygen-com/hyperframes/pull/3868), including an opt-in static-frame reuse path and regression coverage for input identity.

---

## Selected Engineering Results

| Area                      | Result                                                                                                  |
| ------------------------- | ------------------------------------------------------------------------------------------------------- |
| Agent runtime             | **13 native tools · 4 execution paths** with replay, cancellation, and explicit failure semantics       |
| Model/provider evaluation | **100 frozen cases · 141,102 production calls analyzed · 106-way concurrency · 755/755 usable outputs** |
| Agent reliability         | Flaky-tool success **69.7% → 91.2%** across **12 × 500** fault-injection simulations                    |
| Code generation eval      | Preserved **90% structural pass@3** while reducing CodeGen-stage input tokens by **~18%**               |
| Data pipelines            | Recurring ETL **8h → 1.2h (~85%)** across 350+ journals and 500K+ records/month                         |

---

## Technical Stack

**Languages**
Python · TypeScript/JavaScript · Java 21 · Go · SQL

**Agent & LLM Systems**
Pi Core · LangGraph/LangGraph4j · LangChain4j · ReAct · Planner–Executor · MCP · Tool Harnesses · HITL · Context Engineering · RAG · LangSmith

**Backend & Data**
FastAPI · Node.js · Spring Boot · Reactor · PostgreSQL/pgvector · Redis/Lua · Kafka · MongoDB · MySQL · Elasticsearch · Pinecone · SSE/WebSocket

**Frontend**
React/Next.js · Vue 3 · TypeScript

**Cloud, Reliability & Evaluation**
Docker · Kubernetes/ACK · Helm · GitHub Actions · AWS EC2 · Linux · OpenTelemetry · Prometheus/Grafana · RAGAS · Playwright · Replay · Fault Injection

---

## Featured Projects

### [InnerFlow — Stateful Agent Memory & Reliability](https://github.com/LING-6150/Ling-innerflow)

Stateful agent backend focused on memory lifecycle, concurrency, failure semantics, retrieval, and evaluation.

* Diagnosed a **Redis lost-update race** where asynchronous LLM compaction could overwrite concurrent writes; designed atomic Lua prefix replacement with deterministic concurrency and real-Redis integration tests.
* Redesigned tool outcomes around a backward-compatible **SUCCESS / PARTIAL / FAILURE** contract with retry-once and exception fail-safes, raising flaky-tool success **69.7% → 91.2%** across 12 × 500 simulations.
* Built conflict-aware cross-session memory with supersession, context-scoped exceptions, recurrence accumulation, and source provenance; benchmarked against full-history, retrieval, LWW, and extract-only baselines.

`Java 21` `Spring Boot` `Redis/Lua` `Kafka` `Python` `LangGraph4j`

---

### [AI Web Generation Engine](https://github.com/LING-6150/ling-ai-generation-engine) · [Evaluation Framework](https://github.com/LING-6150/llm-codegen-eval)

Natural-language requirements → generated web applications, paired with a reproducible evaluation and regression platform.

* Coordinated **6 agent roles** through typed RequirementSpec, TaskGraph, and ReviewReport contracts with bounded refinement and rollback.
* Bridged token streams into **Reactor SSE on Java 21 virtual threads** with concurrent request isolation and explicit cancellation/error semantics.
* Built a Python evaluation harness with structural checks, **Playwright** browser smoke tests, health gates, failure taxonomy, token attribution, and offline replay; preserved **90% structural pass@3** while cutting CodeGen-stage input tokens by **~18%** in an isolated 10-case × 3-run A/B benchmark.

`Java 21` `Spring Boot` `Vue 3` `TypeScript` `Python` `Playwright` `Redis`

---

### [AI Knowledge Agent Platform](https://github.com/LING-6150/ling-ai-agent)

Autonomous AI agent system integrating RAG pipelines with tool-calling agents.

* Hybrid retrieval: vector search (PGVector HNSW) + BM25 via RRF fusion, cross-encoder reranking (ms-marco-MiniLM-L-6-v2) via Python FastAPI
* ReAct hierarchical agent: `BaseAgent → ReActAgent → ToolCallAgent → LingManus` with stuck-state detection and human-in-the-loop escalation
* 8 tool callbacks + custom MCP Server (Pexels image search, Stdio/SSE transport) + Amap location MCP integration
* LangSmith tracing via OpenTelemetry · SSE streaming · CI/CD with Docker Buildx ARM→amd64

`Spring Boot` `Spring AI` `PGVector` `Python FastAPI` `Vue 3` `AWS EC2` `LangSmith`

---

### [Ling Clinic — AI Healthcare Platform](https://github.com/LING-6150/Ling-clinic-healthcare) · [Live Demo](http://98.93.64.174)

Full-stack clinic platform with a RAG-based AI health assistant grounded in an internal medical knowledge base.

* RAG pipeline: PDF ingestion → SHA-256 dedup → chunking → OpenAI embedding → PGVector (HNSW) → hybrid retrieval → RRF → SSE streaming
* RAGAS evaluation: Faithfulness **0.896** · Answer Relevancy **0.952** · Latency **310ms**
* Patient booking system + admin document upload pipeline + knowledge base management

`Spring Boot` `Vue 3` `PostgreSQL` `PGVector` `OpenAI` `AWS EC2` `Nginx`

---

### [LLM Evaluation Platform](https://github.com/LING-6150/llm-eval-platform)

Distributed system for benchmarking LLM reliability, latency, and output quality.

* Kafka-based async pipeline decoupling model inference (2–37s) from API responses
* Redis Lua atomic caching: latency **1,962ms → 0ms** on cache hits
* Sustained **4,800+ req/sec**, P99 **328ms** · retry strategies + dead-letter queues
* Elasticsearch prompt search · Prometheus + Grafana observability

`Spring Boot` `Apache Kafka` `Redis` `CockroachDB` `Prometheus` `Grafana` `React`

---

### [API Gateway & Integration Platform](https://github.com/LING-6150/API-Integrity-Platform)

Distributed gateway handling authentication, routing, and traffic control across 20+ backend services.

* Redis-based rate limiting and circuit breaker · AK/SK signature authentication · Dubbo RPC integration

`Spring Boot` `Redis` `Dubbo`

---

## Contact

* LinkedIn: [duan-ling-9970ba350](https://www.linkedin.com/in/duan-ling-9970ba350/)
* Email: [duan.lin@northeastern.edu](mailto:duan.lin@northeastern.edu)

