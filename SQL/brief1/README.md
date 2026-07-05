# Brief 1 : L'Architecte & Explorateur SQL — De la Conception Merise aux Jointures Relationnelles

## Description du projet
Dans ce projet complet, vous allez concevoir l'architecture relationnelle de la base de données de l'entreprise via la méthode MERISE. Vous installerez ensuite votre serveur de production **MySQL** et le client **MySQL Workbench** pour traduire vos modèles en tables physiques. Enfin, après avoir peuplé votre base de données, vous écrirez un script d'interrogation analytique (filtres, agrégations, jointures multi-tables) afin de valider la conformité du système et d'extraire des indicateurs d'aide à la décision.

## Référentiels
* Référentiel de compétences Data Analyst / Développeur en IA.

## Compétences techniques et transversales à mobiliser dans ce brief
* **C11DE (Niveau 1)** : Élaborer un MCD, un MLD et implémenter les tables physiques avec leurs clés et types de données.
* **C4 & C9DE (Niveau 1)** : Écrire des requêtes d'insertion (`INSERT`), de mise à jour (`UPDATE`) et d'extraction de données (`SELECT`, `WHERE`, `GROUP BY`, `JOIN`).
* **CT3 (Niveau 1)** : Analyser les contraintes et questions métiers pour les traduire en schémas et en requêtes SQL valides.

## Ressources
Les documents techniques d'exploration suivants sont mis à votre disposition pour réaliser vos jalons :
* **Dossier Technique 1** : Modélisation de bases de données — La méthodologie MERISE (MCD, MLD, MPD).
* **Dossier Technique 2** : Guide d'installation et d'architecture Client-Serveur MySQL.
* **Dossier Technique 3** : Conception physique et création des tables (DDL).
* **Dossier Technique 4** : Manipulation, mise à jour et requêtes d'interrogation fondamentales (DML / DQL 1).
* **Dossier Technique 5** : Fonctions d'agrégation, regroupements et filtrages avancés (DQL 2).
* **Dossier Technique 6** : Les jointures relationnelles (INNER, LEFT, RIGHT, FULL, CROSS) et requêtes multi-tables.
* **Défi Final de Validation** : Plateforme interactive [SQL Island Game](https://sql-island.informatik.uni-kl.de/).
* **Défi Bonus d'Entraînement Avancé** : Jeu d'enquête [SQL Murder Mystery](https://mystery.knightlab.com/index.html).

---
## Contexte du projet

Tu intègres l'équipe Data de la startup **DealFlow**. L'entreprise souhaite centraliser et structurer ses données de ventes (clients, produits, catégories et transactions), actuellement éparpillées sur des tableurs indépendants.

Avant de te donner accès à des volumes de données industriels, ta direction te demande de prouver ton autonomie sur un environnement de test. Ta mission consiste à :

1. **Modéliser** les relations logiques pour éviter toute redondance (méthode MERISE).
2. **Déployer** l'infrastructure physique et créer les tables sur ton serveur local MySQL.
3. **Peupler** la base avec le jeu d'essai fourni.
4. **Développer** un script d'interrogation analytique (filtres, agrégations et jointures) pour extraire les indicateurs de performance clés (KPIs) demandés par les équipes commerciales.

---
## Modalités pédagogiques

### Activité 1 (3h, individuel) — Ingénierie des données & Modélisation MERISE
* **Analyse conceptuelle** : À l'aide du *Dossier Technique 1*, étudiez les principes des entités, des associations et des cardinalités (1:1, N:1, N:M).
* **Passage au MLD/MPD** : Appliquez les règles de transformation Merise pour faire migrer les clés primaires, concevoir les clés étrangères et générer la table intermédiaire indispensable pour les relations plusieurs-à-plusieurs.
* **Mise en pratique** : Réalisez le challenge d'application (Client - Commande - Ligne de commande - Produit - Fournisseur). Analysez la structure cible et préparez les types de données (INT, VARCHAR, DECIMAL, DATE) adaptés à chaque attribut.

### Activité 2 (2h, individuel) — Administration système & Déploiement de l'environnement
* **Mise en place de l'infrastructure** : À l'aide du *Dossier Technique 2*, téléchargez et installez MySQL Server sur votre machine. Configurez de manière sécurisée l'utilisateur administrateur (`root`).
* **Prise en main du client** : Installez **MySQL Workbench**. Configurez la connexion locale avec le serveur et appréhendez l'interface graphique (sections "SCHEMAS", volet d'exécution des requêtes, panneau de sortie "Output").

### Activité 3 (3h, individuel) — DDL & DML : Création des tables et peuplement
* **Implémentation physique (DDL)** : En suivant le *Dossier Technique 3*, écrivez et exécutez le script SQL de création de la base de données `sales_db` et de ses tables (`customer`, `product`, `sale`, `sale_product`, `category`). Assurez-vous d'implémenter correctement toutes les clés primaires, uniques, et les contraintes de clés étrangères.
* **Conversion de type** : Choisissez rigoureusement vos formats de données (ex. `DECIMAL(10,2)` pour la table produit afin d'éviter les erreurs d'arrondis sur les prix).
* **Peuplement (DML)** : Écrivez et exécutez vos requêtes `INSERT INTO` pour injecter l'ensemble du jeu d'essai fourni (30 clients, 5 catégories, 30 produits, et 50 ventes).
* **Maintenance du catalogue** : Pratiquez la modification de données ciblées via `UPDATE` et la suppression via `DELETE` sur des enregistrements de test en veillant à la stricte application de la clause `WHERE`.

### Activité 4 (4h, individuel) — Requêtage analytique, Agrégations & Jointures
* **Extraction et Agrégation (DQL)** : Plongez-vous dans les *Dossiers Techniques 4 et 5*. Développez individuellement les requêtes permettant de répondre aux besoins de la direction (filtres avancés avec `LIKE`, tris, fonctions `COUNT`, `SUM`, `AVG`, sélections regroupées avec `GROUP BY` et filtres de groupes `HAVING`).
* **Jointures multiples** : À l'aide du *Dossier Technique 6*, étudiez de manière approfondie les mécanismes de jointures (`INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN`, `CROSS JOIN`, et l'émulation du `FULL OUTER JOIN` par `UNION`). Développez individuellement les requêtes permettant de croiser vos données pour répondre aux besoins métiers de l'entreprise (ex. associer les ventes aux catégories de produits, lister les clients inactifs via un filtre `IS NULL`, chaîner les jointures multiples et utiliser des alias).
* **Consolidation** : Rassemblez l'intégralité de vos requêtes individuelles (challenges des dossiers 4, 5 et 6) dans un fichier de script `.sql` unique, propre, rigoureusement indenté et commenté.

