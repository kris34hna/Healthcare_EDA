# Healthcare (Heart Disease) Exploratory Data Analysis

Analyzing patient health metrics to uncover patterns and risk factors associated with heart disease.

---

### Brief Summary

An in-depth exploratory data analysis (EDA) on a heart disease dataset (303 patients, 14 clinical features), examining categorical and numerical risk factors through univariate, bivariate, and multivariate analysis to understand what drives heart disease risk.

---

### Overview

This project explores a clinical dataset containing patient demographics and diagnostic measurements to identify patterns related to heart disease likelihood. The analysis covers categorical variables (sex, chest pain type, ECG results, etc.) and numerical variables (age, cholesterol, blood pressure, etc.), examining their individual distributions and their relationships with the target variable (presence of heart disease).

---

### Dataset

|Detail|Info|
|---------|-------|
|File | heart.csv |
|Records | 303 patients (duplicates removed) | 
|Features |14  |
|Data Types | All numeric (Integer & Float) |
|Missing Data | None |

Key Columns:

|Column | Description | 
|-------|-------------|
|age    | Patient age |
|sex    |Gender (Male/Female)|
|cp     |Chest pain type (Asymptomatic, Typical Angina, Atypical Angina, Non-anginal Pain)|
|trtbps |Resting blood pressure|
|chol   |Serum cholesterol|
|fbs    |Fasting blood sugar|
|restecg|Resting ECG results|
|thalachh|Max heart rate achieved|
|exng   |Exercise-induced angina|
|oldpeak|ST depression induced by exercises|
|slp    |Slope of peak exercise ST segment|
|caa    |Number of major vessels colored by fluoroscopy|
|thall  |Thalassemia type|
|output |Target — presence of heart disease|

---

### Tools & Technologies

|Tool | Purpose|
|-----|-------|
|Python | Core language|
|Pandas / NumPy | Data manipulation & cleaning | 
|Matplotlib / Seaborn | Visualizations (countplots, histograms, KDE, heatmaps, pairplots) | 
|Jupyter Notebook | Development environment |

---

### Methods

1 Initial Inspection — Checked shape (303 rows × 14 columns), data types, duplicates, missing values, and descriptive statistics.  
2 Data Cleaning — Identified and removed duplicate rows; verified no missing values remained.  
3 Categorical Encoding for Readability — Mapped numeric codes to descriptive labels (e.g., sex: 0/1 → FEMALE/MALE; cp: 0–3 → Asymptomatic/Typical Angina/Atypical Angina/Non-anginal Pain). 

4 Univariate Analysis

- Categorical — Countplots for sex, chest pain type, fasting blood sugar, ECG results, exercise angina, slope, vessels, thalassemia, and target
- Numerical — Histograms and boxplots for age, resting BP, cholesterol, max heart rate, and ST depression


5 Bivariate Analysis

- Categorical vs Target — Countplots split by heart disease outcome + correlation heatmap
- Numerical vs Target — KDE plots comparing distributions for patients with vs. without heart disease + correlation heatmap

6 Multivariate Analysis

- Pairplot of all numeric variables colored by target
- Full covariance/correlation matrix heatmap across all 14 variables

---

### Key Insights

- 303 patients, 14 variables — all numeric (Integer/Float), with no missing values.
- 207 male vs 96 female patients (68.32% vs 31.68%) — males outnumber females ~2.15x.
- Nearly half of patients (143) report asymptomatic chest pain — the most common category.
- 75.00% of female patients show a higher likelihood of heart disease, compared to 46.86% of male patients — despite men being the majority in the dataset, women appear at higher relative risk in this data.
- Contrary to common assumptions, this dataset shows heart disease risk does not increase with age — in fact, the pattern suggests a decreasing trend, an interesting and counter-intuitive finding.
- Age & Max Heart Rate (thalachh) show a moderate negative correlation (-0.40) — as age increases, max heart rate tends to decrease.
- Sex shows no strong/robust correlation with most other clinical variables.

---

### Results & Conclusion

This EDA revealed several non-obvious patterns in heart disease risk factors — notably that female patients and younger patients showed higher relative risk in this dataset, challenging common assumptions. Chest pain type, max heart rate, and age emerged as clinically meaningful variables with measurable relationships to the target outcome. These findings provide a strong foundation for feature selection in future predictive modeling.

---

### Author & Contact

|Name     |(Your Name)|
|---------|-----------|
|LinkedIn | https://www.linkedin.com/in/krishna-krishna-26a106231/ |
|GitHub   |https://github.com/kris34hna/Healthcare_EDA|


⭐ If you found this project helpful, consider giving it a star!
