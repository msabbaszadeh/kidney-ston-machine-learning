🧬 Kidney Stone Prediction using Machine Learning and AI

This project applies Artificial Intelligence (AI) and Machine Learning (ML) techniques to predict the presence of kidney stones based on various biochemical and physiological parameters.
Using multiple algorithms and automated model comparison, the study identifies the most accurate model for early and reliable detection of kidney stones.

📋 Project Overview

The dataset includes 90 patient records and 7 key features, such as urine gravity, pH, osmolality, conductivity, urea, calcium, and a binary target indicating kidney stone presence (1) or absence (0).

Through data exploration, visualization, correlation analysis, and model benchmarking, this project aims to determine which algorithm performs best for this medical diagnosis task.

⚙️ Workflow Summary

Data Cleaning and Preparation

Removed unnecessary columns (Unnamed: 0)

Verified no missing values or duplicates

Dataset contained 90 clean and balanced entries

Exploratory Data Analysis (EDA)

Used Seaborn and Matplotlib for visualization.

Created pair plots, correlation heatmaps, and relationship plots.

Observed strong correlations:

osmo ↔ urea (0.89)

gravity ↔ osmo (0.85)

calc ↔ target (0.46)

Insights: Higher calcium concentration and urine gravity are often linked to kidney stones.

Data Splitting

Split data into:

Training set: 70%

Test set: 30%

Used train_test_split() with a fixed random state for reproducibility.

🤖 Model Benchmarking with LazyPredict

To identify the best algorithm efficiently, the LazyClassifier from lazypredict was used to automatically train and compare multiple models.

Top Performing Models:

Model	Accuracy	Balanced Accuracy	ROC AUC	F1 Score	Time Taken (s)
XGBClassifier	0.89	0.89	0.89	0.89	0.04
CalibratedClassifierCV	0.89	0.87	0.87	0.89	0.02
ExtraTreesClassifier	0.85	0.86	0.86	0.85	0.06
LinearSVC	0.85	0.84	0.84	0.85	0.01
KNeighborsClassifier ✅	0.85	0.84	0.84	0.85	0.01
