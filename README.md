# 🧠 **Kidney Stone Prediction using Machine Learning**

## 📘 **Project Overview**

This project demonstrates a **machine learning pipeline** for predicting **kidney stone disease** based on clinical and chemical parameters.
It utilizes **Python**, **Pandas**, **Scikit-Learn**, **Seaborn**, and **TensorFlow**, offering **data preprocessing**, **exploratory data analysis (EDA)**, **visualization**, and **model comparison** using **LazyPredict** to identify the most accurate classifier.

---

## ⚙️ **Dataset Description**

The dataset contains **90 samples** with the following features:

* **gravity**
* **ph**
* **osmo**
* **cond**
* **urea**
* **calc**
* **target** → *(0 = No Stone, 1 = Stone)*

✅ **No missing or duplicate values** detected.
✅ **Data is clean and ready for modeling.**

---

## 📊 **Exploratory Data Analysis (EDA)**

* **Pair plots** and **heatmaps** were used to understand correlations.
* **Strong correlations** observed:

  * `gravity` ↔ `osmo` (**r = 0.85**)
  * `urea` ↔ `osmo` (**r = 0.89**)
  * `calc` ↔ `target` (**r = 0.46**)

These correlations suggest that **urine concentration and calcium levels** are key indicators for **kidney stone formation**.

---

## 🤖 **Model Training and Evaluation**

Using **LazyPredict**, multiple supervised machine learning algorithms were automatically tested and compared.

### **Top Performing Models**

| Model                      | Accuracy | F1 Score | ROC AUC  | Time (s) |
| -------------------------- | -------- | -------- | -------- | -------- |
| **XGBClassifier**          | **0.89** | **0.89** | **0.89** | 0.04     |
| **CalibratedClassifierCV** | **0.89** | **0.89** | **0.87** | 0.02     |
| **ExtraTreesClassifier**   | **0.85** | **0.85** | **0.86** | 0.06     |
| **KNeighborsClassifier**   | **0.85** | **0.85** | **0.84** | **0.01** |
| **LinearSVC**              | **0.85** | **0.85** | **0.84** | 0.01     |

---

## 🏆 **Best Model Selection**

After reviewing model performance, the **K-Nearest Neighbors (KNN) Classifier** was chosen due to:

* **High accuracy (85%)**
* **Fastest training time (0.01 seconds)**
* **Stable and interpretable results**

### **Final Model Configuration**

```python
KNeighborsClassifier(n_neighbors=10, leaf_size=5)
```

---

## 📈 **Key Results**

* **Accuracy:** **85%**
* **Balanced Accuracy:** **84%**
* **F1 Score:** **0.85**
* **Training Time:** **0.01 seconds**

---

## 🧩 **Conclusion**

**The K-Nearest Neighbors algorithm proved to be the most efficient and accurate model** for predicting kidney stone disease using this dataset.
Its **speed, simplicity, and interpretability** make it ideal for clinical prediction tasks and real-world deployment scenarios.

---
