# DaCoT Challenge 2026 — Pharma Analytics UEMOA
🇫🇷 [Version française disponible ici](README_FR.md)
> **€1.24M in hidden losses identified. €2.45M margin recovery plan delivered.**  
> 50,000 transactions · 80 pharmacies · 8 UEMOA countries · 5-page Power BI dashboard

![Dashboard Overview](screenshots/page1_synthese.png)

---

## Business Problem

A pharma distribution network operating across West Africa faced two consecutive years
of revenue decline (-1.0% in 2023), with no clear diagnosis available to management.

After analysis: **29.6% of all transactions were sold at a loss** — €1.24M in value
destruction, completely invisible without proper data infrastructure.

**Mission:** Diagnose root causes across 50,000 transactions, quantify the financial
impact, and deliver a prioritized, actionable recovery plan.

---

## Approach

1. **Data audit** — Structured 4 raw tables into a Star Schema model (FaitVentes, DimProduit, DimPharmacie, DimDate)
2. **Exploratory analysis** — Identified loss-making patterns by product, pharmacy, country, and promotion type
3. **Business modeling** — Built 30 DAX measures covering revenue, margin, promotional ROI, and geographic performance
4. **Geospatial mapping** — Azure Maps integration to visualize performance across 8 UEMOA countries
5. **Recommendations** — Delivered a prioritized action plan with quantified impact per initiative

---

## Key Results

| Metric | Value |
|---|---|
| Total revenue (2020–2023) | €14.8M |
| Total margin | €5.94M (40.2%) |
| Hidden losses identified | **€1.24M** (8.4% of revenue) |
| Loss-making transactions | **29.6%** of all sales |
| Promotional ROI | **0.08%** → promotions ineffective |
| Underserved market identified | Senegal: 6 pharmacies / 18M people |
| Recovery plan delivered | **+€2.45M** over 24 months |

---

## Recommendations Delivered

| # | Action | Financial Impact | Timeline | Priority |
|---|---|---|---|---|
| 1 | Strategic re-pricing (20–30 products) | +€800K | 3 months | Critical |
| 2 | Replace promotions with loyalty program | +€250K/year | Immediate | Critical |
| 3 | Senegal market expansion (pilot + scale) | +€117K | 24 months | Medium |
| 4 | Catalog optimization (focus on Stars >50% margin) | +2–3pts margin | 6 months | Medium |
| 5 | Data-driven operating model | Efficiency gains | 12 months | Foundation |

**Total estimated impact: +€2.45M margin over 24 months**

---

## Dashboard — 5 Pages

### Page 1 — Executive Summary
![Synthèse Exécutive](screenshots/page1_synthese.png)
Global KPIs · Revenue & margin trend · Top countries · Loss overview

### Page 2 — Product Performance
![Performances Produits](screenshots/page2_produits.png)
BCG opportunity matrix (Volume vs. Profitability) · Top/bottom performers · Product segmentation

### Page 3 — Issues & Loss Analysis
![Problématiques](screenshots/page3_problematiques.png)
Loss-making transactions · Promotional ROI analysis · Recoverable margin potential

### Page 4 — Geospatial View
![Cartographie](screenshots/page4_cartographie.png)
Azure Maps · Performance by country and city · Pharmacy profile segmentation

### Page 5 — Trends & Action Plan
![Tendances & Recommandations](screenshots/page5_recommandations.png)
Catalog evolution · 150 discontinuations vs 9 launches in 2023 · Prioritized roadmap

---

## Video Walkthrough

[![Watch on YouTube](https://img.shields.io/badge/YouTube-Watch%20Walkthrough-red?logo=youtube)](https://youtu.be/5JlyY4X0Z8w?si=G2geY1MEbTizo5Hm)

20-minute walkthrough covering: business context · methodology · dashboard pages · key insights · recommendations.

---

## Technical Stack

**BI & Modeling**
- Power BI Desktop + Power BI Service
- DAX — 30 calculated measures (time intelligence, complex filters, dynamic KPIs)
- Power Query / M Language — data transformation pipeline
- Star Schema — FaitVentes · DimProduit · DimPharmacie · DimDate

**Visualizations**
- BCG Scatter Matrix (Volume vs. Profitability)
- Azure Maps (geospatial distribution)
- KPI Cards · Gauges · Conditional tables · Hierarchical matrices
- Line charts · Donut charts · Dynamic drill-throughs

**Dataset**
- 50,000 transactions · 150 products · 80 pharmacies · 4-year calendar (2020–2023)
- Synthetic data generated for the DaCoT Challenge 2026

---

## Documentation

| Document | Description |
|---|---|
| [INSIGHTS.md](INSIGHTS.md) | Deep-dive business analysis & methodology |
| [DAX_MEASURES.md](DAX_MEASURES.md) | Complete code for all 30 DAX measures |
| [METHODOLOGY.md](METHODOLOGY.md) | Data architecture, design decisions, best practices |

---

## Repository Structure

```
dacot-challenge-uemoa/
├── README.md
├── INSIGHTS.md
├── DAX_MEASURES.md
├── METHODOLOGY.md
├── data/
│   ├── FaitVentes.csv
│   ├── DimProduit.csv
│   ├── DimPharmacie.csv
│   └── DimDate.csv
├── screenshots/
│   ├── page1_synthese.png
│   ├── page2_produits.png
│   ├── page3_problematiques.png
│   ├── page4_cartographie.png
│   └── page5_recommandations.png
└── pbix/
    └── Challenge_Dacot.pbix
```

---

## Context

**DaCoT Challenge 2026** — organized by Data Community Togo.  
Individual project completed as part of the challenge.  
All data is synthetic and generated specifically for this challenge.

---

## Author

**Boubacar Nikiema** — Data Analyst & BI Consultant

Specialized in financial dashboards, sales & supply chain analytics, and ETL pipelines
using Power BI, SQL, Python and Excel. Based in Morocco, working with clients across
Africa and French-speaking Europe.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-boubacar--nikiema-blue?logo=linkedin)](https://linkedin.com/in/boubacar-nikiema)
[![YouTube](https://img.shields.io/badge/YouTube-BoubacarDataAnalyst-red?logo=youtube)](https://youtube.com/@BoubacarDataAnalyst)
[![Email](https://img.shields.io/badge/Email-nikiemaboubacar%40gmail.com-gray?logo=gmail)](mailto:nikiemaboubacar@gmail.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-data.ngroupmediadigital.com-green)](https://data.ngroupmediadigital.com)

---

*Data: Synthetic, generated for DaCoT Challenge 2026 · Code: MIT License · Dashboard: Open source with attribution*
