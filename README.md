# Financial Fraud in Canada: Insights and Prevention Strategies (2021–2025)

## Project Summary

This project explores real-world financial fraud data from the Canadian Anti-Fraud Centre (CAFC), spanning from January 2021 to March 2025. The goal is to uncover fraud patterns, identify the most affected regions and groups, and suggest actionable insights for prevention and public awareness.

---

## Why I Chose This Topic

As someone starting out in data science, I wanted my portfolio project to be meaningful and rooted in real-world impact. Financial fraud affects thousands of people every year — especially vulnerable populations like seniors and small business owners. 

I chose this topic not just because it's data-rich, but because I believe data science can help protect people. Understanding the patterns behind fraud can help governments, law enforcement, and everyday citizens make better decisions and stay informed.

This project helped me apply real data science skills — from data cleaning to visualization and modeling — while working on a socially important issue.

---

## Objectives

- Understand how fraud trends have evolved in Canada over the last four years.
- Identify which fraud types are most common and which lead to the biggest financial losses.
- Analyze demographic and regional data to determine who is most affected.
- Provide insights and recommendations for awareness and prevention strategies.

---

##  Dataset

- **Source**: [Government of Canada - Open Data](https://open.canada.ca/data/en/dataset/6a09c998-cddb-4a22-beff-4dca67ab892f)
- **Period Covered**: Jan 2021 – Mar 2025
- **Scope**: Fraud type, reported losses, dates, location, demographics (where available)

---

## Tools Used

- Python (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Plotly)
- Jupyter Notebook, GoogleColab
  
---

##  Key Steps in the Project

1. **Data Cleaning** – Fixing column types, handling missing data.
2. **Exploratory Data Analysis (EDA)** – Identifying trends in fraud types, regions, and total losses.
3. **Modeling** – Applied classification models to test prediction feasibility.
4. **Insights & Interpretation** – Explained what the results mean and who they matter to.
5. **Conclusion & Recommendations** – Shared next steps, from policy suggestions to future modeling work.

---

##  Data Cleaning

- Remove Duplicate Columns (Keep English only)
- Rename columns for clarity,
- Removing extra characters and whitespace,
- Converting Dollar_Loss to numeric,
- Converting Date_Received to the correct format
- Standardizing age ranges and other categorical values,
- Handling missing or unspecified entries properly.
---

## EDA - Visualizations & Screenshots

- Grouped fraud cases by province, fraud type, and year to identify patterns.
- Analyzed losses across different fraud categories.
- Assessed regional fraud distribution to detect provincial hotspots.
- Investigated trends in fraud methods (online vs. phone vs. email) and reporting behaviors.

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

##  Key Insights  

###  Regional Trends  
- **Ontario, Quebec, and British Columbia** had the highest fraud cases  
- Some provinces showed disproportionate loss-to-case ratios  

###  Fraud Types & Financial Impact  
- **Investment scams** caused the highest financial losses  
- Followed by **Spear Phishing**, **Timeshare**, and **Romance scams**

###  Demographics  
- Most targeted age group: **30–69**, especially **30–39**  
- Gender split was almost equal; slightly more female victims  

###  Reporting Methods  
- Online methods dominated, followed by phone and email fraud  

---

##  Predictive Modeling

### Goal  
To predict whether a reported fraud case resulted in a **victim losing money** (binary classification).

### Models Used  
- **Logistic Regression**  
- **Decision Tree Classifier**  
- **Random Forest Classifier**

### Performance Summary  
| Model              | Accuracy | F1-Score (Fraud Class) |
|-------------------|----------|-------------------------|
| Logistic Regression | 88%     | 0.78                   |
| Decision Tree      | 88%     | 0.83                   |
| Random Forest      | 88%     | **0.87**               |

- All models reached ~88% accuracy, but **Random Forest** had the best F1-score and recall for identifying actual fraud victims.  
- **Recommended model:** `Random Forest` – it balances precision and recall well for the minority fraud class.

> Fraud detection is inherently imbalanced. Improving recall, even slightly, can prevent real financial loss in real-world use cases.

---

## Conclusion & Recommendations  

This project demonstrated the power of data science in uncovering patterns in Canadian financial fraud. From regional trends to demographic risk factors, and predictive models with solid performance — the findings can help:

- **Public Awareness Campaigns** – Focus on high-risk age groups and regions  
- **Policy & Enforcement** – Allocate resources to regions/types with highest impact  
- **Education Initiatives** – Inform older adults and small business owners on common scam types  
- **Modeling Extensions** – Future work could include time-series forecasting or unsupervised pattern detection  

---

## Project Files  
- `/data`: Raw and processed datasets  
- `/notebooks`: EDA and modeling notebooks  
- `/images`: Visualizations  
- `/reports`: Final insights and presentation slides  

---

##  Acknowledgements  
Data Source: [Canadian Anti-Fraud Centre (Open Data)](https://open.canada.ca/data/en/dataset)

---
