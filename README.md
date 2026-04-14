# 📊 PCB Yield Prediction & Recommendation System

## 🚀 Overview

This project is an **AI-driven PCB (Printed Circuit Board) yield prediction and recommendation system**.
It uses multiple machine learning models to predict manufacturing yield and suggests optimal process parameters based on historical and similar case data.

---

## 🎯 Objectives

* Predict PCB yield (%) using machine learning models
* Compare multiple models and select the best one
* Analyze feature importance
* Provide recommendations using similar historical cases
* Generate structured reports and visualizations

---

## 🧠 Technologies Used

* Python
* Pandas, NumPy
* Scikit-learn
* XGBoost, LightGBM
* Matplotlib, Seaborn

---

## 📁 Project Structure

```
project/
│
├── main1.py                          # Main pipeline script
│
├── tables/                           # Input datasets
│   ├── historical_cleaned.csv
│   ├── synthetic_cleaned.csv
│   ├── top_similar_cases.csv
│   ├── input_case.csv
│
├── output_sheet/                     # Generated outputs
│   ├── model_comparison.csv
│   ├── yield_recommendation_with_used_data.xlsx
│
├── output_figures/                   # Generated plots
│   ├── best_model_actual_vs_predicted.png
│   ├── best_model_residual_plot.png
│   ├── correlation_heatmap.png
│   ├── model_comparison_*.png
│   ├── feature_importance_*.png
│   ├── yield_distribution.png
│   ├── top_similar_case_*.png
│
└── README.md
```

---

## ⚙️ Installation

### 1. Clone the repository

```
git clone <your-repo-link>
cd project
```

### 2. Create virtual environment

```
python -m venv venv
```

### 3. Activate environment

**Windows:**

```
venv\Scripts\activate
```

**Mac/Linux:**

```
source venv/bin/activate
```

### 4. Install dependencies

```
pip install pandas numpy scikit-learn matplotlib seaborn xgboost lightgbm openpyxl
```

---

## ▶️ How to Run

```
python main1.py
```

---

## 📊 Outputs

### 📄 1. Excel Report

Location:

```
output_sheet/yield_recommendation_with_used_data.xlsx
```

Contains:

* Historical data used
* Synthetic data used
* Recommendation sheet

---

### 📈 2. Model Comparison CSV

```
output_sheet/model_comparison.csv
```

Includes:

* MAE, RMSE, R²
* Cross-validation metrics

---

### 📊 3. Visualizations

Saved in:

```
output_figures/
```

Includes:

* Model comparison graphs
* Feature importance plots
* Correlation heatmap
* Residual plots
* Yield distribution
* Similar case analysis

---

## 🧠 Methodology

1. Data preprocessing (historical + synthetic)

2. Feature selection:

   * thickness
   * holes
   * aspect_ratio
   * mat_tg
   * pth_req
   * max_ol_copper

3. Model training:

   * ExtraTrees (Best Model)
   * RandomForest
   * GradientBoosting
   * XGBoost
   * LightGBM
   * KNN

4. Model evaluation:

   * MAE
   * RMSE
   * R²
   * Cross-validation

5. Prediction:

   * Predict yield for new PCB input

6. Recommendation:

   * Use similar historical cases
   * Suggest optimal process parameters (e.g., stack_hi)

---

## 🏆 Key Results

* Best Model: **ExtraTrees Regressor**
* Predicted Yield: ~96%
* Best Achievable Yield (historical): ~100%

---

## ⚠️ Limitations

* Low R² indicates high variability in PCB manufacturing
* Some important process parameters may be missing
* Model performance depends on data quality

---

## 🔮 Future Improvements

* Add more process variables
* Improve feature engineering
* Hyperparameter tuning
* Deploy as web application (Streamlit/Flask)
* Real-time prediction system

---

## 🧠 Conclusion

This system successfully combines:

* Machine Learning
* Case-Based Reasoning
* Data Analysis

to provide **intelligent PCB yield prediction and recommendations**.

---
