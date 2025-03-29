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

![Image](https://github.com/user-attachments/assets/b3f23db3-dbcd-428a-aeb9-361b0e502d07)

- Cleaned Dataset
  
![Image](https://github.com/user-attachments/assets/60f2abe9-619a-4e48-90dd-693f63be2a32)

With missing values resolved, our data is now ready. It's time to save the cleaned dataset.

![Image](https://github.com/user-attachments/assets/9b1f1c5d-4c69-4c88-be91-9d00dfcf817e)

### Data Visualization

![Image](https://github.com/user-attachments/assets/7bb6d8fb-0fd1-42a6-996a-bd0ea4f066cb)

### Findings

- The number of consumer complaints generally increased from 2017 to 2022. The highest number of complaints was recorded in 2022. There is a noticeable drop in complaints after 2022.
- The increase indicates growing consumer awareness and worsening service quality.
- The drop after 2022 could be due to improved service quality or fewer consumers making use of the products.

- The most frequently reported complaint is related to managing an account, with significantly more cases than any other issue.
- Incorrect information on reports and problems with purchases on statements are also prevalent. These issues indicates errors in financial records, billing disputes, or identity verification problems.

- Based on financial products, the highest number of complaints relate to checking or savings accounts, suggesting widespread issues with account management, fees, access, or unauthorized transactions.
- Credit cards and prepaid cards are the second most common source of complaints, possibly due to fraudulent charges, billing disputes, or account closures.
- Credit reporting, credit repair services, and personal finance issues rank third, indicating errors on credit reports, disputes, and difficulties in credit scoring.
- Mortgage-related complaints suggest challenges with loan payments, refinancing, or foreclosure issues.
- Money transfer, virtual currency, and mobile payment issues are also significant, reflecting potential transaction failures or security concerns.

- The majority of complaints (72.33%) were submitted via the Web, indicating that consumers prefer online platforms for reporting issues.
- Referrals (17.5%) and Phone (7.44%) are the next most common submission methods, suggesting that some consumers rely on external sources or direct assistance for filing complaints.
- Postal mail, fax, web referral, and email have negligible usage, possibly due to the convenience of digital methods over traditional forms.

- Majority of Complaints Received a Timely Response 98.33% (58.12K complaints) were responded to on time. Most complaints were handled within the expected timeframe.
- 
