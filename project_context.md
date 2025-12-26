
# **Sentilytics — Multi-Source Customer Feedback Intelligence**

**One-line pitch**
Sentilytics is a system that collects customer feedback from multiple online platforms and analyzes sentiment, topics, and bias to help MSMEs understand customer perception more accurately.

---

## 1. Team Roles & Responsibilities

**Project Lead / AI & Architecture**

* Owns overall system design and technical direction
* Designs ML/NLP components (sentiment, topics, embeddings, bias handling)
* Reviews and integrates code from all modules

**Scraping Engineer**

* Builds Playwright-based scrapers using network interception
* Ensures reliability, pagination handling, and data consistency

**Backend / Data Engineer**

* Handles data ingestion, normalization, and storage
* Designs APIs and database interactions

**Frontend Engineer**

* Builds the analytics dashboard using React
* Focuses on data visualization and usability

**Testing & Documentation**

* Writes test cases, validation checks, and documentation
* Ensures features are reproducible and understandable

> Responsibilities may overlap depending on workload and progress.

---

## 2. Constraints & Goals

**Timeline**

* 8 weeks total
* ~1 hour/day per person (≈ 50–60 hours each)

**Compute Resources**

* Local development machines
* Optional access to an NVIDIA RTX gaming PC for heavier training tasks

**Data Sources**

* Publicly accessible, scraped live data
* Optional use of open datasets (e.g., Yelp) for benchmarking

**Final Deliverable**
A resume-ready, production-style project that includes:

* working multi-platform data ingestion
* meaningful analytics
* clean repository structure
* documentation and demo (screenshots/video)

---

## 3. MVP Scope (Must-Have)

### Data Ingestion

* Playwright-based scraper using network interception
* At least **two platforms** (Google Maps + Twitter/X)
* Structured JSON output (no fragile HTML scraping)

### Data Processing

* Text normalization and language detection
* Sentiment classification using pretrained transformer models
* Topic / aspect extraction using clustering and keyword mapping

### Bias Handling

* Deduplication of repeated reviewers
* Platform-level weighting to reduce overrepresentation bias

### Analytics & Dashboard

* Sentiment distribution overview
* Top topics/aspects
* Time-based sentiment trends
* Basic cross-platform correlation view

### Engineering

* Dockerized services
* GitLab CI for linting, tests, and builds

---

## 4. Non-Functional Requirements

* **Performance:** dashboard responses under 3 seconds for cached queries
* **Privacy:** anonymize usernames and identifiers during ingestion
* **Scalability:** microservice-friendly design (Docker Compose first)

---

## 5. Data Structure (Indicative, Not Fixed)

Example fields (subject to refinement after data discovery):

```json
{
  "source": "google_maps",
  "review_id": "...",
  "business_id": "...",
  "raw_text": "...",
  "normalized_text": "...",
  "language": "en",
  "timestamp": "...",
  "rating": 4,
  "sentiment": "positive",
  "topics": ["service", "pricing"]
}
```

Small real samples will be stored in `/SAMPLE_SCRAPED/`.

---

## 6. Technology Stack (Recommended)

* **Scraping:** Playwright (Python or Node.js)
* **Backend / AI:** Python (FastAPI preferred)
* **Database:** PostgreSQL (+ pgvector for embeddings)
* **Models:** Hugging Face transformers, sentence-transformers
* **Frontend:** React (Vite) with charting libraries
* **DevOps:** Docker, Docker Compose, GitLab CI

Final choices may evolve based on discovery findings.

---

## 7. Bias & Correlation Approach (High-Level)

* Identify and downweight duplicate reviewers
* Apply platform-level weighting to balance skewed data
* Compare trends across platforms using time-series correlation

Exact techniques will be finalized after inspecting real data.

---

## 8. Evaluation & Acceptance Criteria

* Sentiment accuracy ≥ **75%** on a small labeled validation set
* Successful scraping of ≥ **50 reviews per platform**
* Dashboard renders analytics within **3 seconds**
* GitLab CI passes for all merge requests

---

## 9. Project Timeline (Indicative)

* **Weeks 1–2:** Data discovery & scraping validation
* **Weeks 3–4:** Data pipeline + baseline ML models
* **Weeks 5–6:** Bias handling + analytics
* **Week 7:** Dashboard & system integration
* **Week 8:** Testing, documentation, demo preparation

---

## 10. Workflow & Collaboration

* All work is done via feature branches
* Changes are merged through Merge Requests
* No direct pushes to the main branch
* Evidence (logs, samples, screenshots) required for validation work
