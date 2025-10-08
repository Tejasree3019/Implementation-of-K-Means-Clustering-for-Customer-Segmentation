# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1.Import the necessary packages using import statement.

2.Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().

Import KMeans and use for loop to cluster the data.

4.Predict the cluster and plot data graphs.

5.Print the outputs and end the program

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Tejasree.K
RegisterNumber:  212224240168



import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv("/content/Mall_Customers.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.cluster import KMeans
wcss=[]
for i in range(1,11):
  kmeans=KMeans(n_clusters=i,init="k-means++")
  kmeans.fit(data.iloc[:,3:])
  wcss.append(kmeans.inertia_)
plt.plot(range(1,11),wcss)
plt.xlabel("No_of_Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")
km=KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])
y_pred=km.predict(data.iloc[:,3:])
y_pred
data["cluster"]=y_pred
df0=data[data["cluster"]==0]
df1=data[data["cluster"]==1]
df2=data[data["cluster"]==2]
df3=data[data["cluster"]==3]
df4=data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")
plt.legend()
plt.title("Customer Segment")

*/
```

## Output:

<img width="1143" height="319" alt="image" src="https://github.com/user-attachments/assets/82a8038d-89e5-4866-b197-f19a0af78116" />

<img width="474" height="348" alt="image" src="https://github.com/user-attachments/assets/4ff7b345-1a32-4253-9037-acec72cc3c20" />
<img width="755" height="313" alt="image" src="https://github.com/user-attachments/assets/e2b4af35-0060-46dd-9ae1-72d354511ac7" />

<img width="1182" height="778" alt="image" src="https://github.com/user-attachments/assets/0f8f3baa-23e0-42be-b8f8-5fa1f3bb58d9" />
<img width="468" height="128" alt="image" src="https://github.com/user-attachments/assets/c45f893b-9054-450b-9822-e91b90bc1aa7" />

<img width="1124" height="283" alt="image" src="https://github.com/user-attachments/assets/a7e2a84d-2d4b-4b0f-b4b7-075c0c4f8fee" />
<img width="981" height="726" alt="image" src="https://github.com/user-attachments/assets/8d7e8a99-f920-4375-a4be-15b679797a3e" />

## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
