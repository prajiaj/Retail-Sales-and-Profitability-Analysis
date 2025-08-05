# 📊Retail-Sales-and-Profitability-Analysis
This project demonstrates an end-to-end data analytics workflow involving data transformation (ETL), data warehousing, and business intelligence reporting using a retail dataset. The focus is on uncovering trends in sales performance, customer behavior, and profit margins over a 4-year period. 

## 🧩Key objectives include:

  - Identifying top-performing product categories
  - Analyzing regional and segment-level sales
  - Exploring profit margins and discount impacts
  - Creating KPIs and dashboards for decision-making

## 🛠 Technologies & Tools Used
  - Alteryx ETL(Extract, Transform, Load) operations including data cleaning, derived metrics, and binning.
  - Snowflake(Data Warehousing, To store and query the transformed data)
  - Power BI(Data Visualization,KPIs)
  - GitHub(Version Control)
    
## Project Workflow
**1️⃣Data Source**
  - Dataset: Superstore Sales Data (Superstore_Raw.csv)
  - Contains 21 columns including order info, customer, product, sales, profit, discount, etc.
  <br>
  <img width="530" height="625" alt="Souce data directory" src="https://github.com/user-attachments/assets/c119f5b9-0c91-450e-9465-d2abd6d15604" />
  <br>
  <br>
**ETL in Alteryx**   
 - Cleaned missing/duplicate data
 - Created calculated fields:1️⃣Profit Margin = Profit / Sales 2️⃣Margin Tier: Binned Profit Margin into categories (Low, Medium, High)
 - Formatted numeric fields (e.g., rounded to 2 decimals)
 - Exported the result as Superstore_Transformed.csv
 <br>
 <img width="1566" height="846" alt="Alteryx workflow data" src="https://github.com/user-attachments/assets/d8997fb1-423e-400e-88cd-66b7f2d67249" />
 <br>
 <br>

 **Data Warehousing**
  - Created a dedicated Snowflake Database.
  - Loaded the cleaned and enriched dataset into a Snowflake table using the import wizard.
  <br>
  <img width="1597" height="918" alt="Snowflake Load preview" src="https://github.com/user-attachments/assets/12bd7da9-3735-4b10-bb4c-c49ad3e5912b" />
  <br>

  **Visualization in Power BI**  
    - Built 2-page report with:
    - KPIs: Sales, Profit, AOV, Profit Margin, Orders
     <br>
     <img width="577" height="285" alt="KPIs" src="https://github.com/user-attachments/assets/6b1a8eab-30f7-42a2-95da-bd4849f900cd" />
     <br>
     <br> 
## Report Page
  **Executive KPIs at a Glance**
    - Total Sales: $2.30M
    - Total Profit: $2,86,397
    - Total Orders: 5K
    - Total Quantity: 37,873
    - Profit Margin: 12.47%
    - Average Order Value: $458.6
    **Category-Level Insights**
      - Sales and Profit by Category (Bar charts for Technology, Furniture, Office Supplies)
      - Quickly identifies the highest and lowest performing product categories.
    **Segment and Region Analysis**
      - Donut Charts to show quantity distribution by:
      - Customer Segment (Consumer, Corporate, Home Office)
      - Region (West, East, Central, South)
    **Shipping Mode Analysis**
      - Bar chart showing order distribution by Ship Mode: Standard, Second Class, First Class, and Same Day.  
    **Sub-Category Sales Analysis**
      - Bar chart of Sales by Sub-Category (Phones, Chairs, Storage, Tables, etc.)
      - Highlights top-performing products at a granular level.
    **Discount vs. Profit Impact**
      - Line and area chart showing profit trends by discount tiers, visualizing the tradeoff between discounts and profitability.
    **Dynamic Slicers for Filtering**
      - Interactive filters for: Year, Region, Ship, Mode, Category
      - Allows users to drill down into specific dimensions.
      <br>
     <img width="1376" height="773" alt="Report Page" src="https://github.com/user-attachments/assets/cb0d2fac-e08b-4dee-b7c9-f1a1716c1f84" />
     <br>
     <br>
     <br>
 ## Overview Page     
  **Top City Performance**
    - Separate cards showing cities ranked by: Profit, Sales, Orders, Quantity
    - Highlights cities driving most revenue and transactions.
   **Customer-Level Performance Table**
    - Detailed table with: Customer Name, Segment, Ship Mode, Category, Region, City, State, Country, Quantity, Sales, Profit.   
          <br>
          <img width="1358" height="771" alt="Overview Page" src="https://github.com/user-attachments/assets/7c964e1c-7b1a-4dee-af36-a5220ff83d29" />

