# 🕸️ Automated Data Pipeline: Web Scraping to Executive Reporting

Ce projet démontre la mise en place d'un pipeline **ETL (Extract, Transform, Load)** complet et automatisé. Il permet de collecter des données sur le web, de les traiter statistiquement et de livrer un rapport décisionnel directement dans la boîte mail des parties prenantes.

---

## 📌 Vision du Projet
L'objectif est de transformer le Web en une source de données structurée pour aider à la prise de décision. Ce système remplace des heures de veille manuelle par un processus automatisé de 30 secondes.

---

## 🛠️ Architecture Technique

### 1. Ingestion de Données (Extraction)
* **Technologie** : `BeautifulSoup4`, `Requests`.
* **Fonctionnalité** : Scraping multi-pages avec gestion dynamique de la pagination et respect des serveurs via des pauses (`time.sleep`).

### 2. Traitement & Analyse (Transformation)
* **Technologie** : `Pandas`, `Regex`.
* **Opérations** : 
    * Nettoyage des chaînes de caractères et conversion monétaire.
    * Calcul de KPIs (Prix moyen, min, max, volume).
    * Génération de graphiques de distribution avec `Seaborn`.

### 3. Reporting & Livraison (Load/Deliver)
* **Technologie** : `FPDF`, `Smtplib`.
* **Résultat** : 
    * Génération d'un rapport PDF "Executive Summary" avec identité visuelle d'entreprise.
    * Système de notification multi-destinataires par email (SMTP).

---

## 🚀 Fonctionnement du Pipeline

Le script est orchestré par une fonction "Wrapper" (`job()`) qui garantit l'exécution séquentielle des tâches :

1. **Scraper** les données sur plusieurs pages.
2. **Analyser** les tendances du marché.
3. **Générer** un rapport PDF incluant les graphiques.
4. **Envoyer** le rapport par email à une liste prédéfinie de décideurs.

---

## 📂 Structure du Dépôt

* `notebook_complet.ipynb` : Le code source documenté.
* `data/` : Contient le fichier `books_scraped_data.csv` généré.
* `output/` : Contient un exemple du rapport PDF final `Rapport_Analytique_Entreprise.pdf`.
* `images/` : Graphiques de visualisation utilisés dans le rapport.

---

## 📈 Business Insights
Grâce à ce pipeline, une entreprise peut :
- Surveiller la concurrence en temps réel.
- Identifier les anomalies de prix sur le marché.
- Recevoir des rapports consolidés sans aucune intervention humaine.

---

## 👨‍💻 Auteur
**Tomté Hassane** *Étudiant en Master 2 MIDD (Data Engineering)* *Freelance Data Engineer & Software Consultant* *Fondateur de **DemarcheursIT***

---

> *Ce projet a été réalisé dans le cadre d'une spécialisation en automatisation des flux de données et intelligence d'affaires.*
