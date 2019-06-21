# 2019-clashroyale-analytics
Analysis of Clash Royale matchs to generate useful statistics. (Simón Sepúlveda, Matías Saavedra, Daniel Guzmán)


## Overview


In this project we work with a Clash Royale Matches dataset which contains about 700k records of matches. The main objetive is to generate useful statics about the cards and decks performance like the most winning/losing cards/decks, the most used/unused cards, etc. With this information we generate graphics and tables for a good results visualization. 


## Data

We work with a Clash Royale Matches dataset which contains about 700k records of matches in <code>.json</code> format. The dataset starts at 2017 - 07 - 12. The dataset can be found in Kaggle at <url> https://www.kaggle.com/s1m0n38/clash-royale-matches-dataset </url> .

This dataset was chosen because 66.666% of the team are active players and have a lot of fun and also frustration when losing with Clash Royale. The 33.333% remaining are afraid of the fame and sex appeal the game generates on players.

Each tuple of the dataset looks like:

<code>{'players': {'right': {'deck': [['Mega Minion', '9'], ['Electro Wizard', '3'], ['Arrows', '11'], ['Lightning', '5'], ['Tombstone', '9'], ['The Log', '2'], ['Giant', '9'], ['Bowler', '5']], 'trophy': '4258', 'clan': 'TwoFiveOne', 'name': 'gpa raid'}, 'left': {'deck': [['Fireball', '9'], ['Archers', '12'], ['Goblins', '12'], ['Minions', '11'], ['Bomber', '12'], ['The Log', '2'], ['Barbarians', '12'], ['Royal Giant', '13']], 'trophy': '4325', 'clan': 'battusai', 'name': 'Supr4'}}, 'type': 'ladder', 'result': ['2', '0'], 'time': '2017-07-12'}</code>

Each tuple contains:
- `players`: Can be `left` or `right` player.
  - `left/right`: Only for players reference. Contains:
    - `deck`: The player deck with their eight cards played and their level.
    - `trophy`: The player ladder trophies. 
    - `clan`: The player clan.
    - `name`: The player name.
- `type`: The match type. Can be `ladder`, `challenge` or `tournament`.
- `result`: The result of the match in the format `[left,right]`. It can be all combinations beetween `3-0` and `0-3`.
- `time`: The date when match was played.

Also we work with a dataset that contains the attributes of each cards as the Elixir cost, the card type, the card damage, etc. This dataset is used only for add useful information but not for querying. This dataset can be found it at <url>https://www.kaggle.com/swappyk/clash-royale-dataset</url> .


## Methods

MongoDB is used to process the queries made because of its compatibility with the data's format and its already available by the course's faculty members for which this project is developed. 

For each desired statistic a pipeline is designed, which is presented on `Results` with a description of the resulting table (collection).

Python is used to make the visual representation of the data, because of its ease of use for the team and its variety of methods to further process the data (only for ordering, no further data is collected here). For this,we use the <code>matplotlib</code> library  for plotting, <code>pandas</code> and <code>json</code> for loading the exported results and <code>numpy</code> for data processing. This last library is needed because the results are not always congruent between queries: for example on certain matches or kind of cards not all levels are on the databse because of its rarity, so we need to complete or truncate certain results.


## Results

We show some pipelines of the <code>MongoDB</code>'s queries made along with some interesting graphics made on <code>Python</code> with the collections obtained. The whole set of queries can be found on the repository on the `queries.txt` file.

Players with the most played games on ladder type matches by descending order:
![alt text](https://github.com/simaiden/2019-clashroyale-analytics/blob/master/figuras/MasPartidas.png)

Decks played by a particular player
![alt text](https://github.com/simaiden/2019-clashroyale-analytics/blob/master/figuras/MazosJugador.png)


Results obtained by a player playing with a specific deck
![alt text](https://github.com/simaiden/2019-clashroyale-analytics/blob/master/figuras/ResultadosJugador.png)


Times a card was played on a won match grouped by level
![alt text](https://github.com/simaiden/2019-clashroyale-analytics/blob/master/figuras/WinPorCarta.png)

## Conclusion



Summarise main lessons learnt. What was easy? What was difficult? What could have been done better or more efficiently?

## Appendix

You can use this for key code snippets that you don't want to clutter the main text.
