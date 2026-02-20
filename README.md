# Mushroom Classification - Risk-Based Threshold Optimization  

## Project Goal  

The Objective of this project is to build a supervised classification model that distingusishes between **edible** and **poisonous** mushrooms. 

Instead of maximizing accuracy, the goal is:  
> Guarantee that  **no poisonous mushroom is classified as edible** (zero false negatives). 

This makes the problem risk-sensitive rather than accuracy-driven. 

---

## Problem Type  

- Supervised Learining
- Binary Classification 
- Categorical Features Only
- Hard Constraint Thresholds Optimization 

---  

## Workflow 

### 1. Data Preparation 
- Train/Test split (stratified)
- Seperation of features (X) and target (y)  

### 2. Preprocessing 
- Imputation
- OneHotEncoding (categorical features)
- Pipeline Intergration 

### 3. Model 
- Logistic Regression (inside Pipeline) 

### 4. Advanced Classification Strategy 
- Used `predict_proba()` instead of `predict()`
- Searched for optimal decision threshold
- Applied Hard Constraint:
    - FN (False Negatives) = 0 

---

## Final Result 

Using a conservative threshold:

- No poisonuos mushroom classified as edible
- 553 edible mushrooms can be safely consumed
- Trade-off: many edible mushrooms are rejected for safety 

---

## Key Insights 
  
This Project demonstrates:  

- Thresholds are decisions.  
- Accuracy is not always the correct objective.  
- In safety-critical systems, recall constraints dominate performance metrics.  

---

## Technologies Used 

- Python
- pandas 
- scikit-leran
- Logistic Regression
- Pipeline
- Confusion Matrix
- Threshold tuning 

---

## Next Improvements. 

- Cost-sensitive learning
- Imbalanced data techniques
- Alternative classifiers
- ROC-based Threshold search