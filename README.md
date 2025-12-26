# Sentilytics – AI Engine

**An AI-based system for consolidated customer feedback analysis.**

---

## 🚀 Current Status: Phase 1 (Discovery & Validation)
**Goal:** Prove technical feasibility before writing production code.

| Gate | Name | Status | Link |
| :--- | :--- | :--- | :--- |
| **Gate A** | Scraping Viability | 🟡 PENDING | [`docs/validation/gate_A_scraping_viability.md`](docs/validation/gate_A_scraping_viability.md) |
| **Gate B** | Data Usability | 🔴 NOT STARTED | [`docs/validation/gate_B_data_usability.md`](docs/validation/gate_B_data_usability.md) |

---

## 📂 Repository Structure
* **`docs/`** – The "Brain". All research, endpoints, and validation decisions.
* **`scripts/`** – The "Lab". Messy, experimental scripts (Spikes) to test theories.
* **`SAMPLE_SCRAPED/`** – The "Evidence". JSON snippets proving we got the data.
* **`ai_engine/`** – (Empty) Reserved for Phase 2.
* **`api/`** – (Empty) Reserved for Phase 2.

## 🛠 Usage
This repository is currently in **Discovery Mode**.
1. **Do not** try to run a full app; there isn't one yet.
2. **Do** check `scripts/playwright_spike/` for individual scraping experiments.
3. Read **`docs/QUICK_REFERENCE_GUIDE.md`** for context.

## ⚠️ Phase 1 Rules
* **No Production Code:** We are writing scripts to *learn*, not to ship.
* **No Database:** We save data to local JSON files for now.
* **Focus on Risks:** Prioritize "Can we get the data?" over "How do we store it?"