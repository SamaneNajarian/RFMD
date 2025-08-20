💡 Data Mining Final Project: Customer Behavioral Segmentation and Profiling
📚 Project Overview

This project analyzes the behavior of members in a charity group. By leveraging transactional and demographic data, the goal is to segment members, profile their donation patterns, and identify target groups for marketing campaigns.

The dataset includes:

BenefactorsData.csv: Membership information including gender, state, birth date, and how members learned about the charity.

TransactionalData.csv: Transaction details including donation type, amount, and date.

🎯 Project Objectives

Segmentation: Group members based on donation history and behavioral metrics.

Target Market Identification: Identify members with favorable donation patterns for campaign targeting.

Profiling Members: Explore relationships between member characteristics and donation behavior to improve engagement strategies.

🔬 Data Processing & Feature Engineering

Filtered transactions:

Only PaymentAmount > 1000

Only Membership Fee transactions (stable income and loyal donors)

Aggregated transactional data to compute R, F, M, D metrics:

R (Recency): Days since last donation

F (Frequency): Number of donations

M (Monetary): Total donation amount

D (Duration): Number of days between first and last donation

Categorized R, F, M, D into 5-level scores for clustering analysis.

🤖 Modeling & Analysis

K-Means clustering applied on R, F, M, D scores to segment members.

Optimal cluster number selected using:

Elbow method (WSS)

Silhouette score

Clusters analyzed using:

Histograms, boxplots, and radar charts

Cluster profiles interpreted for behavioral insights

Target group identified based on cluster characteristics for marketing strategies.

📊 Visualizations

EDA of raw and aggregated data

Distribution plots for R, F, M, D scores

Cluster visualizations: histograms, boxplots, radar plots

Silhouette and WSS plots to validate clustering

🛠️ Libraries Used

pandas, numpy – data manipulation

matplotlib, seaborn – visualization

ydata-profiling – automated EDA

scikit-learn – clustering and metrics

yellowbrick – KElbowVisualizer for optimal cluster selection

🔗 Usage

Clone the repository

Place BenefactorsData.csv and TransactionalData.csv in the /data folder

Run the Jupyter notebook Customer_Segmentation.ipynb to reproduce analysis and visualizations

📌 Outcomes

Member segmentation based on donation behavior

Insights for targeted marketing campaigns

Profiling for predictive engagement of potential donors
