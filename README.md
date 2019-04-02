# AusOpen2019
Basic ML modelling for Australian Open 2019


The aim of this project is to create a model aiming to predict the winner between two players of a tennis match for the 2019 Australian Open.
One of the main ideas here is to consider the performance differential between two players to help predict the most likely winner.

What I found was that it is possible to make a very accurate model using post-game match statistics. 
Furthermore, for both men's and women's tournaments, the RandomForestClassifier models ranked the model features very similarly.
This indicated that the model features is not biased between men's and women's tournaments. 

However, to get a prediction from the model of a future match between player 1 and player 2, requires estimation of their expected performance.
Obtaining a player's expected performance from their past matches is indeed possible, however, estimating this accurately is difficult.

In this repository, I used a simple approach to estimate a players performance based on their past. 
In particular, I used a simple weighted moving average (exponentially weighted moving average to be specific).
For future considerations, I will incorporate additional features which take into account common opponents between both players
and also a feature describing the past "head-to-head" win-rate between players 1 and 2.
Such features would help estimate a players future performance based on what type of players they played in the past.

