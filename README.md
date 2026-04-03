**Co-developed with @burak-basoglu**

# Demand Forecasting-Based Inventory Management System

A data-driven decision support system that combines **demand forecasting**, **inventory-oriented analysis**, and **customer segmentation** to help businesses reduce stockouts, avoid overstock, and make more informed replenishment decisions.

---

## Overview

Inventory decisions are among the most critical drivers of operational efficiency in retail and supply chain environments. Underestimating demand can lead to **stockouts, lost sales, and dissatisfied customers**, while overestimating demand can result in **excess inventory, increased holding costs, and inefficient capital allocation**.

This project addresses that problem by building an end-to-end analytics workflow that:

- analyzes historical sales behavior,
- forecasts future demand across different time granularities,
- compares forecasting performance across models,
- supports inventory planning decisions with interpretable outputs,
- and enriches the business perspective with **RFM-based customer segmentation**.

The goal is not only to generate predictions, but to turn those predictions into a **practical inventory management and decision support framework**.

---

## Business Problem

Retail businesses need to make accurate stocking decisions in order to balance product availability and cost efficiency.

This project was developed to answer questions such as:

- Which products are likely to experience higher demand in upcoming periods?
- How can future sales be estimated using historical transactional data?
- Which forecasting approach performs better for this demand structure?
- How can forecast outputs support inventory planning and replenishment decisions?
- Which customer groups should be prioritized when inventory pressure or excess stock occurs?

By solving these questions, the system aims to support:

- smarter stock planning,
- reduced overstock and stockout risk,
- better resource allocation,
- and more targeted commercial actions.

---

## Project Objectives

The main objectives of this project are:

- Forecast product demand using historical sales data
- Compare forecasting models and identify the most suitable approach
- Build a business-friendly structure for inventory-oriented decision-making
- Aggregate demand at multiple time levels such as **weekly**, **monthly**, and **quarterly**
- Generate interpretable outputs for dashboarding and monitoring
- Integrate **RFM analysis** to support customer-focused actions, especially for products with stock pressure

---

## Solution Approach

This project follows a structured analytical pipeline:

1. **Data Preparation**
   - Raw sales and product-level data are cleaned and transformed
   - Temporal fields are standardized
   - Sales are aggregated for different forecasting horizons

2. **Exploratory Data Analysis**
   - Sales patterns, seasonality, and distribution behavior are examined
   - Product and time-based trends are analyzed
   - Inventory-relevant insights are extracted

3. **Demand Forecasting**
   - Historical demand is modeled to estimate future sales
   - Forecasting is performed at different aggregation levels
   - Model outputs are compared using performance metrics

4. **Model Evaluation**
   - Alternative forecasting approaches are evaluated against one another
   - Results are summarized in a model comparison layer
   - The best-performing setup is identified for decision support

5. **Customer Segmentation Support**
   - RFM analysis is incorporated to better interpret commercial actions
   - This allows the business to connect inventory decisions with customer value and loyalty patterns

6. **Dashboard / Application Layer**
   - Results are presented in a more accessible format for business interpretation
   - Summary tables and visualization-ready outputs are prepared for decision-makers

---

## Key Features

- Multi-step demand forecasting workflow
- Inventory-focused business framing
- Forecast aggregation at **weekly, monthly, and quarterly** levels
- Model comparison and performance tracking
- RFM-based customer segmentation support
- Dashboard-ready summary outputs
- Streamlit-based application structure for usability and presentation

---

## Tech Stack

**Programming Language**
- Python

**Core Libraries**
- pandas
- numpy
- scikit-learn
- tensorflow
   - recurrent neural networks
        - gru
        - lstm

**Application / Visualization**
- streamlit
- altair

---

## Project Structure

```bash
Demand-forecasting-based-inventory-management-system/
│
├── app.py                         # Streamlit application interface
├── main.py                        # Main execution pipeline
├── eda.py                         # Exploratory data analysis
├── forecasting.py                 # Forecasting workflow
├── rfm.py                         # RFM segmentation logic
├── run_analysis.py                # Analysis runner / helper script
├── requirements.txt               # Project dependencies
│
├── data/
│   ├── df.csv
│   ├── df_merged.csv
│   ├── weekly_sales.csv
│   ├── monthly_sales.csv
│   ├── quarterly_sales.csv
│   ├── aggregated_weekly_sales.csv
│   ├── aggregated_monthly_sales.csv
│   ├── aggregated_quarterly_sales.csv
│   ├── model_comparison.csv
│   ├── dashboard_summary.csv
│   ├── dashboard_summary_main.csv
│   └── rfm_results.csv
│
└── .git/
