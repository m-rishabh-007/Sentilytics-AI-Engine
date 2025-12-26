# ⚡ Quick Reference Guide

**Project:** Sentilytics AI Engine  
**Current Phase:** Discovery & Validation (Week 1)

This file is a map of the repository structure.  
For *how* to work (branching, commits, reviews), see `CONTRIBUTING.md`.

---

## 🗺️ Repository Map

| Directory | Purpose | Key Rule |
| :--- | :--- | :--- |
| **`docs/`** | The "Brain" (Research & Decisions). | If it's not documented here, it didn't happen. |
| **`scripts/`** | The "Lab" (Experimental Code). | Dirty code is allowed here (Spikes). |
| **`SAMPLE_SCRAPED/`** | The "Evidence" (JSON/Screenshots). | Commit **small** samples only. No full datasets. |
| **`data/raw/`** | Local Storage. | **Gitignored.** Store large/real datasets here. |
| **`ai_engine/`** | Production Code (Phase 2). | **Empty for now.** Do not add code here yet. |

---

## 🎯 Current Objectives (Week 1)

| Gate | Goal | Link |
| :--- | :--- | :--- |
| **Gate A** | Prove we can intercept data (Network). | [`docs/validation/gate_A_scraping_viability.md`](docs/validation/gate_A_scraping_viability.md) |
| **Gate B** | Prove the data is usable (Quality). | [`docs/validation/gate_B_data_usability.md`](docs/validation/gate_B_data_usability.md) |
