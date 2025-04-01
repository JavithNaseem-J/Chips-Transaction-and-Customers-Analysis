# Chips Transactions and Customer Analysis

## Overview
Welcome to the Chips Transactions and Customer Analysis project! In this project, you’ll step into the role of a data analyst on Quantium’s retail analytics team, working for the Category Manager for Chips at a supermarket. The goal is to analyze customer purchasing behavior and transaction data to uncover insights about chip sales, customer segments, and trends. These insights will inform a strategic plan for the chip category over the next six months, focusing on increasing sales through targeted marketing and inventory optimization.

## Scenario
You are a data analyst on Quantium’s retail analytics team, tasked by the Category Manager for Chips, Julia, to better understand the types of customers purchasing chips and their behavior. The client wants to identify key customer segments, their purchasing patterns, and the drivers of chip sales to inform the upcoming category review. Your analysis will provide data-driven recommendations to optimize the chip category, supported by compelling insights and visualizations, to gain approval from the supermarket’s leadership.

## Objectives
- Examine transaction and customer data for inconsistencies, missing values, and outliers, ensuring a clean dataset for analysis.
- Analyze purchasing behavior, including total sales, quantity sold, and price per unit across customer segments.
- Identify trends in brand preferences, pack sizes, and seasonal purchasing patterns.
- Provide data-driven recommendations to target specific customer segments and optimize inventory for the chip category.

## Dataset
The dataset consists of two CSV files provided by Quantium:

- **QVI_transaction_data.csv**: Contains transaction details for chip purchases.
  - Columns: `DATE`, `STORE_NBR`, `LYLTY_CARD_NBR`, `TXN_ID`, `PROD_NBR`, `PROD_NAME`, `PROD_QTY`, `TOT_SALES`
- **QVI_purchase_behaviour.csv**: Contains customer demographic data.
  - Columns: `LYLTY_CARD_NBR`, `LIFESTAGE`, `PREMIUM_CUSTOMER`

## Prerequisites
To run this analysis, you'll need the following:

- Python 3.10+
- Jupyter Notebook or JupyterLab
- Required Python libraries:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `seaborn`
  - `plotly`
  - `re` (for regex operations)

Install the dependencies using pip:

```bash
pip install pandas numpy matplotlib seaborn plotly
```

## Methodology
### Data Loading and Cleaning:
- Loaded the transaction and customer data CSV files into pandas DataFrames.
- Checked for missing values, duplicates, and outliers; ensured data types were correct (e.g., `DATE` as datetime).
- Merged the transaction and customer datasets on `LYLTY_CARD_NBR` for a unified analysis dataset.

### Feature Engineering:
- Extracted pack size and brand from `PROD_NAME` using regex.
- Calculated `PRICE_PER_UNIT` as `TOT_SALES / PROD_QTY` to analyze spending patterns.

### Analysis:
- Explored total sales, quantity sold, and price per unit by customer segments (`LIFESTAGE`, `PREMIUM_CUSTOMER`).
- Analyzed seasonal trends, store performance, and pack size preferences.
- Visualized findings using bar charts, heatmaps, and line plots to identify trends in brand performance, customer behavior, and sales patterns.

## How to Run the Analysis
1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/chips-transactions-analysis.git
   cd chips-transactions-analysis
   ```
2. Ensure the `data` directory contains both CSV files (`QVI_transaction_data.csv` and `QVI_purchase_behaviour.csv`).
3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
4. Open `Chips_Transaction_Analysis.ipynb` and run all cells to reproduce the analysis and visualizations.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

---
