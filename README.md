# Product-Recommendation-System

## 📌 Overview
The **Product Recommendation System** is a machine learning project designed to recommend relevant products to users based on their historical interactions. Because real-world user-item interactions are highly sparse, this project utilizes **Singular Value Decomposition (SVD)** for dimensionality reduction and **K-Means Clustering** to group similar users and products. 

The project includes a robust exploratory data analysis (EDA) pipeline and an interactive web application built with **Streamlit** that allows real-time two-way recommendations:
1. **User → Product:** Recommending the best products for a specific user.
2. **Product → User:** Identifying the best target audience (users) for a specific product.

---

## 📊 Dataset Information
The system is trained on an Amazon product ratings dataset (`rating_short.csv`).
* **Total Interactions:** 78,245
* **Unique Users:** 76,430
* **Unique Products:** 40,228
* **Features:** `userid`, `productid`, `rating` (1-5 scale)
* **Sparsity:** ~99.9975% (Highly sparse, requiring latent feature extraction).

---

## ✨ Key Features
* **Exploratory Data Analysis (EDA):** Visualized rating distributions, identified most active users/products, and plotted sparsity heatmaps.
* **Data Preprocessing:** Handled missing values, removed duplicate rows, and eliminated irrelevant features (like timestamps).
* **Dimensionality Reduction:** Applied **SVD (Singular Value Decomposition)** to extract latent features for users and products to handle data sparsity.
* **Clustering Engine:** Trained **K-Means Clustering** models to group users with similar tastes and products with similar engagement profiles.
* **Interactive UI:** A dark-themed, sleek **Streamlit** dashboard for generating real-time recommendations.

---

## 🛠️ Tech Stack
* **Programming Language:** Python 3
* **Data Manipulation & Analysis:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn (SVD, K-Means)
* **Model Serialization:** Joblib
* **Web Framework:** Streamlit

---

## 📂 Project Structure
```text
📦 Product-Recommendation-System
 ┣ 📜 Product_Recommendation_System.ipynb       # Jupyter Notebook with EDA, Model Training, and Evaluation
 ┣ 📜 app.py                                    # Streamlit web application script
 ┣ 📜 rating_short.csv                          # Raw dataset (Add to repo or .gitignore)
 ┣ 📜 user_item_matrix.joblib                   # Serialized user-item matrix
 ┣ 📜 kmeans_user_model.joblib                  # Serialized K-Means User model
 ┗ 📜 kmeans_product_model.joblib               # Serialized K-Means Product model
