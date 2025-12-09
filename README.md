
# Human Cognitive Performance Prediction Using Machine Learning

## Project Overview
This project aims to predict **human cognitive performance** using machine learning models. Cognitive performance refers to an individual’s ability to process information, solve problems, maintain focus, and perform mental tasks efficiently. Predicting it helps identify key lifestyle and demographic factors influencing mental abilities such as **sleep hours, stress level, diet type, and exercise frequency**.

The project uses regression models, including **Linear Regression, Polynomial Regression, KNN Regressor, and a Stacking Regressor ensemble** to improve prediction accuracy.

---

## Team Members
- Margret Atef  
- Karen Ayman  
- Shery Adel  
- Alaria Bahy  
- Marina Wahid  

---

## Dataset
- **Source:** `human_cognitive_performance.csv`  
- **Features:**  
  - `User_ID` – unique identifier (removed during preprocessing)  
  - `Age` – numeric  
  - `Gender` – categorical  
  - `Sleep_Hours` – numeric  
  - `Stress_Level` – numeric  
  - `Diet_Type` – categorical  
  - `Exercise_Frequency` – categorical (Low, Medium, High)  
  - `Cognitive_Score` – target variable  
- **Missing Values:** None  
- **Duplicates:** None  

---

## Preprocessing Steps
1. Removed irrelevant columns: `User_ID` and `AI_Predicted_Score`  
2. Encoded categorical features:  
   - `Gender` and `Diet_Type` → One-hot encoding  
   - `Exercise_Frequency` → Low=0, Medium=1, High=2  
3. Standardized numerical features  
4. Conducted correlation analysis using heatmaps  

---

## Machine Learning Models
1. **Linear Regression** – baseline model to capture linear relationships.  
2. **Polynomial Regression (Pipeline)** – captures non-linear patterns using PolynomialFeatures.  
3. **K-Nearest Neighbors (KNN, k=5)** – predicts based on nearest neighbors in feature space.  
4. **Stacking Regressor (Ensemble)** – combines predictions from base models using Linear Regression as meta-model.

---

## Experimental Setup
- **Programming Language:** Python  
- **Libraries:** pandas, numpy, seaborn, matplotlib, scikit-learn  
- **Platform:** Jupyter Notebook / Google Colab  
- **Train/Test Split:** 80% training, 20% testing  

---

## Results
- Metrics evaluated: **MAE, MSE, R² Score**  
- Stacking Regressor performed best due to combining multiple base models.  
- Key predictive features: **Sleep hours, stress level, and exercise frequency**.  

> For detailed results and plots, see the Jupyter Notebook.

---

## How to Run
1. Clone this repository:
```bash
git clone https://github.com/username/Human_Cognitive_Performance.git
