# COVID-19 Clustering and Classification Project

This repository contains the final project for the Dicoding course "Belajar Machine Learning Pemula".  
The project applies unsupervised learning followed by supervised learning to analyze COVID-19 healthcare capacity data.

The main objective of this project is to group regions based on hospital capacity and COVID-19 patient occupancy, and subsequently use the clustering results as labels for classification.

---

## Project Objectives
- Perform exploratory data analysis (EDA) on COVID-19 healthcare data
- Apply data preprocessing techniques to prepare the dataset
- Group regions using clustering to identify similar characteristics
- Evaluate the optimal number of clusters using multiple evaluation metrics
- Use clustering results as labels for a classification task
- Build and evaluate classification models

---

## Project Workflow
1. Exploratory Data Analysis (EDA)
2. Data Preprocessing
3. Clustering using K-Means
4. Cluster Evaluation
5. Cluster Interpretation
6. Classification using supervised learning algorithms
7. Model Evaluation

---

## Clustering Analysis

Clustering was performed using the K-Means algorithm based on the following features:
- beds_covid (number of COVID-19 hospital beds)
- hosp_covid (number of hospitalized COVID-19 patients)

### Determination of the Optimal Number of Clusters

The number of clusters was evaluated using:
- Elbow Method
- Silhouette Score
- Davies-Bouldin Index
- Calinski-Harabasz Index

The highest Silhouette Score of 0.5995 was obtained at n_clusters = 3.  
The lowest Davies-Bouldin Index of 0.5262 was also achieved at n_clusters = 3.  
The highest Calinski-Harabasz Index was recorded at n_clusters = 5 with a value of 9193.5967.

Although the Calinski-Harabasz Index indicates better separation at n_clusters = 5, consistent results from the Silhouette Score and Davies-Bouldin Index suggest that n_clusters = 3 is the most appropriate choice.

---

## Cluster Characteristics Analysis

### Cluster 0
Dominant region: Kedah  
Average number of COVID-19 beds: 1149.36  
Average number of hospitalized patients: 192.47  

This cluster represents regions with large hospital capacity and high patient occupancy. These areas are typically major healthcare centers or regions with a high number of COVID-19 cases. Effective resource management strategies are required to prevent hospital overcapacity and ensure optimal healthcare services.

---

### Cluster 1
Dominant region: WP Kuala Lumpur  
Average number of COVID-19 beds: 234.82  
Average number of hospitalized patients: 74.28  

This cluster consists of regions with relatively limited hospital capacity and low patient occupancy. This condition may indicate fewer COVID-19 cases or smaller healthcare facilities. Despite the lower burden, efficient referral systems are necessary to anticipate potential sudden increases in cases.

---

### Cluster 2
Dominant region: Sarawak  
Average number of COVID-19 beds: 637.24  
Average number of hospitalized patients: 152.53  

Regions in this cluster show a balanced condition between hospital capacity and patient occupancy. Healthcare services in these regions can still operate without excessive pressure, but continuous monitoring is required to maintain service stability.

---

## Clustering Conclusion

Based on the clustering analysis:
- Cluster 0 requires strong resource management to prevent overcapacity
- Cluster 1 requires improved coordination and referral systems to handle potential case surges
- Cluster 2 shows a relatively balanced condition but still requires continuous monitoring

---

## Classification Stage

The clustering results were then used as labels for the classification task. Two classification algorithms were implemented:
- K-Nearest Neighbors (KNN)
- Random Forest

### Classification Insights

The accuracy obtained from training and testing datasets shows no significant difference, indicating that the models do not experience overfitting. However, increasing the amount of data is recommended to improve the model's ability to capture more diverse patterns. Further experiments with additional classification algorithms are also suggested to enhance performance.

---

## Tools and Libraries
- Python
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Yellowbrick

---

## Notes

This project was developed as the final submission for the Dicoding course "Belajar Machine Learning Pemula" and is intended to serve as a portfolio project demonstrating the application of clustering and classification techniques in machine learning.
