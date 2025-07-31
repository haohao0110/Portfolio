## Credit Card Fraud Detection ML Pipeline
A comprehensive end-to-end machine learning solution for credit card fraud detection, built with Apache Spark and advanced feature engineering techniques. This project demonstrates production-ready ML engineering practices suitable for enterprise-scale financial risk management.

## 🎯 Business Problem
Credit card fraud detection is a critical challenge in the financial industry, requiring real-time processing of massive transaction volumes while maintaining high accuracy and low false positive rates. This project addresses the need for scalable, interpretable fraud detection systems that can handle the complexity of modern payment networks.

## 🔧 Technical Stack
Big Data Processing: Apache Spark, PySpark
Machine Learning: Spark ML, scikit-learn
Programming: Python, SQL
Data Analysis: pandas, NumPy
Visualization: matplotlib, seaborn
Development: Jupyter Notebooks

## 🧠 Key Technical Insights

Feature Engineering: Created 12 new features including mathematical transformations, statistical aggregations, and interaction terms
Strong Predictors: Identified V14 as the strongest fraud predictor with -0.8057 correlation
Scalable Pipeline: Built production-ready Spark ML pipeline with feature preparation and model persistence
Algorithm Comparison: Systematic evaluation of multiple ML algorithms with hyperparameter tuning

## 📁 Project Structure
Credit_Card_Fraud_Detection_ML_Pipeline/
├── notebooks/
│   ├── 01_data_exploration.ipynb      # EDA and data understanding
│   ├── 02_feature_engineering.ipynb   # Advanced feature creation
│   └── 03_model_development.ipynb     # ML modeling and evaluation
├── data/
│   ├── raw/                          # Original dataset
│   └── processed/                    # Engineered features (Parquet)
├── models/
│   ├── best_fraud_detection_model/   # Trained model artifacts
│   └── feature_preparation_pipeline/ # Feature preprocessing pipeline
├── README.md
└── requirements.txt

## 🔍 Feature Engineering Highlights
### Created Features:

amount_log: Log-transformed transaction amounts for normal distribution
v_sum & v_mean: Statistical aggregations of PCA features
amount_zscore: Standardized amount for outlier detection
v1_v2_interaction: Cross-feature interaction terms
amount_above_p95: High-value transaction indicators
### Top Predictive Features:
V14 (r = -0.8057) - Strongest fraud predictor
V12 (r = -0.7686) - Secondary strong predictor
V4 (r = 0.7360) - Positive correlation indicator
v_mean (r = -0.5794) - Engineered feature success

## 💼 Business Impact & Applications
### Fraud Detection Capabilities:
High Accuracy: 99%+ fraud detection rate with minimal false positives
Scalable Processing: Handles 500K+ transactions efficiently
Real-time Ready: Optimized pipeline for production deployment
Interpretable Results: Clear feature importance for business understanding

### Enterprise Applications:
Payment processing fraud prevention
Risk management automation
Compliance and regulatory reporting
Customer protection systems

## ⚠️ Important Notes
While this project achieves exceptional performance metrics (99%+ AUC), it's important to note that:

Results are based on a balanced academic dataset (50/50 fraud ratio)
Real-world fraud detection typically deals with 0.1-1% fraud rates
Production systems face additional challenges like concept drift and regulatory constraints
This project serves as a technical demonstration of ML engineering capabilities
