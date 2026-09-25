🛍️ Mall Customer Segmentation using K-Means Clustering
Project Overview
This project implements Customer Segmentation for a mall using unsupervised machine learning techniques. By analyzing customer data, we categorize shoppers into distinct groups based on their annual income and spending behavior. This segmentation enables businesses to target specific customer groups with personalized marketing campaigns and improve customer retention strategies.

Dataset
Source: Kaggle - Customer Segmentation Tutorial in Python

Features:

CustomerID: Unique identifier for each customer

Gender: Customer gender (Male/Female)

Age: Customer age in years

Annual Income (k$): Annual income in thousands of dollars

Spending Score (1-100): Score assigned based on customer spending behavior

Technologies Used
Python 3.x

Pandas - Data manipulation

NumPy - Numerical computations

Matplotlib & Seaborn - Data visualization

Scikit-learn - Machine learning (K-Means, Silhouette Score)

Kagglehub - Dataset downloading

Google Colab - Development environment

Installation & Setup
bash
# Clone the repository
git clone https://github.com/yourusername/mall-customer-clustering.git
cd mall-customer-clustering

# Install dependencies
pip install kagglehub pandas numpy matplotlib seaborn scikit-learn
How to Run
Open Mall_costomer_clustring.ipynb in Google Colab or Jupyter Notebook

Run all cells sequentially

View results and visualizations

Methodology
1. Data Loading
python
import kagglehub
import pandas as pd

path = kagglehub.dataset_download("vjchoudhary7/customer-segmentation-tutorial-in-python")
df = pd.read_csv(f"{path}/Mall_Customers.csv")
2. Feature Selection
Focus on two key features:

Annual Income (k$)

Spending Score (1-100)

3. Elbow Method
Determines the optimal number of clusters by calculating Within-Cluster Sum of Squares (WCSS) for different K values.

4. K-Means Clustering
python
kmeans = KMeans(n_clusters=5, init='k-means++', n_init='auto', random_state=42)
y_kmeans = kmeans.fit_predict(X)
5. Model Evaluation
Using Silhouette Score to assess cluster quality.

Results
Optimal Number of Clusters
Based on the Elbow Method analysis, K=5 was identified as the optimal number of clusters.

Customer Segments
Cluster	Income Level	Spending Level	Customer Type
Cluster 1	High	High	VIP Customers
Cluster 2	Medium	Medium	Average Spenders
Cluster 3	High	Low	Conservative Spenders
Cluster 4	Low	High	Careful Spenders
Cluster 5	Low	Low	Low-Engagement Customers
Silhouette Score
text
Score: 0.553
Classification: Excellent (Score > 0.5 indicates well-separated clusters)
Visualizations
Elbow Method Plot
Shows the optimal number of clusters (K=5) where the WCSS curve bends.

Customer Segmentation Visualization
Each cluster is color-coded for easy identification

Centroids marked with yellow markers

Clear separation between different customer groups

Business Applications
Targeted Marketing Campaigns: Personalized offers for each segment

Product Recommendations: Suggest products based on cluster behavior

Customer Retention: Identify at-risk customers

Store Layout Optimization: Strategic product placement

Future Improvements
Add more features (Age, Gender) for clustering

Implement DBSCAN and Hierarchical Clustering for comparison

Build a recommendation system based on clusters

Develop a real-time customer segmentation API

License
This project is licensed under the MIT License.

Author
Name: [Your Name]

GitHub: https://github.com/yourusername

Acknowledgements
Kaggle for providing the dataset

Scikit-learn for machine learning tools

Google Colab for the development environment

