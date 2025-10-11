🛍️💰 Clothing Retail Analytics Project

Empowering a small Swiss clothing retail business to save money, save time, and increase income through data-driven insights.

📖 Project Overview

This project analyzes data from a small clothing retail business located across Swiss towns (e.g., Zurich, Geneva, Lausanne, Bern, Basel).
The goal is to leverage data analytics and machine learning to make smarter business decisions — helping the shop:

✅ Save Money: Detect unprofitable products, overstocked inventory, and low-ROI marketing campaigns.
⏱️ Save Time: Optimize restocking schedules and employee work allocation.
💸 Increase Income: Promote high-selling products, focus on loyal customers, and invest in effective marketing channels.

Key Analyses:

Top 10 Products Sold: Identify best-selling items for targeted promotions and inventory planning.

Sales by Day of the Week: Detect peak shopping days for optimal staffing and marketing push.

Marketing Channel ROI: Evaluate campaign performance to spend smarter.

Loss Detection: Spot unprofitable products, excessive stock, or low-performing campaigns.

📊 Dataset Description

This dataset represents 6 key business areas collected over 6 months of operations.

Table	Records	Key Columns	Business Use
Customers (customer_table-sheet1-sourcetable.csv)	150	Customer_ID, Gender, Age, Town, Visit_Frequency_per_month, Loyalty_Status, Email_Domain	Understand demographics and loyalty trends
Products (product_table-sheet1-sourcetable.csv)	50	Product_ID, Product_Name, Category, Cost_Price_CHF, Selling_Price_CHF, Stock_Level_initial	Track product margins and stock levels
Sales (sales_table-sheet1-sourcetable.csv)	200	Sale_ID, Date, Product_ID, Customer_ID, Employee_ID, Quantity, Unit_Price_CHF, Discount_CHF, Total_Price_CHF, Payment_Method, Channel	Analyze profitability and sales trends
Inventory_Restock (inventory_restock-sheet1-sourcetable.csv)	50	Restock_ID, Product_ID, Restock_Date, Units_Ordered, Supplier, Lead_Time_days	Manage suppliers and prevent overstocking
Employees (employee_table-sheet1-sourcetable.csv)	20	Employee_ID, Name, Department, Tenure_years, Monthly_Sales_CHF	Evaluate staff productivity
Marketing (marketing_table-sheet1-sourcetable.csv)	30	Campaign_ID, Channel, Start_Date, End_Date, Budget_CHF, Conversions, Revenue_Generated_CHF	Measure marketing performance and ROI
🚀 Getting Started
Prerequisites

Python 3.8+

Required Libraries:

pip install pandas numpy matplotlib seaborn


CSV files stored in your project directory (./data/).

Setup Instructions
# Clone the repository
git clone https://github.com/your-username/clothing-retail-analytics.git
cd clothing-retail-analytics

# Place CSV files
mkdir data
# (Move your 6 CSVs into the 'data' folder)

# Run analysis
jupyter notebook or Google Colab

🛠️ Code Structure
Script	Function
top_products.py	Finds and visualizes top 10 best-selling products
sales_by_day.py	Analyzes sales trends by weekday
marketing_roi.py	Calculates average ROI by marketing channel
loss_analysis.py	Detects losses due to unprofitable sales, overstocking, or low-ROI campaigns

Each script includes:

Data preprocessing with pandas

Visualizations with Seaborn

Optional export for web dashboards using Chart.js

📈 Visualizations
1️⃣ Top 10 Products Sold

Purpose: Identify products to prioritize for restocking and promotions.

plt.figure(figsize=(12, 6))
sns.barplot(x='Total_Units_Sold', y='Product_Name', hue='Category', data=top_10_products, palette='Set2')
plt.title('Top 10 Products by Units Sold')
plt.show()

2️⃣ Sales by Day of the Week

Purpose: Detect peak days for staffing and discounts.

plt.figure(figsize=(10, 6))
sns.barplot(x='Day_of_Week', y='Total_Sales_CHF', data=sales_by_day, palette='Set2')
plt.title('Sales by Day of the Week')
plt.xticks(rotation=45)
plt.show()

3️⃣ Marketing Channel ROI

Purpose: Identify which channels deliver the highest returns.

plt.figure(figsize=(8, 5))
sns.barplot(x='ROI', y='Channel', data=avg_roi, palette='crest')
plt.title('Average ROI by Marketing Channel')
plt.show()

4️⃣ Loss Analysis

Purpose: Spot where the business is losing money.

plt.figure(figsize=(10, 6))
sns.barplot(x='Profit_CHF', y='Product_Name', data=unprofitable_by_product, palette='Reds_r')
plt.title('Top 10 Unprofitable Products')
plt.show()

💡 Insights & Recommendations
Objective	Data Insight	Business Action
Save Money	Identified unprofitable items and high stock levels	Reduce discounts, sell off slow movers
Save Time	Found peak sales days and long supplier lead times	Schedule staff for busy days, find faster suppliers
Increase Income	Highlighted top-selling products & high-ROI channels	Invest more in best-performing categories and campaigns

Example Findings (from sample data):

👖 Jeans and 👗 Dresses generate 40% of total revenue.

🗓️ Saturday and Sunday have the highest sales activity.

📱 Instagram and Local Flyers yield the best ROI.

🧾 Shoes are often overstocked and discounted, reducing profit.

🖼️ Sample Visuals

Top 10 Products by Units Sold (Category-colored bar chart)

Sales by Day (Highlighting weekend peaks)

ROI by Marketing Channel

Unprofitable Products (Red gradient visualization)

🤝 Contributing

Contributions are welcome!

Fork the repo

Create a new branch

Submit a pull request

Please follow PEP 8 and include clear code comments.

📜 License

Licensed under the MIT License — feel free to use, modify, and share.

📬 Contact

For inquiries, suggestions, or collaborations:
📧 your-email@example.com

Built with 💻 by Bryan Waweru (Nova) — empowering small retail businesses through data.
