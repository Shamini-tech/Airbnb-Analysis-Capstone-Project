# Airbnb Analysis Capstone Project

An exploratory analysis of New York City Airbnb listings from 2019, done in Python in two notebooks: one using pandas and seaborn for exploration and charts, and one using SQL (SQLite and pandasql) to query the same data.

**Author:** Shamini S  
**Contribution:** Individual

---

## Project Overview

Airbnb hosts, travelers and platform stakeholders all benefit from understanding how listings are priced and distributed across a city. This project looks at the NYC 2019 listings data to see how prices differ between boroughs, which room types dominate, where listings are concentrated, and how the numerical variables relate to each other.

## Repository Contents

| File | Description |
|---|---|
| `Airbnb_Bookings_Analysis.ipynb` | Exploratory data analysis with data cleaning and five visual analyses |
| `Airbnb_sqlite_analysis.ipynb` | SQL exploration of the same dataset using `sqlite3` and `pandasql` |
| `AB_NYC_2019.csv` | The dataset (48,895 listings, 16 columns) |
| `requirements.txt` | Python libraries used |

## Dataset

The dataset is the Airbnb NYC 2019 listings file (`AB_NYC_2019.csv`), with 48,895 rows and 16 columns:

- **Listing details:** id, name, host id, host name, neighbourhood group (borough), neighbourhood, latitude, longitude
- **Accommodation attributes:** room type, price, minimum nights
- **Review metrics:** number of reviews, last review date, reviews per month
- **Host and availability:** number of listings per host, days available per year

Source: *[add the link to where you downloaded the dataset]*

## Notebook 1: Exploratory Data Analysis

**Data cleaning:** checked for duplicates (none found), filled missing `reviews_per_month` values with 0, and dropped rows with a missing listing or host name.

**Analyses:**

1. Average price by neighbourhood group (bar chart)
2. Most preferred room types (pie chart)
3. Top 10 neighbourhoods by number of listings (bar chart)
4. Price variation by neighbourhood group (box plot)
5. Correlation between numerical variables (heatmap)

## Notebook 2: SQL Data Exploration

Shows two ways of running SQL on the data from Python:

- **SQLite (`sqlite3`):** the data is stored in a database table and queried with `WHERE`, `BETWEEN`, `GROUP BY`, `HAVING`, `ORDER BY` and `LIMIT`
- **`pandasql`:** SQL, including a `CASE` expression, is run directly on a pandas DataFrame

## Key Findings

- Manhattan has the highest average nightly price (about $197) and the Bronx the lowest (about $88).
- Entire homes/apartments (52.0%) and private rooms (45.7%) make up almost all listings. Shared rooms are only 2.4%.
- Williamsburg and Bedford-Stuyvesant, both in Brooklyn, have the most listings.
- Prices are widely spread, with some listings priced at about $10,000 a night. These extreme values may be data errors and are worth checking.
- Price has only weak correlations with the other numerical variables.

## How to Run

1. Open a notebook in [Google Colab](https://colab.research.google.com/) (File → Upload notebook).
2. Upload `AB_NYC_2019.csv` using the folder icon on the left. The notebooks read it from `/content/AB_NYC_2019.csv`.
3. Choose **Runtime → Run all**.

To run locally instead, install the libraries with `pip install -r requirements.txt` and change the file path in the notebook to where the CSV is saved.

## Tools Used

Python, pandas, NumPy, matplotlib, seaborn, SQLite (`sqlite3`), pandasql, Google Colab
