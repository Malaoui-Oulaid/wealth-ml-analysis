#  Wealth Prediction and Classification using Machine Learning

##  Description du projet

Ce projet vise à analyser et modéliser les déterminants de la richesse à partir de données géospatiales et socio-économiques provenant de plusieurs pays africains.  
Deux types d’analyses ont été réalisées :

1. **Régression** pour prédire une variable continue représentant un indice de richesse.
2. **Classification** pour prédire une variable binaire (*rich* / *poor*).

L’objectif principal est d’évaluer la capacité des modèles de Machine Learning à généraliser leurs prédictions sur des pays non observés lors de l’entraînement (Ghana, Kenya et Nigeria).

---

##  Objectifs

- Explorer et nettoyer les données (gestion des valeurs manquantes).
- Appliquer des méthodes d’apprentissage non supervisé (PCA, K-means).
- Construire des modèles supervisés de régression et de classification.
- Gérer le déséquilibre des classes avec la méthode **SMOTE**.
- Comparer plusieurs modèles (Logistic Regression, Random Forest, XGBoost).
- Sélectionner le meilleur modèle selon les métriques de performance (RMSE, R², Accuracy, ROC AUC).
- Visualiser les résultats (courbes ROC, matrices de confusion).

---

---

##  Technologies utilisées

- **Langage :** R  
- **Framework :** tidymodels  

### Packages principaux :
- `recipes`
- `themis` (SMOTE)
- `yardstick`
- `ggplot2`
- `xgboost`
- `ranger`

---

##  Méthodologie

### 1. Prétraitement des données
- Suppression des variables inutiles (ID).
- Imputation des valeurs manquantes (médiane pour les variables numériques).
- Normalisation des variables numériques.
- Encodage des variables catégorielles (one-hot encoding) avec `recipes`.

### 2. Division des données
- **Train set :** tous les pays sauf Ghana, Kenya, Nigeria.
- **Test set :** Ghana, Kenya, Nigeria.

### 3. Modèles utilisés
- Régression linéaire
- Random Forest
- XGBoost
- Logistic Regression (classification)

### 4. Gestion du déséquilibre des classes
- Application de **SMOTE** uniquement sur l’ensemble d’entraînement.

### 5. Évaluation
- Régression : RMSE, R²  
- Classification : Accuracy, ROC AUC, matrice de confusion, courbe ROC  

---

##  Résultats principaux

- Le modèle **XGBoost avec tuning** a obtenu les meilleures performances pour la classification (*rich/poor*) selon la métrique ROC AUC.
- Le modèle **XGBoost / Random Forest** a montré les meilleures performances pour la régression selon RMSE et R².
- Les courbes ROC indiquent une meilleure capacité de discrimination pour le modèle XGBoost comparé aux autres modèles.

---

##  Visualisations

- Analyse en composantes principales (PCA)
- Clustering K-means
- Courbes ROC comparatives
- Matrices de confusion
- Graphiques de performance des modèles




