
# 📑INTRODUCTION

![Python](https://img.shields.io/badge/Python-100000?style=flat&logo=python&logoColor=FFFFFF&labelColor=5C5C5C&color=3776AB)
![Numpy](https://img.shields.io/badge/NumPy-100000?style=flat&logo=Numpy&logoColor=FFFFFF&labelColor=5C5C5C&color=013243)
![Pandas](https://img.shields.io/badge/Pandas-100000?style=flat&logo=Pandas&logoColor=FFFFFF&labelColor=5C5C5C&color=150458)
![MatPlotLib](https://img.shields.io/badge/MatPlotLib-100000?style=flat&logo=LOT-Polish-Airlines&logoColor=FFFFFF&labelColor=5C5C5C&color=E4637C)
![Plotly](https://img.shields.io/badge/Plotly-100000?style=flat&logo=Plotly&logoColor=FFFFFF&labelColor=5C5C5C&color=3F4F75)
![Jupyter](https://img.shields.io/badge/Jupyter-100000?style=flat&logo=Jupyter&logoColor=FFFFFF&labelColor=5C5C5C&color=F37626)
![postgresql](https://img.shields.io/badge/SQL-100000?style=flat&logo=postgresql&logoColor=FFFFFF&labelColor=5C5C5C&color=CC2927)

This project is based on the following Kaggle competition: Multi-Class Prediction of Obesity Risk https://www.kaggle.com/competitions/playground-series-s4e2/overview

The original data consist of the estimation of obesity levels in people from the countries of Mexico, Peru and Colombia, with ages between 14 and 61 and diverse eating habits and physical condition , data was collected using a web platform with a survey where anonymous users answered each question, then the information was processed obtaining 17 attributes and 2111 records.

The dataset for this competition (both train and test) was generated from a deep learning model trained on the Obesity or CVD risk dataset.

## Evaluation
Submissions are evaluated using the accuracy score.


# PROJECT 

# Exploratory Data Analysis

- There are no missing values

- All the categorical features have very few unique levels, making one-hot-encoding the best choice for this situation

- Numeric variables are continuous since they have enough distinct values

- Target Distribution:
![Target distribution](https://i.postimg.cc/3rtKkgBD/DISTRIBUTION.png)


- Age, height, weight are the most correlated features with target. Focus on them to create new features.

![Correlation](https://i.postimg.cc/y6DL4Kk3/correlation.png)

# Feature Engineering

- We create Body Mass Index variable
BMI = WEIGHT / (HEIGHT/100) **2

- Interaction between gender and alcohol
Gender_Alcohol=GENDER * ALCOHOL

- Relationship between family with overweight, Age, Caloric consumption and Number of meals per day


# BASELINE model

Baseline model using XGBClassifier giving us 88% accuracy without changing anything from the train data, nor creating new features.

# Crossvalidation
Tried using StratifiedKFold vs Train_test_split to see if there was any improvement in accuracy. 

# Final Model Combination: XGB & LGBM

In a new empty DataFrame, we create columns to store score and train/test predictions.

We define weights for each model.

Finally, our predictions get combined, we submit using weighted average.

# Hyperparameter optimization using Optuna

Two optimizations were carried out, one for each model. Using optuna to find the best parameters for each model to increase accuracy.

# Feature importance

![Displaying feature importance](https://i.postimg.cc/Bb9VhZ2F/feature-import.png)


# CONTACT
[Amalio Gómez](https://amaliogomezlopez.com/)

[![GitHub Followers](https://img.shields.io/github/followers/amaliogomezlopez?style=social)](https://github.com/amaliogomezlopez)  
[![LinkedIn Connect](https://img.shields.io/badge/LinkedIn-Connect-blue?style=social&logo=linkedin)](https://www.linkedin.com/in/amaliogomezlopez/)