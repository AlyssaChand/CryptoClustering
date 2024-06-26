# CryptoClustering
These are the sources I used to help write my code: scikit-learn.org, docs.python.org, google, and BCS — watching our cloud recordings, using instructor activity solutions and the class activities as references.

In this assignment, the task is to use Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

Here are the steps I did to achieve this: 

#### 1. Import Required Libraries and Dependencies

![Screenshot 2024-06-20 194528](https://github.com/AlyssaChand/CryptoClustering/assets/151655013/cedc05be-7c27-4e33-809a-4486e55b1f1b)

I added OMP_NUM_THREADS environment variable to 1 to avoid memory leak warnings and used `warnings.filterwarnings` to ignore user warnings.

#### 2. Load the Data into a Pandas DataFrame

![image](https://github.com/AlyssaChand/CryptoClustering/assets/151655013/2d8c74ce-1039-4ac4-bdf8-0232d5d4886e)

#### 3. Generate Summary Statistics and Plot the DataFrame

![image](https://github.com/AlyssaChand/CryptoClustering/assets/151655013/d0056d6a-93df-444f-bece-45589d7fd99a)

![image](https://github.com/AlyssaChand/CryptoClustering/assets/151655013/4acb498a-e0c9-476e-81b0-182282d1568b)

#### 4. Prepare the Data

![image](https://github.com/AlyssaChand/CryptoClustering/assets/151655013/fb0f45fa-82c1-44fb-9fe2-cd8d2c2d4e8a)

I normalized the data using `StandardScaler()` and created the DataFrame with the scaled data.

#### 5. Find the Best Value for k Using the Original Data

![image](https://github.com/AlyssaChand/CryptoClustering/assets/151655013/7c86d73c-37e4-4c9e-9e20-1671e7155f43)

I created a list of k-values from 1 to 11, computed the inertia for each k-value, and plotted the elbow curve.

#### 6. Cluster Cryptocurrencies with K-means Using the Original Data

![image](https://github.com/AlyssaChand/CryptoClustering/assets/151655013/fea228aa-360f-4650-b2da-dc6207ec5f9c)

I initialized and fit the K-means model, predicted the clusters, and added the cluster data to the DataFrame.

![image](https://github.com/AlyssaChand/CryptoClustering/assets/151655013/d671ad4c-51aa-4e78-a8b2-d136dbd79d5d)

Then created a scatter plot of the clusters.

#### 7. Optimize Clusters with Principal Component Analysis (PCA)

![image](https://github.com/AlyssaChand/CryptoClustering/assets/151655013/85b54044-ff45-4b60-99e6-8e0b4e2568db)

I created a PCA model instance and set `n_components=3`, used `fit_transform` to reduce to three principal components, and determined the explained variance. Then I created a new DataFrame with the PCA data.

#### 8. Find the Best Value for k Using the PCA Data

![image](https://github.com/AlyssaChand/CryptoClustering/assets/151655013/a688a88d-2715-4237-8705-318e46e65c47)

I created a list of k-values from 1 to 11, computed the inertia for each k-value, and plotted the elbow curve.

#### 9. Cluster Cryptocurrencies with K-means Using the PCA Data

![image](https://github.com/AlyssaChand/CryptoClustering/assets/151655013/7176616f-a2b9-4afa-9789-d11966e4cf74)

I initialized and fit the K-means model, predicted the clusters, and added the cluster data to the DataFrame.

![image](https://github.com/AlyssaChand/CryptoClustering/assets/151655013/af846db1-094e-47dd-a0f3-3468b942a502)

Then created a scatter plot of the clusters.

#### 10. Visualize and Compare the Results

![image](https://github.com/AlyssaChand/CryptoClustering/assets/151655013/3e7c01dd-fdb2-4aa1-a538-fe1295b45268)

![image](https://github.com/AlyssaChand/CryptoClustering/assets/151655013/21d6259b-2e7b-4ff4-b8c0-f04cc3947504)


