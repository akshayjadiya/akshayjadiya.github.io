---
published: true
---
Design of Experiment based approach for Hyperparameter Tuning

I took the **Design of Experiments** class in the first semester of my MS Data Science Program at Georgia Tech. The course is very different than other Machine Learning classes that I took because of two main reasons – 

1.	The focus of the course was **teaching applications of statistics** (primarily ANOVA and Regression theory) in determining whether independent variables have significant effects on the response variable. This is a slightly different viewpoint than the one adopted during a modeling class (which focuses more on making predictions)

2.	In modeling classes, we do not care about _how_ we got the data, we just _assume there is data_ and we have to create a model. This class actually focused on **how to conduct the experiment, collect the data and then analyze the relationships between inputs and outputs.**

The fundamental thing I learned in that course was – How to **reduce the number of runs of an experiment** so that we have enough data to comment on the relationship between independent and dependent variables. 

Although there are many concepts that I learned during the class that is relevant to building ML models, in this post, I would like to expand upon the project that I did with one of my colleagues. 

Getting straight to the point, our project proposed a **new method to perform Hyperparameter Tuning**. More details about the experiments that we performed can be found on this GitHub repo. There is a PDF file as well that explains each and every concept in great detail and that can also be found on the same repo. To summarise the methodology that we adopted look at the below pictures. 


