# 💡 Data Mining Final Project: Customer Behavioral Segmentation and Profiling

## 📚 Project Overview
This project analyzes the behavior of members in a charity group. By leveraging transactional and demographic data, the goal is to segment members, profile their donation patterns, and identify target groups for marketing campaigns.

### Dataset
- **BenefactorsData.csv**: Membership information including gender, state, birth date, and how members learned about the charity.  
- **TransactionalData.csv**: Transaction details including donation type, amount, and date.

---

## 🎯 Project Objectives
1. **Segmentation**: Group members based on donation history and behavioral metrics.  
2. **Target Market Identification**: Identify members with favorable donation patterns for campaign targeting.  
3. **Member Profiling**: Explore relationships between member characteristics and donation behavior to improve engagement strategies.

---

## 🔬 Data Processing & Feature Engineering
- Filtered transactions:
  - Only `PaymentAmount > 1000`
  - Only `Membership Fee` transactions (to focus on loyal donors)  
- Aggregated transactional data to compute **R, F, M, D metrics**:
  - **R (Recency)**: Days since last donation  
  - **F (Frequency)**: Number of donations  
  - **M (Monetary)**: Total donation amount  
  - **D (Duration)**: Number of days between first and last donation  
- Categorized **R, F, M, D** into 5-level scores for clustering analysis

---

## 🤖 Modeling & Analysis
- **Clustering**: K-Means applied on R, F, M, D scores to segment members  
- **Optimal cluster number** selected using:
  - Elbow method (WSS)  
  - Silhouette score  
- **Cluster analysis**:
  - Histograms, boxplots, and radar charts  
  - Behavioral insights and profiling for each cluster  
- **Target group identification** based on cluster characteristics for marketing strategies

---

## 📊 Visualizations
- Exploratory Data Analysis (EDA) of raw and aggregated data  
- Distribution plots for R, F, M, D scores  
- Cluster visualizations: histograms, boxplots, radar plots  
- Silhouette and WSS plots to validate clustering

---

## 🛠️ Libraries Used
- `pandas`, `numpy` – data manipulation  
- `matplotlib`, `seaborn` – visualization  
- `ydata-profiling` – automated EDA  
- `scikit-learn` – clustering and metrics  
- `yellowbrick` – KElbowVisualizer for optimal cluster selection

---

## 🔗 Usage
1. Clone the repository:  
   ```bash
   git clone https://github.com/SamaneNajarian/RFMD.git


2. Place BenefactorsData.csv and TransactionalData.csv in the /data folder
Run the Jupyter notebook: Customer_Segmentation.ipynb

3. Run the Jupyter notebook: Customer_Segmentation.ipynb


## 📌 Outcomes
- Segmentation of members based on donation behavior
- Insights for targeted marketing campaigns
- Profiling for predictive engagement of potential donors

⚡ Notes

Ensure all required libraries are installed (pip install -r requirements.txt)

This notebook is designed to be run in Python 3.x environment.
