# 2019-clashroyale-analytics
Analysis of Clash Royale matchs to generate useful statistics. (Simón Sepúlveda, Matías Saavedra, Daniel Guzmán)


## Overview


In this project we work with a Clash Royale Matches dataset which contains about 700k records of matches. The main objetive is to generate useful statics about the cards and decks performance like the most winning/losing cards/decks, the most used/unused cards, etc. With this information we generate graphics and tables for a good results visualization. 

State what is the main goal of the project. State what sorts of question(s) you want to answer or what sort of system you want to build. (Questions may be non-technical -- e.g., is there a global correlation between coffee consumption and research output -- so long as they require data analysis or other technical solutions.)

## Data

We work with a Clash Royale Matches dataset which contains about 700k records of matches in <code>.json</code> format. The dataset starts at 2017 - 07 - 12. The dataset can be found in Kaggle at <url> https://www.kaggle.com/s1m0n38/clash-royale-matches-dataset </url> .

This dataset was chosen because 66.666% of the team are active players and have a lot of fun, and also frustration when lose, with Clash Royale. The 33.333% remaining are afraid of the fame and sex appeal generate the game in players.

Each tuple of the dataset looks like:

<code>{'players': {'right': {'deck': [['Mega Minion', '9'], ['Electro Wizard', '3'], ['Arrows', '11'], ['Lightning', '5'], ['Tombstone', '9'], ['The Log', '2'], ['Giant', '9'], ['Bowler', '5']], 'trophy': '4258', 'clan': 'TwoFiveOne', 'name': 'gpa raid'}, 'left': {'deck': [['Fireball', '9'], ['Archers', '12'], ['Goblins', '12'], ['Minions', '11'], ['Bomber', '12'], ['The Log', '2'], ['Barbarians', '12'], ['Royal Giant', '13']], 'trophy': '4325', 'clan': 'battusai', 'name': 'Supr4'}}, 'type': 'ladder', 'result': ['2', '0'], 'time': '2017-07-12'}</code>

Each tuplec contains:
- `players`: Can be `left` or `right` player.
  - `left/right`: Only for players reference. Contains:
    - `deck`: The player deck with their eight cards played and his level.
    - `trophy`: The player ladder trophies. 
    - `clan`: The player clan.
    - `name`: The player name.
- `type`: The match type. Can be `ladder`, `challengue` or `tournament`.
- `result`: The result of the match in the format `[left,right]`. It can be all combinations beetween `3-0` and `0-3`.
- `time`: The date when match was played.

Also we work with a dataset that contains the attributes of each cards as the Elixir cost, the card type, the card damage, etc. This dataset is used only for add useful information but not for (hacer querys). This dataset can be found it at https://www.kaggle.com/swappyk/clash-royale-dataset .


Describe the raw dataset that you considered for your project. Where did it come from? Why was it chosen? What information does it contain? What format was it in? What size was it? How many lines/records? Provide links.

## Methods

Detail the methods used during the project. Provide an overview of the techniques/technologies used, why you used them and how you used them. Refer to the source-code delivered with the project. Describe any problems you encountered.

## Results

Detail the results of the project. Different projects will have different types of results; e.g., run-times or result sizes, evaluation of the methods you're comparing, the interface of the system you've built, and/or some of the results of the data analysis you conducted.

## Conclusion

Summarise main lessons learnt. What was easy? What was difficult? What could have been done better or more efficiently?

## Appendix

You can use this for key code snippets that you don't want to clutter the main text.
