# Customer Segmentation Anlaysis
## Project Overview and Objective
In this data Analysis project, I get to perform customer segmentation analysis for an e-commerce company. 
I will group customers into distinct segments based on their social behavior and purchase patterns, extract some insights 
and use these insights to make informed decisions on targeted marketing strategies, improve customer satisfaction, and enhance overall business strategies.

## Data Source
The data set was downloaded from kaggle as a csv file.

## Tools 
- Pandas (Explaratory Data Analysis and other descriptive Analysis)
- Matplotlib (Data Visualization)
- Seaborn (Data Visualization)
- K-means modelling (Cluster Formation)

## Explatory Data Analysis
EDA involved exploring the data to answer key questions such as;
1. Checking for Null-values
   ```Pandas
   df.isna().sum()
   ```
2. Checking data types for each column
     ```
   df.info()
   ```
3. Finding number of unique entries for each column
  ```Pandas
   df.nunique()
  ```
## Descriptive Analysis
1. Calculating Mean, Frequency, Standard deviation and median for different columns
```Pandas
df.derscibe()
```
2. Calculating Modal Values
```Pandas
df.mode().dropna()
```
##Cluster Fromation.
1. I used the the Standardscaler to standardise my scales   
```from sklearn.preprocessing import StandardScaler
scaler = StandardScaler()
cols_to_cluster = ['Income', 'MntTotal', 'In_relationship', 'Education_status']
df_scaled = df.copy()
df_scaled[cols_to_cluster] = scaler.fit_transform(df[cols_to_cluster])
```
2. I then picked a range of values (1-10), and used the Elbow method to find the most suitable number of clusters
 ```X = df_scaled[cols_to_cluster]
inertia_list = []
for k in range(1,11):
    inertia = KMeans(n_clusters=k , n_init=10).fit(X).inertia_
    inertia_list.append(inertia)
    ```
### Visualization of the Elbow plot



3. I then formed clusters based on the recommended number of clusters, below is a visualization
 ### Clustter Visualization


## Cluster Analysis

  
