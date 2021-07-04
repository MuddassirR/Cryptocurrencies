# Cryptocurrencies

## Overview of Project

The purpose of this analysis was to use unsupervised machine learning to analyze a database of cryptocurrencies and classify them according to similar features. The following methods are used in this analysis:

- preprocessing the database
- reducing data dimensions using principal component analysis
- clustering cryptocurrencies using K-Means
- visualizing classification results with 2D and 3D scatter plots

## Results

After the preprocessing and cleaning phase we have 532 tradable cryptocurrencies in our dataset.

### Clustering using K-Means

![K-means graph](https://github.com/MuddassirR/Cryptocurrencies/blob/main/1.png)

The best k value appears to be 4, hence, we will use an output of 4 clusters to categorize cryptocurrencies.

### Visualizing Cryptocurrencies 

New dataset was created to scale the TotalCoinSupply and TotalCoinsMined colums from the clustered_df, adding coinName from cc_names_df and the Class column from clustered_df.

![results](https://github.com/MuddassirR/Cryptocurrencies/blob/main/2.png)

A table was created featuring tradable currencies using the HVPLOT.TABLE().
![results](https://github.com/MuddassirR/Cryptocurrencies/blob/main/3.png)

2D hvplot scatter plot with x="TotalCoinsMined_scaled", y="TotalCoinSupply_scaled", and by="Class":

Class 2 and Class 3 are the same; Classes 0 and 1 gave out three different Classes: 0, 1, 4.

![results](https://github.com/MuddassirR/Cryptocurrencies/blob/main/4.png)
![results](https://github.com/MuddassirR/Cryptocurrencies/blob/main/5.png)

Using the updated dataframe we created 3D scatter plots to visualize the 4 classes
![results](https://github.com/MuddassirR/Cryptocurrencies/blob/main/6.png)

