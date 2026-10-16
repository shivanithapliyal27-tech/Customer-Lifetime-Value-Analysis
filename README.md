# Customer Lifetime Value (CLV) Analysis

## Project Overview

This project focuses on estimating Customer Lifetime Value (CLV) using historical retail transaction data. The analysis explores customer purchasing behavior, revenue generation, order frequency, and customer segmentation to identify valuable customer groups and support data-driven business decisions.

## Project Objectives

- Analyze historical customer transaction data.
- Clean and prepare retail data for analysis.
- Calculate total revenue and total orders for each customer.
- Calculate Average Order Value (AOV) and customer recency.
- Estimate annualized historical customer revenue.
- Segment customers into four value-based groups.
- Develop business insights and customer retention recommendations.

## Dataset

**Dataset Name:** Online Retail II

**Source:** UCI Machine Learning Repository

Dataset link: https://archive.ics.uci.edu/dataset/502/online+retail+ii

The dataset contains retail transaction records, including invoice numbers, quantities, invoice dates, unit prices, customer IDs, and country information.

The original workbook contains two sheets:
- Year 2009-2010
- Year 2010-2011

## Tools and Technologies

- Python
- Pandas
- Matplotlib
- Microsoft Excel
- Google Colab

## Project Workflow

### 1. Data Loading
Loaded both yearly sheets from the Online Retail II workbook and combined them into one dataset.

### 2. Data Cleaning
- Removed duplicate records.
- Excluded records with missing Customer IDs.
- Excluded cancelled invoices identified by invoice numbers beginning with "C".
- Removed records with non-positive quantities or prices.
- Converted invoice dates into datetime format.

### 3. Revenue Calculation
Calculated transaction-line revenue using:

`Revenue = Quantity × Price`

### 4. Customer-Level Analysis
Calculated the following metrics for each customer:
- Total Revenue
- Total Orders
- Average Order Value
- First Purchase Date
- Last Purchase Date
- Customer Recency
- Estimated Annualized Revenue

### 5. Customer Segmentation
Grouped customers into four categories based on historical revenue:
- Low Value
- Medium Value
- High Value
- Top Value

### 6. Business Analysis
Compared revenue and customer counts across segments to identify opportunities for customer retention and targeted marketing.

## CLV Estimation Method

The baseline annualized historical revenue estimate is calculated as:

`Estimated Annual Revenue = Total Revenue / Observed Purchase Period in Days × 365`

The observed purchase period is measured from the customer's first to last recorded purchase, with a minimum denominator of one day.

This is a simple annualized revenue estimate rather than a validated prediction of future customer lifetime value.

## Deliverables

- Python analysis notebook (`.ipynb`)
- Customer Lifetime Value summary Excel workbook (`.xlsx`)
- Customer-level CLV table
- Customer segment analysis
- Revenue and customer distribution visualizations
- Project report (`.pdf`)

## Key Business Applications

- Identify historically high-revenue customers.
- Support customer retention strategies.
- Develop targeted marketing campaigns.
- Understand customer purchasing patterns.
- Compare revenue contribution across customer segments.

## Assumptions and Limitations

- Revenue is used as a proxy for customer value; it is not the same as profit.
- Annualized revenue estimates may be unusually high for customers with only one purchase or a short observation period.
- The analysis does not include customer acquisition costs, profit margins, discount rates, or future retention probabilities.
- Customer segments are based on historical revenue and do not guarantee future purchasing behavior.
- Results depend on the data-cleaning rules and the available observation period.

## Conclusion

This project demonstrates how Python and Excel can be used to analyze retail transactions, estimate customer revenue metrics, and segment customers by historical value. The findings can help businesses understand purchasing behavior and develop data-driven customer retention strategies.

