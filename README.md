# 🧬 Diabetes Risk Segmentation using Unsupervised Learning

This project applies **unsupervised machine learning techniques** to segment patients based on their risk of developing diabetes.  
Using **K-Means**, **Gaussian Mixture Models (GMM)**, and **DBSCAN**, we identify groups with similar physiological and genetic profiles to support healthcare decision-making.

---

## 📊 Project Overview
The dataset includes variables such as glucose, blood pressure, BMI, age, and pedigree function.  
The main goal is to uncover **actionable patient segments** for clinical or public health interventions.

---

## 🧩 Methodology
1. **Exploratory Data Analysis (EDA):**  
   - Handling missing and incorrect physiological values.  
   - Correlation analysis and feature scaling (StandardScaler).

2. **Modeling & Clustering:**  
   - K-Means (main model) with K selection using Elbow, Silhouette, and Davies–Bouldin Index.  
   - GMM and DBSCAN used for comparison.  
   - Stability analysis using Adjusted Rand Index (ARI) and Normalized Mutual Information (NMI).

3. **Cluster Profiling & Interpretation:**  
   - Seven patient clusters were identified.  
   - Each group was profiled using mean physiological values and diabetes prevalence.  
   - Five out of seven clusters were found **clinically actionable**.

---

## 🩺 Business Validation
Clusters were evaluated based on public health and clinical relevance to:
- Prioritize **high-risk groups** for intervention.  
- Identify **non-actionable low-risk populations**.  
- Optimize healthcare resource allocation.

---

## 🧮 Tools & Libraries
- Python, Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn (KMeans, GMM, DBSCAN, PCA)  
- Jupyter / Google Colab

---

## 📈 Results Summary

| Cluster | Segment Name | Avg Age | BMI | % Diabetic | Actionable |
|---------|---------------|---------|-----|-------------|-------------|
| 0 | Young Genetic Risk | 31.4 | 33.9 | 62% | ✅ |
| 1 | Older Adults with Established Diabetes | 53.0 | 33.6 | 70% | ✅ |
| 2 | Healthy Young Group | 25.0 | 22.4 | 13% | ❌ |
| 3 | Multi-gestational Women | 25.4 | 32.9 | 38% | ✅ |
| 4 | Low-Pressure Young Adults | 25.4 | 22.7 | 10% | ❌ |
| 5 | Obese Youth | 24.7 | 41.2 | 16% | ✅ |
| 6 | Hyperinsulinemic Youth | 31.0 | 32.4 | 62% | ✅ |

---

## 📎 Recommendations
- Focus interventions on Clusters 0, 1, 3, 5, and 6.  
- Exclude low-risk groups (2 and 4) from immediate follow-up.  
- Integrate segmentation into clinical or public health workflows.

---

## ⚙️ Installation
Clone the repository and install dependencies:
```bash
git clone https://github.com/yourusername/Diabetes-Risk-Clustering-ML.git
cd Diabetes-Risk-Clustering-ML
pip install -r requirements.txt
