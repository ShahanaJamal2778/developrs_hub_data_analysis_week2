
# Machine Learning Portfolio Projects

**Customer Segmentation | Time Series Forecasting | Loan Default Risk Optimization**

This repository contains three end-to-end machine learning projects focused on solving real-world business problems using data-driven approaches. Each task demonstrates practical skills in data preprocessing, modeling, evaluation, and translating results into business insights.

---

# Task 1: Customer Segmentation Using Unsupervised Learning

## Objective

Cluster mall customers based on spending behavior and propose targeted marketing strategies for each segment.

## Dataset

**Mall Customers Dataset**
200 records, 5 features:

* CustomerID
* Gender
* Age
* Annual Income (k$)
* Spending Score (1–100)

## Workflow

### 1. Exploratory Data Analysis (EDA)

* Verified dataset integrity (no missing values).
* Analyzed age, income, and spending score distributions.
* Observed:

  * Average age: 38.8 years
  * Average income: $60.6k
  * Average spending score: 50.2

### 2. Clustering with K-Means

* Applied the Elbow Method (WCSS).
* Optimal clusters identified: **5**
* Segmentation based on **Annual Income** and **Spending Score**.

### 3. Dimensionality Reduction

* PCA / t-SNE used for 2D visualization.
* Clear separation between behavioral segments.

## Identified Customer Segments

1. **Moderate Income – Moderate Spending**
   Stable customers with balanced purchasing behavior.

2. **High Income – High Spending**
   Premium segment with strong purchasing power.

3. **Low Income – High Spending**
   Young, highly engaged buyers despite limited income.

4. **High Income – Low Spending**
   Under-engaged affluent customers.

5. **Low Income – Low Spending**
   Budget-sensitive segment with minimal engagement.

## Business Insights & Strategy

* **Cluster 1 (High Income, High Spending)**
  Focus on loyalty programs, premium memberships, early product access.

* **Cluster 2 (Low Income, High Spending)**
  Offer installment plans, student discounts, targeted promotions.

* **Cluster 3 (High Income, Low Spending)**
  Re-engagement campaigns, personalized recommendations.

* **Cluster 4 (Low Income, Low Spending)**
  Value bundles, discount campaigns.

This task demonstrates strong understanding of:

* Unsupervised learning
* Customer behavior analytics
* Translating clusters into actionable marketing strategies

---

# Task 2: Energy Consumption Time Series Forecasting

## Objective

Forecast short-term household energy consumption using historical time-based patterns.

## Dataset

**Household Power Consumption Dataset**

* 2,075,259 original minute-level entries
* Resampled to hourly frequency → 34,589 records

## Feature Engineering

Extracted time-based features:

* Hour
* Day of week
* Day of year
* Month
* Year
* Weekday indicator

Data split:

* 80% Training (27,671 samples)
* 20% Testing (6,918 samples)

## Models Compared

1. ARIMA
2. Prophet
3. XGBoost

## Model Performance

| Model   | MAE  | RMSE |
| ------- | ---- | ---- |
| ARIMA   | 0.58 | 0.81 |
| Prophet | 0.49 | 0.65 |
| XGBoost | 0.48 | 0.66 |

## Key Findings

* **XGBoost** achieved the lowest MAE.
* **Prophet** performed best in minimizing large forecast errors (lowest RMSE).
* **ARIMA** underperformed due to limited ability to model complex seasonality and nonlinear patterns.

## Insights

Tree-based models (XGBoost) and seasonality-aware models (Prophet) are better suited for high-frequency energy data compared to traditional ARIMA.

### Future Improvements

* Hyperparameter tuning
* Incorporating weather and holiday features
* Multi-step forecasting optimization

This task demonstrates:

* Time series preprocessing
* Feature engineering
* Model comparison
* Forecast visualization
* Business-oriented evaluation

---

# Task 3: Loan Default Risk with Business Cost Optimization

## Objective

Predict loan default risk and optimize decision thresholds based on financial impact rather than accuracy alone.

## Dataset

**Home Credit Default Risk Dataset**
614 records, 13 features

## Data Preparation

* Missing values handled using median and mode imputation.
* Categorical features one-hot encoded.
* Target variable label encoded.
* Stratified 80/20 train-test split.

## Business Cost Matrix

* False Positive (Approve defaulting loan): $5000
* False Negative (Reject good loan): $1000

This setup reflects real-world financial risk.

---

## Model Comparison (Default Thresholds)

| Model               | Accuracy | F1 Score |
| ------------------- | -------- | -------- |
| Logistic Regression | 0.86     | 0.91     |
| CatBoost            | 0.81     | 0.87     |

---

## Optimized Threshold Results

| Metric              | Logistic Regression | CatBoost |
| ------------------- | ------------------- | -------- |
| Optimized Threshold | 0.7980              | 0.5051   |
| Total Cost          | **$59,000**         | $74,000  |
| False Positives     | 3                   | 13       |
| False Negatives     | 44                  | 9        |

### Key Insight

Although CatBoost achieved higher accuracy, **Logistic Regression minimized total business cost** by drastically reducing expensive false positives.

This highlights a critical real-world lesson:

> The best model is not always the one with the highest accuracy — it is the one that aligns with business objectives.

## Feature Importance

CatBoost feature importance analysis identified:

* Credit History
* Applicant Income
* Loan Amount

as strong predictors of default risk.

---

# Overall Skills Demonstrated

* Unsupervised Learning (K-Means)
* Dimensionality Reduction (PCA, t-SNE)
* Time Series Forecasting (ARIMA, Prophet, XGBoost)
* Binary Classification
* Cost-Sensitive Learning
* Feature Engineering
* Business-Driven Model Optimization

---

# Conclusion

These three projects collectively demonstrate the ability to:

* Move from raw data to actionable business insights
* Compare models using appropriate metrics
* Optimize decisions based on real financial impact
* Translate technical results into strategic recommendations

The focus throughout these tasks has been not only on model performance, but on solving business problems effectively and responsibly.

---


