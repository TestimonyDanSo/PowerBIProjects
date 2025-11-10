# 🏦 02 Power BI Project - Analyse du Churn Client Bancaire

## Objectif du projet
Ce projet vise à analyser les **facteurs de départ des clients d'une banque (churn)** à l’aide d’un **dashboard interactif Power BI**.  
L’objectif est d’aider les équipes marketing et relation client à **identifier les segments à risque** et à **anticiper les pertes de clients** grâce à une analyse visuelle claire et stratégique.

---

## Données utilisées
Dataset : *Bank Customer Churn Prediction* (Kaggle)  
Lien : [https://www.kaggle.com/datasets/mathchi/churn-for-bank-customers](https://www.kaggle.com/datasets/mathchi/churn-for-bank-customers)

Le jeu de données contient des informations sur les clients d’une banque :  
- Données démographiques : `Age`, `Gender`, `Geography`  
- Données financières : `CreditScore`, `Balance`, `EstimatedSalary`  
- Comportement bancaire : `NumOfProducts`, `HasCrCard`, `IsActiveMember`, `Tenure`  
- Cible : `Exited` (1 = client parti, 0 = client resté)

---

## Étapes réalisées dans Power BI
1. **Import et nettoyage des données** via Power Query :  
   - Suppression des colonnes non pertinentes (`RowNumber`, `CustomerId`, `Surname`)  
   - Typage correct des champs (numériques, booléens, texte)  
2. **Création de mesures DAX clés** :  
   - Taux de churn (%)  
   - Nombre total de clients  
   - Solde et âge moyen des clients churners  
3. **Conception du dashboard** :
   - Section KPI : Taux de churn, Nombre de clients, Clients actifs  
   - Analyse démographique : Churn par âge, genre, ancienneté  
   - Analyse financière : Churn par solde, score de crédit, salaire estimé  

---

## Aperçu des visualisations
Le dashboard Power BI permet de :
- Identifier les **profils clients les plus susceptibles de quitter la banque**  
- Visualiser les **tendances du churn par segment démographique et financier**  
- Comprendre les **facteurs influençant la fidélité client**  

**Visuels principaux :**
- KPI Cards : Taux de churn, Total clients
- Histogramme : Répartition du churn par âge  
- Bar Chart : Churn selon le nombre de produits  
- Donut Chart : Répartition du churn par genre  
- Heatmap : Score de crédit vs ancienneté  

---

## Impact Business
- Aide la banque à **identifier les clients à risque** et à **réduire le taux de désabonnement**  
- Permet une **segmentation client plus intelligente** pour les campagnes de fidélisation  
- Met en avant la **valeur stratégique de la data dans la décision business**

---

## Outils et technologies
- **Power BI Desktop**
- **Power Query** pour la transformation des données  
- **DAX** pour les mesures et indicateurs clés  

---

## Contenu du repository
- `BankChurn.pbix` → fichier Power BI du projet  
- `README.md` → documentation détaillée  
- (Optionnel) `BankChurn.csv` → jeu de données  

---

**Auteur** : *Danielle LOUMDOUOBE NOUETSA*  
*Étudiante en Master MIAGE – Spécialisation Data & Business Intelligence*  
*Aspirante Data Analyst/Data Scientist*

