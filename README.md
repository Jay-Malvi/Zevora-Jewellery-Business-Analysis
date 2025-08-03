# 💎 Jewellery Business Intelligence Dashboard (Python + Power BI)

## 📌 Project Overview
This project focuses on analyzing a **jewellery business dataset** to derive actionable insights using **Python for Data Cleaning & EDA** and **Power BI for visualization**.  
The objective is to:
- Clean and prepare raw sales, inventory, customer, and staff data.
- Perform **EDA (Exploratory Data Analysis)** in Python.
- Automate **business insights generation** (sales, profit, customers, staff performance, restock alerts).
- Build an **interactive Power BI Dashboard** with multiple pages (Sales, Inventory, Customer Insights, Staff, Profit-Leak).

---

## 📂 Dataset Details
The dataset contains the following sheets:
1. **Sales**: OrderID, CustomerID, ProductID, OrderDate, TotalAmount, Profit, etc.
2. **Inventory**: ProductID, ProductName, Category, StockQty, ReorderLevel.
3. **Customers**: CustomerID, Name, Age, City, Occupation, Reference, IsRepeat.
4. **Staff**: StaffID, StaffName, MonthlyTarget.

---

## 🛠 Tools & Technologies
- **Python**: Pandas, NumPy, Matplotlib, Seaborn (for data cleaning & EDA)
- **Power BI**: For dashboard creation & KPI tracking
- **Excel**: For initial data storage and preprocessing

---

## 🔑 Key Features
✅ Data cleaning & transformation using **Python (Pandas)**  
✅ Automated **insight generation** (top products, repeat customers, staff performance)  
✅ EDA visualizations: Sales trends, Profit distribution, Customer demographics  
✅ **Power BI Dashboard** with 7 pages:
  - Dashboard Overview
  - Daily Sales
  - Monthly Summary
  - Inventory & Restock Alerts
  - Staff Performance
  - Customer Loyalty & Insights
  - Profit-Leak & Alerts

---

## 📊 Python EDA (Exploratory Data Analysis)
### Data Cleaning:
- Filled missing values
- Corrected data types (e.g., date fields, numeric columns)
- Removed duplicates
- Created customer **age groups**

### Sample EDA Code:
```python
# Monthly Sales Trend
df['Month'] = df['OrderDate'].dt.to_period('M')
monthly_sales = df.groupby('Month')['TotalAmount'].sum()

plt.figure(figsize=(10,5))
monthly_sales.plot(kind='line', marker='o', color='gold')
plt.title("Monthly Sales Trend")
plt.xlabel("Month")
plt.ylabel("Sales Amount")
plt.show()
