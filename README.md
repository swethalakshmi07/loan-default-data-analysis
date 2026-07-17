# Loan Default Analysis — Power BI Dashboard

An interactive Power BI dashboard analyzing loan default patterns, applicant demographics, and risk metrics for a lending portfolio.

## 📊 Overview

This project explores a loan applicant dataset to identify factors associated with loan defaults — including employment type, credit score, income, age, and marital status — helping surface risk segments and trends across years. Built entirely in Power BI Desktop using DAX measures, area/ribbon/donut visuals, and a decomposition tree for root-cause exploration.

## 🗂️ Dashboard Pages

**1. Loan Default Overview**
- Loan amount by purpose
- Average income by employment type
- Default rate (%) by employment type
- Average loan amount by age group
- Default rate (%) by year

**2. Applicant Demographics**
- Median loan amount by credit score bins
- Average loan by age group and marital status (donut chart)
- Total loan amount (adults) by credit score bins
- Number of loans by education type
- Clustered column breakdown of applicant segments

**3. Final Risk Metrics**
- Area chart trends on risk indicators
- Ribbon chart comparing category rankings over time
- Decomposition tree for drilling into default drivers (e.g., by income, credit score, employment type)

## 🧮 Key DAX Measures

| Measure | Description |
|---|---|
| `Average Loan by Age Group` | Mean loan amount segmented by age bracket |
| `Default Rate by Employment type` | % of loans defaulted, grouped by employment type |
| `Default Rate by Year` | % of loans defaulted per year |
| `Median by Credit score bins` | Median loan amount across credit score ranges |
| `Total Loan (Credit Bins)` | Total loan value by credit score bin |
| `Total Loan (Middle Age Adults)` | Total loan value for the middle-age applicant segment |
| `Loans by Education type` | Count of loans grouped by education level |
| `YOY Default Loans change` | Year-over-year change in defaulted loan count |
| `YOY Loan Amount Change` | Year-over-year change in total loan amount |
| `YTD Loan Amount` | Year-to-date total loan amount |

## 🗃️ Data Model

**Loan_default table** — applicant-level fields:
`Age Groups`, `Credit Score Bins`, `Education`, `EmploymentType`, `HasDependents`, `HasMortgage`, `Income`, `Income Bracket`, `LoanAmount`, `LoanPurpose`, `Loan_Year`, `MaritalStatus`

**Measure table** — holds the standalone DAX measures listed above, kept separate from the data table as a Power BI best practice.

## 🛠️ Tools & Skills Used
- **Power BI Desktop** — data modeling, DAX, report design
- **DAX** — calculated measures for default rates, YoY change, and bracketed aggregations
- **Power Query** — data cleaning, binning (age groups, credit score bins, income brackets)
- **Data Visualization** — area, donut, ribbon, and clustered column charts; decomposition tree for root-cause drill-down


