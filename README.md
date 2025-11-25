# 🏬 Superstore Analytics Dashboard (Tableau)

## 📌 Overview  
The **Superstore Analytics Dashboard** is an interactive Tableau dashboard designed to analyze Sales, Profit, and Order performance across different product categories, regions, and customer segments in the USA.  
This dashboard allows business users to visually explore top-performing categories, sub-categories, states, products, and time-based trends with dynamic metric switching.

---

## 🛠️ Tech Stack  
- 📊 **Tableau Desktop** – Dashboard design & visual analytics  
- 🧮 **Calculated Fields** – Profit Margin, Return Rate, Metric parameter logic  
- 🗂️ **Superstore Dataset** – Sample retail dataset  
- 🎚️ **Parameters & Filters** – Dynamic metrics, region, and year  
- 🧠 **LOD Expressions / Top-N Logic** – For top 5 products based on selected metric  

---

## ⭐ Key Features

### **1️⃣ Dual-Pane Dashboard Layout**
- **Left Pane:**  
  - Company Logo  
  - Metric Selector (Parameter)  
  - Region Filter  
  - Year Filter  
- **Right Pane:**  
  - Six dynamic visualizations  
  - Three dynamic KPI cards  
  - All visuals respond to selected metric & user interaction  

---

### **2️⃣ Dynamic Metric Selection (Parameter Control)**
A Tableau parameter named **`Metric`** allows the user to switch between:
- **Sales**
- **Profit**
- **# Orders**

When a metric is chosen:
- All chart titles update automatically  
  (Example: "Sales by Category" → "Profit by Category")
- Tooltip values change  
- KPI cards adjust values  
- The Top 5 products panel updates  
- Trend line charts reflect the selected metric  

---

### **3️⃣ KPI Cards**
The dashboard displays three high-level KPIs:

- **Sales:** 2.30M  
- **Profit Margin:** 12.47%  
- **Return Rate:** 5.91%

#### Calculations Used:
- **Profit Margin = Total Profit / Total Sales**  
- **Return Rate = Quantity Returned / Quantity Ordered**

---

### **4️⃣ Interactive Visualizations**
The dashboard features the following 6 dynamic charts:

1. **Sales / Profit / Orders by Category**  
2. **Sales / Profit / Orders by Sub-Category**  
3. **Sales / Profit / Orders by State (Filled Map)**  
4. **Sales / Profit / Orders by Segment (Donut Chart)**  
5. **Top 5 Products by Selected Metric**  
6. **Sales Trend / Profit Trend / Order Trend Over Time**  

Each chart dynamically changes based on the selected metric.

---

### **5️⃣ Filter Action on Category Chart**
- Clicking any **Category** (Furniture, Office Supplies, Technology)  
  will filter all other charts:  
  - Sub-Category  
  - State Map  
  - Segment Donut  
  - Sales Trend  
  - Top 5 Products  
  - KPI Cards  

This allows deep-dive insights into each category’s performance.

---

```tableau
{ FIXED : TOP 5 products based on SUM([Selected Metric]) }
