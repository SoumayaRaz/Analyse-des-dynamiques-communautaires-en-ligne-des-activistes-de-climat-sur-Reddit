# Analyse-des-dynamiques-communautaires-en-ligne-des-activistes-de-climat-sur-Reddit
🌍 Analyse des Dynamiques de Communautés sur Reddit : Climat vs Négationnisme
📘 Introduction
Ce projet s'inscrit dans le cadre du Projet Complexe (ProCom) de troisième année ou de deuxième année de Master. Il explore les dynamiques d’interaction entre deux types de communautés sur Reddit :

Celles militant pour la lutte contre le changement climatique

Celles adoptant une posture négationniste vis-à-vis de ce phénomène

❓ Problématique
Existe-t-il des événements sociétaux particuliers susceptibles de stimuler une augmentation des interactions au sein de ces communautés sur Reddit ?

Nous avons cherché à répondre à cette question à travers une exploration systématique des données issues de Reddit.

🎯 Objectifs
Comprendre la dynamique des échanges entre communautés pro-climat et climato-sceptiques.

Utiliser Reddit comme terrain d’étude pour analyser l’évolution et l’intensité des interactions autour de cette controverse.

Identifier les déclencheurs d’activités communautaires : pics de posts, de commentaires, de récompenses, etc.

🧠 Méthodologie
Voici la chaîne de traitement de notre solution, de la compréhension du besoin métier à l'analyse des résultats :

Compréhension du besoin métier

Création et test d’un protocole d’extraction de données

Choix des communautés pertinentes sur Reddit

Scraping des données via API Reddit (OAuth2 + PRAW)

Organisation d’une base de données relationnelle

Exploration statistique et visualisation

Analyses avancées sur les publications et commentaires

🛠️ Extraction des Données Reddit
L'extraction a été réalisée à l'aide de PRAW, une bibliothèque Python pour interagir avec l’API Reddit. Voici un aperçu des méthodes utilisées :

a. Méthode API Reddit avec OAuth2
Authentification sécurisée grâce à des clés d'application.

Collecte automatisée de :

Publications (posts)

Commentaires

Awards et scores de karma

Ciblage de subreddits spécifiques liés au climat et au scepticisme environnemental.

b. Mode d’emploi rapide (via PRAW)
python
Copier le code
import praw

reddit = praw.Reddit(
    client_id="YOUR_CLIENT_ID",
    client_secret="YOUR_CLIENT_SECRET",
    user_agent="ClimateChangeAnalysis by /u/YOUR_USERNAME"
)

subreddit = reddit.subreddit("climate")
for post in subreddit.hot(limit=10):
    print(post.title)
🗃️ Structure des Données
Reddit fonctionne selon une hiérarchie claire :

Subreddit → Collection de publications sur un thème

Post → Point d’entrée d’une discussion

Commentaires → Hiérarchisés en fils de discussions imbriqués

Votes et awards → Mécanismes de réputation pour trier les contenus

Nous avons structuré notre base pour refléter cette organisation :
Subreddits → Posts → Commentaires + Votes + Awards

📊 Analyses Réalisées
Analyse temporelle des pics d’activité

Visualisation des échanges : volumes de commentaires, publications, karma

Comparaison entre les dynamiques des deux camps (pro-climat vs sceptiques)

Identification de topics ou événements déclencheurs de débats

📌 Présentation de Reddit (pour contextualisation)
Reddit est une plateforme fondée en 2005, structurée autour de communautés thématiques appelées subreddits. Chaque contenu est soumis au vote de la communauté, ce qui détermine sa visibilité. Reddit se distingue par :

Son auto-modération communautaire

Sa capacité à faire émerger les tendances populaires

Ses catégories de contenu : Hot, Top, New, Rising

Ce système est au cœur de notre analyse : nous l'avons utilisé pour détecter des changements soudains dans la dynamique de publication et d’engagement.

🔧 Technologies Utilisées
Python 3.10+

PRAW (Python Reddit API Wrapper)

Pandas, NumPy, Matplotlib, Seaborn

SQLite / PostgreSQL (pour stockage des données)

Jupyter Notebooks

📜 Licence
Ce projet est distribué sous licence MIT.

🤝 Contributeurs
RAZZOUK Soumaya
MAHMOUDI Sarra
DERBEL Yassine
ZHENG Ruxin


