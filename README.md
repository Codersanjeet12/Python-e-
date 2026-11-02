# Python-e-
Pytjom e  Visualijattionion
# Bank Marketing Campaign Analysis | EDA + Power BI Dashboard

## Overview
This project analyses a bank's telemarketing campaign data to understand **which customers subscribe to a term deposit** and what drives that decision. It covers the full workflow: data cleaning and EDA in Python, followed by an interactive Power BI dashboard for business insights.

## Dataset
- **Records:** 45,211 customers
- **Features:** 19 columns (after cleaning, extra columns are derived)
- **Target:** `response` (whether the customer subscribed to a term deposit: yes / no)
- **Key columns:** age, salary, balance, marital status, job, education, loan status, contact type, month of contact, call duration, number of contacts, previous campaign outcome

## Data Cleaning (Python)
- Skipped junk header rows while loading the CSV
- Handled missing values: dropped rows with missing `age` (very few), filled `month` with the mode and `response` with `no`
- Split `jobedu` into separate `job` and `education` columns
- Converted `duration` from mixed values (sec/min) into a single numeric column in minutes
- Parsed `month` into `month_name` and `year`, and removed the unused `customerid` column
- Renamed columns for clarity (`housing loan`, `personal loan`)
- Created new features: `age_group`, `balance_group`, `response_flag`

## Exploratory Data Analysis
Univariate, bivariate and multivariate analysis using Matplotlib and Seaborn to study the distribution of customer attributes and their relationship with the subscription outcome.

## Power BI Dashboard
**KPIs:** Total Customers, Subscribers, Conversion Rate, Average Balance

**Visuals:**
- Conversion rate by job, age group and education
- Monthly campaign trend
- Response split (yes / no)
- Impact of previous campaign outcome
- Slicers for job, education, marital status, loans and contact type

**DAX measures used:** Conversion Rate, Total Customers, Subscribers, Avg Balance, Avg Call Duration

## Key Insights
- [Which job groups convert best]
- [Which age group responds most]
- [Effect of call duration on subscription]
- [Best and worst performing months]
- [Impact of previous campaign success]

## Tools & Technologies
Python (Pandas, NumPy, Matplotlib, Seaborn), Jupyter Notebook, Power BI, DAX

## Project Structure
```
├── EDA.ipynb                  # Data cleaning and analysis
├── bank_marketing_clean.csv   # Cleaned dataset used in Power BI
├── dashboard.pbix             # Power BI dashboard
├── dashboard_preview.png      # Dashboard screenshot
└── README.md
```

## How to Run
1. Clone the repository
2. Install dependencies: `pip install numpy pandas matplotlib seaborn`
3. Open `EDA.ipynb` and run all cells to generate the cleaned CSV
4. Open `dashboard.pbix` in Power BI Desktop

## Author
**Sanjeet Kumar**
Post-Graduate Program in Data Science & AI, Digicrome Academy
[LinkedIn] | [GitHub]
