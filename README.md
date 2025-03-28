# Consumer-Complaint Analysis

### Project Overview

This project analyzes customer complaints data to identify trends and common issues. This will help the business improve customer service, address frequent concerns, and enhance overall customer satisfaction.

### Data Source

The dataset for this analysis is sourced from Maven Analytics (https://mavenanalytics.io/data-playground?page=3&pageSize=5)

### Tools

- Python (JupyterLab)
- Microsoft PowerBI

### Imports

I imported pandas for loading, cleaning, manipulating, and analyzing structured data.

![Image](https://github.com/user-attachments/assets/f1c24033-ff21-4bc5-b54e-470ee11bbcf6)

### Data Wrangling

I designed my `wrangle` function to handle missing data efficiently.  
- First, I checked if any columns had more than 50% missing values. Since none met this threshold, I proceeded to drop rows where the **'Company public response'** column was empty. I chose this approach because the number of missing values was small, making deletion a better option than introducing a new category like "Unknown."
- Next, I addressed missing values in the **'Sub-issue'** column. I observed that NaNs only appeared when the **'Issue'** was **"Fraud or scam."** To handle this, I filled the missing values in **'Sub-issue'** with **"Fraud or scam"** for those specific rows.
- Finally, I handled missing values in the **'Sub-product'** column by grouping the data by **'Product'** and filling NaNs with the most frequently occurring value (**mode**) within each group. This ensured that missing **'Sub-product'** values were assigned the most relevant category based on their associated **'Product'** type.
