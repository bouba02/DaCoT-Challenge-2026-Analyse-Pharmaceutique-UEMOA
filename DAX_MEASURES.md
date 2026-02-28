# 📐 Mesures DAX - DaCoT Challenge 2026

Documentation complète des **30 mesures DAX** utilisées dans le dashboard d'analyse pharmaceutique UEMOA.

---

## 📋 Table des matières

1. [Mesures Core Business](#1-mesures-core-business)
2. [Mesures Analytiques Pertes](#2-mesures-analytiques-pertes)
3. [Mesures Promotions](#3-mesures-promotions)
4. [Mesures Catalogue](#4-mesures-catalogue)
5. [Mesures Time Intelligence](#5-mesures-time-intelligence)
6. [Mesures Dérivées](#6-mesures-dérivées)

---

## 1. Mesures Core Business

### CA Total
```dax
CA Total = 
SUM(FaitVentes[PrixStandardEUR]) * SUM(FaitVentes[QuantiteVendue])
```
**Description:** Chiffre d'affaires total (Prix × Quantité)  
**Résultat:** €14,8M (2020-2023)  
**Usage:** KPI principal sur toutes les pages

---

### Marge Totale
```dax
Marge Totale = 
SUM(FaitVentes[MargeEUR])
```
**Description:** Somme des marges en euros  
**Résultat:** €5,94M  
**Usage:** KPI rentabilité

---

### Taux de Marge %
```dax
Taux de Marge % = 
DIVIDE([Marge Totale], [CA Total], 0) * 100
```
**Description:** Pourcentage de marge (Marge/CA)  
**Résultat:** 40,2%  
**Usage:** KPI rentabilité relative

**💡 Note:** `DIVIDE(..., 0)` évite les erreurs #DIV/0!

---

### Qté Vendues
```dax
Qté Vendues = 
SUM(FaitVentes[QuantiteVendue])
```
**Description:** Nombre total d'unités vendues  
**Résultat:** 524 499 unités  
**Usage:** Analyse volume

---

### Nb transactions
```dax
Nb transactions = 
COUNTROWS(FaitVentes)
```
**Description:** Nombre total de transactions  
**Résultat:** 50 000  
**Usage:** Matrice BCG (axe X)

---

### Ca Moyen
```dax
Ca Moyen = 
AVERAGE(FaitVentes[PrixStandardEUR])
```
**Description:** Prix moyen par transaction  
**Usage:** Analyse pricing

---

### CA Moyen Pharmacie
```dax
CA Moyen Pharmacie = 
DIVIDE([CA Total], [Nb Pharmacies], 0)
```
**Description:** CA moyen par point de vente  
**Résultat:** €185K (4 ans) = €46K/an  
**Usage:** Page 4 - Cartographie

---

## 2. Mesures Analytiques Pertes

### % Ventes à Perte
```dax
% Ventes à Perte = 
VAR VentesAPerte = 
    CALCULATE(
        COUNTROWS(FaitVentes),
        FaitVentes[MargeEUR] < 0
    )
VAR TotalVentes = COUNTROWS(FaitVentes)
RETURN
DIVIDE(VentesAPerte, TotalVentes, 0) * 100
```
**Description:** Pourcentage de transactions à marge négative  
**Résultat:** 29,6%  
**Usage:** Page 3 - Alerte centrale

**📝 Explication:**
- `VAR VentesAPerte` filtre transactions avec marge < 0
- `VAR TotalVentes` compte toutes les transactions
- `RETURN` calcule le ratio

---

### Nb Ventes à Perte
```dax
Nb Ventes à Perte = 
CALCULATE(
    COUNTROWS(FaitVentes),
    FaitVentes[MargeEUR] < 0
)
```
**Description:** Nombre de transactions déficitaires  
**Résultat:** 14 800  
**Usage:** Page 2 - KPI alerte

---

### Montant Pertes
```dax
Montant Pertes = 
VAR PertesCumulees = 
    CALCULATE(
        SUM(FaitVentes[MargeEUR]),
        FaitVentes[MargeEUR] < 0
    )
RETURN
ABS(PertesCumulees)
```
**Description:** Total des pertes (valeur absolue)  
**Résultat:** €1,24M  
**Usage:** Page 3 - Card "Pertes cumulées"

**💡 Note:** `ABS()` convertit -€1,24M en +€1,24M pour affichage

---

### Perte Cumulée
```dax
Perte Cumulée = 
CALCULATE(
    SUM(FaitVentes[MargeEUR]),
    FaitVentes[MargeEUR] < 0
)
```
**Description:** Somme des marges négatives (garde signe -)  
**Résultat:** -€1,24M  
**Usage:** Calculs intermédiaires

---

### % CA Perdu
```dax
% CA Perdu = 
DIVIDE([Montant Pertes], [CA Total], 0) * 100
```
**Description:** Pertes en % du CA  
**Résultat:** 8,4%  
**Usage:** Page 3 - Card contexte

---

### % Marge Potentielle
```dax
% Marge Potentielle = 
VAR MargeSansPertes = [Marge Totale] - [Perte Cumulée]
RETURN
DIVIDE(MargeSansPertes, [CA Total], 0) * 100
```
**Description:** Marge théorique si zéro perte  
**Résultat:** 48,6%  
**Usage:** Page 3 - Gauge potentiel

**📝 Calcul:**
- Marge actuelle: €5,94M (40,2%)
- Sans pertes: €5,94M - (-€1,24M) = €7,18M (48,6%)
- **Gain potentiel: +8,4 points**

---

## 3. Mesures Promotions

### CA Promo
```dax
CA Promo = 
CALCULATE(
    [CA Total],
    FaitVentes[Promotion] = "Oui"
)
```
**Description:** CA avec promotion  
**Résultat:** €7,37M  
**Usage:** Page 3 - Comparaison promo

---

### CA Non Promo
```dax
CA Non Promo = 
CALCULATE(
    [CA Total],
    FaitVentes[Promotion] = "Non"
)
```
**Description:** CA sans promotion  
**Résultat:** €7,41M  
**Usage:** Page 3 - Comparaison promo

---

### Marge % Promo
```dax
Marge % Promo = 
CALCULATE(
    [Taux de Marge %],
    FaitVentes[Promotion] = "Oui"
)
```
**Description:** Taux marge sur ventes promo  
**Résultat:** 40,25%  
**Usage:** Page 3 - Analyse ROI

---

### Marge % Non Promo
```dax
Marge % Non Promo = 
CALCULATE(
    [Taux de Marge %],
    FaitVentes[Promotion] = "Non"
)
```
**Description:** Taux marge sur ventes normales  
**Résultat:** 40,18%  
**Usage:** Page 3 - Analyse ROI

---

### Différence de marge
```dax
Différence de marge = 
[Marge % Promo] - [Marge % Non Promo]
```
**Description:** Écart de rentabilité Promo vs Normal  
**Résultat:** 0,08% ≈ 0  
**Usage:** Page 3 - Conclusion promos

**💡 Insight:** Les promotions n'ont quasiment aucun impact positif!

---

## 4. Mesures Catalogue

### Nb Produit
```dax
Nb Produit = 
DISTINCTCOUNT(DimProduit[NomProduit])
```
**Description:** Nombre total de produits (catalogue complet)  
**Résultat:** 150  
**Usage:** Métriques catalogue

---

### Nb Produits Actifs
```dax
Nb Produits Actifs = 
CALCULATE(
    DISTINCTCOUNT(DimProduit[NomProduit]),
    DimProduit[EstArrete] = "Non"
)
```
**Description:** Produits en vente  
**Résultat:** 68  
**Usage:** Page 5 - KPI catalogue

---

### Nb Produits Discontinués
```dax
Nb Produits Discontinués = 
CALCULATE(
    DISTINCTCOUNT(DimProduit[NomProduit]),
    DimProduit[EstArrete] = "Oui"
)
```
**Description:** Produits arrêtés  
**Résultat:** 82  
**Usage:** Page 5 - Donut catalogue

---

### CA Produits Arrêtés
```dax
CA Produits Arrêtés = 
CALCULATE(
    [CA Total],
    DimProduit[EstArrete] = "Oui"
)
```
**Description:** CA généré par produits discontinués  
**Usage:** Analyse fin de vie

---

### % Produits Stars
```dax
% Produits Stars = 
VAR TableProduits = VALUES(DimProduit[NomProduit])
VAR NbStars = 
    COUNTROWS(
        FILTER(
            TableProduits,
            [Taux de Marge %] > 50
        )
    )
VAR NbTotal = COUNTROWS(TableProduits)
RETURN
DIVIDE(NbStars, NbTotal, 0) * 100
```
**Description:** % de produits avec >50% marge  
**Résultat:** 42,7%  
**Usage:** Page 2 - KPI qualité

**📝 Logique:**
1. Créer table des produits
2. Filtrer ceux avec marge >50%
3. Compter et calculer le ratio

---

### Nb Lancements
```dax
Nb Lancements = 
CALCULATE(
    DISTINCTCOUNT(DimProduit[ID_Produit]),
    YEAR(DimProduit[DateLancement]) = SELECTEDVALUE(DimDate[Annee])
)
```
**Description:** Nouveaux produits lancés dans l'année  
**Usage:** Page 5 - Line chart innovation

**⚠️ Note:** Nécessite une année sélectionnée

---

### Nb Arrêts
```dax
Nb Arrêts = 
CALCULATE(
    DISTINCTCOUNT(DimProduit[ID_Produit]),
    YEAR(DimProduit[DateArret]) = SELECTEDVALUE(DimDate[Annee])
)
```
**Description:** Produits arrêtés dans l'année  
**Usage:** Page 5 - Line chart innovation

---

## 5. Mesures Time Intelligence

### Croissance YoY %
```dax
Croissance YoY % = 
VAR AnneeActuelle = SELECTEDVALUE(DimDate[Annee])
VAR AnneePrecedente = AnneeActuelle - 1

VAR CAActuel = 
    CALCULATE(
        [CA Total],
        DimDate[Annee] = AnneeActuelle
    )

VAR CAPrecedent = 
    CALCULATE(
        [CA Total],
        DimDate[Annee] = AnneePrecedente,
        REMOVEFILTERS(DimDate)
    )

RETURN
IF(
    ISBLANK(AnneeActuelle) || CAPrecedent = 0,
    BLANK(),
    DIVIDE(CAActuel - CAPrecedent, CAPrecedent, 0) * 100
)
```
**Description:** Croissance vs année N-1  
**Usage:** Page 5 - Line chart évolution  
**Résultats:**
- 2021: +2,5%
- 2022: -0,4%
- 2023: -1,0%

**📝 Logique:**
- Récupère année actuelle du contexte
- Compare avec année précédente
- `REMOVEFILTERS` permet d'accéder à N-1 même si filtré

---

### Dernière Croissance
```dax
Dernière Croissance = 
VAR DerniereAnnee = MAX(DimDate[Annee])
VAR AvantDerniereAnnee = DerniereAnnee - 1

VAR CA_Dernier = 
    CALCULATE(
        [CA Total],
        DimDate[Annee] = DerniereAnnee
    )

VAR CA_AvantDernier = 
    CALCULATE(
        [CA Total],
        DimDate[Annee] = AvantDerniereAnnee
    )

RETURN
IF(
    CA_AvantDernier = 0,
    BLANK(),
    DIVIDE(CA_Dernier - CA_AvantDernier, CA_AvantDernier, 0) * 100
)
```
**Description:** Croissance dernière année (automatique)  
**Résultat:** -1,0% (2023 vs 2022)  
**Usage:** Page 5 - KPI card

**Différence vs Croissance YoY:**
- **Croissance YoY:** Dynamique (dépend année sélectionnée)
- **Dernière Croissance:** Fixe (toujours 2023 vs 2022)

---

### Tendance
```dax
Tendance = 
IF([Dernière Croissance] < 0, "📉 DÉCLIN", "📈 CROISSANCE")
```
**Description:** Indicateur visuel de tendance  
**Résultat:** "📉 DÉCLIN"  
**Usage:** Page 5 - Label dynamique

---

## 6. Mesures Dérivées

### Nb Pharmacies
```dax
Nb Pharmacies = 
DISTINCTCOUNT(DimPharmacie[ID_Pharmacie])
```
**Description:** Nombre de points de vente  
**Résultat:** 80  
**Usage:** Page 4 - KPI réseau

---

### Nb Pays
```dax
Nb Pays = 
DISTINCTCOUNT(DimPharmacie[Pays])
```
**Description:** Nombre de pays couverts  
**Résultat:** 8 (UEMOA)  
**Usage:** Page 4 - KPI géographique

---

### Colonne 1
```dax
Colonne 1 = 1
```
**Description:** Constante pour comptages  
**Usage:** Calculs intermédiaires

---

## 📊 Statistiques des mesures

**Répartition par catégorie:**
- Core Business: 7 mesures
- Analytiques Pertes: 6 mesures
- Promotions: 5 mesures
- Catalogue: 6 mesures
- Time Intelligence: 3 mesures
- Dérivées: 3 mesures

**Total: 30 mesures DAX**

---

## 🎯 Best Practices appliquées

### 1. Gestion des erreurs
```dax
DIVIDE([Marge], [CA], 0)     // Évite #DIV/0!
IF(ISBLANK(X), BLANK(), ...) // Gère valeurs manquantes
```

### 2. Variables (VAR)
```dax
VAR AnneeActuelle = SELECTEDVALUE(DimDate[Annee])
VAR CAActuel = CALCULATE(...)
RETURN ...
```
**Avantages:**
- ✅ Code lisible
- ✅ Performances optimisées
- ✅ Débogage facilité

### 3. Context Transition
```dax
CALCULATE(
    [CA Total],
    FaitVentes[Promotion] = "Oui"
)
```
`CALCULATE` modifie le contexte de filtre.

### 4. Filtres sur mesures
```dax
FILTER(
    VALUES(DimProduit[NomProduit]),
    [Taux de Marge %] > 50
)
```
**⚠️ Important:** On ne peut pas filtrer directement sur une mesure dans CALCULATE.  
Il faut utiliser FILTER + itération sur une table.

### 5. Time Intelligence
```dax
REMOVEFILTERS(DimDate)
```
Permet d'accéder aux autres années dans comparaisons.

---

## 🔧 Dépannage courant

### ❌ Erreur: "Cannot filter on measure"

**Problème:**
```dax
CALCULATE([CA Total], [Taux de Marge %] > 40)
```

**Solution:**
```dax
VAR TableProduits = VALUES(DimProduit[NomProduit])
RETURN
COUNTROWS(
    FILTER(TableProduits, [Taux de Marge %] > 40)
)
```

### ❌ Erreur: Division par zéro

**Problème:**
```dax
[Marge] / [CA]
```

**Solution:**
```dax
DIVIDE([Marge], [CA], 0)
```

### ⚠️ Mesure retourne BLANK

**Causes fréquentes:**
- Aucune valeur dans `SELECTEDVALUE()`
- Filtre vide
- Division par zéro

**Solution:** Tester avec `IF(ISBLANK(...))`

---

## 📚 Ressources

**Documentation DAX:**
- [DAX Guide](https://dax.guide) - Référence complète
- [SQLBI](https://www.sqlbi.com/articles/) - Articles experts
- [Microsoft Learn](https://learn.microsoft.com/en-us/dax/) - Documentation officielle

**Tutoriels vidéo:**
- Curbal (Espagnol/Anglais)
- Guy in a Cube (Anglais)
- SQLBI (Anglais)

**Communauté francophone:**
- Power BI de A à Z (YouTube)
- Forum Power BI France

---

## 📝 Checklist utilisation

Avant d'utiliser ces mesures dans un nouveau projet:

- [ ] Adapter les noms de tables (`FaitVentes`, `DimProduit`, etc.)
- [ ] Vérifier les noms de colonnes (`MargeEUR`, `Promotion`, etc.)
- [ ] Tester les mesures avec données réelles
- [ ] Valider les résultats vs Excel
- [ ] Documenter les modifications

---

**Dernière mise à jour:** 28 février 2026  
**Auteur:** Boubacar Nikiema  
**Projet:** DaCoT Challenge 2026 - Analyse Pharmaceutique UEMOA  
**Dashboard:** [Power BI Service](https://app.powerbi.com/links/iMdvWW9tFd)
