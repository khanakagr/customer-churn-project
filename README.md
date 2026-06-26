# Customer Churn Prediction & Segmentation

## Project Overview

This project focuses on predicting customer churn using machine learning techniques and identifying customer segments for targeted business strategies. The objective is to accurately identify customers likely to churn and estimate potential revenue impact.

---

## Objectives

* Predict customer churn using classification models
* Handle class imbalance effectively
* Optimize model performance using hyperparameter tuning
* Segment customers based on behavior and churn probability
* Estimate business impact in terms of revenue

---

## Methodology

### 1. Data Preprocessing

* Handled missing values and encoded categorical variables
* Performed train-test split (80-20)
* Applied stratification to maintain class balance

---

### 2. Model Building

#### Baseline Model

* Random Forest Classifier
* Initial performance evaluated using accuracy, recall, precision, and F1-score

#### Handling Class Imbalance

* Used `class_weight='balanced'` in Random Forest

#### Hyperparameter Tuning

* Tuned parameters such as:

  * Number of trees (`n_estimators`)
  * Maximum depth (`max_depth`)

---

### 3. Model Evaluation

Evaluation metrics used:

* Accuracy
* Recall (primary metric)
* Precision
* F1 Score
* ROC-AUC Score

---

## Results

| Model                  | Accuracy | Recall  | Precision | F1 Score |
| ---------------------- | -------- | ------- | --------- | -------- |
| Baseline Random Forest | 79.2%    | 51.7%   | 67.4%     | 58.6%    |
| Balanced Random Forest | 79.2%    | 51.0%   | 67.8%     | 58.2%    |
| Tuned Random Forest    | 78.0%    | 75.2%   | 58.8%     | 66.0%    |

* The **Tuned Random Forest** achieved the highest recall, making it the best model for identifying churn customers.

### Cross-Validation Results

* Mean CV Accuracy: **77.9%**
* Mean CV Recall: **73.0%**

---

## ROC-AUC Performance

* ROC-AUC Score: **0.84**
* Demonstrates strong ability to distinguish between churn and non-churn customers

---

The final tuned Random Forest model achieved:

- Recall: 75.2% (primary metric)
- Accuracy: 78.0%
- Precision: 58.8%
- F1 Score: 66.0%
- ROC-AUC: 0.84

---

## Customer Segmentation

K-Means clustering was applied using:

* Tenure
* Monthly Charges
* Total Charges
* Churn Probability

### Identified Segments:

* **Budget Loyal Customers**
* **High Risk New Customers**
* **Loyal Premium Customers**

This segmentation helps in targeted marketing and retention strategies.

---

## Business Impact Analysis

* Total Customers Evaluated: 1409
* Actual Churners: 400
* Correctly Predicted Churners: 301
* Missed Churners: 99

### Revenue Estimation:

* Average Revenue per Customer: $65

* **Estimated Revenue Saved:** $19565

* **Potential Revenue Lost:** $6435

---

## Key Insights

* Handling class imbalance significantly improved recall
* Hyperparameter tuning enhanced model performance
* Recall is more important than accuracy for churn prediction
* Customer segmentation provides actionable business insights

---

## Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn
* Seaborn, Matplotlib

---

## Conclusion

The project successfully developed a churn prediction model with strong recall performance and provided actionable customer segmentation insights. The model can help businesses proactively retain high-risk customers and reduce revenue loss.

---

## Author

Khanak Agrawal  
[LinkedIn](https://www.linkedin.com/in/khanak-agrawal-51025037b/) | [GitHub](https://github.com/khanakagr)
