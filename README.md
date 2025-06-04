# Financial Fraud in Canada: Insights and Prevention Strategies (2021–2025)
(images/fraud_canada.png)
## Project Overview

This project analyzes real-world financial fraud reports collected by the Canadian Anti-Fraud Centre (CAFC) from January 2021 to March 2025. 
The primary goal is to understand fraud trends across time, geography, and demographics — and to build predictive models that classify whether a report led to actual monetary loss.

Fraud affects thousands of Canadians every year, especially seniors, small business owners, and online users. By uncovering trends and building detection models, this project aims to support public awareness, policy guidance, and fraud prevention.

## Objectives

- Understand how fraud has evolved in Canada over the last four years.
- Identify the most frequent and costly types of fraud.
- Analyze which demographic groups and regions are most affected.
- Build classification models to predict financial loss outcomes.
- Provide actionable insights for prevention, education, and enforcement.

## Dataset Summary

- Source: Canadian Anti-Fraud Centre – Open Data Portal  
- Period Covered: Jan 2021 – Mar 2025  
- Scope: Fraud type, dollar loss, date received, location, demographics, solicitation method  
- Notes: Data is based on public reports and may contain inconsistencies or partial information.

## Tools & Technologies

- Languages & Libraries: Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Plotly  
- Environment: Jupyter Notebook / Google Colab  
- Workflow: EDA → Preprocessing → Modeling → Interpretation

## Data Cleaning Tasks

- Removed French duplicate columns (kept English for consistency)
- Renamed columns for clarity
- Converted Dollar_Loss to numeric format
- Standardized date formats and age ranges
- Handled missing and unspecified entries appropriately

## Exploratory Data Analysis (EDA)

Key visualizations included:

- Trends in fraud volume and dollar loss over time
- Heatmaps and bar charts by province
- Top fraud types by frequency and financial impact
- Fraud delivery methods (email, phone, online)
- Demographic breakdowns by age and gender


Visualizations:
- Trends in fraud volume and losses over time ![image](https://github.com/user-attachments/assets/9ebd29a6-61fc-45c5-a095-449b01d24eb5)
- ----------------------------------------------------------------
- Top fraud types by cost and frequency ![image](https://github.com/user-attachments/assets/693789a6-09a5-4538-b74e-dc9e00eb4181)
- -----------------------------------------------------------------
- Regional breakdowns (heatmaps, bar charts) 	![image](https://github.com/user-attachments/assets/9557f0e1-a7cc-40f4-bec2-244fb9b2980b)
- -----------------------------------------------------------------
-  Choropleth Map  ![image](https://github.com/user-attachments/assets/595d8159-98cf-4d19-acfd-be4ec87001dc)
-  -----------------------------------------------------------------
- Common Fraud Patterns ![image](https://github.com/user-attachments/assets/d3673140-7a12-4c4b-a912-61f6360d5789)
- -----------------------------------------------------------------
- Confusion matrix from machine learning evaluation ![image](https://github.com/user-attachments/assets/1c59a352-8337-46da-9ee0-15b91d35bbe1)

---

## Key Insights

### Regional Trends

- Ontario, Quebec, and BC reported the most fraud cases.
- Some provinces had disproportionately high financial losses per case.

### Fraud Types

- Investment scams led to the highest financial losses.
- Followed by: Spear Phishing, Timeshare Fraud, Romance Scams.

### Demographics

- Age group 30–69 (especially 30–39) was most targeted.
- Slightly more female victims overall.

### Fraud Methods

- Online solicitation was most common, followed by phone and email.

## Predictive Modeling

**Goal**: Classify whether a fraud report led to a confirmed victim with monetary loss (Victim vs. Attempt)

### Models Used

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier

### Model Performance Summary

| Metric / Model     | Random Forest | Logistic Regression | Decision Tree |
|--------------------|----------------|----------------------|---------------|
| Accuracy           | 93%            | 92%                  | 93%           |
| Recall (Loss)      | 0.94           | 0.98                 | 0.91          |
| Precision (Loss)   | 0.81           | 0.77                 | 0.81          |
| F1-score (Loss)    | 0.87           | 0.86                 | 0.86          |
| False Negatives    | 1018           | 290                  | 1406          |
| False Positives    | 3636           | 4767                 | 3481          |

### Model Selection Scenarios

| Use Case                                 | Best Model          | Why                                              |
|------------------------------------------|---------------------|--------------------------------------------------|
| Maximize fraud detection (low FN)        | Logistic Regression | Highest recall (0.98), lowest false negatives    |
| Balanced recall & precision              | Random Forest       | Strong F1-score and best trade-off               |
| Simple & interpretable for deployment    | Decision Tree       | Easy to explain; decent performance              |

**Recommended Model**: Random Forest – Ideal balance between false positives and false negatives in fraud detection.

## Recommendations

- **Public Awareness Campaigns**: Target high-risk age groups (30–69) with updated fraud trends.
- **Policy Focus**: Allocate resources to high-loss fraud types (e.g., investment scams).
- **Education Programs**: Inform vulnerable groups (seniors, small businesses) about common scams.
- **Model Deployment**: Consider using Random Forest or Logistic Regression in real-time fraud flagging systems.
- **Future Work**:
  - Time-series forecasting of fraud volume
  - Unsupervised clustering for new fraud typologies
  - Deeper feature engineering (e.g., NLP on report text if available)

## Repository Structure

/data → Raw and cleaned datasets
/notebooks → Jupyter notebooks (EDA + modeling)
/images → Visualizations used in analysis and reports
/reports → Presentation slides and summary report


## Acknowledgements

- **Data Source**: Canadian Anti-Fraud Centre (Open Data)  
- **Notebook**: Full notebook available [here](https://github.com/helenzhupnyk/Financial_Fraud_Canada/blob/main/notebooks/Financial_Fraud_Canada_Data_Analysis_And_Modeling.ipynb)


---
