# Telangana-PDS-Analytics-Multi-Dimensional-Shop-Performance-Clustering-and-Anomaly-Profiling

Telangana PDS Analytics: Multi-Dimensional Shop Performance Clustering and Anomaly Profiling

📌 Project Overview

The Telangana State Civil Supplies Department manages thousands of Fair Price Shops (FPS) to ensure food security across the state. Monitoring shop performance and identifying unusual transaction patterns at scale is a significant challenge.

This project leverages 7.5 years of transactional, card status, and geospatial data to perform exploratory analysis, cluster shops based on operational behavior, detect anomalies, and provide an interactive dashboard for decision-making.

The solution helps policymakers identify high-performing shops, detect potential fraud, optimize supply-chain logistics, and evaluate the impact of government initiatives such as the One Nation One Ration Card (ONORC) scheme.

🎯 Business Objectives
1. Policy Impact Analysis

Analyze how ONORC has influenced transaction behavior across urban and rural regions.

2. Fraud Prevention

Identify shops with unusual transaction-to-card ratios that may indicate:

Ghost beneficiaries
Stock diversion
Abnormal utilization patterns
3. Logistics Optimization

Detect high-portability shops requiring more frequent stock replenishment.

4. Shop Segmentation

Group FPS shops into meaningful behavioral clusters for targeted policy interventions.


🛠️ Tech Stack
Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-Learn
Streamlit
Folium
Plotly
PCA
K-Means Clustering
DBSCAN


📂 Dataset Description
Transactions Data

Contains:

Monthly transactions
Commodity distribution
Portability metrics
Transaction counts
Card Status Data

Contains:

Ration card information
Eligibility details
Card status metrics
FPS Location Data

Contains:

Shop coordinates
District information
Shop status (Active/Inactive)


📁 Project Structure
Telangana-PDS-Analytics/
│
├── data/
│   ├── transactions/
│   ├── card_status/
│   └── fps_locations/
│
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_eda.ipynb
│   ├── 03_feature_engineering.ipynb
│   └── 04_clustering.ipynb
│
├── streamlit_app/
│   ├── app.py
│   └── assets/
│
├── reports/
│   ├── cluster_profile_report.pdf
│   └── final_presentation.pdf
│
├── requirements.txt
├── README.md


🔄 Project Workflow
Step 1: Data Acquisition & Consolidation
Download yearly CSV files from Telangana Open Data Portal.
Merge transaction datasets.
Merge card status datasets.
Join datasets using:
shopNo
distCode
Create a unified master dataset.


📊 Exploratory Data Analysis (EDA)
Trend Analysis

Analyze:

Other Shop Transactions growth
Portability trends (2023–2025)
Correlation Analysis

Study relationships between:

Total Ration Cards (totalRcs)
Number of Transactions (noOfTrans)
Commodity Analysis

Visualize distributions of:

Rice
Wheat
Sugar
Other commodities

using:

Histograms
Boxplots
District-wise comparisons
Seasonality Analysis

Identify:

Festival spikes
Harvest season patterns
Monthly transaction trends


⚙️ Feature Engineering


Utilization Ratio
Utilization Ratio =
No. of Transactions / Total Ration Cards


Portability Ratio

Portability Ratio =
Other Shop Transactions / Total Transactions
Commodity Intensity

Example:

Rice-to-Wheat Ratio
Volatility Features

Calculate:

Transaction standard deviation
Commodity distribution variability
Year-over-year changes


🤖 Clustering Methodology
Data Scaling
StandardScaler()

Used before clustering to normalize all features.

Principal Component Analysis (PCA)

Reduce high-dimensional feature space into:

2D Components
3D Components

for visualization and clustering efficiency.

K-Means Clustering

Create behavioral shop segments such as:

Cluster	Description
0	Urban High-Volume Hubs
1	Rural Low-Volume Shops
2	High Portability Centers
3	Seasonal Demand Shops
4	Mixed Behavior Shops
DBSCAN

Used to identify:

Outliers
Anomalous shops
Noise points

Potential indicators of:

Fraud
Data issues
Unusual customer movement


📈 Model Evaluation
Elbow Method

Determine optimal number of clusters.

Silhouette Score

Evaluate clustering quality.

Cluster Purity

Measure alignment with:

Urban districts
Rural districts
DBSCAN Validation

Assess:

Number of outliers detected
Density-based separation


🌍 Streamlit Dashboard
Features
District Filter

Filter insights by district.

Year Filter

Analyze yearly changes.

Cluster Visualization

View cluster assignments interactively.

Geospatial Map

Color-coded FPS locations using Folium.

Shop Search Tool

Search using:

shopNo

View:

Shop performance
Cluster assignment
Cluster average comparison

📌 Key Visualizations
Transaction Growth Trends
Portability Analysis
Correlation Heatmap
Commodity Distribution
PCA Scatter Plot
K-Means Cluster Plot
DBSCAN Outlier Detection
District-wise Performance
Geospatial Cluster Map

📋 Results
Interactive Dashboard

Provides real-time monitoring of FPS performance.

Cluster Profiling Report

Defines characteristics of:

Typical shops
High-performing shops
Outlier shops
Geospatial Hotspot Analysis

Identifies concentration zones for:

High-portability shops
Anomalous shops
Operational clusters

🚀 Installation

Clone the repository:

git clone https://github.com/your-username/Telangana-PDS-Analytics.git

Navigate to project folder:

cd Telangana-PDS-Analytics

Install dependencies:

pip install -r requirements.txt

Run Streamlit application:

streamlit run app.py

📦 Requirements
pandas
numpy
matplotlib
seaborn
scikit-learn
streamlit
folium
plotly
geopandas
📊 Expected Outcomes

✔ Identification of behavioral shop segments

✔ Detection of anomalous FPS shops

✔ Evaluation of ONORC policy impact

✔ Improved logistics planning

✔ Interactive decision-support dashboard

👨‍💻 Skills Demonstrated
Data Cleaning & Integration
Exploratory Data Analysis
Feature Engineering
Time-Series Analytics
PCA
K-Means Clustering
DBSCAN
Geospatial Analytics
Dashboard Development
Data Storytelling

📚 References
Telangana Open Data Portal
Streamlit Documentation
Scikit-Learn Documentation
Folium Documentation

📜 License

This project is developed for educational and analytical purposes as part of a Data Science & Machine Learning Capstone Project.
