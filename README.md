# 🌸 Projet de Classification Binaire : Iris Dataset

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-76B900?style=for-the-badge&logo=python&logoColor=white)

## 📖 Aperçu du Projet

Ce projet est une exploration pratique des algorithmes de **Machine Learning** appliquée au célèbre jeu de données *Iris*. L'objectif principal est de comprendre et d'implémenter manuellement une stratégie de classification **"One-vs-Rest"** (Un contre tous) en utilisant des machines à vecteurs de support (SVM).

[cite_start]Plutôt que d'utiliser une classification multi-classes automatique, ce projet construit explicitement **trois classifieurs binaires distincts**[cite: 94], chacun entraîné pour reconnaître une espèce spécifique :
1.  **Iris Setosa** vs les autres
2.  **Iris Virginica** vs les autres
3.  **Iris Versicolor** vs les autres

## 🛠️ Stack Technique

* **Langage :** Python
* **Environnement :** Jupyter Notebook
* **Analyse de données :** Pandas, NumPy
* **Machine Learning :** Scikit-Learn (`LinearSVC`, `StandardScaler`, Metrics)
* **Visualisation :** Matplotlib, Seaborn

## 📊 Méthodologie et Fonctionnalités

Le notebook suit un workflow de Data Science rigoureux :

### 1. Préparation des Données
* Chargement et séparation du dataset en ensembles d'entraînement et de test (**Train/Test split**).
* [cite_start]**Standardisation** des données via `StandardScaler` pour optimiser la convergence du SVM[cite: 102].

### 2. Entraînement des Modèles (SVM)
Utilisation de l'algorithme **LinearSVC**. Pour chaque espèce, les étiquettes cibles sont converties en format binaire (`True` pour l'espèce cible, `False` pour les autres).

### 3. Optimisation des Hyperparamètres
Recherche de la meilleure performance en testant différentes valeurs pour le paramètre de régularisation **C** (marge de séparation) : `[0.01, 0.1, 1, 10, 100]`.

### 4. Évaluation des Performances
Analyse détaillée des résultats pour chaque classifieur via :
* [cite_start]**Matrice de Confusion :** Pour visualiser les Vrais Positifs et Faux Négatifs[cite: 101].
* [cite_start]**Courbe ROC & AUC :** Pour mesurer la capacité de discrimination du modèle[cite: 101].
* **Rapport de classification :** Précision et Rappel.

## 🚀 Installation et Utilisation

1.  **Cloner le dépôt :**
    ```bash
    git clone [https://github.com/ton-user/iris-classification.git](https://github.com/ton-user/iris-classification.git)
    cd iris-classification
    ```

2.  **Installer les dépendances :**
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn jupyter
    ```

3.  **Lancer le Notebook :**
    ```bash
    jupyter notebook iris_classification.ipynb
    ```

---

## 🇬🇧 English Summary

**Project:** Manual Binary Classification on Iris Dataset

**Goal:** Implement a "One-vs-Rest" classification strategy from scratch using `LinearSVC` to distinguish between the three Iris species independently.

**Key Features:**
* **3 Distinct Binary Classifiers:** Manual implementation for Setosa, Virginica, and Versicolor.
* **Data Scaling:** Applied `StandardScaler` to normalize features.
* **Hyperparameter Tuning:** Grid search over `C` values to optimize margins.
* **Evaluation:** Analysis using ROC Curves, AUC scores, and Confusion Matrices.

**Tech Stack:** Python, Scikit-Learn, Pandas, Seaborn.
