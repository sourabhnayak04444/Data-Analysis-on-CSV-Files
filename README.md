# Data-Analysis-on-CSV-Files

Pandas Sales Data Analysis 📊
This project is a simple data analysis exercise (Task 5) focused on analyzing sales data from a sales_data.csv file. It uses the Pandas library for data manipulation and aggregation, and Matplotlib (via Pandas' built-in .plot() function) to create visualizations.

🚀 Objective
The main goal is to load a sales CSV, perform basic data analysis to understand sales performance, and generate insightful charts.

This analysis answers three main questions:

What are the total sales for each product?

What is the sales distribution across different regions?

What are the total sales for each product category?

🔧 Tools Used
Python

Pandas: For data loading, manipulation, and aggregation (groupby, sum).

Matplotlib: For creating visualizations (bar chart and pie chart).

💻 Analysis Logic
The script follows a clear, step-by-step process to analyze the sales data:

Import Libraries: First, it imports the necessary libraries: Pandas (aliased as pd) for data handling and Matplotlib.pyplot (aliased as plt) for plotting.

Load Data: It uses the Pandas read_csv() function to load the sales_data.csv file into a DataFrame, which is like a spreadsheet or table in Python.

Inspect Data (Optional but Recommended): The script prints the first 5 rows using df.head() to confirm the data loaded correctly. It also uses df.info() to get a summary of the columns, data types, and check for any missing values.

Perform Aggregation: This is the core analysis step. The groupby() function is used to segment the data, and sum() is used to calculate totals for those segments.

Sales by Product: It groups all rows by the 'Product' column and then sums up the 'Sales' for each unique product.

Sales by Region: It groups all rows by the 'Region' column and sums up the 'Sales' for each region.

Sales by Category: It groups all rows by the 'Category' column and sums up the 'Sales' for each category.

Visualize Data: The script uses the built-in .plot() function directly on the aggregated Pandas data to create charts:

Product Sales: A bar chart (kind='bar') is created from the sales_by_product data. This is ideal for comparing the total sales of different, distinct items.

Region Sales: A pie chart (kind='pie') is created from the sales_by_region data. The autopct parameter is used to automatically add percentage labels, making it easy to see each region's share of the total sales.

Display Plots: plt.show() is called after each plot to display the visualization.
