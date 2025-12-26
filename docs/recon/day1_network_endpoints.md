# Network Recon Log – Day 1 (Google Maps)

**Target:** Google Maps Reviews (Browser Network Traffic)  
**Goal:** Identify the specific API endpoints used to fetch review data.

---

## 📍 Endpoint 1: The "Scroll" API (Priority)
*This is the endpoint that triggers when scrolling down to load more reviews.*

### Request Details
- **Method:** `[GET / POST]`
- **URL Pattern:** `...`
- **Critical Query Params:**
  - `[Param Name]`: `[Value / Purpose]`
  - `[Param Name]`: `[Value / Purpose]`

### Response Analysis
- **Format:** `[JSON / Protobuf / HTML]`
- **Can we decode it?** [ ] Yes  [ ] No
- **Key Data Found:**
  - [ ] User Name
  - [ ] Review Text
  - [ ] Rating
  - [ ] Timestamp

---

## 📍 Endpoint 2: Initial Page Load (Fallback)
*The URL loaded when you first open the business page.*

- **URL:** `...`
- **Observation:**  
  (e.g., Is data embedded in a `<script>` tag? Is it in the HTML body?)

---

## 🛑 Dead Ends & Blockers
- **Attempt 1:** (e.g., "Tried removing parameter X, got 403 Forbidden")
- **Attempt 2:** 
