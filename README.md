# Customer Travel Prediction using Random Forest

## Project Overview
This project focuses on predicting whether a customer will book a travel package based on their profile and travel preferences. Using a dataset of customer information, I developed a **Random Forest Classifier** to make these predictions. The notebook covers all essential steps, from data cleaning and exploratory analysis to model training and evaluation.

---

## Dataset Used
- **Source:** `Travel.csv`  
- **Content:** The dataset includes features such as:
  - `Age`
  - `TypeofContact`
  - `CityTier`
  - `Occupation`
  - `Gender`
  - `MaritalStatus`
  - `Passport`  
- **Target Variable:** `ProdTaken`  
  Indicates whether a customer booked the package (`1`) or not (`0`).

---

## My Approach: A Step-by-Step Breakdown

### 1. Data Cleaning & Exploratory Analysis (EDA)
- **Handling Missing Values:**  
  Null values were handled using:
  - Mode for categorical features
  - Median for numerical features  
  This approach ensures minimal bias in skewed data.
  
- **Data Exploration:**  
  - Count plots and value counts were used to understand the distribution of the target variable.  
  - Observed that the dataset is **imbalanced**, with fewer customers actually booking packages.

---

### 2. Feature Engineering & Preprocessing
- **Categorical Encoding:**  
  Converted categorical variables (`TypeofContact`, `Occupation`, etc.) to numerical format using **one-hot encoding**.
  
- **Data Splitting:**  
  The dataset was split into:
  - **Training set:** 80%  
  - **Testing set:** 20%  

---

### 3. Model Training & Evaluation
- **Algorithm:** Random Forest Classifier  
  Chosen for its robustness, ability to handle imbalanced datasets, and high performance.
  
- **Training:**  
  The model was trained on the preprocessed training data.
  
- **Evaluation Metrics:**  

| Metric      | Value      | Interpretation |
|------------|------------|----------------|
| Accuracy    | 0.936      | About 93.6% of predictions (both positive and negative) are correct. |
| Precision   | 0.978      | Of all predicted buyers, 97.8% were actual buyers. High precision → fewer false positives. |
| Recall      | 0.686      | Only 68.6% of actual buyers were correctly identified. Some potential customers are missed. |
| F1 Score    | 0.806      | Harmonic mean of precision and recall; balances false positives and false negatives. |

> **Note:** The model shows very high precision but moderate recall. This means it is very reliable in predicting buyers (less wasted marketing cost), but some potential buyers are still missed. Future iterations could focus on improving recall to capture more potential customers.



