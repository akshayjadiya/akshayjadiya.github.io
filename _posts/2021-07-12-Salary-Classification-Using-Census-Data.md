---
published: true
---
Predict whether an individual earns less than $50k or more using US Census data

> Problem Statement - An organization wants to identify people in an available census dataset who earn more than $50k, so that it can target them via emails to solicit funds for a charity.

_Note - This project was done as a part of Udacity ML Nanodegree Program._ 

Exact details of the dataset and the analysis code can be found in [this](https://github.com/akshayjadiya/Udacity/blob/master/finding_donors.ipynb) Jupyter Notebook. The aim of this article is to provide a high level overview of the steps taken and the reasons behind them. This article complements the information present in the notebook, so you can quickly read the article for main ideas and thoroughly go through the notebook for in-depth treatment of topic.  

The project can be divided into 4 major steps - 

1. Data Exploration
2. Data Preprocessing
3. Trying different types of classification algorithms
4. Evaluating selected models and choosing the best
5. Model Tuning (Hyperparameter Optimization)
6. Looking at Feature Importance to improve model explanability
7. Feature Selection and evaluating performance

**The above steps reflect the typical workflow that is being used in a short ML project.** Let's go through each of them briefly in this article. Detailed description can be found in the Jupyter Notebook and/or hyperlinks in the article.

## Step 1 - Data Exploration
**Aim** - Familiarize yourself with the dataset i.e. **variables available (their types and distributions), missing values (types and reasons for their presence), identify target & feature variables and check for class imbalance**

**Process** - Use pandas `describe()`, `isna()` methods, make histograms to check the distribution of numerical variables, `value_counts()` method to check distribution of categorical variables

## Step 2 - Data Preprocessing
**Aim** - Many ML algorithms expect data in some format to work. Major preprocessing steps involve(not in order) - 
- Dealing with missing data (removing or imputing)
- Outlier Treatment (removing or transforming data)
- Normalizing numerical data 
- Encoding of categorical variables (Onehot , Label)
- Split data into test and train

Curious about what should be the order? **Read this amazing** [post](https://machinelearningmastery.com/data-preparation-without-data-leakage/).

**Process** - Pandas and Sklearn provide methods / classes for all of the above (check Jupyter Notebook for implementation)

## Step 3 - Trying different types of classification algorithms
**Aim** - Since sklearn has made our life so simple by providing us with implementations of all the major ML algorithms, we just have to write a few lines of code to try them out for our preprocessed data separated into features and targets. 

**Process** - Write a function to pass the preprocessed data through different algorithms (for example - Logistic Regression, Naive Bayes Classifier, SVM, AdaBoost , Random Forest etc.)

## Step 4 - Evaluating models
**Aim** - Define an evaluation metric and compare the models selected during step 3 using the same metric. **The choice of evaluation metric depends on business objective and class imbalance of the dataset**. For example - if the problem statement is classifying email as spam, it is important that there are as less false positives as possible because we don't want a non-spam important email to end up in the spam folder. Therefore, we need to prioritize improving 'precision' more than 'recall' (as a spam email landing in the normal folder is less harmful than the non spam email landing in the spam folder). 

**Read** [this](https://towardsdatascience.com/beyond-accuracy-precision-and-recall-3da06bea9f6c) article to get clarity on precision and recall metrics.

## Step 5 - Hyperparameter Optimization
**Aim** - After decided the best performing algorithm, it's time to tune hyperparameters of the associated model to get the optimal model. 

**Process** - Use sklearn's `GridSearchCV` to define values for each hyperparameter and search for the best model over all value combinations. `RandomizedSearchCV` can also be used to reduce computations.

## Setp 6 & 7 - Feature Importance and Feature Selection
**Aim** - Many times we have our model trained on hundreds of features. **It becomes hard to explain the outputs of the model** and make simple rules to broadly define characteristics of each of the segment in our model.
For example - business people would like simple definitions for people earning < $50k like unmarried people <35 years of age , natives of south east asian countries who have a college degree having occupations like craft repairs , handlers-cleaners etc. 

Therefore, we **need to see which of the features in our feature set are most important for the classification** so that we can take only those and drop others. The accuracy or any other evaluation metric most probably will take a hit but often we can find a balance. 

In sklearn's implementation of models like Random Forest, AdaBoost etc. we can directly find feature importances by calling the `feature_importance_` attribute of the trained model.
