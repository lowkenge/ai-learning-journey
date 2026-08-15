# Data Sanitization Policy

**Repo:** `~/ai-learning`  
**Author:** [Your Name]  
**Date:** 2026-08-15  
**Applies to:** All code, notebooks, datasets, screenshots, and blog content in this portfolio.

---

## 1. The Golden Rule

Every project in this portfolio is built on **synthetic or public data only**.  
No real production data from any employer, client, or regulated system is ever committed, published, or shared.

---

## 2. Never Publish

The following items are **strictly prohibited** in this repo, in any branch, issue, or commit history:

| Category | Examples |
|---|---|
| **Identifiers** | Real TXIDs, Lot Numbers, Serial Numbers, Container IDs, Work Order IDs |
| **Infrastructure** | Internal hostnames, IP addresses, connection strings, DB schemas, API endpoints |
| **Code & IP** | Employer source code (Camstar, Opcenter, Mendix modules), proprietary algorithms |
| **Documents** | Real SOPs, work instructions, batch records, validation protocols |
| **Visuals** | Production screenshots, photos of factory floors with visible ID labels |
| **Performance Data** | Real yield, scrap, cycle time, OEE, or quality metrics tied to actual products |

---

## 3. What Is Allowed

| Approach | Example |
|---|---|
| **Describe the problem shape** | "Reconciling transaction IDs against lot records in an MES" |
| **Synthetic data** | CSVs generated with NumPy/Faker that mirror the *schema* and *distribution* of real data |
| **Public datasets** | UCI ML Repository, Kaggle public datasets, government open data |
| **Anonymized mock-ups** | Manually crafted JSON/XML that resembles real structures but contains zero real values |

---

## 4. Synthetic Data Checklist

Before any dataset is committed:

- [ ] All IDs are generated (UUIDs, random sequences) — not copied from production
- [ ] Names, locations, and product codes are fictional
- [ ] Distributions are realistic, but values do not match any real record
- [ ] File contains a header comment/note confirming it is synthetic

---

## 5. Pre-Commit Verification

Run this mental check before every `git push`:

&gt; *"If my former employer's security team, a regulator, or a hiring manager saw this commit, would I be comfortable explaining every byte of it in public?"*

If the answer is no, revert and sanitize.

---

## 6. Scope

This policy applies to:
- Jupyter notebooks
- Python scripts and SQL files
- Markdown blog drafts
- README examples
- Embedded screenshots or diagrams
- Video walkthroughs (screen recordings must use mock data)

---

## 7. Rationale (for portfolio readers)

I maintain this policy because my background is in **regulated medical-device manufacturing** (MES / Camstar / Opcenter / Mendix). In these environments, data integrity and IP protection are not optional — they are compliance requirements. Treating my public portfolio with the same rigor demonstrates the operational maturity I bring to AI engineering roles.

---

*Last reviewed: 2026-08-15*