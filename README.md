# 🏦 Bank Loan Default Risk Analysis

## 📘 Case Study Overview

This project conducts an in-depth **Exploratory Data Analysis (EDA)** on a loan application dataset. The goal is to identify patterns and risk indicators that help financial institutions make informed loan approval decisions. The dataset includes key applicant details such as income, employment history, credit behavior, loan amount, and demographics.

---

## 🎯 Objectives

- Identify high-risk applicants using data patterns
- Improve loan approval strategy with data-backed insights
- Reduce rejection of low-risk, creditworthy applicants
- Highlight top features associated with default risk

---

## 🛠️ Tools & Technologies

| Tool           | Purpose                                      |
|----------------|----------------------------------------------|
| **Excel 2022** | Data cleaning, analysis, visualizations      |
| **Google Docs**| Report writing and documentation             |

**Excel Features Used:**

- **Functions**: `IF`, `ISBLANK`, `COUNT`, `COUNTIF`, `CORREL`, `QUARTILE`, `MEDIAN`
- **Charts**: Bar, Pie, Box Plot, Scatter, Heatmap
- **Features**: Pivot Tables, Conditional Formatting, Filters

---

## 🔍 Methodology

### 1. Missing Data Handling
- **Detection**: Used `ISBLANK()`, `COUNTBLANK()`, and `IF()`
- **Imputation**:
  - Numerical: Replaced with **median**
  - Categorical: Replaced with **most frequent category**
- **Outcome**: Reduced sparsity, improved dataset completeness

### 2. Outlier Detection
- Applied **Interquartile Range (IQR)** method:
  ```excel
  Q1 = QUARTILE.EXC(range, 1)
  Q3 = QUARTILE.EXC(range, 3)
  IQR = Q3 - Q1
  Lower Bound = Q1 - 1.5 * IQR
  Upper Bound = Q3 + 1.5 * IQR
- Focused on: CNT_CHILDREN, AMT_INCOME_TOTAL, YEARS_BIRTH, AMT_GOODS_PRICE

- Visuals: Box plots, scatter plots

### 3. Target Imbalance Analysis
- Counted class values using COUNTIF() and COUNT()

- Found ~92% of applicants are non-defaulters

- Visuals: Pie chart and bar chart

### 4. Exploratory Data Analysis
- Univariate Analysis: Examined individual features (e.g. income) with histograms, AVERAGE, MEDIAN, MODE

- Segmented Univariate: Split by TARGET (0 = no default, 1 = default)

- Bivariate Analysis: Used pivot tables and scatter plots

Example: Income vs Avg Credit

### 5. Correlation Analysis
- Used CORREL() to analyze relationships between features and TARGET

- Segmented by defaulters and non-defaulters

- Identified strong predictors:
 - EXT_SOURCE_2

 - DAYS_EMPLOYED

 - AMT_CREDIT

---

### 📊 Key Insights
- Applicants with low EXT_SOURCE scores have a higher default risk

- Longer employment history correlates with lower default likelihood

- Very high or low credit amounts may indicate higher risk

- Recommend focusing on EXT_SOURCE_2, DAYS_EMPLOYED, AMT_CREDIT in future risk models

  ---

## 🚀 How to Use This Project

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/IMDB-Movies-Analysis.git
   cd IMDB-Movies-Analysis
2. Open the Excel file in /dataset/imdb_movies.xlsx
3. View insights in /IMDB_Movies_Report.pdf or open individual visuals in /visuals

---

## 📬 Contact
📧 24anjalisahni@gmail.com
🔗 https://www.linkedin.com/in/anjali-sahni-481b44238/
🌐 GitHub: https://github.com/Anjalisahni24

