---
published: true
---
Predict whether an individual earns less than $50k or more using US Census data

Problem Statement - An organization wants to identify people in an available census dataset who earn more than $50k, so that it can target them via emails to solicit funds for a charity.

Note - This project was done as a part of Udacity ML Nanodegree Program.

Exact details of the dataset and the analysis code can be found in [this](https://github.com/akshayjadiya/Udacity/blob/master/finding_donors.ipynb) Jupyter Notebook. The aim of this article is to provide a high level overview of the steps taken and the reasons behind them.

The project can be divided into 4 major steps - 

1. Data Exploration
2. Data Preprocessing
3. Trying different types of classification algorithms
4. Evaluating selected models and choosing the best
5. Model Tuning (Hyperparameter Optimization)
6. Looking at Feature Importance to improve model explanability
7. Feature Selection and evaluating performance

The above steps reflect the typical workflow that is being used in a short ML project. Let's go through each of them briefly in this article. Detailed description can be found in the Jupyter Notebook and/or hyperlinks in the article.

## Step 1 - Data Exploration
Aim - Familiarize yourself with the dataset i.e. variables available (their types and distributions), missing values (types and reasons for their presence), identify target & feature variables and check for class imbalance 

Process - Use pandas `describe()`, `isna()` methods, make histograms to check the distribution of numerical variables, `value_counts()` method to check distribution of categorical variables

## Step 2 - Data Preprocessing
Aim -
