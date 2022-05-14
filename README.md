![Cover](images/cover_image.png)

# **PREDICTING MOVIES BOX OFFICE REVENUES**

## Table of Contents
1. Introduction
2. Project Objective
3. About the Data
4. Project Overview
5. Conclusion

## Introduction

Movies are one of the most universal forms of entertainment; people in every part of the world crowd into theaters waiting for the projector's light to hit the big screen. Before the COVID pandemic stroke in 2020, the global yearly revenue generated by the movie industry was estimated to be \$41.7 billion.   

The myriad of different stories to tell, the creative freedom the cinematographic art allows, is arguably what really
makes movies so attractive. Beneath this romantic view, however, we need to keep in mind that film studios are in business to make a profit; for the most part, the prospect of multimillion revenues is really what convinces stakeholders to invest in the production of a flick.

## Project Objective

In this project we use machine-learning modeling to predict movies' box office gross revenues; to reach this goal, we rely on information such as movies' budget, genres, release date and popularity. 

Along the way, through data wrangling and exploratory analysis, we unveil interesting statistical facts involving movies. By the end of the project, we have a clear idea of what are the factors that more greatly influence the revenue of a film.   

## About the Data

To train our models we use a variety of metadata about 3,000 different movies. The dataset containing this information can be downloaded from [this](https://www.kaggle.com/competitions/tmdb-box-office-prediction/data) Kaggle page and was originally obtained using the API of [The Movie Database](https://www.themoviedb.org/) (TMDB), a popular website which collects extensive data about motion pictures and TV shows.    

## Project Overview

The project is divided into 3 main steps:
- **Step 1**: *Loading the Data and Identifying the Target Variable*.
- **Step 2**: *Data Wrangling, Exploratory Analysis and Feature Engineering*: this is the most extensive part and it is functional to getting the data ready for modeling.
- **Step 3**: *Predictive Modeling and Performance Evaluation*: here we actually train the regression models and predict the movies' revenues; models' performance is evaluated using the Logarithmic Root Mean Squared Error metric (LMSE).

## Conclusion

After analyzing and visualizing the data, we found out that:
- Movies revenues show a strong correlation with movies budgets.
- *The Avengers*, *Furious 7* and *Avengers: Age of Ultron* are the three movies with highest box office gross.
- About 20% of the movies we have available are part of a collection/series. These kind of movies tend to have higher revenues.
- All movies we consider have been released between 1921 and 2017. The year with the most number of movie releases is 2013.
- September, October and December are the most popular months for movie releases; Friday is the most popular day.
- *Drama* is the most frequent genre, followed by *Comedy* and *Thriller*. The most profitable genres, however, are not necessarily the most frequent. Among the top ones we find *Adventure* and *Animation*; on the bottom there are *Foreign Movies*.

We used machine learning to predict the values of the log transformed revenues. We trained four different types of models: a Linear Regression, a Ridge Regression, a Random Forest and a Gradient Boosting regressor. After comparing their performances, we concluded that the most accurate predictions were achieved through Gradient Boosting. In this case we obtained a LMSE value of 1.4438.   

The features that had the biggest impact when making predictions were *revenue* and *popularity score*.