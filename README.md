# AI Workforce Data — Open Datasets by Meo Advisors

![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)
![Datasets: 6](https://img.shields.io/badge/datasets-6-blue)
![Rows: 155k+](https://img.shields.io/badge/rows-155%2C497-green)
![Updated: daily](https://img.shields.io/badge/updated-daily-brightgreen)

> The most comprehensive **open data on how AI is reshaping the US workforce** — **1,016 occupations** ranked by automation risk, **134,278 US companies** scored for AI-adoption opportunity, **12,623 WARN layoff events**, and more.
>
> Maintained by **[Meo Advisors](https://meoadvisors.com)**. Free under CC BY-NC 4.0. Refreshed daily. CSV + JSON.

**Live download manifest:** https://data.meoadvisors.com/datasets/manifest.json
**Browse + visualize:** https://meoadvisors.com/datasets/

---

## 📊 The datasets

| Dataset | Rows | What it is | Download | Explore |
|---|--:|---|---|---|
| **AI Occupational Impact Index** | 1,016 | Every BLS/O\*NET occupation scored 0–100 for AI automation risk, with task-level exposure and median wage | [CSV](https://meoadvisors.com/api/datasets/occupations.csv) · [JSON](https://meoadvisors.com/api/datasets/occupations.json) | [jobs-replaced-by-ai](https://meoadvisors.com/jobs-replaced-by-ai/) |
| **AI Adoption Index (US Companies)** | 134,278 | US companies scored for AI cost-out opportunity by industry, revenue band, and tech stack | [CSV](https://meoadvisors.com/api/datasets/ai-opportunities.csv) · [JSON](https://meoadvisors.com/api/datasets/ai-opportunities.json) | [ai-opportunities](https://meoadvisors.com/ai-opportunities/) |
| **AI Adoption Leaderboards** | 6,822 | Ranked leaderboards of AI-adoption opportunity by state, city, industry, and cross-cut cohort | [CSV](https://meoadvisors.com/api/datasets/leaderboards.csv) · [JSON](https://meoadvisors.com/api/datasets/leaderboards.json) | [leaderboards](https://meoadvisors.com/ai-opportunities/leaderboard/) |
| **Software AI Replaceability** | 594 | Software products/categories scored for how replaceable they are by AI/agentic tools | [CSV](https://meoadvisors.com/api/datasets/software-replaceability.csv) · [JSON](https://meoadvisors.com/api/datasets/software-replaceability.json) | [software-ai-replaceability](https://meoadvisors.com/software-ai-replaceability/) |
| **AI Platforms Catalog** | 164 | Catalog of AI platforms/tools with category and capability metadata | [CSV](https://meoadvisors.com/api/datasets/ai-platforms.csv) · [JSON](https://meoadvisors.com/api/datasets/ai-platforms.json) | [ai-platforms](https://meoadvisors.com/ai-platforms/) |
| **WARN Layoff Atlas** | 12,623 | US WARN Act layoff notices, normalized by state, employer, date, and headcount | [CSV](https://meoadvisors.com/api/datasets/warn-layoffs.csv) · [JSON](https://meoadvisors.com/api/datasets/warn-layoffs.json) | [warn-layoff-atlas](https://meoadvisors.com/research/warn-layoff-atlas/) |

All six carry [schema.org/Dataset](https://schema.org/Dataset) markup and are designed to be machine-readable and citable.

---

## 🧭 Why this exists

Everyone is asking two questions — *"Will AI take my job?"* and *"Where is the AI ROI?"* — but the underlying data is scattered across McKinsey, Goldman Sachs, WEF, BLS, and O\*NET PDFs. This repository consolidates it into clean, versioned, machine-readable datasets that anyone can download, analyze, and cite.

**How it compares:** other open AI-job datasets cover ~100 occupations. The AI Occupational Impact Index covers **1,016** (the full BLS SOC taxonomy), and it sits alongside a **134,278-company** adoption index and a **12,623-event** layoff atlas — no other free source combines all three.

---

## 🔬 Methodology

Scoring methodology, sources, and limitations are documented per dataset on the Meo Advisors site:

- **Occupational AI impact** — built from BLS employment, O\*NET task data, and AI-occupational-exposure (AIOE) research. → https://meoadvisors.com/jobs-replaced-by-ai/
- **Company AI adoption** — firmographics + tech-stack signals + a TCA/DIY cost-out framework. → https://meoadvisors.com/ai-opportunities/
- **Full methodology & sources** → https://meoadvisors.com/research/

---

## 🚀 Quick start

```bash
# Grab the occupational risk index as CSV
curl -L https://meoadvisors.com/api/datasets/occupations.csv -o occupations.csv

# Or pull everything from the manifest
curl -L https://data.meoadvisors.com/datasets/manifest.json
```

```python
import pandas as pd
df = pd.read_csv("https://meoadvisors.com/api/datasets/occupations.csv")
print(df.sort_values("ai_impact_score", ascending=False).head(20))
```

---

## 📚 Cite this

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

---

## ⚖️ License

Released under **[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/)** — free to use for research, journalism, and education **with attribution** to [Meo Advisors](https://meoadvisors.com). For commercial licensing, [get in touch](https://meoadvisors.com/contact/).

---

## 🏢 About Meo Advisors

[Meo Advisors](https://meoadvisors.com) helps mid-market companies deploy agentic AI on a pay-for-performance basis — measuring real cost-out, not promising it. We publish this data because the AI-and-work conversation deserves better numbers. Explore the interactive tools at **[meoadvisors.com](https://meoadvisors.com)**.

*Found this useful? A ⭐ helps others discover it — and corrections/PRs are welcome.*
