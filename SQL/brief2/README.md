# Brief 2 : L'Analyste & Métricien SQL — Des Structures Avancées aux Fonctions Analytiques de Catalogue

**Description rapide du projet :** 

Dans ce brief, vous allez endosser le rôle d'un Data Analyst utilisant l'environnement **SQLite via DBeaver**. En vous basant sur l'historique de la base de données de films (`movies.sqlite`), vous allez expérimenter et valider des concepts SQL de niveau avancé : les sous-requêtes imbriquées, la création de vues réutilisables, l'utilisation de Common Table Expressions (CTE) et le déploiement des fonctions de fenêtrage (Window Functions). 

L'objectif final est de générer un rapport de performance métier (KPIs) et de formuler une recommandation stratégique en binôme pour éclairer les choix d'investissement de la direction.

---

## 1. Référentiels de Compétences

### Compétences techniques et transversales mobilisées :
* **C4. Extraire des données** en développant des scripts personnalisés SQL pour récupérer des informations précises et pertinentes (Niveau 2 - Transposer).
* **C5. Mener des analyses exploratoires** en calculant des techniques statistiques descriptives (Niveau 2 - Transposer).
* **C20. Identifier les indicateurs clés à calculer** en interrogeant les besoins métier afin de structurer les analyses nécessaires à des prises de décisions stratégiques (Niveau 2 - Transposer).
* **CT3. Définir le périmètre d’un problème rencontré** en adoptant une démarche inductive.
* **CT4. Rechercher de façon méthodique des pistes de résolutions** au problème rencontré afin de le résoudre (Niveau 2 - Transposer).
* **CT6. Présenter un travail réalisé** en synthétisant ses résultats, sa démarche et en répondant aux questions (Niveau 2 - Transposer).

---

## 2. Ressources Disponibles

