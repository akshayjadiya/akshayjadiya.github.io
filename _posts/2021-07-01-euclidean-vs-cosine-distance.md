---
published: false
---
How using Euclidean distance vs. Cosine similarity affects KNN results.

If you don't know or forgot how KNN works, please read this great article before moving ahead. Also, if are a bit rusty on the concept of calculating distance between two data points, read this simple article here.

Okay! Hope you're now comfortable with the basic concepts. 

The aim of this article is to - 
1. Compare 10 nearest neighbors of a query document when using Euclidean distance vs. Cosine similarity measure to calculate the distance between the two documents
2. Explore why there is a difference in the results

I will use a dataset of wikipedia documents about famous people to build the KNN model and then look at 10 nearest neighbor of Barack Obama. If you want to understand how to process the data to so that it can be fed into the KNN model, read my post on document representation. The dataset that I have used can be found here.

