# 🚀 Duan Ling | Full-Stack Engineer (AI-Integrated Systems)

Master’s Student in Information Systems @ Northeastern University  

I build production-ready full-stack systems and integrate intelligent AI workflows into scalable backend architectures.

---

## 🧠 Core Focus

- End-to-end Full-Stack Development (Frontend → Backend → Database → Cloud)
- AI-Augmented Web Applications (LLM + Tool Calling + RAG)
- High-Concurrency Backend Systems (SSE Streaming, WebSocket, Rate Limiting)
- Distributed Systems & API Gateway Architecture
- Cloud Deployment & Reverse Proxy Optimization (AWS EC2 + Nginx)

---

## ⚙️ Tech Stack

**Languages:** Java, Python, SQL, JavaScript  
**Frontend:** Vue 3, React  
**Backend:** Spring Boot, Redis, MySQL, PostgreSQL, Dubbo  
**AI & LLM:** Spring AI, LangChain4j, LangGraph4j, RAG, PGVector  
**Distributed Systems:** ShardingSphere, Redis, Caffeine  
**Cloud & DevOps:** AWS EC2, Docker, Nginx, GitHub Actions  
**Observability:** Prometheus, Grafana, Micrometer  

---

# 🌟 Featured Projects

---

## 🏗 AI Web Application Generation Platform  
🔗 https://github.com/LING-6150/ling-ai-generation-engine  

Production-grade full-stack AI system converting natural language prompts into deployable web applications.

- Designed multi-mode AI generation pipeline (HTML / Multi-file / Vue 3) with LLM routing
- Eliminated concurrent request serialization caused by synchronous SSE parsing, improving latency by **28%**
- Built secure Tool Calling system enabling incremental code modification
- Implemented distributed token-bucket rate limiting and daily token quota control
- Deployed on AWS EC2 with Nginx reverse proxy, ensuring stable real-time streaming

---

## 🧠 AI Knowledge Agent Platform  
🔗 https://github.com/LING-6150/ling-ai-agent  

Autonomous agent system with production RAG pipeline and multi-LLM routing.

- Designed layered agent architecture (BaseAgent → ReAct → ToolCall → LingManus)
- Built RAG pipeline using PostgreSQL + PGVector (HNSW indexing)
- Implemented non-blocking SSE streaming sustaining 41 req/min under concurrent load
- Containerized and deployed on AWS EC2

---

## 🌐 API Gateway & Integration Platform  
🔗 https://github.com/LING-6150/API-Integrity-Platform  

Centralized gateway for authentication, routing, and distributed traffic control.

- Designed API Gateway managing 20+ services
- Implemented circuit breaking and Redis-backed rate limiting
- Developed AK/SK signature-based authentication with replay protection
- Integrated Dubbo RPC with graceful degradation strategies

---

## 🖼 AI Image Cloud Platform  
🔗 https://github.com/LING-6150/your-image-repo  

AI-powered collaborative image management system designed for scalability and high concurrency.

- Designed real-time collaboration backend using WebSocket synchronization with optimistic locking, maintaining sub-200ms latency under 100+ concurrent users
- Built RBAC-based access control and hybrid search pipeline combining metadata indexing with semantic retrieval
- Reduced database contention via ShardingSphere and multi-level caching (80%+ cache hit rate)
- Integrated object storage + CDN distribution for scalable image delivery
- Implemented AI-driven tagging and semantic indexing for similarity search

---

## 📊 GitHub Stats

<img align="center" src="https://github-readme-stats.vercel.app/api?username=LING-6150&show_icons=true&theme=tokyonight" />

<img align="center" src="https://github-readme-stats.vercel.app/api/top-langs/?username=LING-6150&layout=compact&theme=tokyonight" />

---

## 📫 Contact

LinkedIn: https://www.linkedin.com/in/duan-ling-9970ba350/  
Email: duan.lin@northeastern.edu  

---

⭐ Open to Full-Stack / Backend / AI Application Engineering opportunities
