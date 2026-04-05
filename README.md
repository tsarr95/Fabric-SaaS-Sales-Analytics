# Analyse des Ventes SaaS — Microsoft Fabric

## Présentation

Ce projet montre comment construire une architecture Lakehouse moderne pour analyser
les revenus d'une entreprise SaaS. L'objectif était de couvrir l'intégralité du cycle
de la donnée — de l'ingestion brute jusqu'à la visualisation finale, en utilisant
notre Saas Microsoft Fabric.

## Stack technique

L'utilisation du language de programmation PySpark et Spark SQL pour le
traitement des données, T-SQL pour le requêtage analytique, Delta Lake pour le
stockage en tables ACID, et Power BI en mode Direct Lake pour la visualisation.

## Pipeline de données

Les données transactionnelles sont d'abord simulées via un Notebook Spark, puis
nettoyées et enrichies en Python avec le calcul automatique de la TVA à 20%. Les
résultats sont ensuite validés par des requêtes SQL sur le point de terminaison
analytique de Fabric, avant d'être exposés dans un dashboard Power BI présentant
le chiffre d'affaires par type de forfait : Basic, Premium et Ultra.

## Résultats

Le plan Premium ressort comme le plus rentable avec 780 € TTC de revenu généré,
tandis que le plan Basic concentre le plus grand volume de transactions.
