# Lichess-Dataset-Exploration-Visualisation

Introduction et description du projet :

Ce projet a pour objectif d’analyser un dataset réel de parties d’échecs issues de la plateforme Lichess.org, disponible sur Kaggle. 
L’idée est de mettre en pratique des outils couramment utilisés en science des données avec Python (notamment pandas, numpy et matplotlib) afin de manipuler, explorer et visualiser un large volume de données.
L’analyse s’intéresse en particulier à la relation entre l’écart d’Elo entre deux joueurs et la probabilité de victoire du joueur le mieux classé. D’autres aspects liés aux parties, tels que l’avantage des Blancs, seront également étudiés.

Ce travail permet ainsi de développer des compétences en analyse de données, tout en apportant des conclusions pertinentes sur le comportement réel du système Elo.

Source du datatset et autres informations :
https://www.kaggle.com/datasets/datasnaek/chess

Objectifs personnels :
- se familiariser avec l'étude de large jeu de données et des modules python communément utilisés en science des données (en particulier pandas, numpy et matplotlib),
- appliquer les savoirs acquis en cours (probabilités, programmation python).

Objectifs du projet :
- permettre de visualiser de façon claire et pertinente les données obtenues,
- analyser la relation entre l’écart d’Elo entre deux joueurs et la probabilité de victoire du joueur le mieux classé

Outils utilisés :
Python3 (librairies : Numpy, pandas,matplotlib)
Jupyter Notebook

Résultats attendus :
- Visualisation claire de la distribution des classements Elo,
- Étude l’influence de l’écart d’Elo sur le résultat des parties,
- Mise en évidence (ou non) d’un avantage mesurable pour les Blancs.

Conclusions : 

- Le jeu de données en quelques chiffres :

  Nbr total de parties :  20058

  Nbr total de joueurs différents : 15635
  
  Moyenne du classement élo des joueurs : 1592.73
  
  Médiane du classement élo des joueurs : 1564.0
  
  Classement élo maximum : 2723
  
  Classement élo minimum : 784
  
Les questions soulevées par l'analyse exploratoire :

- Pourquoi autant de joueurs aux alentours de 1500 élo ?
  Effectivement on remarque un grand nombre entre 1400 et 1600 élos ; ils représentent à eux seuls 58.15 % des joueurs et plus de 8% des joueurs à exactement 1500. Cette surreprésentation s'explique par de nombreux facteurs :
  - Glicko 2 est le système de classement sur lequel se base Lichess et dans ce système chaque nouveau joueur commence avec un élo égal à 1500,
  - La majorité des joueurs sont moyens ou peu actifs,
  - La distribution naturelle centrée sur la moyenne (rappel une gaussienne centrée),
  - Le système de rating maintient un équilibre statistique,
  
- L'avantage des blancs étant largement démontré en général, l'est-il réellement dans notre jeu de données ?

  Nbr victoires blancs : 10001 (49.9%)

  Nbr victoires noirs : 9107 (45.4%)
  
  Nbr matchs nuls : 950 (4.7%)
  
  -> Soit 49.9% de victoires blanches contre 45.4% de victoires noires, les blancs ont bien un net avantage par rapport aux blancs dans notre étude.

- Le système élo, appliqué à notre jeu de données, avantage-t-il bien les joueurs d'un élo supérieur ? Le fait-il de manière cohérente (application mathématique) ?
  t
- Les échecs, un jeu frustrant ?
  t
  
Ouvertures :


Sources :
https://lichess.org/page/rating-systems
https://fr.wikipedia.org/wiki/Classement_Elo

Licence :
Projet académique réalisé à des fins d’apprentissage.  
Les données appartiennent à leurs auteurs respectifs (Lichess.org, Kaggle).
