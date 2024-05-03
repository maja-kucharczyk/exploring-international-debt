# Exploring the International Debt BigQuery Data

## Project Overview

The [International Debt Statistics](https://datacatalog.worldbank.org/search/dataset/0038015) dataset by The World Bank has reported the external debt of low- and middle-income countries and regions each year since 1970 (The World Bank, 2024). Debt is categorized by hundreds of different indicators. Google hosts the International Debt Statistics as a public BigQuery dataset called [International Debt](https://console.cloud.google.com/marketplace/product/the-world-bank/international-debt) (Google, 2024).

This repo contains a notebook (.ipynb) in which I explored the International Debt BigQuery data.

## Installation and Setup

### Code and Resources Used

- **Editor**: JupyterLab 4.0.11
- **Python Version**: 3.12.3

### Python Packages Used
- Data Manipulation:
  - `pandas` 2.2.2
  - `pandas-gbq` 0.22.0
- Data Visualization:
  - `matplotlib` 3.8.4
  - `seaborn` 0.13.2

## Data

### Dataset
- **Google BigQuery Dataset**: Google (2024)
- **Data Source**: The World Bank (2024)

### Project Files
- **kucharczyk_exploring_international_debt.ipynb**: notebook including code and output

### Data Exploration

The notebook (.ipynb) provides all details relating to data exploration.

After inspecting the international_debt table in the BigQuery dataset, I found that all 3.28 million rows had null year values and 94% of the rows had null debt values. In total, there were 138,152 rows with non-null and non-zero debt values, of which 2,467 were unique. The unique rows were grouped and joined to other tables in the dataset to determine the highest-debt countries, total debt owed by all countries, and debt per income group, region, and debt indicator. Due to the null debt and year values in the international_debt table, the BigQuery dataset currently appears limited in its use for exploring aggregate debt and temporal aspects. If the BigQuery dataset is fixed, the SQL queries can be rerun to derive accurate estimates.

## References

Google. 2024. International Debt. [https://console.cloud.google.com/marketplace/product/the-world-bank/international-debt](https://console.cloud.google.com/marketplace/product/the-world-bank/international-debt)

The World Bank. 2024. International Debt Statistics. [https://datacatalog.worldbank.org/search/dataset/0038015](https://datacatalog.worldbank.org/search/dataset/0038015)