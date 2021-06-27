---
published: false
---
# Difference between bag of words and TFIDF model - An Example

We all know that using TF-IDF values instead of bag of words is a better way of representing documents. 
Using TF-IDF basically reduces the weight of very common words that don't really help us differentiate documents. Common words like 'and' , 'the' , 'very' , 'an' etc. are present in all the documents irrespective of the theme of the document.

Let's look at an example and see the difference.

I used the People Wiki dataset for the analysis which can be found [here](https://www.kaggle.com/sameersmahajan/people-wikipedia-data).

I applied the below 3 steps to the dataset to compare the performance of bag-of-words vs TFIDF - 
1.Convert the dataset's `text` column into bag-of-words / TFIDF
2.Build a KNN model using the generated features
3.Find top 10 neighbors of 'Joe Biden'

## Results with the bag-of-words model


