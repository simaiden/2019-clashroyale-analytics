# 2019-clashroyale-analytics

# Analysis of Clash Royale matchs to generate useful statistics. (Simón Sepúlveda, Matías Saavedra, Daniel Guzmán)

Clash Royale is a mobile game where two players play against each other with the objective of destroying the opponent's buildings using a set of cards of 8 cards (deck). There are 3 buildings per player in a match and whoever destroys more buildings in 2 minutes wins. Destroying 3 enemy's buildings grants an immediate win. In order to play a card an "elixir" cost must be payed, which goes up to 10 elixir droplets in a match and fills over time. Over matches, a player's cards level up, up to level 13.

This project's objective is to generate statistics about the outcome of matches to give the players information about the current "meta" and results of matches, like the most used deck, the most given result, number of close matches, number of draws, etc.



## Overview

The main goal of the project is to provide useful statistics about the game to players, like the most used deck, the most winning deck, the most common outcome, etc, and represent them visually to rapidly interpret the information given. The objective of this is to provide a tool to enhance the gameplay of players.

State what is the main goal of the project. State what sorts of question(s) you want to answer or what sort of system you want to build. (Questions may be non-technical -- e.g., is there a global correlation between coffee consumption and research output -- so long as they require data analysis or other technical solutions.)

## Data

The data used consists of a 400k matches database on .JSON format available on https://www.kaggle.com/s1m0n38/clash-royale-matches-dataset.

This dataset contains info about both players name, deck (card, level), number of trophies (the higher the "better"), clan name, type of match, outcome of the match and date. It was chosen because the high number of matches available and the dates are recent, so the matches are relatively updated with the current version of it.

Describe the raw dataset that you considered for your project. Where did it come from? Why was it chosen? What information does it contain? What format was it in? What size was it? How many lines/records? Provide links.

## Methods

MongoDB is used to process the querys made because of its compatibility with the data's format and its already available by the course's faculty members for which this project is developed.

The results shown per query consist of the data transformation to have the desired result (pipeline).  

Detail the methods used during the project. Provide an overview of the techniques/technologies used, why you used them and how you used them. Refer to the source-code delivered with the project. Describe any problems you encountered.

## Results

Detail the results of the project. Different projects will have different types of results; e.g., run-times or result sizes, evaluation of the methods you're comparing, the interface of the system you've built, and/or some of the results of the data analysis you conducted.

## Conclusion

Summarise main lessons learnt. What was easy? What was difficult? What could have been done better or more efficiently?

## Appendix

You can use this for key code snippets that you don't want to clutter the main text.
