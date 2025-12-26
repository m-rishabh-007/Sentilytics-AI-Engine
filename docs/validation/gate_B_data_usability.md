# Gate B – Data Usability

## Objective
Confirm the data is analytically meaningful for Aspect-Based Sentiment Analysis (ABSA), rather than just "technically scrapable."

## Success Criteria (Must Meet All)

### 1. Text Quality & Noise
* **Length:** ≥ 80% of reviews must have ≥ 5 tokens (ignoring emojis/URLs).
* **Language:** ≥ 90% identifiable language (English, Hindi, or Mixed).
* **Noise Ceiling:** ≤ 20% spam, templates, or empty "Thanks" messages.

### 2. Aspect Signal (Manual Check of 20 Reviews)
* **Basic Signal:** ≥ 60% (12/20) contain at least one clear aspect (e.g., *service, delivery, price*).
* **Complexity:** ≥ 30% (6/20) contain multiple aspects (Critical for ABSA vs. simple sentiment).

### 3. Metadata Utility
*Must contain at least 2 of the following:*
* Rating / Score
* Timestamp
* Author / Business Identifier
* Social Proof (Likes/Replies)

## Hard Fail Conditions
* Text is predominantly short (<3 words) or generic.
* Content is mostly broadcasts/announcements (not opinions).
* Impossible to distinguish between different entities or timeframes.

## Evaluation Result
* **Verdict:** PASS / FAIL
* **Rationale:** (Briefly justify the decision based on the sample data)