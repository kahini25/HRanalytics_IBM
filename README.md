# HRanalytics_IBM
# Employee Attrition Prediction – IBM HR Analytics

## Project Overview
This project analyzes the **IBM HR Analytics Employee Attrition & Performance dataset** to understand key factors influencing employee turnover and predict attrition using multiple **machine learning models**.  

The project combines **data preprocessing, visualization (Tableau), and machine learning** to derive actionable insights for HR departments to improve employee retention and satisfaction.

---

## Dataset Information

**Source:** [Kaggle - IBM HR Analytics Employee Attrition & Performance](https://www.kaggle.com/datasets/pavansubhasht/ibmhr-analytics-attrition-dataset?resource=download)  
**Rows:** 1470  **Columns:** 35  

The dataset includes features such as employee demographics, job satisfaction, salary, performance metrics, and attrition status.

| Category | Examples |
|-----------|-----------|
| Employee Demographics | Age, Gender, Marital Status |
| Work Environment | Department, DistanceFromHome, EnvironmentSatisfaction |
| Compensation | MonthlyIncome, StockOptionLevel, PercentSalaryHike |
| Career Progression | YearsAtCompany, YearsSinceLastPromotion |
| Target Variable | Attrition (Yes/No) |

---

## Technologies Used

| Component | Tools/Libraries |
|------------|----------------|
| Programming Language | Python |
| Data Analysis | pandas, numpy |
| Data Preprocessing | LabelEncoder, MinMaxScaler |
| Machine Learning Models | LogisticRegression, RandomForestClassifier, SVC, DecisionTreeClassifier, KNeighborsClassifier |
| Evaluation & Visualization | matplotlib, seaborn, sklearn.metrics |
| Dashboard Visualization | Tableau |

---

## Project Workflow

### 1. Data Preprocessing
- Loaded dataset and inspected structure using `df.info()` and `df.describe()`.
- Checked for missing values and dropped redundant columns (e.g., `Over18`).
- Detected and removed outliers using the **IQR (Interquartile Range)** method.
- Encoded categorical features using **Label Encoding** for both binary and multi-class columns.
- Applied **Min-Max Scaling** to normalize numerical features between `[0, 1]`.

### 2. Data Visualization (Tableau)
Key insights visualized using Tableau dashboards:
- Gender distribution: 60% male and 40% female employees.
- Average age by department and role: HR managers (avg. 50.5 yrs) older than R&D managers (avg. 47.7 yrs).
- Employee count by role and gender: Sales Executives (194 males vs. 132 females).
- Treemap of marital status and gender: Majority are married males (401).
- Education field distribution: Life Sciences (606) and Medical (464) dominate.
- Average monthly income by role: HR Managers ($18,089) and R&D Managers ($17,130) earn the most.
- Attrition trend by experience: Higher attrition among employees with fewer years at the company.

### 3. Feature Selection
Selected columns with a correlation coefficient greater than 0.1 relative to the `Attrition` variable.

### 4. Model Building and Evaluation
Applied and compared multiple classifiers:
- Logistic Regression
- Random Forest
- Support Vector Machine (SVM)
- Decision Tree
- K-Nearest Neighbors (KNN)

Each model was trained and tested using an 80/20 split and evaluated on:
- Accuracy
- Precision
- Recall
- F1-Score

Visualizations included confusion matrices and bar charts comparing model performance.

---

## Results Summary

| Model | Accuracy | Precision | Recall | F1-Score |
|--------|-----------|------------|----------|-----------|
| Logistic Regression | Moderate | Good interpretability | Balanced | Suitable |
| Random Forest | High Accuracy | Robust | Good Recall | Best Performer |
| SVM | Good | May overfit | Moderate Recall |  |
| Decision Tree | Decent | Easy to interpret | Moderate |  |
| KNN | Lower | Sensitive to scaling | Low Recall |  |

**Random Forest** delivered the best overall performance.

---

## Insights
- Employees with frequent overtime, lower job satisfaction, or long commutes are more likely to leave.
- Income level and years at company are strong indicators of retention.
- Departmental and role-based trends show higher attrition in sales and research roles.

---

## Final Dashboard (Tableau)
The interactive Tableau dashboard summarizes:
- Attrition distribution by demographic and job role
- Average income and satisfaction comparisons
- Role-based and gender-based workforce composition

*(Attach dashboard image or Tableau link here if available)*

---

## How to Run the Project

### Prerequisites
Ensure Python 3.8+ and the following libraries are installed:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
