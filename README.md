Let's Regress Chess

## Abstract

Can we accurately predict the ratings of chess players based on data from one of their games? One model we found tried to predict chess rating from the player’s annotation of a game (qualitative information) [5]. We plan to find a dataset with thousands of chess games and information about them [1] and hope to accurately predict a player’s rating within a few hundred rating points.

## Introduction/Background

Chess, and specifically online chess, has been booming in popularity in the past year. In addition, chess is one of the most famous games of all time and something that our entire team enjoys. This project would allow players to evaluate their performances in specific games rather than as a whole. Previously, machine learning has been used to calculate Elo ratings for online chess players based on their overall performance in every game they have played competitively [2].

## Problem Definition

The problem that this project will consider is using a single chess match (the input) to try and estimate the rating of one or both of the players (the output). The possible inputs to our model that this dataset offers includes the start/end times, number of turns, winner, time increment, rating of both players, all moves in standard chess notation, information on the opening, and more. We want our model to output what the players’ rating is, therefore this is a prediction problem where we assume that players of a given rating will play consistently enough so that the “noise” in their performances will look roughly normal.

## Methods

A simple baseline we plan to use is a function taking into account whether or not the player won the match and in how many moves. This will not be very accurate, so to improve upon this baseline, we plan to test out a few different models such as linear regression and recurrent neural networks. Although chess is a popular machine learning topic, we have not found specific examples of using these methods to solve this problem as of now, so there could be some novelty.

## Metrics

We can use Mean Squared Error to evaluate how accurately we predict ratings relative to their labels. This should work well since chess ratings are integer values. Additionally, we plan to test the model using k-fold cross-validation.

## Potential Results

If we use moves to determine projected rating, our most basic methods would most likely minimize error by settling around the average. With better methods, we could differentiate between sequences of moves played by advanced versus beginner players, given current board position. Another potential comparison would lie in determining the most influential moves in having a high or low rating. Certain strategies might only be known by stronger players or may only be played by inexperienced ones. On the other hand, it could be found that no specific moves have a strong impact on rating, and that skill level in chess is determined by a ratio of good to bad moves.

## Conclusion

Through this project, we have begun to learn how to define a problem and plan a solution using machine learning principles. We hope to learn more about the implementation of various methods as it relates to our problem.

## Bibliography

[1] Chess Game Dataset (Lichess) https://www.kaggle.com/datasnaek/chess  
  
[2] Finding Elo https://www.kaggle.com/c/finding-elo   
  
[3] G. Di Fatta, G. M. Haworth and K. W. Regan, "Skill rating by Bayesian inference," 2009 IEEE Symposium on Computational Intelligence and Data Mining, Nashville, TN, USA, 2009, pp. 89-94, doi: 10.1109/CIDM.2009.4938634.  
  
[4] Glickman, Mark E., and Albyn C. Jones. (1999) Rating the chess rating system CHANCE-BERLIN THEN NEW YORK12 (1999). 21-28.
  
[5] Scheible, Christian and Schutze, Hinrich, “Picking the Amateur’s Mind - Predicting Chess Player Strength from Game Annotations,” The 25th International Conference on Computational Linguistics, pages 311-321, Dublin, Ireland, 2014  
