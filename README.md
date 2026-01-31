🚢 Projet Titanic : Prédiction de Survie (Machine Learning)
📋 Description du Projet
Ce projet est une application classique de Machine Learning supervisé sur le célèbre jeu de données du Titanic. 
L'objectif est de créer un modèle capable de prédire si un passager a survécu ou non au naufrage, en se basant sur ses caractéristiques personnelles (âge, sexe, classe sociale, prix du billet, etc.).

C'est un exercice complet qui couvre tout le cycle de vie d'un projet Data Science : du nettoyage des données brutes à l'évaluation du modèle prédictif.

🎯 Objectif
Type de problème : Classification binaire.

Cible (Target) : Colonne Survived (0 = Décédé, 1 = Survivant).

Métrique d'évaluation : Précision (Accuracy).

⚙️ Méthodologie
Mon approche s'est structurée en 4 étapes clés :

1. Nettoyage des Données et Gestion des Valeurs Manquantes
Le jeu de données brut contient des lacunes, notamment sur l'âge (Age) et les numéros de cabine (Cabin).

Exemple d'action : Remplacement des âges manquants par la médiane ou une imputation basée sur le titre de civilité (Mr, Mrs, Miss).

2. Analyse Exploratoire des Données (EDA)
Cette phase cruciale permet de comprendre les facteurs déterminants de la survie.

Observation clé n°1 : L'influence du sexe et de la classe Le protocole "Les femmes et les enfants d'abord" est visible dans les données. Les femmes de 1ère classe ont eu un taux de survie nettement supérieur aux hommes de 3ème classe.
<img width="567" height="432" alt="image" src="https://github.com/user-attachments/assets/1408d096-9009-46b5-935b-34aed851539f" />

<img width="571" height="432" alt="image" src="https://github.com/user-attachments/assets/e2c7b928-2a83-4ed2-9808-2dc207353b68" />
diagramme des corrélations 
<img width="776" height="665" alt="image" src="https://github.com/user-attachments/assets/02b52862-abf1-4c36-b9bd-c3b5f0f28f41" />

3. Feature Engineering (Création de variables)
Pour améliorer le modèle, j'ai créé de nouvelles caractéristiques à partir des existantes :

FamilySize : Combinaison de SibSp (frères/époux) et Parch (parents/enfants) pour savoir si le passager voyageait seul.

Extraction de titres : Isoler les "Mr", "Mrs", "Miss" des noms pour affiner l'imputation de l'âge et le statut social.

Encodage : Transformation des variables catégorielles (Sexe, Port d'embarquement) en variables numériques (One-Hot Encoding ou Label Encoding) pour qu'elles soient lisibles par les algorithmes.

4. Modélisation
J'ai testé plusieurs algorithmes pour ce problème de classification :

Régression Logistique (Baseline)

Random Forest Classifier

📊 Résultats
Le meilleur modèle retenu est le Randim forest
**Meilleur score de Cross-Val : 84.96%
Note : Ce score a été obtenu après optimisation des hyperparamètres et validation croisée. via le Grid Search.

💻 Technologies Utilisées
Langage : Python

Manipulation de données : Pandas, NumPy

Visualisation : Matplotlib, Seaborn

Machine Learning : Scikit-Learn

🚀 Comment exécuter ce projet
Cloner le dépôt.

Installer les dépendances : pip install pandas numpy seaborn scikit-learn matplotlib

Lancer le Jupyter Notebook : titanic.ipynb







