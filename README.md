# 🏢 Crexi Real Estate Data Scraper

This project is a web scraping script designed to collect commercial real estate data from [Crexi](https://www.crexi.com). The collected data includes building names, addresses, broker names, and broker phone numbers from different U.S. states.

## 📁 Project Structure

The project includes multiple `.csv` files, each containing scraped data for a specific state or region:

- `crexi_302.csv`
- `crexi_Arizona.csv`
- `crexi_Florida_1.csv`
- `crexi_Florida_2.csv`
- `crexi_Florida_3.csv`
- `crexi_Georgia_482.csv`
- `crexi_New_Mexico.csv`
- `crexi_North_Carolina.csv`
- `crexi_Ohio.csv`
- `crexi_Oklahoma.csv`
- `crexi_Texas1.csv`
- `crexi_Texas2.csv`

Each file contains rows with the following columns:

- `Building Name`
- `Address`
- `Broker`
- `Broker Phone`

## 🧠 How it works (script overview)

> ⚠️ Note: The scraping script is not included in this repo for privacy reasons.

The script uses:
- `cloudscraper` to bypass anti-bot protections
- `pandas` to handle and save data
- `re` for regular expression parsing
- A loop to go through listing pages by state

Typical data extraction looks like:
```python
rows.append({
    'Building Name': name,
    'Address':       address,
    'Broker':        broker_name,
    'Broker Phone':  phone
})
