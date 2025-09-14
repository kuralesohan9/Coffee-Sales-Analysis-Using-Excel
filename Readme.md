
# Coffee Sales Analysis

## 📌 Project Overview

This project analyzes coffee sales data using **Excel**.  
The dataset includes three raw sheets:

- **Orders** → Order details with Product ID & Customer ID
- **Customers** → Customer information (Name, Email, Country)
- **Products** → Coffee details (Coffee Type, Roast Type, Size, Unit Price, etc.)

I have built relationships between these sheets using lookup formulas to create a **consolidated Orders sheet**, then developed pivot tables and an interactive dashboard.

---

## 🔧 Data Preparation

1. **Orders Sheet Enhancements**

   - Fetched **Customer Name, Email, Country** from the _Customers_ table using `INDEX + MATCH`.
   - Fetched **Coffee Type, Roast Type, Size, Unit Price, Sales** from the _Products_ table using `INDEX + MATCH`.

   Example formula used:

   ```excel
   =INDEX(products!$A$1:$G$49, MATCH(orders!$D2, products!$A$1:$A$49, 0), MATCH(orders!I$1, products!$A$1:$G$1, 0))
   ```


2. **Sales Calculation**

   - Added a `Sales` column in Orders sheet as:

     ```excel
     =Size * Unit Price
     ```

---

## 📊 Analysis with Pivot Tables

- **Total Sales**: Aggregated across all orders.
- **Top 5 Customers**: Based on total purchase value.
- **Sales by Country**: Distribution of revenue across different regions.

---

## 🎛 Dashboard Features

An interactive **Coffee Sales Dashboard** created using Pivot Tables and Slicers:

- **Slicers**: Filter by Size and Roast Type.
- **KPIs**: Total Sales, Top Customers, Sales by Country.
- **Visuals**: Charts and tables for quick insights.

---

## 🗂 Project Structure

```
📂 Coffee-Sales-Analysis
│── 📊 Coffee_Sales_Dashboard.xlsx   # Excel file with processed data, analysis & dashboard
│── Dashboard.png
│── 📊 Raw_Coffee_Orders_Data.xlsx   # Excel file with raw data
│── README.md                        # Project documentation
```

---

## 🚀 How to Use

1. Download or clone this repository:

   ```bash
   git clone https://github.com/kuralesohan9/Coffee-Sales-Analysis.git
   ```

2. Open **Coffee_Sales_Dashboard.xlsx** in Excel.
3. Explore the **Orders** sheet, Pivot Tables, and Dashboard.
4. Use slicers to filter sales insights interactively.

---

## 📈 Insights

- Identified **top 5 customers** contributing the most to sales.
- Found **country-wise sales distribution**.
- Analyzed how **coffee size and roast type** impact sales performance.

---

## 🛠 Tools Used

- **Microsoft Excel** (Data cleaning, formulas, pivot tables, dashboard)
- **INDEX + MATCH** for lookups
- **XLOOKUP** for lookups
- **Pivot Tables & Charts** for analysis
- **Slicers** for interactivity

---
