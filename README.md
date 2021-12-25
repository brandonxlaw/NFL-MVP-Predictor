# Predicting the 2021 NFL MVP
This project looks to collect different statistics from an NFL season to train different logistic regression models to predict the NFL MVP for any given season.

## Introduction
I have been a football fan since elementary school (Go Ravens) and since I started my master’s degree at the University of Toronto in Human-Centred Data Science, I thought this would be a great opportunity to combine the two. The paper by **Ryan Brill** and **Ryan Wiesman** [1] guided my process and thinking throughout the project which lead me to shift my focus from determining a prediction model with the highest accuracy to understanding which factors have the biggest impact on predictions.

## Background
Most people might be familiar with the concept of the Most Valuable Player (MVP), so the National Football League (NFL) awards a player that is deemed the “most valuable” during the regular season. “Most valuable” is a very abstract term that requires an understanding of different nuances when it comes to analyzing the current season. Questions of their past season performance, team injuries, and impact to winning can play a factor when it comes to picking a winner.

The was data using the nflfastR repo [2], developed by nflverse, which provides play-by-play game log statistics for every game from 1990 to the most recent game.

## Process (WIP)
Documentation for my process is currently a WIP as the goal of my project pivoted. I will be updated my repo overtime so feel free to checkout my notebook for more details. 

## Prediction for 2021
[2021/12/25] As of Week 16 of the 2021 season, the model gives Tom Brady the highest probability to win MVP. However, current NFL discourse suggests that Aaron Rodgers is the MVP frontrunner despite having a "lesser" statistical season. This seems to be the nuances that using prediction models is missing, and a few statistics are inaccurate.
![CleanShot 2021-12-25 at 10 38 21@2x](https://user-images.githubusercontent.com/39353286/147388490-5cdcae94-f19a-41c8-8d67-42501ca13564.png)


## Sources
[1] https://ryansbrill.com/pdf/sports_analytics_articles/qbmvp.pdf
[2] https://github.com/nflverse/nflfastR-data/tree/master/data
[3] https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html
