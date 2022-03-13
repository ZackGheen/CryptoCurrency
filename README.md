# **CrytoCurrency Analysis using Unsupervised Machine Learning Algorithm**
--------------------------------------------------------------------------

## **Resources**
------------------

* **Data**: crypto_data.csv from CryptoCompare 
* **Software**: Jupyter Notebooks 6.3.0, ML libraries; scikit-learn, Plotly, hvplot, and Pandas

# **Overview**
------------------
The goal of this project was to create a Identier system for all the available CryptoCurrencies based on the data we obtained (crypto_data.csv). To do this we used scikit-learn's PCA and K-Means Libraries.

Initially the dataset was cleaned to exclude currencies that weren't currently traded and not currently mined. The final dataset has 532 different currencies.

Data for string Columns ("**Algorithm**", and "**ProofType**") was then transformed and scaled using get_dummies() and StandardScaler()

![image](https://user-images.githubusercontent.com/93295751/158043651-28ccb511-866c-40e1-bc6c-66469f45cd14.png)

Scikit's PCA library was then used to reduce the scaled data to three components:
![image](https://user-images.githubusercontent.com/93295751/158043678-8d45d27e-0d0c-45a3-a843-ca3900dce3ad.png)


Clustering using scikit's KMeans() resulted in an elbow curve which suggested four clusters:

![image](https://user-images.githubusercontent.com/93295751/158043720-f96920d0-a2ae-40de-b93e-fb46d75bd79f.png)

We combined the original dataset and the PCA dataset and set KMeans predictions as class:

![image](https://user-images.githubusercontent.com/93295751/158043750-8998ca11-cd21-4cae-9af1-a7565d6dcb3f.png)

The combined dataset was visualized using Plotly Express Scatter 3d:

![image](https://user-images.githubusercontent.com/93295751/158043771-9415387b-cd30-422c-8c76-8d081cde9cc5.png)

Transforming the 'Total Coins Mined' and 'Total Coins Supply' columns using scikit's MinMaxScaler():

![image](https://user-images.githubusercontent.com/93295751/158043787-70331aeb-3449-4177-bb9c-230ebf3c4dd3.png)

Finally, visualizing the scaled dataset to show class distribution using hvplot's scatter function:

![image](https://user-images.githubusercontent.com/93295751/158043797-f610d6d1-2a5a-4582-9de9-1c34a9a6f091.png)




