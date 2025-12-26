# Contributing Guidelines

## 1. Golden Rules
1. **Never push to `main`.** All work must go through a Merge Request.
2. **Evidence or it didn't happen.** Every MR must include proof (logs/screenshots).
3. **Clean History.** Do not commit secrets, `node_modules`, `venv`, or large datasets.

## 2. Branching Strategy
Use the following prefix convention for your branches:
* `setup/...`  – Project structure, config, installation
* `recon/...`  – Scripts for data scraping experiments
* `docs/...`   – Updating markdown files or guides
* `fix/...`    – Correcting a mistake

**Example:** `recon/google-maps-fetch`, `docs/update-gate-a`

## 3. Commit Messages
Write clear, descriptive messages. Start with a verb.
* ❌ Bad: "update", "fixed stuff", "added file"
* ✅ Good: "feat: add playwright script for scroll handling"
* ✅ Good: "docs: update Gate A criteria with new findings"

## 4. The Review Process
1. Create your Merge Request (MR) using the template.
2. Assign the Project Lead as the reviewer.
3. Once approved and merged, delete your branch.