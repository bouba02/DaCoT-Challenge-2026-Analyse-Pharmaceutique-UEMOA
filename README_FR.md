# DaCoT Challenge 2026 — Analyse Pharmaceutique UEMOA

> **€1,24M de pertes cachées identifiées. Plan de récupération de €2,45M livré.**  
> 50 000 transactions · 80 pharmacies · 8 pays UEMOA · Dashboard Power BI 5 pages

🇬🇧 [English version available here](README.md)

![Dashboard Overview](screenshots/page1_synthese.png)

---

## Problème Business

Un réseau de distribution pharmaceutique opérant en Afrique de l'Ouest enregistrait
deux années consécutives de déclin du chiffre d'affaires (-1,0% en 2023), sans
diagnostic clair disponible pour la direction.

Après analyse : **29,6% de toutes les transactions étaient réalisées à perte** —
soit €1,24M de destruction de valeur, totalement invisible sans infrastructure
de données adaptée.

**Mission :** Diagnostiquer les causes profondes sur 50 000 transactions, quantifier
l'impact financier et livrer un plan d'action priorisé et chiffré.

---

## Démarche

1. **Audit des données** — Structuration de 4 tables brutes en modèle Star Schema (FaitVentes, DimProduit, DimPharmacie, DimDate)
2. **Analyse exploratoire** — Identification des transactions déficitaires par produit, pharmacie, pays et type de promotion
3. **Modélisation business** — Construction de 30 mesures DAX couvrant le CA, les marges, le ROI promotionnel et la performance géographique
4. **Cartographie** — Intégration Azure Maps pour visualiser les performances sur les 8 pays UEMOA
5. **Recommandations** — Plan d'action priorisé avec impact financier chiffré par initiative

---

## Résultats Clés

| Indicateur | Valeur |
|---|---|
| CA total (2020–2023) | €14,8M |
| Marge totale | €5,94M (40,2%) |
| Pertes cachées identifiées | **€1,24M** (8,4% du CA) |
| Transactions déficitaires | **29,6%** des ventes |
| ROI promotionnel constaté | **0,08%** → promotions inefficaces |
| Marché sous-exploité identifié | Sénégal : 6 pharmacies / 18M habitants |
| Plan de récupération livré | **+€2,45M** sur 24 mois |

---

## Recommandations Livrées

| # | Action | Impact Financier | Délai | Priorité |
|---|---|---|---|---|
| 1 | Re-pricing stratégique (20–30 produits) | +€800K | 3 mois | Critique |
| 2 | Remplacement des promos par un programme fidélité | +€250K/an | Immédiat | Critique |
| 3 | Expansion Sénégal (pilote + déploiement) | +€117K | 24 mois | Moyenne |
| 4 | Optimisation catalogue (focus produits Stars >50% marge) | +2–3pts marge | 6 mois | Moyenne |
| 5 | Passage à un pilotage data-driven | Gains d'efficacité | 12 mois | Fondation |

**Impact total estimé : +€2,45M de marge sur 24 mois**

---

## Dashboard — 5 Pages

### Page 1 — Synthèse Exécutive
![Synthèse Exécutive](screenshots/page1_synthese.png)
KPIs globaux · Évolution CA & marge · Top pays · Aperçu des pertes

### Page 2 — Performances Produits
![Performances Produits](screenshots/page2_produits.png)
Matrice opportunités Volume vs Rentabilité · Top/bottom performers · Segmentation produits

### Page 3 — Problématiques & Analyse des Pertes
![Problématiques](screenshots/page3_problematiques.png)
Transactions déficitaires · Analyse ROI promotionnel · Marge récupérable

### Page 4 — Cartographie Géographique
![Cartographie](screenshots/page4_cartographie.png)
Azure Maps · Performance par pays et ville · Segmentation par profil de pharmacie

### Page 5 — Tendances & Plan d'Action
![Tendances & Recommandations](screenshots/page5_recommandations.png)
Évolution du catalogue · 150 arrêts vs 9 lancements en 2023 · Feuille de route priorisée

---

## Vidéo de Présentation

[![Voir sur YouTube](https://img.shields.io/badge/YouTube-Voir%20la%20vidéo%20complète-red?logo=youtube)](https://youtu.be/5JlyY4X0Z8w?si=G2geY1MEbTizo5Hm)

Présentation complète de 20 minutes : contexte business · méthodologie · pages du dashboard · insights clés · recommandations.

---

## Stack Technique

**Business Intelligence & Modélisation**
- Power BI Desktop + Power BI Service
- DAX — 30 mesures calculées (time intelligence, filtres complexes, KPIs dynamiques)
- Power Query / Langage M — pipeline de transformation des données
- Modèle en étoile — FaitVentes · DimProduit · DimPharmacie · DimDate

**Visualisations**
- Matrice BCG (Volume vs Rentabilité)
- Azure Maps (distribution géographique)
- Cartes KPI · Jauges · Tables conditionnelles · Matrices hiérarchiques
- Graphiques en courbes · Donuts · Drill-throughs dynamiques

**Données**
- 50 000 transactions · 150 produits · 80 pharmacies · Calendrier 2020–2023
- Données synthétiques générées pour le DaCoT Challenge 2026

---

## Documentation

| Document | Contenu |
|---|---|
| [INSIGHTS.md](INSIGHTS.md) | Analyse business approfondie & méthodologie |
| [DAX_MEASURES.md](DAX_MEASURES.md) | Code complet des 30 mesures DAX |
| [METHODOLOGY.md](METHODOLOGY.md) | Architecture des données, choix de conception, bonnes pratiques |

---

## Structure du Repository

```
dacot-challenge-uemoa/
├── README.md                    # Version anglaise
├── README_FR.md                 # Ce fichier (version française)
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

## Contexte

**DaCoT Challenge 2026** — organisé par la Data Community Togo.  
Projet individuel réalisé dans le cadre du challenge.  
Toutes les données sont synthétiques et générées spécifiquement pour ce challenge.

---

## Compétences Démontrées

**Business Intelligence**
- Diagnostic business et analyse exploratoire
- Création de dashboards décisionnels multi-pages
- Data storytelling et recommandations stratégiques chiffrées
- Formation et documentation pour utilisateurs finaux

**Techniques**
- Modélisation dimensionnelle (Star Schema)
- DAX avancé (time intelligence, filtres contextuels, mesures dynamiques)
- Visualisation de données (choix pertinents selon le message)
- Cartographie géospatiale (Azure Maps)

**Acumen Business**
- Analyse de rentabilité produit et pricing
- Segmentation et scoring géographique
- Optimisation de catalogue
- Quantification d'impact financier

---

## Auteur

**Boubacar Nikiema** — Data Analyst & Consultant BI

Spécialisé en dashboards financiers, analytics Sales & Supply Chain et pipelines ETL
avec Power BI, SQL, Python et Excel. Basé au Maroc, j'interviens auprès d'entreprises
en Afrique et en Europe francophone.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-boubacar--nikiema-blue?logo=linkedin)](https://linkedin.com/in/boubacar-nikiema)
[![YouTube](https://img.shields.io/badge/YouTube-BoubacarDataAnalyst-red?logo=youtube)](https://youtube.com/@BoubacarDataAnalyst)
[![Email](https://img.shields.io/badge/Email-nikiemaboubacar%40gmail.com-gray?logo=gmail)](mailto:nikiemaboubacar@gmail.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-data.ngroupmediadigital.com-green)](https://data.ngroupmediadigital.com)

---

*Données : Synthétiques, générées pour le DaCoT Challenge 2026 · Code : Licence MIT · Dashboard : Open source avec attribution*
