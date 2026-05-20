# NCES IPEDS Postsecondary Education Analysis

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter)
![Data](https://img.shields.io/badge/Data-Federal%20IPEDS%20AY%202023--24-4CAF50)

## Overview

An exploratory analysis of U.S. postsecondary education trends using three federal administrative datasets from the **NCES Integrated Postsecondary Education Data System (IPEDS)** — covering 4,000+ institutions for Academic Year 2023–24.

The analysis addresses three research questions around distance education adoption, program completion patterns, and the relationship between online enrollment and institutional output.

---

## Data Sources

All datasets are publicly available from [NCES IPEDS](https://nces.ed.gov/ipeds/use-the-data).

| File | Survey Component | Description |
|------|-----------------|-------------|
| `EFFY2024_dist.csv` | 12-Month Enrollment | Distance education enrollment by institution and level (AY 2023–24) |
| `CIPCode2020.csv` | CIP Codes | Classification of Instructional Programs — program titles and codes |
| `C2024_A.csv` | Completions | Program completions by institution, CIP code, and award level (AY 2023–24) |

---

## Research Questions & Findings

### Q1 — Distance Enrollment by Level
Aggregated distance participation across undergraduate, graduate, and first-professional categories, computing share of exclusively online, hybrid, and in-person enrollment.

### Q2 — Top CIP Program Fields by Completion Volume
Ranked 2-digit CIP program families by total completions nationwide — identifying the ten highest-output fields across all institutions.

### Q3 — Distance Enrollment vs. Program Completions (Correlation)
Examined whether institutions with higher shares of exclusively online undergraduates produce more or fewer completions.

> **Finding:** Pearson r = −0.029 (p < 0.05) — statistically significant but negligible negative correlation. Distance enrollment share alone is not a meaningful predictor of institutional completion output.

---

## Visualizations

| Chart | Description |
|-------|-------------|
| Stacked bar | Distance enrollment proportions by level (exclusively online / hybrid / in-person) |
| Horizontal bar | Top 10 CIP program fields by total completion volume |
| Scatter + regression | Distance enrollment % vs. total completions across 4,000+ institutions |

---

## Key Variables

| Variable | Description |
|----------|-------------|
| `EFYDETOT` | Total 12-month enrollment |
| `EFYDEEXC` | Exclusively distance-enrolled students |
| `EFYDESOM` | Some distance enrollment (hybrid) |
| `EFYDENON` | No distance enrollment |
| `CTOTALT` | Total program completions |
| `CIPCODE` | Classification of Instructional Programs code |
| `AWLEVEL` | Award level (certificate, bachelor's, master's, doctorate) |
| `UNITID` | Unique institution identifier |

---

## Tech Stack

| Library | Purpose |
|---------|---------|
| `pandas` | Dataset ingestion, merging, aggregation |
| `numpy` | Numerical calculations |
| `matplotlib` | Bar charts and scatter plots |
| `scipy` | Pearson correlation and p-value computation |

---

## Setup & Usage

```bash
# 1. Clone
git clone https://github.com/SaiTejaPortfolioDS/Nces-ipeds-analysis.git
cd Nces-ipeds-analysis

# 2. Install dependencies
pip install pandas numpy matplotlib scipy jupyter

# 3. Download IPEDS data files from https://nces.ed.gov/ipeds/use-the-data
#    Place in project root:
#      - EFFY2024_dist.csv
#      - CIPCode2020.csv
#      - C2024_A.csv

# 4. Launch notebook
jupyter notebook Nces_ipeds_analysis.ipynb
```

---

## Author

**Mohan Venkata Pavan Sai Teja Kattiboyina**
MS Business Analytics & AI — University of Texas at Dallas

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?logo=linkedin)](https://www.linkedin.com/in/saitejakmvp/)
[![Portfolio](https://img.shields.io/badge/Portfolio-saitejaportfolio.com-00897B)](https://saitejaportfolio.com)
