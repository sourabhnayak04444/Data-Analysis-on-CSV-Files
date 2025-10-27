# Data-Analysis-on-CSV-Files

# Pandas Sales Data Analysis 📊

This project is a simple data analysis exercise (Task 5) focused on analyzing sales data from a `sales_data.csv` file. It uses the Pandas library for data manipulation and aggregation, and Matplotlib (via Pandas' built-in `.plot()` function) to create visualizations.

---

## 🚀 Objective

The main goal is to load a sales CSV, perform basic data analysis to understand sales performance, and generate insightful charts.

This analysis answers three main questions:
1.  What are the total sales for each product?
2.  What is the sales distribution across different regions?
3.  What are the total sales for each product category?

---

## 🔧 Tools Used

* **Python**
* **Pandas:** For data loading, manipulation, and aggregation (`groupby`, `sum`).
* **Matplotlib:** For creating visualizations (bar chart and pie chart).

---

## 💻 Analysis Code

This is the complete Python script used for the analysis.

```python
import pandas as pd
import matplotlib.pyplot as plt

# 1. Load CSV using Pandas
df = pd.read_csv('sales_data.csv')

# Display the first 5 rows
print("--- First 5 Rows ---")
print(df.head())

# Display data info
print("\n--- Data Info ---")
df.info()

# 2. Use groupby() and sum()
# Calculate total sales per product
sales_by_product = df.groupby('Product')['Sales'].sum()
print("--- Total Sales by Product ---")
print(sales_by_product)

# Calculate total sales per region
sales_by_region = df.groupby('Region')['Sales'].sum()
print("\n--- Total Sales by Region ---")
print(sales_by_region)

# Calculate total sales per category
sales_by_category = df.groupby('Category')['Sales'].sum()
print("\n--- Total Sales by Category ---")
print(sales_by_category)

# 3. Use plot()
# Plot Total Sales by Product
sales_by_product.plot(kind='bar', title='Total Sales by Product')
plt.xlabel('Product')
plt.ylabel('Total Sales ($)')
plt.xticks(rotation=45)
plt.show()

# Plot Sales Distribution by Region
sales_by_region.plot(kind='pie', autopct='%1.1f%%', title='Sales Distribution by Region')
plt.ylabel('') # Hide the 'Sales' y-label for pie charts
plt.show()
