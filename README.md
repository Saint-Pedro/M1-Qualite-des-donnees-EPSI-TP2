# M1-Qualite-des-donnees-EPSI-TP2
# Analyse de la Qualité des Données - OpenFoodFacts

Ce projet a été réalisé dans le cadre du TP "Qualité des Données". L'objectif est de préparer les données pour une application mobile d'aide au choix alimentaire en utilisant un jeu de données OpenFoodFacts (`food_sample.parquet`). Le projet inclut un audit de qualité avec **Great Expectations**, un nettoyage des données brutes, et la mise en place de règles de validation métier.

## L'Équipe
* **TAVENART Tuan**
* **LAURENS Astin**
* **ROBIGO Louis**
* **FOUSSENI Charif**

---

## Objectifs du projet

1.  **Profilage des données :** Exploration du dataset (119 532 entrées) pour identifier les problèmes structurels (colonnes JSON, types mixtes) et les valeurs manquantes.
2.  [cite_start]**Audit de la qualité (Great Expectations) :** Définition de règles de validation (complétude, unicité, validité) et calcul d'un score de conformité initial [cite: 29-30].
3.  **Traitement et Nettoyage :**
    * [cite_start]Mise à plat des colonnes complexes (dictionnaires dans `product_name`, etc.)[cite: 58].
    * [cite_start]Standardisation des types (str, float)[cite: 56].
    * [cite_start]Dédoublonnage pour garantir un produit unique par ligne[cite: 57].
4.  [cite_start]**Logique Métier et Monitoring :** Identification des valeurs nutritionnelles aberrantes et proposition d'indicateurs de surveillance pour les mises à jour hebdomadaires[cite: 79].

## Structure du Projet

Le projet respecte les bonnes pratiques d'organisation de fichiers :

```text
.
├── data/
│   ├── raw/          # Données brutes (food_sample.parquet)
│   └── processed/    # Données nettoyées (df_clean) prêtes pour l'analyse
├── src/              # Notebooks et scripts de traitement
├── requirements.txt  # Dépendances Python (pandas, great_expectations, pyarrow)
└── README.md         # Documentation du projet
```
## Résultats Clés
* **Audit Initial : Taux de succès de 40% sur les données brutes.**
* **Après Nettoyage : Amélioration du score à 60% de succès après restructuration et typage.**
  
## Installation et Prérequis
**Le projet est conçu pour fonctionner sur Google Colab ou un environnement local Python.**
**pip install -r requirements.txt**
