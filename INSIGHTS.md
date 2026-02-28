# 💡 Business Insights - DaCoT Challenge 2026

Ce document détaille les 5 insights majeurs identifiés dans l'analyse du réseau pharmaceutique UEMOA et les recommandations actionnables associées.

---

## 📋 Table des matières

1. [Insight 1: Pricing défaillant - €800K récupérables](#insight-1-pricing-défaillant)
2. [Insight 2: Promotions inefficaces - ROI ≈ 0](#insight-2-promotions-inefficaces)
3. [Insight 3: Sénégal sous-exploité - €700K potentiel](#insight-3-sénégal-sous-exploité)
4. [Insight 4: Catalogue déséquilibré](#insight-4-catalogue-déséquilibré)
5. [Insight 5: Besoin de maturité analytics](#insight-5-besoin-de-maturité-analytics)

---

## Insight 1: Pricing défaillant

### 🔍 Constat

**€1,24M de pertes sur 4 ans**, soit **8,4% du CA total**.

**29,6% des transactions** sont réalisées à perte (14 800 ventes sur 50 000).

L'analyse du TOP 10 produits déficitaires révèle que **10 produits concentrent €400K de pertes**.

| Produit | Catégorie | CA Total | Marge Totale | Taux Marge | Nb Ventes Perte |
|---------|-----------|----------|--------------|------------|-----------------|
| Produit Générique 105 | Prescription | €34 170 | **-€54 750** | -160,2% | 370 |
| Produit Générique 136 | Bien-être | €28 495 | **-€78 091** | -274,1% | 361 |
| Produit Générique 46 | OTC | €60 897 | **-€42 697** | -70,1% | 354 |
| Produit Générique 132 | OTC | €18 579 | **-€59 084** | -318,0% | 348 |
| Produit Générique 49 | Soins Personnels | €18 215 | **-€70 229** | -385,6% | 341 |
| Produit Générique 60 | Soins Personnels | €24 010 | **-€71 520** | -297,9% | 338 |
| Produit Générique 94 | Bien-être | €47 448 | **-€41 184** | -86,8% | 334 |
| Produit Générique 89 | Bien-être | €19 316 | **-€44 784** | -231,9% | 330 |
| Produit Générique 107 | Prescription | €40 585 | **-€43 175** | -106,4% | 329 |
| Produit Générique 147 | OTC | €24 213 | **-€68 803** | -284,2% | 320 |

**Total TOP 10:** €574K de pertes sur 7 produits

Par extrapolation, **20-30 produits déficitaires génèrent 65% des pertes totales**, soit **€806K**.

### 🎯 Root Cause Analysis

**Pourquoi ces produits perdent de l'argent?**

1. **Pricing non aligné avec les coûts réels**
   - Prix de vente < Coût d'achat + frais
   - Absence de révision systématique des prix
   - Coûts d'approvisionnement qui ont augmenté sans ajustement

2. **Stratégie "prix bas" généralisée**
   - Positionnement "low cost" non ciblé
   - Tous les produits traités de la même manière
   - Pas de segmentation stratégique

3. **Faible rotation des produits déficitaires**
   - Ces produits représentent seulement **7% du volume total**
   - Impact limité sur le trafic client
   - Risque faible de perte de CA en cas de re-pricing

### ✅ Recommandation: Stratégie pricing différenciée

**Segmentation des 68 produits actifs en 3 tiers:**

**Tier 1: Produits d'Appel (~15-20 produits)**
- Objectif: Générer du trafic
- Pricing: Coût + 15-20% (marge faible acceptable)
- Exemples: Paracétamol, produits de base très demandés
- Justification: Attirent les clients qui achètent ensuite d'autres produits

**Tier 2: Produits Standards (~40-50 produits)**
- Objectif: Volume et rentabilité équilibrée
- Pricing: Coût + 40% (marge cible actuelle)
- Exemples: Génériques courants, produits de rotation moyenne
- Justification: Cœur du business, marge saine

**Tier 3: Produits Premium (~15-20 produits)**
- Objectif: Maximiser la marge unitaire
- Pricing: Coût + 60% ou plus (value-based pricing)
- Exemples: Équipement médical, produits spécialisés
- Justification: Clients moins sensibles au prix, forte valeur perçue

**Méthodologie d'implémentation:**

**Phase 1: Analyse (Semaines 1-2)**
- Calculer l'élasticité-prix sur les données historiques
- Identifier les produits substituables (risque de cannibalisation)
- Benchmarker 3-5 concurrents majeurs UEMOA
- Segmenter les 68 produits actifs dans les 3 tiers

**Phase 2: Test A/B (Semaines 3-6)**
- Sélectionner 3 pharmacies pilotes (Niger, Burkina, Sénégal)
- Appliquer nouveaux prix sur 20-30 produits déficitaires
- Mesurer quotidiennement: volume, CA, marge, trafic client
- Objectif: Confirmer que perte de volume < 10%

**Phase 3: Rollout (Semaines 7-12)**
- Si KPIs atteints → Déploiement sur les 80 pharmacies
- Formation des managers (2 jours): justification commerciale des prix
- Mise à jour du système de pricing automatique
- Communication clients: "Ajustement qualité-prix"

**Gestion des risques:**

| Risque | Probabilité | Impact | Mitigation |
|--------|-------------|--------|------------|
| Perte de clients | Moyenne | Moyen | Programme fidélité compensatoire |
| Réaction concurrents | Faible | Moyen | Différenciation service + conseil |
| Refus pharmaciens | Faible | Élevé | Incentives sur marge, pas sur volume |
| Erreur de calcul | Faible | Critique | Double validation CFO + Commercial |

### 📊 Impact chiffré

**Scénarios:**

| Scénario | Perte Volume | Marge Récupérée | Probabilité |
|----------|--------------|-----------------|-------------|
| Pessimiste | -20% | +€500K | 15% |
| **Réaliste** | **-10%** | **+€800K** | **70%** |
| Optimiste | -5% | +€1,1M | 15% |

**ROI:**
- Coût du projet: ~€65K (temps analyste + formation + système)
- Gain attendu: €800K (scénario réaliste)
- **ROI: 1230%**
- **Payback: 1 mois**

**Impact sur KPIs globaux:**
- Taux de marge: 40,2% → **44,5%** (+4,3 points)
- % Ventes à perte: 29,6% → **<15%** (-14,6 points)
- Marge totale annuelle: €1,48M → **€1,88M** (+27%)

---

## Insight 2: Promotions inefficaces

### 🔍 Constat

**Analyse comparative avec/sans promotion:**

| Métrique | Avec Promo | Sans Promo | Différence |
|----------|------------|------------|------------|
| CA Total | €7,37M | €7,41M | -€40K (-0,5%) |
| Marge Totale | | | |
| Taux Marge | 40,25% | 40,18% | **+0,08%** |

**Conclusion: ROI promotionnel ≈ 0**

On dépense de l'énergie commerciale et du budget promo pour un gain de marge de **0,08%**, statistiquement nul.

### 🎯 Root Cause Analysis

**Pourquoi les promos ne marchent pas?**

1. **Promotions généralisées non ciblées**
   - Promos sur tout le catalogue, pas de focus
   - Tous les clients bénéficient, même les fidèles qui achèteraient de toute façon
   - Dilution de l'impact

2. **Pas de segmentation client**
   - Traitement identique pour client 1ère visite vs client 10e achat
   - Pas de distinction entre clients à fort/faible potentiel
   - Gaspillage de budget promo sur clients perdus

3. **Effet de cannibalisation**
   - Clients réguliers attendent les promos au lieu d'acheter plein prix
   - Formation d'un comportement d'achat opportuniste
   - Érosion de la marge sur clients déjà acquis

### ✅ Recommandation: Programme Loyalty ciblé

**Arrêt des promotions généralisées**

**Remplacer par segmentation RFM (Recency, Frequency, Monetary):**

**Segment 1: Champions (15% clients, 45% CA)**
- Recency: <30 jours
- Frequency: >10 achats/an
- Monetary: >€5K/an
- **Action:** PAS de promo (déjà fidèles)
- **Offre:** Services VIP (livraison prioritaire, conseil pharmacien dédié)

**Segment 2: Potentiels (25% clients, 30% CA)**
- Recency: <60 jours
- Frequency: 5-10 achats/an
- Monetary: €2-5K/an
- **Action:** Promos CIBLÉES sur produits premium uniquement
- **Objectif:** Upgrade vers Champions (augmenter panier moyen)

**Segment 3: At-Risk (20% clients, 15% CA)**
- Recency: >90 jours
- Frequency: <5 achats/an
- Monetary: <€2K/an
- **Action:** Campagne win-back agressive (promo forte)
- **Deadline:** Si pas de réponse en 60j → laisser partir

**Segment 4: Perdus (40% clients, 10% CA)**
- Recency: >180 jours
- **Action:** AUCUNE promo (coût > bénéfice potentiel)
- **Réallocation:** Budget vers Potentiels

**Programme Loyalty:**

```
SYSTÈME À POINTS
1€ dépensé = 1 point
100 points = €5 de remise (équivalent 5%)

TIERS:
┌─────────────────────────────────────┐
│ 🥉 BRONZE (0-500 pts)               │
│    Remise: 3%                       │
│    Offre: Newsletter mensuelle      │
├─────────────────────────────────────┤
│ 🥈 SILVER (501-2000 pts)            │
│    Remise: 5%                       │
│    Offre: Livraison gratuite        │
│    Conseil: SMS rappel renouvellement│
├─────────────────────────────────────┤
│ 🥇 GOLD (2001+ pts)                 │
│    Remise: 7%                       │
│    Offre: Conseils santé personnalisés│
│    Priorité: Nouveaux produits      │
└─────────────────────────────────────┘
```

**Avantages vs Promos classiques:**

| Critère | Promos Actuelles | Loyalty Program |
|---------|------------------|-----------------|
| Coût | €600K/an (estimé) | €350K/an |
| Ciblage | Aucun | RFM précis |
| Fidélisation | Faible | Forte (gamification) |
| Data collection | Non | Oui (profil client) |
| ROI | 0,08% | 15-20% estimé |

### 📊 Impact chiffré

**Économies directes:**
- Coût promos actuelles: ~€600K/an
- Coût loyalty program: €350K/an (système + remises)
- **Économie nette: €250K/an**

**Gains indirects:**
- Hausse rétention clients: +15% (benchmark industrie)
- Impact CA: +€1,2M sur 2 ans
- Lifetime Value clients: +25%

**Total impact sur 24 mois: +€1,45M**

---

## Insight 3: Sénégal sous-exploité

### 🔍 Constat

**Analyse de densité du réseau:**

| Pays | Population | Nb Pharmacies | Habitants/Pharmacie | Index vs Moyenne |
|------|------------|---------------|---------------------|------------------|
| **Sénégal** | 18M | 6 | **3 000 000** | **166%** ⚠️ |
| Guinée-Bissau | 2,1M | 7 | 300 000 | 17% |
| Niger | 26M | 15 | 1 733 333 | 96% |
| Burkina Faso | 23M | 12 | 1 916 667 | 106% |
| Mali | 22M | 11 | 2 000 000 | 111% |
| Togo | 9M | 10 | 900 000 | 50% |
| Côte d'Ivoire | 28M | 10 | 2 800 000 | 155% |
| Bénin | 13M | 9 | 1 444 444 | 80% |
| **Moyenne UEMOA** | - | - | **1 806 944** | **100%** |

**Constat:** Le Sénégal a **66% moins de pharmacies** que la moyenne UEMOA rapporté à sa population.

**Performance actuelle Sénégal:**
- CA Total: **€1,062M** (4 ans), soit **€265K/an**
- CA/Pharmacie: **€177K/an**
- Marge: **39,1%**
- Nb Ventes à perte: 1 124 (faible)

**Conclusion:** Le marché sénégalais performe correctement malgré une couverture limitée. Fort potentiel de scaling.

### 🎯 Opportunité d'expansion

**Scénario cible:**

Si on ramène le Sénégal à la densité moyenne UEMOA:
- Habitants/pharmacie cible: 1,8M (moyenne)
- Nb pharmacies nécessaires: 18M / 1,8M = **10 pharmacies**
- Gap actuel: 10 - 6 = **4 nouvelles pharmacies**

**Potentiel CA additionnel:**
- CA moyen actuel/pharmacie: €177K (4 ans), soit **€44K/an**
- 4 nouvelles pharmacies × €44K/an = **€176K/an**

**Projection sur 24 mois (avec montée en charge):**
- Année 1 (70% capacité): €176K × 70% = €123K
- Année 2 (100% capacité): €176K × 100% = €176K
- **CA cumulé 24 mois: €299K**
- **Marge nette (39,1%): €117K**

**ROI:**
- Investissement 4 dépôts: €640K (estimé)
- Marge nette 24 mois: €117K
- **ROI 24 mois: 18%** (faible)
- Break-even: ~10 ans

**Conclusion:** L'expansion Sénégal présente un ROI modeste. Une analyse approfondie du potentiel de croissance du marché local est nécessaire avant investissement.

### ✅ Recommandation: Expansion pilotée

**Scoring des opportunités géographiques:**

Méthodologie de priorisation basée sur 5 critères pondérés:

| Critère | Poids | Dakar | Thiès | Saint-Louis |
|---------|-------|-------|-------|-------------|
| Démographie | 30% | 3,7M | 970K | 1,1M |
| Économie (PIB/hab) | 25% | Élevé | Moyen | Moyen |
| Accès santé actuel | 20% | Faible | Très faible | Faible |
| Concurrence | 15% | Fort | Modéré | Faible |
| Infrastructure | 10% | Excellent | Bon | Moyen |
| **SCORE /100** | - | **87** | **76** | **68** |

**Roadmap d'expansion:**

**Q2 2024: Étude de marché approfondie**
- Benchmark 15 pharmacies concurrentes Dakar (prix, assortiment, services)
- Enquête 500 consommateurs: habitudes achat, sensibilité prix, besoins non couverts
- Analyse flux logistiques: coût transport, délais approvisionnement
- Identification zones commerciales stratégiques (bureaux, résidentiel, hôpitaux)
- Coût: €15K
- Livrable: Business plan détaillé 3 zones Dakar

**Q3 2024: Pilote Dakar Zone 1 (Plateau)**
- Profil: Pharmacie Moyenne, Type Urbain (segment le plus performant)
- Localisation: Quartier Plateau (forte densité bureaux, pouvoir d'achat élevé)
- Catalogue: 80 produits "Stars" (marge >50%)
- Investissement: €180K (local, stock, système, formation)
- Objectif 6 mois: €90K CA, 45% marge
- KPIs suivi: CA mensuel, panier moyen, taux de marge, NPS clients

**Q4 2024: Décision Scale**

Si KPIs atteints (CA >€80K, marge >42%):
- ✅ Ouverture 2e dépôt Dakar (Zone résidentielle - Almadies)
- ✅ Planification Thiès pour Q1 2025
- ✅ Planification Saint-Louis pour Q2 2025

Si KPIs non atteints:
- ⏸️ Pause expansion
- 🔍 Analyse root cause (prix? assortiment? emplacement? service?)
- 🔧 Ajustement stratégie sur pilote existant
- 📊 Re-test 3 mois avant nouvelle décision

**Q1-Q2 2025: Déploiement si pilote réussi**
- Thiès (1 dépôt): €140K investissement
- Saint-Louis (1 dépôt): €140K investissement

### 📊 Impact chiffré

**Investissement total (4 dépôts):**
- Dakar 1: €180K
- Dakar 2: €180K
- Thiès: €140K
- Saint-Louis: €140K
- **Total: €640K**

**Projection CA (méthode conservative):**

| Année | Nb Dépôts | CA/Dépôt Moyen | CA Total | Marge (44%) |
|-------|-----------|----------------|----------|-------------|
| 2024 | 1 | €80K | €80K | €35K |
| 2025 | 4 | €130K | €520K | €229K |
| 2026 | 4 | €195K (maturité) | €780K | €343K |

**Marge nette cumulée 24 mois:** €264K (après maturité Dakar)  
**ROI:** 41% sur 2 ans  
**Break-even:** 18-22 mois selon profil dépôt

**Scénario optimiste (+20% CA):** Marge €410K, ROI 64%  
**Scénario pessimiste (-20% CA):** Marge €190K, ROI 30%

---

## Insight 4: Catalogue déséquilibré

### 🔍 Constat

**Évolution du catalogue 2020-2023:**

| Année | Lancements | Arrêts | Net |
|-------|------------|--------|-----|
| 2020 | 40 | 0 | +40 |
| 2021 | 39 | 0 | +39 |
| 2022 | 62 | 0 | +62 |
| 2023 | 9 | 150 | **-141** ⚠️ |

**État actuel:**
- Produits actifs: **68**
- Produits discontinués: **82** (54,7% du catalogue)
- Ratio lancement 2023: **9** (vs 62 en 2022, -85%)

**Problème:** En 2023, rationalisation drastique mais innovation stoppée.

**Risque:** Catalogue qui se vide progressivement, perte de compétitivité.

### 🎯 Analyse par segment (Matrice BCG)

D'après le scatter "Volume vs Rentabilité" (Page 2):

**Distribution visuelle des 68 produits actifs:**

**Stars (Haut-Droite):** ~25-30 produits
- Fort volume (>333 transactions/an)
- Forte marge (>40%)
- **Action:** GARDER absolument, augmenter stock sécurité

**Cash Cows (Bas-Droite):** ~20-25 produits
- Fort volume
- Faible marge (<40%)
- **Action:** Re-pricer +10-15% OU bundling avec Stars

**Niches (Haut-Gauche):** ~10-15 produits
- Faible volume (<333 transactions)
- Forte marge (>40%)
- **Action:** Tester promo 3 mois → Décision keep/kill

**Questions (Bas-Gauche):** ~8-10 produits
- Faible volume
- Faible marge
- **Action:** ARRÊTER pour libérer cash et espace

### ✅ Recommandation: Portfolio dynamique

**Objectif:** Maintenir un catalogue de 70-80 produits actifs avec renouvellement 15-20%/an.

**Actions 2024:**

**1. Élimination sélective**
- Identifier les 8-10 "Questions" les plus faibles
- Analyser stock résiduel: vendre à prix cassé ou détruire
- Timeline: Fin Q1 2024
- Cash libéré: ~€50K (stock)

**2. Optimisation Cash Cows**
- Re-pricing test sur 5 produits pilotes (+10%)
- Bundling stratégique (ex: Paracétamol + Vitamine C)
- Timeline: Q2 2024

**3. Développement Niches**
- Campagne promo ciblée sur 5 produits Niches à potentiel
- Si volume ×2 en 3 mois → Migration Stars
- Si stagnation → Arrêt
- Timeline: Q2-Q3 2024

**4. Innovation ciblée**

**Gap analysis - Catégories sous-représentées:**

| Catégorie | % Catalogue | Marge Moy | Opportunité |
|-----------|-------------|-----------|-------------|
| Équipement Médical | ~15% | 48,7% | ⭐⭐⭐ Forte |
| Prescription | ~20% | 31,0% | Faible |
| OTC | ~25% | 34,2% | Faible |
| Bien-être | ~20% | 45,9% | ⭐⭐ Moyenne |
| Soins Personnels | ~20% | 45,7% | ⭐⭐ Moyenne |

**Nouveaux lancements 2024:**

**Q2 2024:** 5 produits Équipement Médical (diagnostic)
- Thermomètres digitaux haut de gamme
- Tensiomètres connectés
- Oxymètres de pouls
- Glucomètres nouvelle génération
- Stéthoscopes professionnels

**Q3 2024:** 5 produits Bien-être Premium
- Compléments alimentaires bio
- Huiles essentielles thérapeutiques
- Probiotiques avancés
- Vitamines seniors spécialisées
- Soins pédiatriques premium

**Q4 2024:** 5 produits Soins Personnels
- Dermocosmétiques
- Solaires haute protection
- Hygiène intime premium

**Total 2024:** 15 lancements (vs 9 en 2023)

### 📊 Impact chiffré

**Résultat attendu:**

| Métrique | 2023 | 2024 Cible | Évolution |
|----------|------|------------|-----------|
| Produits actifs | 68 | 73 | +7% |
| Lancements | 9 | 15 | +67% |
| Arrêts | 150 | 10 | -93% |
| Net | -141 | +5 | Positif ✓ |
| % Stars | 42,7% | 48% | +5,3pts |
| Marge moyenne | 40,2% | 42-43% | +2pts |

**Impact financier:**
- Amélioration mix produit: +2 points de marge
- Sur CA €3,7M/an: **+€74K marge annuelle**

---

## Insight 5: Besoin de maturité analytics

### 🔍 Constat

**État actuel:** Dashboard rétrospectif excellent.

**Ce qu'on a:**
- ✅ Diagnostic historique (ce qui s'est passé)
- ✅ Analyse causale (pourquoi ça s'est passé)
- ✅ Segmentation produits/clients/géo

**Ce qui manque:**
- ❌ Prédiction (ce qui va se passer)
- ❌ Prescription automatisée (que doit-on faire)
- ❌ Alertes temps réel
- ❌ Tracking implémentation recommandations

### 🎯 Échelle de maturité analytics

```
NIVEAU 1: DESCRIPTIF ✅ [ACTUEL]
"Qu'est-ce qui s'est passé?"
→ Dashboard Power BI
→ KPIs historiques
→ Rapports statiques

NIVEAU 2: DIAGNOSTIC ⏳ [Q2 2024]
"Pourquoi ça s'est passé?"
→ Root cause analysis automatisée
→ Détection anomalies
→ Alertes sur seuils critiques

NIVEAU 3: PRÉDICTIF 🔮 [Q3 2024]
"Qu'est-ce qui va se passer?"
→ Forecast CA/Marge par produit
→ Prédiction arrêt produit (ML)
→ Scoring client (churn risk)

NIVEAU 4: PRESCRIPTIF 🎯 [Q4 2024]
"Que doit-on faire?"
→ Recommandation pricing automatique
→ Optimisation stock par pharmacie
→ Suggestion produits à lancer/arrêter
```

### ✅ Recommandation: Roadmap Data-Driven

**Quick Wins (30-60 jours):**

**1. Alertes automatisées**
```
Email auto si:
• Produit passe en marge négative
• Pharmacie baisse >15% vs mois précédent
• Stock <7 jours sur produit Star
• Ventes à perte >35% dans une pharmacie
```

**2. Dashboard Managers Pharmacies**
```
Vue personnalisée par dépôt:
• Performance vs moyenne réseau
• Classement /80
• Top 5 actions prioritaires data-driven
• Alertes spécifiques
```

**3. Scoring Performance Automatique**
```
Note /100 pour chaque pharmacie:
• CA (30%)
• Marge (30%)
• Mix produit Stars (20%)
• % Ventes à perte (20%)

Incentive managers sur score (bonus si >75)
```

**Moyen terme (Q2-Q3 2024):**

**4. Modèle prédictif CA**
```python
# Forecast CA par produit
- Prophet (Facebook) pour série temporelle
- Features: tendance, saisonnalité, promotions, jours fériés
- Horizon: 3 mois
- Précision cible: ±10%
```

**5. Analyse sentiment client**
```
Si données avis disponibles:
- NLP sur commentaires pharmacies
- Identification problèmes récurrents
- Priorisation améliorations service
```

**Long terme (Q4 2024):**

**6. Optimisation pricing ML**
```
Modèle pour recommander prix optimal:
- Input: coût, concurrent, élasticité, stock
- Output: prix maximisant marge × volume
- Test sur 10 produits pilotes
```

**7. Optimisation stock**
```
Forecast demande + calcul stock optimal:
- Minimiser coût stockage
- Éviter ruptures produits Stars
- Réduire surstocks Questions
```

### 📊 Impact chiffré

**Gains d'efficacité:**

| Initiative | Temps gagné | Coût évité | Valeur |
|------------|-------------|------------|--------|
| Alertes auto | 10h/mois analyste | - | €6K/an |
| Dashboard managers | 20h/mois direction | - | €12K/an |
| Forecast précis | Réduction ruptures | €30K/an | €30K/an |
| Optimisation stock | -15% stock moyen | €45K/an | €45K/an |

**Total gains estimés: €93K/an**

**Investissement:**
- Développement BI: €40K
- Formation équipes: €10K
- Maintenance annuelle: €15K
- **Total: €65K**

**ROI Année 1: 143%**

---

## 🎯 Synthèse des 5 Insights

| # | Insight | Impact | Délai | Priorité |
|---|---------|--------|-------|----------|
| 1 | Pricing défaillant | **€800K** | 3 mois | 🔴 Critique |
| 2 | Promotions inefficaces | **€250K/an** | Immédiat | 🔴 Critique |
| 3 | Sénégal sous-exploité | **€117K** (24m) | 24 mois | 🟢 Moyenne |
| 4 | Catalogue déséquilibré | **€74K/an** | 6 mois | 🟢 Moyenne |
| 5 | Maturité analytics | **€93K/an** | 12 mois | 🟢 Fondation |

**Impact total estimé: €2,45M sur 24 mois**

**Breakdown:**
- Pricing: €800K (récupération immédiate)
- Loyalty: €500K (€250K × 2 ans)
- Sénégal: €117K (expansion pilotée)
- Catalogue: €148K (€74K × 2 ans)
- Analytics: €186K (€93K × 2 ans)
- Rétention clients (effet loyalty): €700K (15% hausse rétention)

---

## 📚 Méthodologie d'analyse

**Outils utilisés:**
- Power BI Desktop pour visualisation
- DAX pour calculs métrique business
- Excel pour analyse exploratoire
- Matrice BCG pour segmentation produits
- RFM (implicite) pour segmentation clients
- Scoring multicritère pour expansion géo

**Sources de données:**
- 50 000 transactions (FaitVentes)
- 150 produits (DimProduit)
- 80 pharmacies (DimPharmacie)
- Calendrier 4 ans (DimDate)

**Hypothèses clés:**
- Élasticité-prix: -0,8 à -1,2 selon segment
- Taux de churn sans action: 15%/an
- Maturation nouveau dépôt: 18 mois
- Croissance marché UEMOA: +4%/an

---

**Dernière mise à jour:** 28 février 2026  
**Auteur:** Boubacar Nikiema, Data Analyst
