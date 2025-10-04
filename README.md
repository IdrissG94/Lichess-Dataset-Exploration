
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

  Nbr victoires blancs : 10476 (52.22 %)

  Nbr victoires noirs : 9582 (47.78 %)
  
  ->  52.22 % de victoires blanches contre 47.78% de victoires noires, les blancs ont bien un net avantage par rapport aux blancs dans notre étude. Cela entre en adéquation avec des études plus sérieuses sur l'avantage des blancs aux échecs qui estiment les chances de victoires des blancs entre  52-55 % sur Lichess.

- Le système Elo est-il appliqué de manière cohérente dans les données ?

  En utilsant la formule mathématiques liée au classement élo : P(Victoire)=1/(10^(-ΔElo/400​) , où ΔElo = Elofavori​−Eloadversaire​ et désigne la différence d'élo entre deux joueurs.

  
|   ΔElo    | Victoires du mieux classé attendues | Observations       |
| --------- | ----------------------------------- | ------------------ |
| 0–50      | ≈ 52–55 %                           | 51.5 %             |
| 50–100    | ≈ 55–60 %                           | 58.3 %             |
| 100–200   | ≈ 60–70 %                           | 65.7 %             | 

En général, oui le système élo est appliqué de manière cohérente dans nos données.

- Les échecs, un jeu frustrant ? Etude via les raisons de fin de partie :
  
  Abandon : 55.6 %
  
  Echec et mat : 31.5 %
  
  Temps : 8.4 %
  
  Nul : 4.5 %

  Ces chiffres montrent que la majorité des joueurs ne jouent pas jusqu’au bout de la partie. Plus d’une partie sur deux se termine par abandon, ce qui peut témoigner d’une forme de découragement, de frustration ou simplement d’un réalisme stratégique dès qu’une position est jugée perdante.

  À l’inverse, seules 31,5 % des parties vont jusqu’à l’échec et mat, ce qui rappelle qu’en pratique, le mat "sur l’échiquier" reste minoritaire malgré le fait que tout le jeu tourne autour justement de cette menace.

  Les fins au temps (8,4 %) soulignent l’impact du contrôle de cadence et du jeu rapide : la pression chronométrique joue un rôle non négligeable, notamment dans les parties en ligne.

  Enfin, les parties nulles (4,5 %) restent marginales dans ce dataset, ce qui laisse penser que l'équilibre parfait est rare à ces niveaux Elo, ou que les joueurs préfèrent tenter leur chance plutôt que forcer une nulle théorique.

  Ces tendances peuvent être interprétées sous l’angle psychologique : entre résignation, erreur sous pression et absence de finalisation jusqu’au mat, les échecs apparaissent non seulement comme un jeu de stratégie, mais aussi comme un jeu de gestion émotionnelle.


Ouvertures :


Sources :
https://lichess.org/page/rating-systems
https://fr.wikipedia.org/wiki/Classement_Elo

Licence :
Projet académique réalisé à des fins d’apprentissage.  
Les données appartiennent à leurs auteurs respectifs (Lichess.org, Kaggle).
