# Projet-BI-4 : Analyse des Dépenses IT

## 1. Contexte du Projet
Ce projet vise à analyser les dépenses IT d'une organisation sur une période donnée.  
Il compare les dépenses réelles aux budgets prévus et aux prévisions (Forecast), et met en lumière les écarts par département, groupe de coûts et pays.  
Le but est d’identifier les zones de surconsommation, les postes les plus coûteux, et les axes d'amélioration potentiels.

## 2. Objectifs
- Analyser les dépenses réelles par rapport aux budgets et aux prévisions
- Identifier les départements IT en dépassement budgétaire
- Visualiser la répartition géographique et fonctionnelle des coûts
- Détecter les périodes critiques (ex : pics de dépenses)
- Mettre en évidence les catégories de dépenses principales (ex : External Labor, Hardware Maintenance)

## 3. Étapes de la Conception du Dashboard

### a. Préparation des Données
- Normalisation des colonnes : Date, Département, Type de coût, Pays, Montants
- Suppression ou traitement des valeurs nulles (notamment dans les prévisions)
- Création de nouvelles mesures pour faciliter l'analyse (ex : Ecart Budget vs Réel)

### b. Création des KPI & Visualisations

#### • KPI 1 : Dépense totale vs Budget vs Prévision
- Variables : Actual, Budget, Forecast
- Visualisation : Cartes de résumé + graphes temporels
- Intérêt : Suivre la performance financière globale

#### • KPI 2 : Dépassement budgétaire par département
- Variables : IT Department, Budget, Actual
- Visualisation : Graphique bulles et histogrammes
- Intérêt : Cibler les départements à risque

#### • KPI 3 : Répartition des dépenses par type de coût
- Variables : Cost Element
- Visualisation : Treemap + histogramme
- Intérêt : Identifier les principaux postes de dépenses

#### • KPI 4 : Répartition géographique des dépenses
- Variables : Country
- Visualisation : Carte géographique
- Intérêt : Localiser les principaux centres de coûts

#### • KPI 5 : Analyse mensuelle et trimestrielle des écarts
- Variables : Date, Actual, Budget
- Visualisation : Séries temporelles
- Intérêt : Détecter les pics inhabituels de dépenses

## 4. Résultats et Insights Clés
- Les dépenses totales sont légèrement inférieures au budget prévu.
- 13 départements affichent un dépassement supérieur à 10%.
- Les coûts d'External Labor représentent une part très significative du budget total.
- Le mois de décembre est critique avec un dépassement maximal de 7M.
- Environ 35% des prévisions sont manquantes, ce qui limite la qualité des analyses prévisionnelles.

## 5. Structure du Projet
- `IT_Expenses.pbix` → Fichier Power BI contenant le dashboard interactif
- `data/` → Fichiers sources (si applicable)
- `screenshots/` → Captures d'écran des pages du dashboard
- `README.md` → Document de présentation du projet

## 6. Perspectives d'Amélioration
- Intégration de données supplémentaires sur les contrats fournisseurs pour mieux analyser External Labor.
- Création d'indicateurs de performance par chef de département.
- Automatisation de l’actualisation des données.
- Mise en place d'alertes automatiques en cas de dépassement budgétaire.
