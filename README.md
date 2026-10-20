**Pima Indians Diabetes — Clustering Analysis**



**Overview**



This project explores unsupervised learning techniques on the Pima Indians Diabetes dataset. It includes exploratory data analysis, data preprocessing, dimensionality reduction, and the implementation and evaluation of multiple clustering algorithms.



The project was developed as part of a Data Mining course assignment.



**Dataset**



The dataset contains 768 records, eight input features, and one target variable (`Outcome`).



\- \*\*Features:\*\* Pregnancies, Glucose, BloodPressure, SkinThickness, Insulin, BMI, DiabetesPedigreeFunction, Age

\- \*\*Target:\*\* `Outcome` (diabetes status)

\- \*\*Format:\*\* CSV



The `Outcome` variable is used to compare clustering results with the known labels; it is not included among the clustering input features.



\*\*Dataset source:\*\* \[Pima Indians Diabetes Dataset — UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Pima+Indians+Diabetes)



**Project Structure**



```text

.

├── clustering\_analysis.ipynb

├── exploratory\_data\_analysis.ipynb

├── diabetes.csv

├── README.md

└── .gitignore

```



**Methodology**



 *1. Exploratory Data Analysis*

\- Dataset structure, data types, and descriptive statistics

\- Class distribution and feature distributions

\- Correlation analysis

\- Checks for missing, zero, and duplicate values

\- Visualization of diabetes-related patterns



 *2. Data Preprocessing*

\- Treatment of zero values in selected medical measurements

\- Imputation using mean or median values

\- Outlier inspection and preprocessing

\- Feature standardization using `StandardScaler`



 *3. Dimensionality Reduction*

\- Principal Component Analysis (PCA)

\- Visualization and analysis in the reduced feature space



 *4. Clustering Algorithms*

The project explores and compares the following methods:



\- \*\*Hierarchical Agglomerative Clustering:\*\* Single, Complete, Average, Ward, and Centroid linkage

\- \*\*DBSCAN:\*\* Density-based clustering and parameter exploration

\- \*\*Self-Organizing Map (SOM):\*\* Neural-network-based representation and clustering

\- \*\*K-Means:\*\* Centroid-based clustering

\- \*\*Fuzzy C-Means:\*\* Soft clustering with membership degrees

\- \*\*Particle Swarm Optimization (PSO):\*\* Optimization of cluster centroids



 *5. Evaluation*

Clustering performance is examined using internal evaluation metrics, including:



\- Silhouette Score

\- Davies–Bouldin Index

\- Calinski–Harabasz Index



Where applicable, cluster assignments are also compared with the known `Outcome` labels using external evaluation metrics.



 *Technologies*



\- Python

\- Pandas and NumPy

\- Matplotlib and Seaborn

\- Scikit-learn

\- SciPy

\- MiniSom

\- scikit-fuzzy



 *Installation*



Install the required libraries:



```bash

pip install pandas numpy matplotlib seaborn scikit-learn scipy minisom scikit-fuzzy

```



**How to Run**



1\. Clone or download this repository.

2\. Ensure `diabetes.csv` is in the same directory as the notebooks.

3\. Open the notebooks in Jupyter Notebook or JupyterLab.

4\. Run `exploratory\_data\_analysis.ipynb` to explore the dataset.

5\. Run `clustering\_analysis.ipynb` to execute preprocessing, dimensionality reduction, clustering, and evaluation.



The notebooks load the dataset using a relative path:



```python

pd.read\_csv("diabetes.csv")

```



**Notes and Limitations**



\- Clustering is an unsupervised task; cluster labels do not inherently correspond to diabetes classes.

\- The `Outcome` variable is retained for evaluation and comparison, not as a clustering feature.

\- Results depend on preprocessing choices, dimensionality reduction, and algorithm parameters.

\- DBSCAN may identify noise points or produce a single cluster for some parameter settings; such results should be interpreted carefully.



*Purpose*



This project demonstrates the application and comparison of unsupervised learning techniques, dimensionality reduction, and clustering evaluation on a real-world medical dataset.



\*\*Author:\*\* Tahereh Hematiyan

