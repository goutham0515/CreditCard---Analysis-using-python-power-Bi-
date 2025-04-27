
 # 📊 Credit Behavior Analysis Project

* ## 🧠 Introduction

This project focuses on analyzing the credit behavior of individuals using a provided credit card dataset.
The main goals are:

## 🔍 Data Preprocessing

* 📈 Insight Derivation through Visualization

* 🛡️ Strategy Development for Credit Risk Management and Customer Segmentation

## 📚 Dataset Context
* 👥 Demographic & Credit Data: Includes age, income, employment status, and credit history.

* ⚖️ Risk Assessment: Predicts credit risk and potential loan defaults (NPAs).

* 💼 Financial Decision-Making: Assists lenders in evaluating borrower reliability.

* 💸 Loss Minimization: Helps financial institutions reduce risk exposure.

## 🗂️ Key Attributes
🔢 Numerical fields: Debt Ratio, Monthly Income, Age, Credit Lines, Delinquency History.

## 🏷️ Categorical fields: Gender, Region, Occupation, Education.

* 🛠️ Techniques Used for Data Preprocessing
* ✂️ Interquartile Range (IQR)
* Used to detect and manage outliers in columns like MonthlyIncome, NumberOfDependents, and DebtRatio.

* Q1 = df['MonthlyIncome'].quantile(0.25)
* Q3 = df['MonthlyIncome'].quantile(0.75)
* IQR = Q3 - Q1
* lower_bound = Q1 - 1.5 * IQR
* upper_bound = Q3 + 1.5 * IQR
## 📏 Capping Method
Applied to cap outlier values to normalize the data.


* df['MonthlyIncome'] = np.where(df['MonthlyIncome'] > upper_bound, upper_bound, df['MonthlyIncome'])
* df['MonthlyIncome'] = np.where(df['MonthlyIncome'] < lower_bound, lower_bound, df['MonthlyIncome'])

## 🎯 Purpose

* 👥 Customer Profiling: Identify patterns and segment clients by financial behaviors.

* 🛡️ Credit Risk Management: Assess default risks to inform better lending decisions.

* 🎯 Targeted Offerings: Create personalized loan products and marketing strategies.

## 📊 Visualizations (Using Power BI)
* 📋 Overview Dashboard:

 ![Image](https://github.com/user-attachments/assets/2c40da01-c2cc-442f-b2e1-11fbdee238f2) 

* Key financial metrics, debt ratios, and delinquency trends.

## 👥 Customer Segmentation:

* Analyzing differences by gender, occupation, and education.

## 📈 Trend Analysis:

* Debt ratio trends, real estate loans, and age-income relationships.

## 🌍 Geographical Analysis:

* Credit behavior distribution across global regions.

## 🧩 Strategy Development

## 🟢 Good Customers:

* High creditworthiness, timely payments, low debt ratios, stable credit history.

##  🔴 Bad Customers:

Frequent late payments, high debt ratios, inconsistent financial habits.

