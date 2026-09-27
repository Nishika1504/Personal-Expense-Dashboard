# Personal Expense Dashboard -- Power BI

![Power
BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Domain](https://img.shields.io/badge/Domain-Power%20BI-purple?style=for-the-badge)
![Dataset](https://img.shields.io/badge/Dataset-1000%20Transactions-blue?style=for-the-badge)

## 👩‍💻 Internship Information

**Name:** Nishika Kumari\
**Intern ID:** CITS8816\
**Domain:** Power BI\
**Project:** Personal Expense Dashboard\
**Internship Organization:** CODTECH IT SOLUTIONS

------------------------------------------------------------------------

## 📌 Project Overview

The **Personal Expense Dashboard** is an interactive Business
Intelligence project developed using **Microsoft Power BI**.

The project transforms personal expense transaction data into a clear,
interactive, and professional dashboard. It helps users understand
spending patterns, monitor expenses, compare categories, analyze payment
methods, and explore individual transactions.

The project uses a dataset containing **1,000 personal expense
transactions** covering the year **2025**.

The dashboard uses a consistent **dark plum/purple and white theme** for
a clean professional presentation.

------------------------------------------------------------------------

## 🎯 Project Objectives

-   Analyze personal spending patterns.
-   Track total expenses and number of transactions.
-   Monitor monthly spending trends.
-   Identify major expense categories.
-   Compare category and subcategory spending.
-   Analyze expenses by payment method.
-   Compare Needs vs Wants.
-   Analyze expenses by city.
-   Identify top merchants based on spending.
-   Provide detailed transaction-level information.
-   Create an interactive and user-friendly Power BI dashboard.
-   Demonstrate practical Power BI and Business Intelligence skills.

------------------------------------------------------------------------

## 🗂️ Dataset Information

The dataset contains **1,000 expense records**.

  Column             Description
  ------------------ -------------------------------------------------
  `Expense_ID`       Unique identifier for each expense
  `Date`             Date of the transaction
  `Category`         Main expense category
  `Subcategory`      Detailed expense type
  `Description`      Short description of the expense
  `Amount_INR`       Expense amount in Indian Rupees
  `Payment_Method`   Method used for payment
  `City`             City associated with the expense
  `Merchant`         Merchant or service provider
  `Need_or_Want`     Indicates whether the expense is a Need or Want

### Main Categories

-   Food
-   Transport
-   Shopping
-   Bills & Utilities
-   Entertainment
-   Health
-   Education
-   Travel
-   Personal
-   Rent

### Payment Methods

-   UPI
-   Debit Card
-   Credit Card
-   Cash
-   Net Banking
-   Wallet

------------------------------------------------------------------------

# 📊 Dashboard Structure

## 🏠 Page 1 -- Executive Dashboard

Provides a high-level overview of personal expenses.

### KPI Cards

-   **Total Expenses**
-   **Total Transactions**
-   **Average Expense**
-   **Maximum Expense**

### Visualizations

-   Monthly Expense Trend
-   Expense by Category
-   Expense by Payment Method
-   Needs vs Wants
-   Top 10 Merchants

### Interactive Filters

-   Category
-   City
-   Payment Method
-   Need / Want

------------------------------------------------------------------------

## 📈 Page 2 -- Expense Analysis

Provides deeper insights into spending patterns.

### Analysis Included

-   Expense by Category and Subcategory
-   Monthly Expense by Category
-   Expense by City
-   Needs vs Wants by Category
-   Payment Method Distribution
-   Category-level expense comparison

This page helps users understand **where and how their money is being
spent**.

------------------------------------------------------------------------

## 📋 Page 3 -- Transaction Details

Provides a detailed view of individual expense records.

### Transaction Fields

-   Expense ID
-   Date
-   Category
-   Subcategory
-   Description
-   Amount
-   Payment Method
-   City
-   Merchant
-   Need / Want

### Interactive Filters

-   Category
-   City
-   Payment Method
-   Need / Want

This page allows users to move from high-level insights to individual
transaction records.

------------------------------------------------------------------------

# 🧮 DAX Measures

### Total Expenses

``` dax
Total Expenses =
SUM(Expenses[Amount_INR])
```

### Total Transactions

``` dax
Total Transactions =
COUNTROWS(Expenses)
```

### Average Expense

``` dax
Average Expense =
AVERAGE(Expenses[Amount_INR])
```

### Maximum Expense

``` dax
Maximum Expense =
MAX(Expenses[Amount_INR])
```

------------------------------------------------------------------------

# 📅 Date Table

A separate Date Table is used for time-based analysis.

It includes:

-   Date
-   Year
-   Month Number
-   Month
-   Month Year
-   Quarter

Example:

``` dax
DateTable =
CALENDAR(
    MIN(Expenses[Date]),
    MAX(Expenses[Date])
)
```

Additional columns:

``` dax
Year = YEAR(DateTable[Date])
```

``` dax
Month Number = MONTH(DateTable[Date])
```

``` dax
Month = FORMAT(DateTable[Date], "MMMM")
```

``` dax
Month Year = FORMAT(DateTable[Date], "MMM YYYY")
```

The `Month` column is sorted using `Month Number` to keep the months in
chronological order.

------------------------------------------------------------------------

# 🔗 Data Model

The report uses a simple date-to-expenses relationship:

``` text
DateTable
    |
    | 1 : *
    |
Expenses
```

Relationship:

``` text
DateTable[Date] → Expenses[Date]
```

------------------------------------------------------------------------

# 🎨 Dashboard Design

The dashboard uses a consistent dark plum/purple and white theme.

### Primary Color

``` text
#782058
```

### Supporting Colors

``` text
White      #FFFFFF
Light Pink #F4DCE9
Soft Pink  #E8B4D0
Dark Gray  #333333
```

------------------------------------------------------------------------

# 🛠️ Tools & Technologies

-   Microsoft Power BI Desktop
-   Power Query
-   DAX
-   Microsoft Excel / CSV
-   Data Modeling
-   Data Visualization
-   Business Intelligence

------------------------------------------------------------------------

# 🔄 Project Workflow

``` text
Raw Expense Data
       ↓
Data Loading
       ↓
Data Validation
       ↓
Data Cleaning
       ↓
Data Modeling
       ↓
Date Table Creation
       ↓
DAX Measures
       ↓
Data Visualization
       ↓
Interactive Filters
       ↓
Dashboard
       ↓
Business Insights
```

------------------------------------------------------------------------

# 📌 Key Features

-   1,000 expense transactions
-   Interactive Power BI dashboard
-   Three dashboard pages
-   KPI cards
-   Monthly trend analysis
-   Category and subcategory analysis
-   City-wise expense analysis
-   Payment method analysis
-   Needs vs Wants analysis
-   Top 10 merchant analysis
-   Transaction-level details
-   Interactive slicers
-   DAX calculations
-   Date table and relationship
-   Professional dark plum theme

------------------------------------------------------------------------

# 💡 Business Questions Answered

The dashboard can help answer:

1.  What is the total amount spent?
2.  How many transactions were recorded?
3.  What is the average expense per transaction?
4.  Which category has the highest spending?
5.  Which subcategory contributes most to spending?
6.  How does spending change month by month?
7.  Which city has the highest expenses?
8.  Which payment method is used most?
9.  How much is spent on Needs versus Wants?
10. Which merchants account for the highest spending?
11. What individual transactions contribute to total expenses?
12. How do spending patterns change when filters are applied?

------------------------------------------------------------------------

# 📁 Suggested GitHub Repository Structure

``` text
Personal-Expense-Dashboard-PowerBI/
│
├── README.md
│
├── Dataset/
│   ├── personal_expense_1000_dataset.csv
│   └── personal_expense_1000_dataset.xlsx
│
├── PowerBI/
│   └── Personal_Expense_Dashboard.pbix
│
└── Screenshots/
    ├── executive-dashboard.png
    ├── expense-analysis.png
    └── transaction-details.png
```

> Add your `.pbix` file and dashboard screenshots to the repository
> before submitting the project.

------------------------------------------------------------------------

# 🚀 How to Use

1.  Clone or download this repository.
2.  Open `PowerBI/Personal_Expense_Dashboard.pbix` in Power BI Desktop.
3.  If prompted, reconnect the report to the dataset in the `Dataset/`
    folder.
4.  Explore the three report pages.
5.  Use the slicers to interactively filter the dashboard.

------------------------------------------------------------------------

# 📷 Project Screenshots

After uploading your screenshots to GitHub, use:

``` markdown
## Executive Dashboard

![Executive Dashboard](Screenshots/executive-dashboard.png)

## Expense Analysis

![Expense Analysis](Screenshots/expense-analysis.png)

## Transaction Details

![Transaction Details](Screenshots/transaction-details.png)
```

------------------------------------------------------------------------

# 🎓 Skills Demonstrated

-   Power BI Dashboard Development
-   Power Query
-   Data Cleaning
-   Data Modeling
-   DAX
-   KPI Development
-   Time-Series Analysis
-   Interactive Reporting
-   Business Intelligence
-   Dashboard UI/UX Design
-   Data Analysis
-   Data Visualization

------------------------------------------------------------------------

# 👩‍💻 Author

**Nishika Kumari**\
**Intern ID:** CITS8816\
**Domain:** Power BI\
**Internship:** CODTECH IT SOLUTIONS

------------------------------------------------------------------------

## ⭐ Project Summary

The **Personal Expense Dashboard** demonstrates how raw financial
transaction data can be transformed into an interactive Business
Intelligence solution using Power BI.

The project combines data modeling, DAX calculations, interactive
filtering, and data visualization to provide a complete view of personal
spending behavior.

------------------------------------------------------------------------

## 📄 Internship Submission

**Project:** Personal Expense Dashboard\
**Name:** Nishika Kumari\
**Intern ID:** CITS8816\
**Domain:** Power BI
