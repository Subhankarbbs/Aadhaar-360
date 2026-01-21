# 🇮🇳 Aadhaar 360 | Integrated Analytics & Forecasting System

**Aadhaar 360** is a comprehensive dual-module Streamlit application designed to streamline Aadhaar Seva Kendra (ASK) operations. It combines real-time operational analytics with a machine learning engine to forecast biometric update workloads.

![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=Streamlit&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-%233F4F75.svg?style=for-the-badge&logo=plotly&logoColor=white)

## 🚀 Key Features

The system is divided into two core modules accessible via a unified sidebar navigation:

### 1. 📊 Aadhaar 360 Dashboard (Analytics)
A role-based dashboard offering distinct views for citizens and administrators:
* **👤 Citizen Utility Mode:**
    * **Real-time Status:** Checks if centers are operational or in "Camp Mode."
    * **Wait Time Prediction:** Estimates center traffic using probabilistic modeling.
    * **Action Guide:** Recommends Online vs. Physical visits based on update type.
* **👮 Admin Command Center:**
    * **Cluster Intelligence:** Auto-categorizes districts (e.g., "High Growth," "Fraud Risk") using K-Means clustering.
    * **District Comparison:** Side-by-side performance metrics comparison.
    * **Neonatal Gap Analysis:** Identifies discrepancies between birth rates and child enrolments.
    * **Fraud Detection Radar:** Monitors specific metrics like "Ghost Village Proxy" and Operator Error Rates.

### 2. ⚙️ Biometric Model Manager (ML Ops)
An administrative interface for managing the Machine Learning lifecycle:
* **Data Ingestion & Validation:** Upload monthly CSVs with automated checks for nulls, placeholders, and numeric logic.
* **Auto-Retraining:** Merges new data with the master dataset and retrains the prediction model on the fly.
* **Forecasting Engine:** Predicts future biometric update volumes (Age 5-17 vs. 18+) for specific districts and timeframes.

## 🛠️ Tech Stack
* **Frontend:** Streamlit
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Plotly Express / Graph Objects
* **Machine Learning:** Scikit-Learn (KMeans Clustering, Regression Models)
* **Persistence:** Joblib (Model artifact saving/loading)

## 📂 Project Structure
```text
├── main.py                # Main application entry point (Integrated System)
├── data_cleanning.py      # Module for data validation and cleaning checks
├── train_model.py         # Module for ML model training and saving
├── requirements.txt       # Python dependencies
├── aadhaar_district_analytics_final_cleaned.csv  # Analytics Dataset
├── Dataset_Cleaned.csv    # Master ML Training Dataset
└── biometric_model_v1.pkl # Pre-trained Model Artifact
