
# 🍽️ Zomato Bangalore Restaurants – Data Cleaning & EDA

This project involves cleaning and analyzing the Zomato restaurant dataset for Bangalore to make it suitable for insights, modeling, and visualization.

---

## 🧹 1. Data Cleaning Summary

### 🎯 Objective
To clean and preprocess the Zomato Bangalore dataset by handling missing values, fixing duplicates, correcting data types, and consolidating multi-row entries.

### 🔧 Process Overview

1. **Data Loading & Checks**
   - Loaded using `pandas` and explored with `.info()`, `.nunique()`, `.head()`.

2. **Cleaning URLs & Removing Duplicates**
   - Removed redundant URL context parameters.
   - Detected multiple rows per restaurant due to variations in category.

3. **Dropping Columns**
   - Removed `phone`, `menu_item`, and `dish_liked` due to high null counts or low relevance.

4. **Rating Imputation**
   - Cleaned `rate` column, extracted ratings from `reviews_list`, and filled missing values using grouped means (by `url`, `name`, `rest_type`), finishing with global mean.

5. **Cost for Two**
   - Renamed, cleaned, and converted the column. Missing values filled based on restaurant type averages.

6. **Restaurant Type & Cuisines**
   - Filled missing `rest_type` using mode by `listed_in(type)`.
   - Filled missing `cuisines` as `"Unknown"`.

7. **Location & City**
   - Filled missing `location` from `address`, then dropped `address` and `listed_in(city)`.

8. **Grouping Duplicate Entries**
   - Grouped by `url` and aggregated to create single entries per restaurant.

9. **Final Fixes**
   - Used restaurant name and type to impute final missing values in rating and cost.

✅ Final Result:
- No nulls or duplicates.
- All columns cleaned and properly typed.
- Dataset ready for EDA and modeling.

---

## 📊 2. Exploratory Data Analysis Summary

### 📋 Overview
- Confirmed 12,453 unique restaurants and 8,758 unique names.
- All columns validated and cleaned.

### 🍴 Restaurant Names
- Café Coffee Day had the most branches (54), followed by Domino’s and Just Bake.

### ⭐ Ratings
- Most ratings ranged from 3.5 to 4.0.
- Top-rated chains: Truffles, Onesta.

### 🗳️ Votes
- Majority had <300 votes, but some had >16,000.
- Restaurants with both table booking & online ordering had more votes and higher ratings.

### 💵 Cost for Two
- Typically ₹200–₹600.
- Higher costs for restaurants offering table booking.

### 📦 Online Order & Table Booking
- 52% offer online ordering.
- Only 8% support table booking.
- Combined services led to better engagement.

### 🏢 Restaurant Type
- Most common: Quick Bites, Casual Dining, Cafes.

### 🧾 Listed Category
- Mostly listed as Delivery and Dine-out; niche tags like Cafes and Desserts also present.

### 🍛 Cuisines
- North Indian most common, followed by Chinese and South Indian.
- Multi-cuisine restaurants common.

---

## 📍 Location Analysis

- **Whitefield** had the most restaurants (884).
- **Indiranagar** was the most popular based on votes (~250k).
- **Lavelle Road** and **Sankey Road** had highest average ratings (4.0).
- **Sankey Road** also had highest average cost (~₹2500).
- **Race Course Road** and **St. Marks Road** also notable for high quality.

---

## 🏆 Best Locations in Bangalore

Based on combined factors like rating, cost, votes, cuisine variety, and availability:

- **Whitefield**
- **Indiranagar**
- **Koramangala 5th Block**

These locations are ideal dining zones offering excellent variety and high customer engagement.

---

## 📁 Files Included

- `zomato.csv`
- `Zomato Data Cleaning.ipynb`
- `Fully Cleaned Zomato Data.csv`
- `Zomato Data Cleaning Summary.pdf`
- `Zomato Cleaned Data EDA.ipynb`
- `Zomato Data EDA Summary.pdf`

---

## 🛠️ Tools Used

- Python (Pandas, NumPy)
- Jupyter Notebook
- Seaborn, Matplotlib

---

## 🙌 Author & Contact

This project was carried out as part of personal learning and portfolio building.  
For questions or collaborations, feel free to reach out on GitHub or LinkedIn.
