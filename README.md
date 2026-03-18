## 🌍 World GDP - ETL Pipeline
This project is a complete ETL (Extract, Transform, Load) pipeline that gathers GDP data of countries from a Wikipedia archive. It automates the process of data collection, cleans the currency formatting, converts the scale, and stores the results in multiple formats.

## 🛠️ Project Architecture
Stage,Function,Description
Extract,extract(),Scrapes the archived Wikipedia page using BeautifulSoup.
Transform,transform(),Converts USD Millions (string) to USD Billions (float) and rounds to 2 decimal places.
Load,load_to_csv/db(),Saves the cleaned data to Countries_by_GDP.csv and World_Economies.db.
Logging,log_progress(),Records every step with a timestamp in etl_project_log.txt.
