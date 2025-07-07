Analyse des Dynamiques Communautaires sur Reddit autour du Changement Climatique
🎯 Introduction

Dans le cadre du Projet Complexe (ProCom) de troisième année ou deuxième année de master, il nous a été confié comme tâche d’analyser les dynamiques des interactions des communautés se battant en faveur du changement climatique d’une part, et des communautés en faveur du négationnisme de ce dernier.

❓ Problématique

Examiner et déterminer l’existence d’événements sociétaux particuliers susceptibles de stimuler une augmentation des interactions au sein des communautés d’activistes impliquées dans la lutte contre le changement climatique, ainsi que des communautés qui soutiennent le négationnisme climatique sur Reddit.

🎯 Objectifs

L’objectif principal de ce projet est de saisir la dynamique des échanges entre les différentes communautés impliquées dans le débat sur le changement climatique, en particulier sur la plateforme Reddit.

Reddit, en tant que réseau social structuré autour de sous-communautés appelées subreddits, offre un terrain propice à l’analyse des échanges en ligne. Les interactions entre utilisateurs (posts, commentaires, votes, récompenses) constituent des indicateurs clés que nous avons exploités pour mieux comprendre les dynamiques communautaires.

Les étapes suivies dans ce projet sont les suivantes :

• Récolte automatique des éléments d’interaction (posts, commentaires) grâce à un scraper basé sur la bibliothèque PRAW
• Compréhension des besoins du métier et adaptation de notre approche
• Transformation des données pour les rendre exploitables par des algorithmes de suivi de communautés
• Utilisation et adaptation de métriques pertinentes afin de mieux caractériser ces communautés
• Construction d’une base de données structurée et interrogeable par l’utilisateur final

🧭 Contextualisation : Présentation de Reddit

Reddit est un forum social fondé en 2005, structuré autour de thématiques appelées subreddits. Chaque subreddit fonctionne comme une communauté indépendante avec ses propres règles, modérateurs et types de contenu. Les utilisateurs ("redditors") y partagent des liens, images, textes ou vidéos, qui sont ensuite soumis aux votes de la communauté.

Fonctionnalités clés :

• Votes positifs/négatifs : influencent la visibilité des contenus
• Commentaires imbriqués : favorisent des discussions hiérarchisées
• Awards : récompensent les contenus jugés de qualité
• Karma : mesure la réputation des utilisateurs

Catégories de tri des publications :

• Hot : contenus très engageants récents
• Top : contenus les plus votés sur différentes périodes
• New : dernières publications
• Rising : contenus en pleine ascension

Cette richesse fonctionnelle fait de Reddit une plateforme d’étude idéale pour observer les dynamiques d’engagement communautaire autour de sujets sensibles ou polarisants comme le climat.

🧪 La chaîne de traitement de notre solution

Afin de répondre aux besoins exprimés, nous avons adopté une méthodologie rigoureuse, articulée autour des étapes suivantes :

Compréhension du besoin métier du commanditaire

Élaboration d’un protocole d’extraction des données Reddit

Tests unitaires du protocole de scraping

Sélection des subreddits pertinents pour l’étude

Extraction des données (posts, commentaires) via l’API Reddit

Structuration des données dans une base relationnelle

Exploration et analyses descriptives des données

Analyses avancées, incluant le suivi des dynamiques communautaires

🔍 Protocole d’extraction des données Reddit

L’extraction a été réalisée via l’API officielle de Reddit, en particulier à l’aide de la bibliothèque Python PRAW (Python Reddit API Wrapper), en mode authentifié avec OAuth2.

Deux types d’accès API

a. API publique (open access)

Accès libre sans authentification
Format JSON accessible via les URLs, par exemple :
https://www.reddit.com/r/python/hot.json

b. API authentifiée (OAuth2)

Requiert une inscription en tant que 
développeur pour obtenir un client ID et un secret
Permet un accès plus large aux données (historiques de commentaires, messages privés, etc.)
Utilisée dans notre projet via la configuration OAuth2 dans PRAW

Étapes du scraping

• Création d’une application Reddit pour récupérer les identifiants
• Configuration dans PRAW des clés : client_id, client_secret, user_agent, username, password
• Définition des critères de scraping : subreddit, période, type de contenu
• Boucle de récupération avec filtrage des champs utiles : auteur, score, date, nombre de commentaires, texte, award, etc.
• Stockage des données en format brut (JSON ou CSV)
• Nettoyage et transformation vers une base SQL

🧠 Perspectives

Ce projet ouvre des perspectives intéressantes :

• Suivi de l’évolution temporelle des opinions et sujets
• Détection de pics d’activité liés à l’actualité
• Cartographie des interactions entre communautés
• Création de tableaux de bord pour les chercheurs ou décideurs publics

🛠️ Technologies utilisées

• Langage : Python 3.x
• Librairies : PRAW, Pandas, Matplotlib, Seaborn, NetworkX
• Base de données : PostgreSQL
• Outils : Jupyter Notebook, VS Code, Git, GitHub

📄 Licence

Ce projet est réalisé à des fins pédagogiques dans le cadre du cursus universitaire. Toute réutilisation du code ou des données est libre tant qu’elle respecte les droits d’auteur liés aux sources utilisées (API Reddit, bibliothèques open-source).

🤝 Remerciements

Merci à notre encadrant·e et à toute l’équipe pédagogique pour leur accompagnement, ainsi qu’à la communauté Reddit pour l’ouverture de leurs données via l’API.
