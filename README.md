# Instacart Customer Behavior Prediction (Machine Learning)

## Authors

Haeyeon Jeong | Sai Rachana Kandikattu | Snehitha Tadapaneni  

---

## Project Overview

This project develops a machine learning pipeline to predict customer purchasing behavior on Instacart. By leveraging large-scale transactional and product-level data, the model identifies patterns in user activity and predicts whether a product will be reordered.

The project covers the full machine learning workflow, including data preprocessing, feature engineering, model training, and evaluation.

---

## Background & Motivation

The online grocery market is rapidly expanding, making customer behavior prediction increasingly important. As highlighted in the project presentation, online grocery sales reached significant growth levels, emphasizing the need for accurate prediction systems.

Understanding reorder behavior helps improve:
- Customer retention  
- Personalized recommendations  
- Business competitiveness  

---

## Objectives

- Predict whether a user will reorder a product  
- Build a scalable machine learning pipeline  
- Identify key features influencing purchasing behavior  
- Compare multiple models to determine the best-performing approach  

---

## Dataset

The dataset used in this project is the **Instacart Market Basket Analysis Dataset**, available on Kaggle:

https://www.kaggle.com/datasets/psparks/instacart-market-basket-analysis  

This dataset contains millions of grocery orders from Instacart and includes multiple relational tables such as:

- Orders  
- Products  
- Order-Product relationships (prior & train)  
- Aisles  
- Departments  

Due to its large size, a sampled subset was used for efficient processing and modeling.

---

## Methodology

### 1. Data Preparation
- Merged multiple datasets (6 tables)  
- Sampled large datasets for efficiency  
- Cleaned and structured relational data  

### 2. Feature Engineering
A total of **43 new features** were created, including:

- User-level features (ordering frequency, reorder ratio)  
- Product-level features (popularity, reorder counts)  
- User-product interaction features  
- Time-based features (day of week, hour of day)  

---

### 3. Modeling

The following models were trained and compared:

- Logistic Regression  
- Random Forest Classifier  
- XGBoost Classifier  

Hyperparameter tuning was performed using GridSearchCV to optimize performance

---

## Results

| Model | F1 Macro Score |
|------|--------------|
| Logistic Regression | 0.8919 |
| Random Forest | 0.9011 |
| XGBoost | **0.9022 (Best)** |

XGBoost achieved the highest performance, demonstrating strong capability in capturing complex patterns in customer behavior 

---

## Key Insights

- User reorder behavior is highly personalized and consistent  
- Product popularity strongly influences reorder probability  
- Add-to-cart position reflects purchase priority  
- Ensemble models (especially XGBoost) outperform simpler models  

---

## Environment Setup

This project is designed to run in **Google Colab**.

### Setup Steps:
- Mount Google Drive  
- Include required utility and model files ([utilities](./utilities), code.ipynb)
- Ensure dataset is uploaded to Drive  

Note: Colab is recommended for compatibility with file paths and dependencies.

---

## Technologies Used

- Python  
- Pandas, NumPy  
- Scikit-learn  
- XGBoost  
- Matplotlib, Seaborn  
- Google Colab  

---

## Project Structure
code.ipynb

Sections:

- Data Preparation
- Data Preprocessing
- Feature Engineering
- Model Training
- Hyperparameter Tuning
- Evaluation & Insights
