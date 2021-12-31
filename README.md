# Predicting the 2021 NFL MVP
This project looks to collect different statistics from an NFL season to train different logistic regression models to predict the NFL MVP for any given season.

## Introduction
I have been a football fan since elementary school (Go Ravens!) and since I started my master’s degree at the University of Toronto in Human-Centred Data Science, I thought this would be a great opportunity to combine the two. The paper by Ryan Brill and Ryan Wiesman [1] guided my process and thinking throughout the project

## Background
Most people might be familiar with the concept of the Most Valuable Player (MVP), so the National Football League (NFL) awards a player that is deemed the “most valuable” during the regular season. “Most valuable” is a very abstract term that requires an understanding of the different nuances in any sport. Questions of their past season performance, player and/or team injuries, and their impact on winning all come into account when picking a winner.

## Data Collection
There is no definitive criteria for measuring a player for MVP, but the statistics that are arguably the most important are yards, touchdowns, team record, interceptions and EPA. The EPA can be used to add situational context which calculates the scoring probability of a play. All of these statistics were provided by the nflfastR dataset [2]. 

Collecting the statistics by player required looping through each play of every season, aggregating the totals on a per-game level then tracking the totals and the associated player. I decided to follow Ryan Brill and Ryan Wiesman’s [1] technique for ranking certain statistics, this is consistent with the development of the sport seeing as there is no minimum threshold to achieve but rather, performance is relative. For each season, a column was inserted with a “1” to indicate the winner of the MVP.

![CleanShot 2021-12-31 at 18 42 03@2x](https://user-images.githubusercontent.com/39353286/147841144-064c58bd-c767-4ef0-9777-bbd5338bd730.png)

## Training the Model

I used scikit-learn’s LogisticRegression model [3] and trained the model using all of the seasons before 2017 and tested using the seasons of 2017 and after. The table below displays the coefficient the model produced for each feature.

![CleanShot 2021-12-31 at 18 42 57@2x](https://user-images.githubusercontent.com/39353286/147841158-2b3c354a-6f89-4ccd-89a0-6215413bc004.png)

## Results
Both models scored a 71% (10/14 correct predictions), with Model 1 predicting most recent MVP winners more correctly while Model 2 predicted past MVP winners more correctly. The probability was calculated using the predict_proba function from the model, and it was inserted into the dataframe.

![CleanShot 2021-12-31 at 18 44 03@2x](https://user-images.githubusercontent.com/39353286/147841175-3e9621c6-0067-4ca9-b1b0-ea52769cd6b4.png)

## Predictions

(12/25/2021) As of Week 16 of the 2021 season, both models give Aaron Rodgers the highest probability to win MVP. Current NFL discourse suggests that Aaron Rodgers is the MVP frontrunner despite having a "lesser" statistical season than his peers.

### Model 1 Prediction

![CleanShot 2021-12-31 at 18 46 17@2x](https://user-images.githubusercontent.com/39353286/147841206-571e3547-e8c1-4132-b99f-4e9205aa94fc.png)

### Model 2 Prediction

![CleanShot 2021-12-31 at 18 46 47@2x](https://user-images.githubusercontent.com/39353286/147841211-f5ff19f1-d351-46f5-8d9b-c6c3e413e0e1.png)

## Sources
[1] https://ryansbrill.com/pdf/sports_analytics_articles/qbmvp.pdf
[2] https://github.com/nflverse/nflfastR-data/tree/master/data
[3] https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html


