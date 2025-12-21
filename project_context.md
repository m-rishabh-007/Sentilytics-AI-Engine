Project name & 1-line pitch
Sentilytics — multi-source AI feedback consolidation + bias compensation for MSMEs.

Roles & responsibilities (who does what)

You: architecture reviewer, ML/NLP lead, code reviewer.

Member A: Playwright scraper + scraping CI.

Member B: Data pipeline & DB.

Member C: Frontend dashboard (React).

Member D: Testing & docs.

Constraints & goals (be explicit)

Timeline: 8 weeks (2 months), working ~1 hr/day (≈56 hrs).

Compute: small local dev machines; optional GPU: friend’s gaming PC (NVIDIA RTX—available for training heavy ops).

Data: scraped live data + optional Yelp open dataset.

Deliverable: resume-ready, production-style microservices + GitLab CI, documented readme, demo video.

MVP scope (must-have for the deadline)

Playwright network-interception scraper for 2 platforms (Google Maps + Twitter/X) that saves JSON.

Normalization + basic sentiment classifier (pretrained transformer, fine-tune if time).

Topic/aspect extraction (clustering + keyword mapping).

Bias-compensation module (platform weighting + duplicate reviewer dedupe).

Dashboard that shows sentiment distribution, top topics, time trend and a basic correlation matrix across platforms.

Dockerized microservices + GitLab CI for build/test.

Non-functional requirements

Response latency for dashboard requests < 3s for cached queries.

Data privacy: anonymize PII in ingestion.

Scalability: microservices, simple K8s-friendly Docker compose.

Data & schema

Example fields: source, review_id, business_id, raw_text, normalized_text, language, timestamp, rating, sentiment, topics, embedding_vector

Provide small sample JSON(s) in /data/samples/ (upload these to repo).

Tech stack (recommended)

Scraper: Playwright (Node or Python).

Backend microservices: Python FastAPI (AI engine) + Java Spring Boot for API façade only if needed (but keep single-language to save time). I recommend FastAPI + uvicorn.

DB: PostgreSQL. Vector store: Postgres + pgvector (or Milvus later).

Embeddings / models: sentence-transformers (all-MiniLM-L6 for prod embeddings); Hugging Face transformers for sentiment.

Frontend: React (Vite) + Recharts / Chart.js or Tailwind.

CI/CD: GitLab CI (pipelines for lint/test/docker build).

Containerization: Dockerfiles for each service.

Dev infra: Docker Compose for local, optional deploy with GitLab pages/Heroku/AWS later.

Bias compensation & correlation plan (short)

Detect duplicate reviewers via hashed user identifier and downweight repeats.

Platform weighting: compute platform_weight = 1 / (platform_review_count ^ alpha) and apply to aggregated scores.

Propensity score correction: estimate probability a user posts on platform A vs B, reweight accordingly.

Correlation: compute cross-platform time series and Pearson / DTW to measure lagged correlation.

Evaluation & acceptance tests

Sentiment accuracy on small labeled set ≥ 75% (MVP).

Dashboard loads sample analytics within 3s.

Scraper successfully saves structured JSON for N=50 items from each platform.

GitLab pipeline passes on PRs (lint + unit tests).

Milestones & weekly plan (see next section).

GitLab workflow rules (issue templates, MR checklist — see below).

Contact / repo links (when available).