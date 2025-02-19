# CryptoClustering

For this project the goal is to use my knowledge of Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

#Prepare Data

Before being able to make my predictions, I had to use the StandardScaler() function to normalize the data from the CSV file, afterwards I created a new DatFrame and set the indec as the "coin_id".
For the PCA model, I also used the original DataFrame to perform a PCA and reduce the features into 3 principal components and a new DataFrame was created using the PCA components and "coin_id" as the index

#Find best value for K Using Scaled DataFrame & PCA DataFrame

Once the new DataFrame was created, I used the elbow method to creat a list of my k values, and an emoty list toi store inertia values, a loop was coded to compute the inertia with each possible k value, afterwards the data was plotted in an elbow curve. 
By doing the it 2 different ways it can help demosntrate which model would be ideal to find the most optimal k value. In both cases the k value was the same. In real life that may not be the case. 

#Cluster Cryptocurrencies with K-means Using the Scaled DataFrame & PCA DataFrame

For both cases, I first initialize the K-means model with the best k value which was 4. Fit the K-means model using the corresponding scaled DataFrame, and formed my predictions. Than a copy of the scaled DataFrame was made and a new cloumn was added called "predicted clusters", afterwards a scatter plot was created to view the clusters. 
By doing it the different ways, we can see how the clusters change and the amount of data placed in each cluster. 
