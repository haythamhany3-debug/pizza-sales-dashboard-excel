# 🍕 Pizza Sales Dashboard (Excel)

An interactive **Excel dashboard** that analyzes pizza sales data and turns it into clear, actionable insights: revenue, orders, customers, best and worst sellers, and ordering patterns over time. It is built with **Pivot Tables, Pivot Charts, Slicers and a Timeline**, so every visual updates instantly when you filter the data.

---

## 📌 Project Overview

| Item | Details |
|------|---------|
| **Tool** | Microsoft Excel |
| **Techniques** | Excel Tables, Calculated Columns, Pivot Tables, Pivot Charts, Slicers, Timeline, Dashboard Design |
| **Data period** | 2015 (January – December) |
| **Data size** | ~500 rows, 13 columns |
| **Language** | Bilingual column headers (English / Arabic) |

The goal is to help a pizza business answer questions like:

- How much revenue are we making, and from how many orders and customers?
- Which pizzas sell best, and which sell worst?
- Which pizza category and size bring in the most revenue?
- Which months and weekdays are busiest?

---

## 📊 Dashboard Features

### KPI Cards
- **Total Sales** (revenue)
- **Total Customers**
- **Total Orders**
- **Total Quantity** sold

### Charts
| Chart | Type | Insight |
|-------|------|---------|
| Total Sales by Category | Doughnut | Revenue share of Chicken, Classic, Supreme and Veggie pizzas |
| Total Sales by Size | Pie | Revenue share of S, M, L and XL sizes |
| Monthly Order Volume Peaks | Line | Seasonality and peak months (Jan to Dec) |
| Weekly Order Distribution | Column | Which weekdays get the most orders |
| Top 5 Best Selling Pizzas | Bar | Highest revenue pizzas |
| Bottom 5 Least Selling Pizzas | Bar | Lowest revenue pizzas, candidates for menu review |

### Interactive Filters
- **Slicer: Pizza Size** (S / M / L / XL)
- **Slicer: Pizza Category** (Chicken / Classic / Supreme / Veggie)
- **Timeline: Order Date** (filter by month)

> 💡 **Note:** The screenshot in this repo is captured with the **Classic** category filter applied. That is why the KPIs show **$2,275 sales, 149 orders, 149 customers and 152 items**. Clear the slicers to see the totals for the full dataset.

---

## 🖼️ Screenshots

| Dashboard | Pivot Tables |
|-----------|--------------|
| `images/dashboard.png` | `images/pivot_tables_1.png`, `images/pivot_tables_2.png` |

---

## 🗂️ Dataset Description (`Data.xlsx`)

The data sheet is an Excel Table (`Table1`) with these columns:

| Column | Description |
|--------|-------------|
| `order_id` | Unique order number |
| `pizza_id` | Pizza identifier (e.g. `classic_dlx_m`) |
| `Customer Name` | Name of the customer |
| `quantity` | Number of pizzas ordered |
| `order_date` | Date of the order |
| `WeekDay` | Day of the week of the order |
| `order_time` | Time of the order |
| `unit_price` | Price of one pizza |
| `Sales` | Calculated column: `unit_price × quantity` |
| `pizza_size` | S, M, L or XL |
| `pizza_category` | Chicken, Classic, Supreme or Veggie |
| `pizza_ingredients` | List of ingredients |
| `pizza_name` | Name of the pizza |

---

## 🧮 Pivot Tables Used

1. **Orders by Weekday**: Count of `order_id` by `WeekDay`
2. **Orders by Month**: Count of `order_id` by month of `order_date`
3. **Sales by Category**: Sum of `Sales` by `pizza_category` (shown as % of total)
4. **Sales by Size**: Sum of `Sales` by `pizza_size` (shown as % of total)
5. **Top 5 Pizzas**: Sum of `Sales` by `pizza_name`, Top 10 filter (Top 5)
6. **Bottom 5 Pizzas**: Sum of `Sales` by `pizza_name`, Top 10 filter (Bottom 5)
7. **KPI Pivots**: Sum of `Sales`, Sum of `quantity`, Count of `order_id`, Count of `Customer Name`

All pivot tables share the same slicers and timeline through report connections.

---

<img width="677" height="263" alt="image" src="https://github.com/user-attachments/assets/61a062fe-3209-459b-8b2f-459f8219fb91" />


- **Peak months:** August and October have the highest order volume (17 orders each), followed by May and June (15 each). February is the lowest (5).
- **Busiest day:** Friday leads with 29 orders, then Saturday (25) and Monday (23). Wednesday is the slowest (11).
- **Best sellers (Classic filter):** The Classic Deluxe Pizza ($459) and The Greek Pizza ($402).
- **Sales by size:** S (34%) and L (30%) generate most of the revenue; XL is the smallest at 12%.
- **Sales by category (full data):** Classic 26.96%, Veggie 28.04%, Supreme 24.32%, Chicken 20.67%.

*Insights depend on the filters applied. Re-check after changing slicers.*

---

## 🚀 How to Use

1. Download or clone the repository.
2. Open the dashboard workbook in **Microsoft Excel** (2016 or later recommended).
3. Use the **slicers** and **timeline** on the right to filter the dashboard.
4. To refresh after editing the data: **Data → Refresh All**.

```bash
git clone https://github.com/<your-username>/pizza-sales-dashboard-excel.git
```

---

## 📁 Repository Structure

```
pizza-sales-dashboard-excel/
├── Data.xlsx                  # Source data (Excel Table)
├── Pizza_Sales_Dashboard.xlsx # Dashboard workbook (pivots + charts + slicers)
├── images/
│   ├── dashboard.png          # Dashboard screenshot
│   ├── pivot_tables_1.png     # Pivot tables screenshot
│   └── pivot_tables_2.png     # Pivot tables and KPI screenshot
└── README.md
```

---

## 🛠️ Skills Demonstrated

- Data cleaning and preparation in Excel
- Calculated columns and structured references
- Pivot Tables and Pivot Charts
- Slicers, Timelines and connected reports
- KPI design and dashboard layout
- Business storytelling with data

---

## 📬 Contact

Feel free to open an issue or reach out for feedback and collaboration.

⭐ If you found this project useful, please give it a star!
