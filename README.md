# DA 2011 - Salary Prediction Project

## 📊 Project Overview

This project explores a real-world salary dataset to build predictive models that estimate salaries based on various factors such as experience level, job title, employment type, company size, and location. The project compares traditional Linear Regression with a Neural Network (MLP) approach to identify the most effective prediction model.

---

## 🎯 Objectives

1. **Predict salaries** based on employee and company characteristics
2. **Compare model performance** between Linear Regression and Neural Networks
3. **Identify key factors** that influence salary levels in the dataset
4. **Provide actionable insights** for salary benchmarking and career planning

---

## 📁 Repository Structure

```
salary-prediction-project/
│
├── notebook.ipynb           # Main Jupyter notebook (all code & analysis)
├── salaries.csv            # Original dataset
├── salaries_cleaned.csv    # Cleaned dataset (generated)
└── README.md               # Project documentation
```

---

## 📁 Dataset

**File:** `salaries.csv`

### Features:
- `work_year`: Year of salary data
- `experience_level`: Experience level (EN, MI, SE, EX)
- `employment_type`: Type of employment (FT, PT, CT, FL)
- `job_title`: Job position/role
- `salary`: Original salary amount
- `salary_currency`: Currency of original salary
- `salary_in_usd`: **Target variable** - Salary converted to USD
- `employee_residence`: Employee's country of residence
- `remote_ratio`: Percentage of remote work (0, 50, 100)
- `company_location`: Company's country location
- `company_size`: Company size (S, M, L)

---

## 👥 Team Contributions

### Data Cleaning & Preprocessing
**Contributor:** Pramuditha R.M.H

#### Tasks Completed:
1. **Data Loading**
   - Loaded dataset from `salaries.csv`
   - Initial data inspection and validation
   - Displayed dataset structure and first few rows

2. **Column Management**
   - Dropped unnecessary columns: `salary` and `salary_currency`
   - Retained `salary_in_usd` as the target variable
   - Reduced from 11 to 9 columns

3. **Missing Value Analysis**
   - Comprehensive check for null values across all columns
   - Verified data completeness
   - **Result:** No missing values found ✓

4. **Categorical Data Handling**
   - Analyzed job title frequency distribution
   - Identified rare job titles (appearing < 5 times)
   - Grouped 106 rare job titles into 'Other' category
   - Reduced unique job titles from 347 to 242
   - Preserved data quality while reducing dimensionality

5. **Data Validation & Summary**
   - Generated statistical summaries for numerical features
   - Analyzed distributions of categorical variables:
     - Experience levels
     - Employment types
     - Job titles (top 10)
     - Company sizes
     - Employee residence (top 10)
     - Company locations (top 10)
   - Documented data characteristics for modeling

6. **Output Generation**
   - Saved cleaned dataset as `salaries_cleaned.csv`
   - Created comprehensive data cleaning report with metrics

#### Key Decisions:
- **No outlier removal**: Extreme salaries are valid (e.g., executive roles, specialized positions)
- **Rare category threshold**: Set at 5 occurrences to balance dimensionality reduction and information retention
- **Data preservation**: Maintained all valid records to ensure robust model training
- **Column selection**: Removed redundant columns while keeping all predictive features

#### Code Section in Notebook:
**Section:** "Data Cleaning & Preprocessing"
- Data loading and initial exploration
- Column dropping
- Missing value analysis
- Rare job title grouping
- Data summary and validation
- Cleaned data export

---

## 🔍 Data Cleaning Summary

### Statistics:

| Metric | Before Cleaning | After Cleaning |
|--------|----------------|----------------|
| **Total Rows** | 105,434 | 105,434 |
| **Total Columns** | 11 | 9 |
| **Unique Job Titles** | 347 | 242 |
| **Missing Values** | 0 | 0 ✓ |
| **Rows in 'Other' Category** | 0 | 216 |

### Columns Dropped:
- `salary` - Redundant with salary_in_usd
- `salary_currency` - All values converted to USD

### Columns Retained:
- `work_year`
- `experience_level`
- `employment_type`
- `job_title` (cleaned)
- `salary_in_usd` (target)
- `employee_residence`
- `remote_ratio`
- `company_location`
- `company_size`

---

## 📈 Analysis Pipeline (in notebook.ipynb)

### 1. Data Cleaning & Preprocessing
*Contributor: Pramuditha R.M.H *
- Load and inspect data
- Drop unnecessary columns
- Handle rare categories
- Validate data quality

---

## 🤖 Models Implemented

### 1. Linear Regression (Statsmodels)


### 2. Neural Network (PyTorch MLP)

---

## 📊 Model Performance


---

## 🚀 How to Run

### Prerequisites:
```bash
pip install pandas numpy matplotlib seaborn statsmodels torch scikit-learn
```

### Execution:
1. Ensure `salaries.csv` is in the same directory as `notebook.ipynb`
2. Open `notebook.ipynb` in Jupyter Notebook or JupyterLab
3. Run all cells sequentially (Cell → Run All)

---

## 📝 Key Findings


---

**Last Updated:** October 2025  
**Project Status:** In Progress 🚧  
**Notebook Ready:** Yes ✓