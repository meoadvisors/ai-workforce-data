# AI Workforce Data — Open Datasets on How AI Is Reshaping Work

![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)
![Datasets: 6](https://img.shields.io/badge/datasets-6-blue)
![Rows: 155,497](https://img.shields.io/badge/rows-155%2C497-green)
![Coverage: United States](https://img.shields.io/badge/coverage-United%20States-blue)
![Updated: daily](https://img.shields.io/badge/updated-daily-brightgreen)

**The most comprehensive open data on AI and the US workforce** — **1,016 occupations** ranked by AI automation risk, **134,278 US companies** scored for AI-adoption opportunity, **12,623 WARN-Act layoff notices**, plus software-replaceability and AI-platform reference data. Six machine-readable datasets, **155,497 rows** total, free under CC BY-NC 4.0, refreshed daily.

Maintained by **[Meo Advisors](https://meoadvisors.com)** · Browse + visualize at **[meoadvisors.com/datasets](https://meoadvisors.com/datasets/)** · Live manifest: **[data.meoadvisors.com/datasets/manifest.json](https://data.meoadvisors.com/datasets/manifest.json)**

> If you're researching **which jobs are most at risk from AI**, **how fast companies are adopting AI**, or the **labor-market impact of automation**, this repository consolidates data that is otherwise scattered across dozens of BLS tables, O\*NET files, and consultancy PDFs into clean CSV + JSON you can download and cite.

---

## 📚 Table of contents

- [The datasets at a glance](#-the-datasets-at-a-glance)
- [1. AI Occupational Impact Index](#1-ai-occupational-impact-index--1016-occupations)
- [2. AI Adoption Index (US Companies)](#2-ai-adoption-index-us-companies--134278-companies)
- [3. AI Adoption Leaderboards](#3-ai-adoption-leaderboards--6822-rankings)
- [4. Software AI Replaceability Index](#4-software-ai-replaceability-index--594-products)
- [5. AI Platforms Catalog](#5-ai-platforms-catalog--164-platforms)
- [6. WARN Layoff Atlas](#6-warn-layoff-atlas--12623-notices)
- [Methodology](#-methodology)
- [Who uses this data](#-who-uses-this-data)
- [How to use](#-how-to-use)
- [How this compares](#-how-this-compares)
- [Updates & freshness](#-updates--freshness)
- [How to cite](#-how-to-cite)
- [FAQ](#-faq)
- [License](#-license)
- [About Meo Advisors](#-about-meo-advisors)

---

## 📊 The datasets at a glance

| # | Dataset | Rows | What it answers | Download | Explore |
|--:|---|--:|---|---|---|
| 1 | AI Occupational Impact Index | 1,016 | Which jobs are most/least exposed to AI automation? | [CSV](https://meoadvisors.com/api/datasets/occupations.csv) · [JSON](https://meoadvisors.com/api/datasets/occupations.json) | [jobs-replaced-by-ai](https://meoadvisors.com/jobs-replaced-by-ai/) |
| 2 | AI Adoption Index (US Companies) | 134,278 | Which companies are adopting AI, and where's the cost-out opportunity? | [CSV](https://meoadvisors.com/api/datasets/ai-opportunities.csv) · [JSON](https://meoadvisors.com/api/datasets/ai-opportunities.json) | [ai-opportunities](https://meoadvisors.com/ai-opportunities/) |
| 3 | AI Adoption Leaderboards | 6,822 | How does AI adoption rank by state, city, and industry? | [CSV](https://meoadvisors.com/api/datasets/leaderboards.csv) · [JSON](https://meoadvisors.com/api/datasets/leaderboards.json) | [leaderboards](https://meoadvisors.com/ai-opportunities/leaderboard/) |
| 4 | Software AI Replaceability | 594 | Which software categories can AI agents replace? | [CSV](https://meoadvisors.com/api/datasets/software-replaceability.csv) · [JSON](https://meoadvisors.com/api/datasets/software-replaceability.json) | [software-ai-replaceability](https://meoadvisors.com/software-ai-replaceability/) |
| 5 | AI Platforms Catalog | 164 | Which enterprise AI platforms exist, and how enterprise-ready are they? | [CSV](https://meoadvisors.com/api/datasets/ai-platforms.csv) · [JSON](https://meoadvisors.com/api/datasets/ai-platforms.json) | [ai-platforms](https://meoadvisors.com/ai-platforms/) |
| 6 | WARN Layoff Atlas | 12,623 | Where are mass layoffs happening, and how many cite AI? | [CSV](https://meoadvisors.com/api/datasets/warn-layoffs.csv) · [JSON](https://meoadvisors.com/api/datasets/warn-layoffs.json) | [warn-layoff-atlas](https://meoadvisors.com/research/warn-layoff-atlas/) |

All six carry [schema.org/Dataset](https://schema.org/Dataset) markup, are versioned, and are designed to be cited.

---

## 1. AI Occupational Impact Index — 1,016 occupations

A 0–100 **AI automation-risk score** for every detailed occupation in the US Bureau of Labor Statistics **Standard Occupational Classification (SOC)** taxonomy — the most complete occupation-level **"jobs replaced by AI"** ranking we're aware of (most public lists cover ~100 jobs; this covers all 1,016).

**Each row includes:**
- **AI Exposure Score (0–100)** — composite of task-level automation feasibility and the academic AI Occupational Exposure (AIOE) index
- **Employment (2024)** and **projected employment (2034)** from BLS
- **Median annual wage** (BLS OEWS)
- **Automation timeline** — expected window for material automation (1–3y / 3–7y / 7–15y / 15+y)
- **SOC major group** (e.g., *Office and Administrative Support*)
- **Wage exposure** — median wage × employment × exposure, i.e. the annual labor cost sitting in automatable tasks

**Sources:** BLS Occupational Employment and Wage Statistics (OEWS); BLS Employment Projections 2024–2034; O\*NET 30.2 task data; Felten, Raj & Seamans (2021) AIOE.

**Use it to:** rank the highest- and lowest-risk occupations, model workforce-transition exposure by SOC family, or chart whether AI risk concentrates in high- or low-wage work. Interactive explorer: **[meoadvisors.com/jobs-replaced-by-ai](https://meoadvisors.com/jobs-replaced-by-ai/)**.

## 2. AI Adoption Index (US Companies) — 134,278 companies

A 0–100 **AI-adoption score** for 134,278 US companies, built from *observed* signals rather than self-reported surveys — the largest public company-level AI-adoption dataset we publish.

**Each row includes:** AI Adoption Score (0–100); letter grade (A–D by quartile); NAICS-2 industry; headquarters state and city; employee size band; AI/ML-relevant **tech-stack signals**; cohort rank within industry + geography; and an estimated annualized **AI cost-out / savings opportunity** in USD.

**Sources:** firmographics (People Data Labs), technographics (BuiltWith / Wappalyzer), and content signals (AI-titled job postings, public case studies, executive disclosures).

**Use it to:** find the AI leaders and laggards in any industry or state, size the AI cost-out opportunity for a sector, or build account-prioritization models. Interactive explorer: **[meoadvisors.com/ai-opportunities](https://meoadvisors.com/ai-opportunities/)**.

## 3. AI Adoption Leaderboards — 6,822 rankings

Pre-computed leaderboards that rank AI adoption across **all 50 states, 300+ metros, 1,200+ cities, and 100+ NAICS industries**, plus cross-cut cohorts. Each leaderboard carries a company count, average and median score, grade distribution, and its top companies — ready-made for "**AI adoption by state/industry**" comparisons without crunching the full company index. Explore: **[meoadvisors.com/ai-opportunities/leaderboard](https://meoadvisors.com/ai-opportunities/leaderboard/)**.

## 4. Software AI Replaceability Index — 594 products

594 enterprise software products scored 0–100 for how completely an **AI agent layer could replace or substantially augment them** — across CRM, ERP, marketing automation, customer service, finance, HR, and developer tools. Includes a workflow-modularity score and the known AI-native challenger per category. Useful for build-vs-buy and "**what SaaS will AI replace**" analysis. Explore: **[meoadvisors.com/software-ai-replaceability](https://meoadvisors.com/software-ai-replaceability/)**.

## 5. AI Platforms Catalog — 164 platforms

A reference catalog of 164 enterprise AI platforms and tools — LLMs, AI agents, RAG, vector databases, orchestration, and observability — each tagged with category, an enterprise-readiness score (SOC2, SLAs, multi-tenancy, deployment options), pricing tier, and integration coverage. Useful for vendor evaluation and competitive landscaping. Explore: **[meoadvisors.com/ai-platforms](https://meoadvisors.com/ai-platforms/)**.

## 6. WARN Layoff Atlas — 12,623 notices

12,623 federally-mandated **WARN-Act layoff notices** filed by US employers, normalized across all 50 state labor agencies for company name, NAICS industry, location, effective/notice date, and affected-worker count — plus an **AI-attribution likelihood** score estimating whether each layoff is AI/automation-driven. The most useful open source for tracking **AI-related layoffs** and workforce displacement over time. Explore: **[meoadvisors.com/research/warn-layoff-atlas](https://meoadvisors.com/research/warn-layoff-atlas/)**.

---

## 🔬 Methodology

Every score is **falsifiable and sourced** — we publish the inputs and the formula, not a black box:

- **Occupational AI risk** combines O\*NET task-level automation feasibility, BLS employment + wage data, and the peer-reviewed AIOE index. Full method: [meoadvisors.com/jobs-replaced-by-ai](https://meoadvisors.com/jobs-replaced-by-ai/).
- **Company AI adoption** blends firmographics, technographics, and public content signals into a composite 0–100 score with industry/geography cohort ranking. Full method: [meoadvisors.com/ai-opportunities](https://meoadvisors.com/ai-opportunities/).
- **WARN AI-attribution** uses LLM classification of notice text cross-referenced with company tech-stack signals.

Methodology notes, sources, and limitations for all datasets: **[meoadvisors.com/research](https://meoadvisors.com/research/)**.

## 👥 Who uses this data

- **Journalists & researchers** writing about AI and jobs — cite a real, current 1,016-occupation risk ranking instead of a stale 2013 estimate.
- **Policymakers & economists** modeling workforce transition and regional automation exposure.
- **Operators & investors** sizing the AI cost-out opportunity by company, industry, or geography.
- **Data scientists & developers** who want clean, machine-readable CSV/JSON with stable URLs.

## 🚀 How to use

```bash
# Download any dataset as CSV (stable canonical URL, 302 → CDN)
curl -L https://meoadvisors.com/api/datasets/occupations.csv -o occupations.csv

# Or pull the manifest listing all six with row counts + freshness
curl -L https://data.meoadvisors.com/datasets/manifest.json
```

```python
import pandas as pd
jobs = pd.read_csv("https://meoadvisors.com/api/datasets/occupations.csv")
print(jobs.sort_values("ai_impact_score", ascending=False).head(20))  # highest AI-risk jobs
```

```r
jobs <- read.csv("https://meoadvisors.com/api/datasets/occupations.csv")
head(jobs[order(-jobs$ai_impact_score), ], 20)
```

## 📈 How this compares

| | This dataset | Typical public alternatives |
|---|---|---|
| Occupations ranked for AI risk | **1,016** (full BLS SOC) | ~50–100 |
| Companies scored for AI adoption | **134,278** | rarely public |
| Layoff records with AI attribution | **12,623** | fragmented per-state |
| Format | CSV + JSON, schema.org/Dataset | PDF tables |
| Price | **Free** (CC BY-NC 4.0) | paywalled reports |

## 🔄 Updates & freshness

Datasets refresh **daily** and are served from a CDN at stable URLs, so the canonical links above always point at the latest snapshot. The [manifest](https://data.meoadvisors.com/datasets/manifest.json) reports per-dataset row counts and last-updated timestamps.

## 📚 How to cite

**Plain:**
> Meo Advisors (2026). *AI Workforce Data: Open Datasets on AI's Impact on the US Workforce.* https://meoadvisors.com/datasets/

**BibTeX:**
```bibtex
@misc{meoadvisors_ai_workforce_data_2026,
  title        = {AI Workforce Data: Open Datasets on AI's Impact on the US Workforce},
  author       = {{Meo Advisors}},
  year         = {2026},
  howpublished = {\url{https://meoadvisors.com/datasets/}},
  note         = {CC BY-NC 4.0}
}
```

## ❓ FAQ

**Which jobs are most at risk of being replaced by AI?**
The [AI Occupational Impact Index](#1-ai-occupational-impact-index--1016-occupations) ranks all 1,016 BLS occupations 0–100; data-entry, routine administrative, and repetitive-task roles score highest, while jobs heavy in judgment, physical dexterity, and interpersonal work score lowest. Download the CSV to sort the full ranking.

**Where can I download free data on AI and jobs?**
Right here — all six datasets are free under CC BY-NC 4.0 as CSV + JSON via the links above, with no signup.

**How is AI automation risk scored?**
By combining O\*NET task-level automation feasibility, BLS employment and wage data, and the peer-reviewed AIOE index into a 0–100 composite. See [Methodology](#-methodology).

**Which companies are adopting AI the fastest?**
The [AI Adoption Index](#2-ai-adoption-index-us-companies--134278-companies) scores 134,278 US companies; the [Leaderboards](#3-ai-adoption-leaderboards--6822-rankings) rank adoption by state, city, and industry.

**Are AI-driven layoffs measurable?**
The [WARN Layoff Atlas](#6-warn-layoff-atlas--12623-notices) tracks 12,623 layoff notices with an AI-attribution likelihood score.

**Can I use this commercially?**
The license is CC BY-NC 4.0 (free for research, journalism, and education with attribution). For commercial use, [contact Meo Advisors](https://meoadvisors.com/contact/).

## ⚖️ License

Released under **[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/)** — free to use for research, journalism, and education **with attribution** to [Meo Advisors](https://meoadvisors.com). For commercial licensing, [get in touch](https://meoadvisors.com/contact/).

## 🏢 About Meo Advisors

[Meo Advisors](https://meoadvisors.com) helps mid-market companies deploy **agentic AI on a pay-for-performance basis** — measuring real cost-out instead of promising it. We publish this data because the AI-and-work conversation deserves better numbers. Explore our research and interactive tools:

- 🔎 [Jobs Replaced by AI](https://meoadvisors.com/jobs-replaced-by-ai/) — occupation risk explorer
- 🏢 [AI Opportunities](https://meoadvisors.com/ai-opportunities/) — company AI-adoption scores
- 📊 [Public Datasets](https://meoadvisors.com/datasets/) — this full catalog
- 🧭 [How It Works](https://meoadvisors.com/how-it-works/) · [Agentic Enterprise](https://meoadvisors.com/agentic-enterprise/)

*Found this useful? A ⭐ helps others discover it, and corrections / PRs are welcome.*
