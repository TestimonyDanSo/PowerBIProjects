# 💳 03 Power BI Project – Expense Dashboard

## Objectif du projet
Ce projet vise à mettre en place un **suivi clair et interactif des dépenses** via un dashboard Power BI.
Il s’appuie sur un flux de données structuré **Excel → Snowflake (ODS → DWH/Datamart) → Power BI**, avec un **contrôle de qualité** pour fiabiliser les analyses.

---

## Architecture (vue d’ensemble)
1. **Saisie / source** : fichier Excel de dépenses  
2. **Ingestion & stockage** : Snowflake (zone **ODS** puis **DWH/Datamarts**)  
3. **Qualité des données** : règles de contrôle (types, valeurs nulles, doublons, cohérence)  
4. **Restitution** : **Power BI** (KPI + filtres dynamiques + analyses par catégories/temps)

---

## Données utilisées
- **Source** : fichier Excel de saisie des dépenses (ex : date, montant, catégorie/sous-catégorie, moyen de paiement, etc.)
- **Objectif data** : standardiser les champs (formats date/nombres), améliorer la cohérence des libellés et permettre l’agrégation fiable.

---

## Étapes réalisées (Data Pipeline)
### 1) Préparation / nettoyage
- Typage des colonnes (date, numérique, texte)
- Gestion des valeurs manquantes (ex : “Non renseigné” / 0 selon le cas)
- Harmonisation des catégories/sous-catégories
- Détection des doublons et incohérences

### 2) Chargement & organisation dans Snowflake
- Chargement en **ODS** (staging)
- Structuration en **DWH/Datamarts** pour l’analyse (tables prêtes pour le reporting)
- Suivi de la qualité et traçabilité des corrections

### 3) Modélisation Power BI
- Modèle orienté reporting (type **étoile** : dimensions + table de faits)
- Mesures DAX pour les KPI
- Gestion des filtres et des interactions (drill-down, segmentation, période, catégorie)

---

## Dashboard Power BI (contenu)
Exemples d’analyses généralement incluses :
- **KPI** : Total dépenses, dépenses moyennes, nb de transactions, etc.
- **Analyse temporelle** : évolution mensuelle / journalière
- **Répartition** : par catégorie / sous-catégorie / description de dépense
- **Filtres dynamiques** : période, catégorie, sous-catégorie (et autres selon le modèle)

---

## Outils & technologies
- **Power BI Desktop** (Power Query + DAX)
- **Snowflake** (ODS, DWH/Datamarts)
- **Excel** (source de données)

---

## Contenu du repository
- `03 Power BI Project - Suivi depenses.pbix` → Dashboard Power BI
- `SAISIE_DEPENSE.xlsx` → Données source (saisie des dépenses)
- `README.md` → Documentation du projet

---

## Comment utiliser le projet
1. Cloner le repo
2. Ouvrir le fichier `.pbix` avec **Power BI Desktop**
3. Vérifier la source de données (Excel ou Snowflake selon ton paramétrage)
4. Actualiser le modèle (Refresh) pour mettre à jour les visuels

---

## Auteur
**Danielle LOUMDOUOBE NOUETSA**  
*Étudiante en Master MIAGE – Spécialisation Data & Business Intelligence*  
*Orientation : Data Analyse / BI / Data Science* 
