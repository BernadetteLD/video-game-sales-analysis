 **Insight into Video Game Sales Analysis.**

**Purpose:**
This project analyses video game sales data to uncover global trends, top-performing platforms and games, and regional preferences by genre. Using Tableau, it demonstrates how interactive dashboards can communicate key business insights effectively.

Note: This is one of my first projects using Tableau. It reflects my learning process in data visualization and dashboard creation, and I aim to continue improving my analytical and visualization skills.

Dataset Source: Kaggle: Video Game Sales  
https://www.kaggle.com/datasets/gregorut/videogamesales  

### Key Columns Used:
- Name → Game name  
- Platform → Console / system  
- Year → Year of release  
- Genre → Game genre  
- NA_Sales, EU_Sales, JP_Sales, Other_Sales → Regional sales (millions)  
- Global_Sales → Total global sales (millions)

-------------------

**Questions & Analysis:**

### Q1: Which platforms had the highest global sales over time?

**Fields used:**
- Platform  
- Year  
- SUM(Global_Sales)

**Chart used:** Line chart  

**Steps:**
- Year → Columns (filtered from 2000–2020)  
- SUM(Global_Sales) → Rows  
- Platform → Color  
- Optional: Top 10 filter  

**Insight:**  
Platforms such as DS, PS2, and Wii show strong sales peaks, particularly around 2006–2010, indicating a period of high console market activity.


### Q2: Top 10 Best-Selling Games Globally and by Region

**Fields used:**
- Name  
- Global_Sales  
- NA_Sales  
- EU_Sales  
- JP_Sales  
- Other_Sales  

**Chart:**  
Bar chart (stacked by region)  

**Steps:**
- Name → Rows  
- SUM(Global_Sales) → Columns  
- Filter Top 10 by SUM(Global_Sales)  
- Measure Names → Color (show regions)  

**Insight:**  
Wii Sports is the top-selling game, with very high sales in North America. Games like GTA and Mario Kart also perform strongly. Overall, North America and Europe dominate global sales, while Japan and other regions contribute less.

### Q3: How Did Different Genres Perform in Different Regions?

**Fields used:**
- Genre  
- NA_Sales  
- EU_Sales  
- JP_Sales  
- Other_Sales  

**Chart:**  
Side-by-side bar chart or stacked bar chart  

**Steps:**
- Genre → Rows  
- Measure Values → Columns  
- Filter Measure Names → NA_Sales, EU_Sales, JP_Sales, Other_Sales  
- Measure Names → Color  

**Insight:**
- Action & Sports → strong in NA & EU  
- RPG → strong in JP  
- Shooter → dominates NA  

### Q4: Trends — Are Sales Increasing or Decreasing Over the Years?

**Fields used:**
- Year  
- Global_Sales  

**Chart:**  
Line chart  

**Steps:**
- Year → Columns  
- SUM(Global_Sales) → Rows  
- Add Trend Line (Analytics pane → Trend Line → Linear)  

**Insight:**  
Sales grew until around 2008–2010, then declined. Adding Platform as color helps identify which consoles drove the growth.


## Dashboard

**Title:**  
Video Game Sales Analysis Dashboard  

**Layout:**
- Top: Trend Over Time | Platform Over Time  
- Bottom: Genre by Region | Top 10 Games  

**Interactivity:**
- Add filter: Platform / Genre / Name → Show Filter  
- Apply to all worksheets → dashboard updates dynamically  

**Presentation Mode Tips:**
- Dashboard Size → Automatic or Custom (e.g., 1920×1080)  
- Chart Fit → Entire View  
- Use tiled layout for proper scaling  
-----------
## Key Steps Taken (for every sheet)

- Filtered out NULL values  
- Used Top N filters for clarity  
- Added labels and tooltips for better understanding  
------------
## Conclusion

The analysis shows that the video game industry experienced strong growth until around 2008–2010, followed by a gradual decline. Platforms such as DS, Wii, and PS2 played a major role in driving peak sales.  

Regional analysis highlights that North America and Europe dominate the market, while Japan shows distinct preferences for certain genres like RPGs.  

This project demonstrates how data visualization can be used to identify trends, compare performance, and communicate insights effectively.


## Interactive Dashboard
[View on Tableau Public](https://public.tableau.com/views/VideoGameSalesAnalysisDashboard_17750292751070/VideoGameSalesAnalysisDashboard?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
