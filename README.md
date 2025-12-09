# Human Cognitive Performance Prediction Using Machine Learning

## Project Overview

This project aims to predict human cognitive performance using machine learning models. Cognitive performance refers to an individual’s ability to process information, solve problems, maintain focus, and perform mental tasks efficiently. Predicting it helps identify key lifestyle and demographic factors influencing mental abilities such as sleep hours, stress level, diet type, and exercise frequency.

We implemented regression models, including Linear Regression, Polynomial Regression, KNN Regressor, and a Stacking Regressor ensemble to improve prediction accuracy. Each base model was trained individually before being combined in the stacking ensemble, where Linear Regression acts as the meta-model to generate optimized final predictions.

## Team Members

* Margret Atef
* Karin Ayman
* Shery Adel
* Alaria Bahy
* Marina Wahid

## Dataset

* **Source:** human_cognitive_performance.csv
* **Features:**

  * User_ID – unique identifier (removed during preprocessing)
  * Age – numeric
  * Gender – categorical
  * Sleep_Hours – numeric
  * Stress_Level – numeric
  * Diet_Type – categorical
  * Exercise_Frequency – categorical (Low, Medium, High)
  * Cognitive_Score – target variable
* **Missing Values:** None
* **Duplicates:** None

## Preprocessing Steps

* Removed irrelevant columns: **User_ID** and **AI_Predicted_Score**
* Encoded categorical features:

  * **Gender** and **Diet_Type** → One-hot encoding
  * **Exercise_Frequency** → Ordinal Encoding (Low=0, Medium=1, High=2)
* Standardized numerical features
* Conducted correlation analysis using heatmaps

## Machine Learning Models

* **Linear Regression:** Baseline model to capture linear relationships.
* **Polynomial Regression (Pipeline):** Captures non-linear patterns using PolynomialFeatures(degree=2).
* **K-Nearest Neighbors (KNN, k=5):** Predicts based on nearest neighbors in feature space.
* **Stacking Regressor (Ensemble):** Combines predictions from base models with Linear Regression as the meta-model.

## Experimental Setup

* **Programming Language:** Python
* **Libraries:** pandas, numpy, seaborn, matplotlib, scikit-learn
* **Platform:** Jupyter Notebook / Google Colab
* **Train/Test Split:** 80% training, 20% testing

## Results

* **Metrics evaluated:** MAE, RMSE, R² Score
* **Stacking Regressor** performed best due to combining multiple base models.
* Key predictive features: Sleep hours, stress level, and exercise frequency.
* For detailed results and plots, see the Jupyter Notebook.

## How to Run

1. Clone this repository:

```
git clone https://github.com/margret12344/Human_Cognitive_Performance.git
```

2. Navigate to the repository folder:

```
cd Human_Cognitive_Performance
```

3. Install required libraries (if not already installed):

```
pip install -r requirements.txt
```

4. Open the Jupyter Notebook to explore data preprocessing, model training, and results.

## Repository Link

[GitHub Repository](https://github.com/margret12344/Human_Cognitive_Performance)
