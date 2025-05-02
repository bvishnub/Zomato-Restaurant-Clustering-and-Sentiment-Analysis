# 🍽️ Zomato Restaurant Data Analytics

## Overview

This project provides an end-to-end analysis of Zomato restaurant data using machine learning and natural language processing. It includes clustering of restaurants into distinct business segments based on key features, as well as sentiment analysis of customer reviews to gauge satisfaction and perception.

The goal is to deliver actionable insights that:
- Help customers discover the best-suited restaurants based on preferences.
- Enable Zomato to optimize offerings and strategies based on customer behavior and feedback.

---

## 📊 Project Snapshots

- 📌 Clustering of restaurants by cost, rating, cuisine type, and revenue
- 💬 Sentiment analysis of customer reviews using supervised ML
- 📈 Model evaluations with business-driven conclusions

---

## 🛠️ Skills & Technologies Used

- **Python** – Programming and data analysis
- **Pandas, NumPy** – Data wrangling
- **Scikit-learn** – Clustering, model evaluation
- **NLTK, TextBlob, spaCy** – Natural language processing
- **Matplotlib, Seaborn** – Visualization
- **Jupyter Notebook** – Development environment

---

## Objective

The objective of this project is to:

- Segment restaurants into meaningful customer categories using clustering
- Analyze customer sentiments to assess satisfaction
- Provide insights that support Zomato in targeting promotions and service improvements
- Assist customers in making informed dining choices

---

## 🔍 Clustering Analysis & Insights

### ✅ Final Model Chosen: **K-Means Clustering**

K-Means was chosen based on its superior performance across evaluation metrics, cluster quality, and business relevance.

#### 🔢 Evaluation Summary

- **Silhouette Score**:  
  - `0.462` for k=3 (optimal and interpretable)  
  - `0.541` for k=15 (overfitting)

- **WCSS (Within-Cluster Sum of Squares)**:  
  - k=3: Low (best compactness and cohesion)  
  - k=5: Slightly higher, less efficient than 3

#### ❌ Other Models

- **DBSCAN**:  
  - Silhouette Score: `0.179`  
  - Struggled with noise and weak separation (6 noise points)

- **Hierarchical Clustering**:  
  - Max Silhouette Score: `0.393`  
  - Less scalable and harder to interpret

---

## 📌 Cluster Breakdown Using Key Features

### **Cluster 0: High-Cost, High-Quality Restaurants**

- **Cost**: Premium pricing  
- **Average Rating**: 3.96  
- **Revenue**: $140,861  
- **Cuisine Type**: Diverse international  
- **Audience**: Luxury-seeking customers  
- **Business Implication**: Upscale promotions, elite targeting

---

### **Cluster 1: Mid-Tier Dining**

- **Cost**: Moderate pricing  
- **Average Rating**: 3.36  
- **Revenue**: $63,398  
- **Cuisine Type**: Mix of local and international  
- **Audience**: Balanced-value seekers  
- **Business Implication**: Mid-range offers, value-based campaigns

---

### **Cluster 2: Budget-Friendly Restaurants**

- **Cost**: Very affordable  
- **Average Rating**: 3.54  
- **Revenue**: $31,607  
- **Cuisine Type**: Local and budget  
- **Audience**: Price-sensitive customers  
- **Business Implication**: Discounts, loyalty programs, high-volume strategy

---

## 💬 Sentiment Analysis Model Evaluation

### ✅ Final Model Chosen: **Logistic Regression**

Logistic Regression was selected due to its consistent, high performance and interpretability.

#### 📈 Model Performance

| Metric      | Before Tuning | After Tuning |
|-------------|----------------|--------------|
| Accuracy    | 0.8774         | 0.8759       |
| Precision   | 0.8772         | 0.8760       |
| Recall      | 0.8774         | 0.8759       |
| F1-Score    | 0.8759         | 0.8741       |

#### ❌ Other Models

- **Random Forest**:  
  - Accuracy: `0.8649`  
  - F1-Score: `0.8619`  
  - Did not outperform Logistic Regression

- **Naive Bayes**:  
  - Accuracy: `0.8338`  
  - F1-Score: `0.8224`  
  - Lowest metrics; excluded from tuning

---

### 🔍 Why Logistic Regression Was Chosen

- **Consistent performance** with minimal tuning
- **Simple and interpretable**
- **Well-suited for small and structured text datasets**
- **Reliable for binary classification of sentiments**

---

## 📈 Key Takeaways

- K-Means (k=3) provided the most useful business segmentation.
- Logistic Regression achieved the highest accuracy in identifying customer sentiment.
- The segmentation insights can directly power targeted campaigns, service design, and UX improvement.

---


