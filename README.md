# Cryptocurrencies

#### In supervised learning, the input data already has a paired outcome, which is plugged in to train the model to predict outcomes in new datasets. For example, we want to build a model that, when given unfamiliar data, can accurately predict the outcomes.

### In unsupervised learning, there are two key differences from the above approach:

    - There are no paired inputs and outcomes.
    - The model uses a whole dataset as input.

### Unsupervised learning is used in one of the following two ways:

    - Transform the data to create an intuitive representation for analysis or to use in another machine learning model; or
    - Cluster or determine patterns in a grouping of data, rather than to predict a classification.

## Types of Unsupervised Learning: Transformations and Clustering

### Transformations
We use transformations when we need to take raw data and make it easier to understand. Transformations also can help prepare data so that it can be used for other machine learning algorithms. 
For example, if you had cable TV viewer data, it might contain location, viewing duration, and viewer churn and retention during commercials and after programs ended. 
Transformations can reduce the dimensional representation, which simply means we’ll be decreasing the number of features used for the model or analysis. After doing so, the data can either be processed for use in other algorithms or narrowed down so it can be viewed in 2D.

### Clustering Algorithms
We use clustering algorithms to group similar objects into clusters. For example, if a cable service wants to group those with similar viewing habits, we would use a clustering algorithm.

## Objectives

#### The goals for this challenge are for you to:

    - Prepare the data for dimensions reduction with PCA and clustering using K-means.
    - Reduce data dimensions using PCA algorithms from sklearn.
    - Predict clusters using cryptocurrencies data using the K-means algorithm form sklearn.
    - Create some plots and data tables to present your results.

# Data Selection

### Before moving data to our unsupervised algorithms, complete the following steps for preparing data:

1. Data selection
2. Data processing
3. Data transformation

Data selection entails making good choices about which data will be used. Consider what data is available, what data is missing, and what data can be removed. For example, say we have a dataset on city weather that consists of temperature, population, latitude and longitude, date, snowfall, and income. After looking through the columns, we can readily see that population and income data don’t affect weather. We might also notice some rows are missing temperature data. In the data selection process, we would remove the population and income columns as well as any rows that don’t record temperatures.

### Data Processing

Data processing involves organizing the data by formatting, cleaning, and sampling it. In our dataset on city weather, if the date column has two different formats—mm-dd-yyyy (e.g., 01-23-1980) and month-data-year (e.g., jan-23-1980)—we would convert all dates to the same format.

### Data Transformation

Data transformation entails transforming our data into a simpler format for storage and future use, such as a CSV, spreadsheet, or database file. Once our weather data is cleaned and processed, we would export the final version of the data as a CSV file for future analysis.

## Reducing Data Dimensions Using PCA

Use the PCA algorithm from sklearn (Links to an external site.) to reduce the dimensions of the X DataFrame down to three principal components.

Once you have reduced the data dimensions, create a DataFrame named “pcs_df” that includes the following columns: PC 1, PC 2, and PC 3. Use the crypto_df.index as the index for this new DataFrame.

### Clustering Cryptocurrencies Using K-means

Use the KMeans algorithm from sklearn to cluster the cryptocurrencies using the PCA data.

### Complete the following tasks:

    - Create an elbow curve to find the best value for K, and use the pcs_df DataFrame.
    - Once you define the best value for K, run the K-means algorithm to predict the K clusters for the cryptocurrencies’ data. Use the pcs_df to run the K-means algorithm.
    - Create a new DataFrame named “clustered_df,” that includes the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class. You should maintain the index of the crypto_df DataFrames as is shown below:

    The DataFrame shows nine columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC1, PC 2, PC 3, CoinName, and Class. It contains ten rows with the following headings: 42, 404, 1337, BTC, ETH, LTC, DASH, XMR, ETC, and ZEC.

## Create data visualizations to present the final results.

### Complete the following tasks:

    1. Create a 3D scatter plot using Plotly Express to plot the clusters using the clustered_df DataFrame. You should include the following parameters on the plot: hover_name="CoinName" and hover_data=["Algorithm"] to show this additional info on each data point.
    2. Use hvplot.table to create a data table with all the current tradable cryptocurrencies. The table should have the following columns: CoinName, Algorithm, ProofType, TotalCoinSupply, TotalCoinsMined, and Class.
    3. Create a scatter plot using hvplot.scatter to present the clustered data about cryptocurrencies having x="TotalCoinsMined" and y="TotalCoinSupply" to contrast the number of available coins versus the total number of mined coins. Use the hover_cols=["CoinName"] parameter to include the cryptocurrency name on each data point.

