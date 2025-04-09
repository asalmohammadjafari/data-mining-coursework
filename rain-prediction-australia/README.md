# 🌧️ Rainfall Prediction

## 🎯 Objective

Predict whether it will rain the next day based on historical climate data using machine learning models.

## 📁 Dataset

- **Source**: [Rain in Australia](https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package)
- **Description**: Contains approximately 10 years of daily weather observations from various locations across Australia. The target variable, `RainTomorrow`, indicates whether it rained the following day.

## 🔄 Workflow

### 1. Data Preparation
- Removed unnecessary columns (e.g., `Unnamed: 0`)
- Extracted and mapped month information from dates
- Converted categorical rain indicators (Yes/No) to binary (0/1)
- Handled missing values using backfill and forward fill
- Removed outliers using IQR
- Applied one-hot encoding to categorical features
- Normalized data using `StandardScaler`

### 2. Feature Selection & EDA
- Used a Decision Tree to evaluate feature importances
- Selected top features based on importance scores
- Visualized data using:
  - Correlation heatmap
  - Histograms
  - Box plots
  - Scatter plots and bar charts

### 3. Modeling & Evaluation
Implemented and evaluated three models:
- **Decision Tree**
- **Support Vector Machine (SVM)**
- **K-Nearest Neighbors (KNN)**

**Metrics used**:  
✅ Accuracy  
✅ Precision  
✅ Recall  
✅ F1 Score  
✅ Confusion Matrix

> SMOTE for class imbalance was included but commented out.

## 🛠 Tools Used

- Python, Jupyter Notebook  
- `pandas`, `numpy`, `matplotlib`, `seaborn`  
- `scikit-learn` (for modeling and evaluation)  
- `imbalanced-learn` (for optional SMOTE)

---

