# Flipkart Mobile Phone Web Scraping and Data Extraction using Python

A Python web scraping project that extracts mobile phone listings from Flipkart, parses unstructured HTML content, and transforms raw text into a clean, structured dataset using Requests, BeautifulSoup, Pandas, and Regular Expressions.

## Overview

This project scrapes mobile phone product data from Flipkart search result pages, handles bot-detection using custom HTTP headers, and parses raw HTML into structured fields. Unstructured feature text is converted into clean columns (Processor, RAM, ROM, Battery, Display Size, Camera) using Regex pattern matching. The final dataset is cleaned, type-converted, and exported to CSV for further analysis.

## Key Features

- Web scraping of live e-commerce data using Requests and BeautifulSoup
- HTTP header spoofing to bypass 403 Forbidden bot-blocking errors
- HTML parsing and DOM traversal using CSS class selectors
- Multi-page scraping with pagination handling (automated loop across 10+ pages)
- Text preprocessing and feature engineering using Regular Expressions (Regex)
- Extraction of structured attributes from unstructured text: Brand, Processor, RAM, ROM, Battery, Display Size, Camera
- Data cleaning and type conversion using Pandas (string to float, currency formatting)
- Missing value handling with NumPy
- Export of cleaned dataset to CSV format
- Data analysis ready output using Pandas DataFrame

## Tech Stack and Tools

- **Programming Language:** Python
- **Libraries:** Requests, BeautifulSoup4, Pandas, NumPy, Regular Expressions (re), Matplotlib, Seaborn
- **Techniques:** Web Scraping, HTML Parsing, Data Extraction, Data Cleaning, Data Wrangling, Regex Text Processing, Data Preprocessing
- **Environment:** Jupyter Notebook

## Project Workflow

1. **Send HTTP Request** — Request the Flipkart search results page using the Requests library.
2. **Bypass Bot Detection** — Add a browser User-Agent header to avoid HTTP 403 errors.
3. **Parse HTML** — Use BeautifulSoup to parse the page content and locate product elements by CSS class.
4. **Extract Raw Fields** — Pull product name, price, rating, number of ratings/reviews, and feature list for each listing.
5. **Automate Pagination** — Loop through multiple search result pages to collect a larger dataset.
6. **Structure the Data** — Load extracted data into a Pandas DataFrame.
7. **Clean and Convert** — Convert price and rating fields from string to numeric (float) types.
8. **Feature Engineering with Regex** — Extract Brand, Processor, RAM, ROM, Battery, Display Size, and Camera details from unstructured text using Regex patterns.
9. **Finalize Dataset** — Reorder columns and drop intermediate/raw columns.
10. **Export Data** — Save the final cleaned dataset as a CSV file (`Flipkart Phones.csv`).

## Dataset Output Columns

| Column | Description |
|---|---|
| Brand | Mobile phone manufacturer |
| Product_name | Full product title |
| Processor | Processor/chipset name |
| RAM | RAM capacity |
| ROM | Storage capacity |
| Battery | Battery capacity (mAh) |
| Display_Size | Screen size (inches) |
| Camera | Camera configuration |
| No_of_ratings | Total number of ratings |
| No_of_reviews | Total number of reviews |
| Rating | Average product rating |
| Price | Product price (INR) |

## How to Run This Project

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/flipkart-mobile-phone-web-scraping.git
   ```
2. Install the required dependencies:
   ```bash
   pip install requests beautifulsoup4 pandas numpy matplotlib seaborn
   ```
3. Open the Jupyter Notebook:
   ```bash
   jupyter notebook Web_Scraping.ipynb
   ```
4. Run all cells to scrape data and generate `Flipkart Phones.csv`.

## Skills Demonstrated

Python Programming, Web Scraping, Data Extraction, HTML/DOM Parsing, BeautifulSoup, Requests Library, Regular Expressions (Regex), Data Cleaning, Data Wrangling, Data Preprocessing, Pandas, NumPy, Exploratory Data Analysis (EDA) readiness, CSV Data Export, Problem Solving, Automation.

## Future Improvements

- Migrate to Selenium or Playwright for JavaScript-rendered content and dynamic pagination
- Add automated data validation and outlier detection
- Schedule periodic scraping using cron jobs or Airflow for price tracking
- Build an exploratory data analysis (EDA) notebook with visualizations
- Store data in a relational database instead of CSV

## Disclaimer

This project is intented for portfiloio purposes only

## Author
**Noman Ellahi**