Les ressources techniques indispensables sont structurées et partagées dans le dépôt de votre formation :
* **Dossier technique 1 (`1.Sous_requetes_CTE_Vues.md`) :** Concepts d'imbrication, clauses `WITH` (CTE) et structures `CREATE VIEW`.
* **Dossier technique 2 (`2.Window_Functions.md`):** Concepts de fenêtrage `OVER`, `LAG`, `LEAD`, `NTILE` et `PERCENT_RANK`.
* **Base de données :** Fichier [`movies.sqlite`](https://drive.google.com/drive/folders/1ckeBbaCql0QJjtLB5RCeUNL7eBKxyVoK?ths=true) à importer dans votre client SQL.
* **Outil de travail :** Client SGBD [DBeaver](https://dbeaver.io/download/) configuré en mode SQLite.

---

## 3. Contexte du Projet

L’entreprise **CinéStream** prépare son plan d'acquisition et d'investissement de catalogue. Le Directeur des Contenus vous confie l'analyse de l'historique du cinéma mondial stocké dans la base `movies.sqlite`. Vos prédécesseurs ont échoué à bâtir des rapports stables car leurs requêtes étaient trop longues, imbriquées à l'infini, lentes et impossibles à maintenir. 

Pour mener à bien votre mission, vous devez assimiler les deux dossiers de documentation technique (R1 et R2) mis à votre disposition. Vous appliquerez ces concepts avancés pour isoler des données précises, analyser les variations temporelles de notes et classifier efficacement le catalogue. L'ensemble de votre travail prendra la forme d'un dossier technique validé individuellement, d'un script consolidé et d'un mini-rapport de performance métier rédigé en binôme contenant une recommandation d'achat exclusive.

---

## 4. Modalités Pédagogiques & Déroulement

### 🔹 Activité 1 : Expérimentation, Isolation & Vues Virtuelles (6h, en binômes)
* Configuration de l'espace de travail sur DBeaver avec la base `movies.sqlite`.
* Assimilation et mise en pratique de la **Ressource R1** (Sous-requêtes et Vues).
* Résolution collective des problématiques de filtrage complexe : extraction des films surperformant la moyenne globale, isolation des réalisateurs prolifiques, et refactorisation du code vers des structures lisibles basées sur des blocs `WITH` (CTE).
* Création de structures de données virtuelles réutilisables via l'instruction `CREATE VIEW`.
* *Livrable intermédiaire : Chaque membre du binôme complète et prépare son propre fichier de réponses au Dossier technique 1.*

### 🔹 Activité 2 : Fonctions Analytiques & Métriques Temporelles (1j, en binômes)
* Assimilation et mise en pratique de la **Ressource R2** (Window Functions).
* Écriture de scripts exploitant la clause `OVER()` couplée à `PARTITION BY` pour calculer des statistiques par segment (genre, réalisateur) sans écraser les lignes de détails.
* Analyse des trajectoires et des dynamiques de production des cinéastes à l’aide des fonctions de navigation chronologique (`LAG` / `LEAD`).
* Segmentation du catalogue en intervalles de distribution équilibrés en manipulant les fonctions de répartition (`NTILE` et `PERCENT_RANK`).
* *Livrable intermédiaire : Chaque membre du binôme complète et prépare son propre fichier de réponses au Dossier technique 2.*

### 🔹 Activité 3 : "Pair Analytics Challenge" & Recommandation Métier (3h, en binômes)

* **Consolidation technique :** Rassemblez et fusionnez l'intégralité de vos requêtes SQL issues des dossiers R1 et R2 dans un script final unique, propre et commenté.
* **Production du livrable :** Établissez un rapport de performance commun au format Markdown (`kpi_report.md`) afin de présenter de manière structurée l'ensemble des indicateurs et KPIs extraits de la base de données.
* **Question Métier (Bonus) :** En fin de rapport, répondez de manière argumentée à la problématique stratégique suivante :
> 🎯 *"Si CinéStream ne devait signer qu'un seul nouveau contrat d'exclusivité basé sur la rentabilité historique et la stabilité des notes, quel profil précis de réalisateur (budget, genre, dynamique de progression) préconiseriez-vous pour maximiser notre retour sur investissement ?"*

### 🔹 Activité 4 : Restitution & Feedback Flash (1h, collectif)

* **Restitution collaborative :** Chaque binôme dispose de 5 à 10 minutes maximum pour présenter ses conclusions à l'oral à l'ensemble de la promotion.
* **Partage de connaissances :** Au-delà des chiffres bruts, chaque groupe partage ses retours d'expérience : bonnes pratiques, astuces d'optimisation, pièges syntaxiques évités (ex : sur l'usage du `LAG` ou des percentiles) ou méthodes de travail collaboratif adoptées.

---

### Modalités d'évaluation

* **Exactitude technique et conformité des scripts SQL** (exécutables et sans erreurs).
* **Capacité à expliquer à l'oral :**
* Le rôle et la structure d'une Window Function (`PARTITION BY`, `ORDER BY`).
* L'intérêt et la logique d'organisation d'une clause `WITH` (CTE).
* La différence d'usage entre une sous-requête, une CTE et une Vue virtuelle.


* **Utilisation correcte de DBeaver** pour exécuter, optimiser et documenter les scripts.
* **Qualité de la présentation flash (Activité 4) :** Clarté, respect du temps (5-10 min) et valeur ajoutée des astuces partagées avec la promotion.
* **Qualité et cohérence du mini-rapport rendu** (structure, tableaux de KPIs complets).

### Livrables

#### À rendre Individuellement :

1. **Dossier Technique 1 (`r1_sous_requetes_nom.sql`)**
* Contient les requêtes d'application sur les sous-requêtes, les CTE et les Vues.
* Code commenté.


2. **Dossier Technique 2 (`r2_fct_analytique_nom.sql`)**
* Contient les requêtes sur les Window Functions, le positionnement (`LAG`/`LEAD`) et les répartitions (`NTILE`/`PERCENT_RANK`).
* Code commenté.


#### À rendre en Binôme (Commun) :

1. **Script SQL Consolidé (`cinestream_final_audit.sql`)**
* Fichier unique regroupant l'intégralité des requêtes du challenge nettoyées.
* Mots-clés SQL standardisés en MAJUSCULES et code rigoureusement indenté et bien commenté.


2. **Le Mini-Rapport de Performance (`kpi_report.md`, format Markdown)**
* Doit contenir :
* Les tableaux bruts de KPIs extraits (Top réalisateurs, tranches budgétaires, groupes percentiles).
* En bonus : La recommandation stratégique rédigée (15–20 lignes) pour le Directeur des Contenus.
* Les astuces ou pièges syntaxiques identifiés durant le projet.

### Critères de performance

* **Les requêtes SQL sont exactes**, optimisées et immédiatement reproductibles sur DBeaver.
* **Les structures avancées** (CTE, Vues, Fenêtrage) sont utilisées à bon escient pour simplifier et structurer le code.
* **Les conclusions et les KPIs** présentés dans le rapport sont justes et fidèles aux données de la base.
* **Le partage devant la promo est instructif :** les astuces et bonnes pratiques présentées apportent une réelle valeur aux autres apprenants.
* **Les livrables sont clairs**, aérés, structurés, rédigés de manière professionnelle et respectent scrupuleusement les conventions de nommage.