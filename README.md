# 💵 Banknote Counterfeit Detection

## 📌 Overview

This project aims to detect counterfeit banknotes using machine learning techniques based on geometric measurements.

The goal is to compare unsupervised and supervised approaches to identify the most reliable method for classification.

---

## 🎯 Business Problem

Financial institutions need reliable tools to detect counterfeit banknotes.

This project builds and evaluates models to automatically classify banknotes as **genuine** or **counterfeit** based on their physical characteristics.

---

## 📊 Dataset

* **170 banknotes**

  * 100 genuine
  * 70 counterfeit
* **6 numerical features** (dimensions in mm)
* **1 target variable**: `is_genuine`

Features include:

* `diagonal`
* `height_left`
* `height_right`
* `margin_low`
* `margin_up`
* `length`

---

## 🔍 Methodology

The project follows a complete data science workflow:

### 1. Exploratory Data Analysis (EDA)

* Distribution analysis
* Statistical tests (Student test)
* Correlation analysis

### 2. Dimensionality Reduction

* Principal Component Analysis (PCA)
* Visualization of class separation

### 3. Unsupervised Learning

* KMeans clustering
* Evaluation using confusion matrix

### 4. Supervised Learning

* Logistic Regression
* Train/test split (80/20)
* Model evaluation

### 5. Model Optimization

* Feature selection
* Reduced model with similar performance

---

## 📈 Results

| Model                    | Type         | Accuracy |
| ------------------------ | ------------ | -------- |
| KMeans                   | Unsupervised | ~95%     |
| Logistic Regression      | Supervised   | ~100%    |
| Optimized Logistic Model | Supervised   | ~100%    |

---

## 🧠 Key Insights

* The dataset shows a **strong natural separation** between genuine and counterfeit banknotes.
* KMeans performs well despite being unsupervised, confirming the robustness of the data structure.
* Logistic Regression provides **near-perfect classification performance**.
* A reduced model using fewer variables achieves the same performance, improving interpretability.

---

## 🖼️ Visualizations

### PCA Projection (True vs Predicted)

*(add your screenshot here)*

### Confusion Matrices

*(add your screenshots here)*

---

## 🧱 Project Structure

```text
.
├── data/
│   └── notes.csv
├── notebooks/
│   └── banknote_counterfeit_detection.ipynb
├── iimages/
    ├── pca_plot.png
    ├── confusion_matrix_kmeans.png
    ├── confusion_matrix_logistic.png
├── requirements.txt
└── README.md
```

---

## ⚙️ Tech Stack

* Python
* Pandas / NumPy
* Matplotlib / Seaborn
* Scikit-learn
* Statsmodels

---

## 🚀 How to Run

```bash
pip install -r requirements.txt
```

Then open the notebook:

```bash
jupyter notebook notebooks/banknote_counterfeit_detection.ipynb
```

---

## 👨‍💻 Author

**Mohammed Mokeddem**

---

## ⭐ Key Takeaway

This project demonstrates how combining **exploratory analysis, dimensionality reduction, and machine learning** can lead to highly accurate classification systems, even with relatively small datasets.
