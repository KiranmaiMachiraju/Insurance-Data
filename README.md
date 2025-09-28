# 🏥 Insurance Cost Analysis & Prediction Dashboard

An end-to-end data analysis and machine learning project to explore the **drivers of health insurance charges** and **predict future costs** using regression techniques. The entire pipeline — from data cleaning to modeling and dashboard visualization — was built in **Python (Pandas)** within **Databricks**, without using PySpark.

---

## 📊 Project Overview

This project aims to:

- Understand how demographic and lifestyle factors affect medical insurance charges.
- Develop predictive models that estimate insurance charges for new individuals.
- Present findings through a clear and intuitive **Databricks dashboard** tailored for non-technical stakeholders.

---

## 🧪 Methodology

1. **Data Cleaning & Preprocessing**
   - Handled categorical variables using `pd.get_dummies`.
   - Engineered new features like `is_obese` based on BMI thresholds.

2. **Exploratory Data Analysis (EDA)**
   - Used **Pandas**, **Matplotlib**, and **Seaborn** to uncover insights:
     - Smokers pay **~4x more** on average.
     - Obese individuals tend to have significantly higher charges.
     - Age and number of children show moderate correlation.
     - The **southeast** region had the **highest average charges**.

3. **Model Building**
   - Trained six models using **Scikit-learn**:
     - Linear Regression
     - Ridge Regression
     - Decision Tree Regressor
     - Random Forest Regressor
     - Gradient Boosting Regressor
     - Support Vector Regressor
   - Evaluated using **MSE** and **R² Score** on test data.

---

## 🧾 Results Summary

| Model                     | MSE          | R² Score |
|--------------------------|--------------|----------|
| Gradient Boosting        | 18.25M       | 0.882    |
| Random Forest            | 20.55M       | 0.868    |
| Linear Regression        | 33.48M       | 0.784    |
| Ridge Regression         | 33.52M       | 0.784    |
| Decision Tree            | 45.83M       | 0.705    |
| Support Vector Regressor | 166.50M      | -0.072   |

- ✅ **Gradient Boosting** performed best with **R² = 0.88**, indicating it explains 88% of the variance in charges.
- ❌ SVR severely underperformed and is not suitable for this dataset.
- Linear models still achieved acceptable performance, making them interpretable options for some use cases.

---

## 📌 Key Findings

- **Smoking** is the single biggest cost driver. Smokers face drastically higher premiums.
- **Obesity** is another major factor. Individuals with BMI > 30 incur higher costs.
- **Age** and **number of children** show increasing trends, but less sharply.
- Regional disparities exist, with the **southeast** showing consistently higher average charges.
- Predictive models can generalize well, especially tree-based ensemble methods.

---

## 📊 Dashboard Features (Built in Databricks)

- **Visual insights** via histograms, boxplots, and scatterplots on:
  - Age vs Charges
  - BMI vs Charges
  - Smoking status distribution
  - Charges by Region
- **Model Comparison Table** embedded to show performance metrics.
- A clean layout tailored for **stakeholders and decision-makers**.
- Built-in prediction logic for future inputs (extendable via widgets).

> 💡 Dashboard is hosted on Databricks Community Edition.
> 📎 *(You can add your public notebook link here)*

---

## 🧰 Tools & Technologies

| Category        | Tools Used                                 |
|----------------|---------------------------------------------|
| Language        | Python 3                                    |
| Data Handling   | Pandas                                       |
| Visualization   | Matplotlib, Seaborn                          |
| Modeling        | Scikit-learn                                 |
| Platform        | Databricks (Community Edition)              |
| Techniques      | EDA, Regression Modeling, Feature Engineering, Dashboarding |

---
