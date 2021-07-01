---
published: false
---
How using Euclidean distance vs. Cosine similarity affects KNN results.

If you don't know or forgot how KNN works, please read this great article before moving ahead. Also, if are a bit rusty on the concept of calculating distance between two data points, read this simple article here.

Okay! Hope you're now comfortable with the basic concepts. 

The aim of this article is to - 
1. Compare 10 nearest neighbors of a query document when using Euclidean distance vs. Cosine similarity measure to calculate the distance between the two documents
2. Explore why there is a difference in the results

I will use a dataset of wikipedia documents about famous people to build the KNN model and then look at 10 nearest neighbor of Barack Obama. If you want to understand how to process the data to so that it can be fed into the KNN model, read my post on document representation. The dataset that I have used can be found here and the analysis Jupyter notebook here.

The below picture shows first few rows of the dataset.

![data_few_rows.JPG]({{site.baseurl}}/_posts/data_few_rows.JPG)


First, let's use the Euclidean distance measure and look at the neighbors. What we can do simply is - 
1. Create a bag-of-words representation of the `text` column of the dataset using sklearn's `CountVectorizer`
2. Calculate the IDF of the document using the below formula 

![tfidf_formula.JPG]({{site.baseurl}}/_posts/tfidf_formula.JPG)

3. Multiply the bag-of-words frequencies (**T**erm**F**requency) with the **IDF** values calculated above
4. Build a KNN model with metric parameter as 'euclidean'
5. Use the model to get top 10 neighbors of Barack Obama

First 3 steps can be done as shown below - 

![make_tf_idf.JPG]({{site.baseurl}}/_posts/make_tf_idf.JPG)

The top 10 results that we get are - 

![euc_results.JPG]({{site.baseurl}}/_posts/euc_results.JPG)
