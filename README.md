
# 🍽️ Zomato Bangalore Restaurants – Data Cleaning & EDA

This project focuses on cleaning and analyzing the Zomato Restaurants dataset specific to Bangalore. The goal is to make the data analysis-ready and extract meaningful insights about the restaurant landscape in the city.

---

## 🧹 1. Data Cleaning Summary

The original dataset contained various inconsistencies, missing values, and duplicate records across restaurant branches. The following steps were carried out to clean the data:

- Removed extra parameters from the `url` field and identified duplicate entries.
- Dropped unnecessary columns such as `phone`, `menu_item`, and `dish_liked`.
- Cleaned and standardized the `rate` column:
  - Removed `/5`, converted to float, and handled values like `"NEW"` and `"-"`.
  - Filled missing ratings using review text (`reviews_list`), grouped means (by `url`, `name`, `rest_type`), and final mean imputation.
- Converted `cost_for_two` values to float by removing commas.
- Handled missing `rest_type` using mode from `listed_in(type)`, and filled missing `cuisines` as `"Unknown"`.
- Grouped restaurants by `url` to merge multiple entries per branch into a single row using aggregation functions.
- Verified that no null values remained and all columns had proper data types.

✅ Final Output: A clean dataset with **no missing values**, **no duplicates**, and **uniform formatting**, ready for EDA.

---

## 📊 2. Exploratory Data Analysis Summary

The cleaned dataset was analyzed to understand restaurant trends in Bangalore. Here's how the EDA was structured:

### 🧾 Data Overview
- Confirmed data completeness and structure.
- Identified 12,453 unique restaurants (by URL) and 8,758 unique names.

### 🍽️ Restaurant Names
- **Café Coffee Day**, **Domino’s Pizza**, and **Just Bake** had the most branches across Bangalore.

### ⭐ Ratings
- Most ratings ranged from 3.5 to 4.0.
- Average ratings calculated to identify highly rated chains like **Truffles** and **Onesta**.

### 🗳️ Votes
- Majority of restaurants received fewer than 300 votes.
- Restaurants offering both **online ordering** and **table booking** had significantly higher votes.

### 💰 Cost for Two
- Typically ranged between ₹200–₹600.
- Higher costs observed for restaurants with table booking services.

### 📦 Online Order & Table Booking
- 52% support online ordering; only 8% support table booking.
- Restaurants offering both services showed better customer engagement.

### 🏢 Restaurant Type
- Most common types: **Quick Bites**, **Casual Dining**, **Cafes**.

### 📋 Listed Categories
- Major Zomato categories: **Delivery**, **Dine-out**.

### 🍛 Cuisines
- **North Indian** cuisine was the most common, followed by **Chinese** and **South Indian**.

### 📍 Location Analysis
- Top restaurant-dense areas: **Whitefield**, **Indiranagar**, **Koramangala 5th Block**, **HSR Layout**.

---

## 🏆 Best Locations in Bangalore (Final Insight)

By combining all factors—**restaurant count, votes, ratings, cuisine diversity, and services**—the best food zones in Bangalore were found to be:

- **Whitefield**
- **Indiranagar**
- **Koramangala 5th Block**

These areas offer the richest restaurant experience with high-quality service, variety, and customer engagement.

---

## 📁 Files Included

- `Zomato Data Cleaning.ipynb` – Complete notebook for data preprocessing.
- `Zomato Cleaned Data EDA.ipynb` – Exploratory Data Analysis on the cleaned dataset.
- `Fully Cleaned Zomato Data.csv` – Final processed dataset ready for modeling or dashboards.

---

## 📌 Tools Used

- Python (Pandas, NumPy)
- Matplotlib, Seaborn, Plotly
- Jupyter Notebook

---

## 📈 Future Work

- Build interactive dashboards using Power BI / Tableau.
- Develop recommendation systems or predictive models.
- Analyze trends over time if temporal data is available.

---

## 📬 Contact

For questions or collaborations, feel free to reach out via GitHub or LinkedIn.
