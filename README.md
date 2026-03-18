## 🌍 World GDP - ETL Pipeline
This project is a complete ETL (Extract, Transform, Load) pipeline that gathers GDP data of countries from a Wikipedia archive. It automates the process of data collection, cleans the currency formatting, converts the scale, and stores the results in multiple formats.

## 🛠️ Project Architecture
* Stage,Function,Description *

Extract,extract(),Scrapes the archived Wikipedia page using BeautifulSoup.

Transform,transform(),Converts USD Millions (string) to USD Billions (float) and rounds to 2 decimal places.

Load,load_to_csv/db(),Saves the cleaned data to Countries_by_GDP.csv and World_Economies.db.

Logging,log_progress(),Records every step with a timestamp in etl_project_log.txt.

## 🚀 How to Run
# 1. Install Dependencies
Make sure you have the necessary Python libraries:
pip install requests pandas numpy beautifulsoup4

# 2. Execute the Pipeline
Run the main script from your terminal:
python3 etl_project_gdp.py

## 📈 Output & Results
* Once the script completes, you will find: *
 *Countries_by_GDP.csv:* A structured dataset of world economies.

 *World_Economies.db:* A database table named Countries_by_GDP.

 *etl_project_log.txt:* A log file showing exactly when each phase started and finished.

 # Automated Query
 At the end of the process, the script automatically runs a SQL query to display all countries with a GDP greater than or equal to 100 Billion USD.

 ## 📝 Technical Notes
 *Source:* International Monetary Fund (IMF) data archived via the Wayback Machine.

 *Data Cleaning:* The script handles commas in numeric strings and filters out non-country rows automatically.

 *Database:* Uses sqlite3 for local storage, replacing the table on each run to ensure data is current.
