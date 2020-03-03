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




# Data Selection

### Before moving data to our unsupervised algorithms, complete the following steps for preparing data:

1. Data selection
2. Data processing
3. Data transformation

Data selection entails making good choices about which data will be used. Consider what data is available, what data is missing, and what data can be removed. For example, say we have a dataset on city weather that consists of temperature, population, latitude and longitude, date, snowfall, and income. After looking through the columns, we can readily see that population and income data don’t affect weather. We might also notice some rows are missing temperature data. In the data selection process, we would remove the population and income columns as well as any rows that don’t record temperatures.

## Data Processing

Data processing involves organizing the data by formatting, cleaning, and sampling it. In our dataset on city weather, if the date column has two different formats—mm-dd-yyyy (e.g., 01-23-1980) and month-data-year (e.g., jan-23-1980)—we would convert all dates to the same format.

## Data Transformation

Data transformation entails transforming our data into a simpler format for storage and future use, such as a CSV, spreadsheet, or database file. Once our weather data is cleaned and processed, we would export the final version of the data as a CSV file for future analysis.