### Activité 5 (2h, en binômes) — Le Grand Défi Final : SQL Island
* **Immersion et Co-working** : Connectez-vous en binôme sur l'application **SQL Island**.
* **Logique collaborative** : Utilisez l'ensemble de la syntaxe apprise et validée durant vos exercices et explorations individuelles pour résoudre l'enquête textuelle à deux, débloquer les situations et obtenir votre certificat de réussite collectif.

### Activité 6 (Optionnelle - 2h, individuel ou binôme) — Activité Bonus : SQL Murder Mystery
* Immersion et Enquête : Accédez à la plateforme SQL Murder Mystery. Une mine d'or de données policières vous attend pour résoudre un crime grâce à vos compétences SQL SQL.
* Objectif d'entraînement : Conçu pour faire le pont vers un niveau avancé, ce défi vous demande de naviguer en autonomie complète dans un schéma inconnu. Vous devrez inspecter les tables de la base de données, croiser les rapports de police, les témoignages des suspects et les indices (adhésions à la salle de sport, plaques d'immatriculation) à l'aide de jointures et de filtres textuels précis pour identifier le coupable et le commanditaire.

### Activité 7 (1h, collectif) — Restitution & Code Review
* **Partage technique** : Présentation au tableau par certains binômes de la logique de leurs requêtes de jointures complexes et de regroupements.
* **Débriefing** : Analyse partagée avec la formatrice sur les pièges classiques rencontrés (erreurs de syntaxe, confusion entre `LEFT JOIN` et `INNER JOIN`, oubli du critère d'évaluation des valeurs manquantes `IS NULL` ou fausses pistes lors de l'enquête criminelle).

---

## Modalités d'évaluation
* **Évaluation du livrable technique** : Exécution complète et sans erreur du script SQL final sur MySQL Workbench.
* **Validation de la démarche** : Cohérence des schémas de modélisation (MCD/MLD) produits lors de la phase conceptuelle.
* **Explication du code en binôme** : Capacité à expliciter oralement l'ordre d'exécution logique d'une requête SQL (FROM -> JOIN -> WHERE -> GROUP BY -> HAVING -> SELECT -> ORDER BY -> LIMIT) et à justifier le choix stratégique d'un type de jointure par rapport à un autre.
* **Jalon d'immersion** : Validation visuelle du certificat de réussite de l'exercice en binôme *SQL Island*.
* **Bonus avancé (Optionnel)** : Validation de l'enquête *SQL Murder Mystery* par la découverte du nom du coupable et du commanditaire secret via la commande de vérification de la plateforme.

## Livrables
1. Un document ou croquis contenant le **MCD** et le **MLD** du challenge de modélisation Merise initial.
2. Une capture d'écran prouvant la réussite de la mission collective sur **SQL Island**.
3. (Optionnel) Une capture d'écran de l'écran de succès du SQL Murder Mystery ou le code SQL final ayant permis de démasquer le cerveau du crime.
4. Un fichier de script SQL unique, parfaitement indenté et documenté, nommé `sales_db_master_script.sql`, structuré comme suit :
    * `-- PARTIE 1 : Structure (DDL)` : Requêtes de création de la base, des tables, contraintes et altérations (Dossier Technique 3).
    * `-- PARTIE 2 : Manipulation & Requêtes simples (DML/DQL)` : Requêtes d'insertions et sélections fondamentales (Dossier Technique 4).
    * `-- PARTIE 3 : Agrégations & Regroupements` : Requêtes basées sur le GROUP BY, HAVING et fonctions statistiques (Dossier Technique 5).
    * `-- PARTIE 4 : Jointures Relationnelles & Cas Pratiques` : Requêtes combinant plusieurs tables, identification d'éléments orphelins et auto-jointures (Dossier Technique 6).

## Critères de performance
* Le script SQL est entièrement fonctionnel, robuste et s'exécute sans aucune erreur de syntaxe dans MySQL Workbench.
* Les contraintes d'intégrité (clés étrangères, unicité) sont respectées et protègent efficacement la base contre les anomalies de données.
* Les jeux de résultats retournés sont exacts et précis (absence de lignes dupliquées accidentellement, gestion rigoureuse des valeurs `NULL`).
* Le code respecte les standards professionnels de visibilité : mots-clés SQL écrits rigoureusement en MAJUSCULES, structure indentée, et chaque requête est documentée par un commentaire précédé de `--`.