   [📥 Download the .pbix file]
   (https://drive.google.com/file/d/1vxiivUzFAmn_4lHsiglUVjSDR8R3Pngn/view?usp=drive_link)

# -- ! Asian Paints Sales & Dealer Analytics Dashboard ! --
### *Interactive 5-Page Power BI Dashboard for Revenue, Profit, Region, Product & Dealer Insights*

[![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/DAX-Measures-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)](https://learn.microsoft.com/en-us/dax/)
[![Star Schema](https://img.shields.io/badge/Data%20Model-Star%20Schema-4CAF50?style=for-the-badge&logo=databricks&logoColor=white)](https://learn.microsoft.com/en-us/power-bi/guidance/star-schema)
[![CSV](https://img.shields.io/badge/Data-11%20CSV%20Files-FF6F00?style=for-the-badge&logo=files&logoColor=white)](#-dataset)

<br/>

> *"Data tells you what happened — a good dashboard tells you what to do next."*

</div>

---

## 📋 Table of Contents

- [📌 Overview](#-overview)
- [🎯 Problem Statement](#-problem-statement)
- [✨ Key Features](#-key-features)
- [🏗️ Project Structure](#️-project-structure)
- [🗂️ Dataset](#️-dataset)
- [🔄 Project Workflow](#-project-workflow)
- [📊 Dashboard Pages](#-dashboard-pages)
- [🧮 DAX Measures](#-dax-measures)
- [🛠️ Tech Stack](#️-tech-stack)
- [📈 Results & Insights](#-results--insights)
- [🏆 Advantages](#-advantages)
- [🚀 How to Use](#-how-to-use)
- [📄 License](#-license)
- [👤 Author](#-author)
- [🙏 Acknowledgements](#-acknowledgements)

---

## 📌 Overview

The **Asian Paints Sales & Dealer Analytics Dashboard** is an interactive **Power BI** report that turns raw sales, dealer, inventory, target and marketing data into a clear business view. It has **5 report pages** with a common navigation bar, KPI cards, slicers and a mix of charts, so leadership can move from the big picture down to region, product and dealer level in a few clicks.

This project is designed to:
- Build a clean **star-schema data model** from 11 CSV files
- Write reusable **DAX measures** for revenue, profit, margin, target achievement and growth
- Compare **actual vs target** performance across regions, products and time
- Present insights through a consistent, navigable multi-page dashboard

---

## 🎯 Problem Statement

> **Objective:** Build an executive-level dashboard that shows how Asian Paints is performing across revenue, profit, orders, regions, products and dealers.

Business teams need quick answers to questions like:

| ❓ Question | 📊 Where it is answered |
|------------|-------------------------|
| How much revenue and profit are we making? | Overview |
| Are we meeting our revenue and profit targets? | Overview, Regional Performance |
| Which zones, regions and states perform best? | Regional Performance |
| Which products and categories drive sales? | Product Analysis |
| Which dealers contribute most revenue? | Dealer Performance |
| How are we trending month to month and year to year? | Trends & Forecasting |

---

## ✨ Key Features

| Feature | Description |
|--------|-------------|
| 📑 **5 Report Pages** | Overview, Regional Performance, Product Analysis, Dealer Performance, Trends & Forecasting |
| 🧭 **Page Navigation Bar** | Top menu to jump between pages |
| 🎛️ **Geographic Slicers** | Filter by Zone, Region, State and City |
| 💳 **KPI Cards** | Revenue, Profit, Orders, Profit Margin %, Target Achievement % and more |
| 🎯 **Actual vs Target** | Sales and profit compared with revenue and profit targets |
| 📆 **Time Intelligence** | YTD Revenue, YTD Profit and YoY Revenue Growth % |
| 🧮 **Custom DAX Measures** | Revenue in Crore, dealer averages in Lakh, margin and achievement % |
| 🗂️ **Star Schema Model** | Dimension tables linked to fact tables for fast, accurate filtering |

---

## 🏗️ Project Structure

```
📦 Assianpaints-dashboard/
│
├── 📊 assianpaints_dashboard.pbix   ← Power BI report (data model + 5 pages)
│
├── 📁 screenshots/                  ← Image of every dashboard page
│
└── 📄 README.md                     ← Project documentation
```

---

## 🗂️ Dataset

The model is built from **11 CSV files**, split into dimension and fact tables.

| 📂 Table | 📄 Type | 🔍 Purpose |
|----------|---------|-----------|
| `DimDate` | Dimension | Calendar: Year, Quarter, Month, MonthName |
| `DimRegion` | Dimension | Zone → Region → State → City hierarchy |
| `DimProduct` | Dimension | Product and category details |
| `DimDealer` | Dimension | Dealer information |
| `DimCustomer` | Dimension | Customer details |
| `FactSales` | Fact | Quantity, Sales Amount, Discount, Net Sales, Cost, Profit |
| `FactTargets` | Fact | Revenue Target and Profit Target |
| `FactInventory` | Fact | Opening and Closing Stock |
| `FactDealerVisits` | Fact | Dealer visits and visit-based revenue |
| `MarketingCampaigns` | Fact | Campaign budgets |
| `ProductCostMaster` | Reference | Product cost data |

---

## 🔄 Project Workflow

```
Raw CSV Files (11)
      │
      ▼
┌─────────────────────────────┐
│   Load into Power BI        │  ← Power Query: clean & shape data
└────────────┬────────────────┘
             │
             ▼
┌─────────────────────────────┐
│   Build Star Schema         │  ← Relationships: Dim ↔ Fact
└────────────┬────────────────┘
             │
             ▼
┌─────────────────────────────┐
│   Write DAX Measures        │  ← Revenue, Profit, Margin, Target %, YTD, YoY
└────────────┬────────────────┘
             │
             ▼
┌─────────────────────────────┐
│   Design 5 Report Pages     │  ← KPI cards, charts, slicers, navigation
└────────────┬────────────────┘
             │
             ▼
     Insights & Decisions ✅
```

---

## 📊 Dashboard Pages

### 1️⃣ Overview (Executive Overview)

> The one-page summary for leadership.

- 💳 KPI cards: **Total Revenue, Total Profit, Total Orders, Profit Margin %, Target Achievement %**
- 📈 Net Sales trend (line chart) and monthly revenue (column chart)
- 🍩 Net Sales vs Profit Target (donut chart)
- 🌳 Product-wise Net Sales vs Revenue Target (treemap)
- 🎛️ Slicers: Zone, Region, State, City

### 2️⃣ Regional Performance

> How each geography is performing.

- 💳 KPI cards: Total Revenue, Total Profit, Total Orders, Profit Margin %, Target Achievement %
- 📊 Revenue and profit targets by product (bar chart)
- 📣 Sales Amount vs Marketing Budget (column chart)
- 💸 Discount Amount vs Net Sales (line and column combo)
- 📉 Quantity sold over time (line chart)
- 🧾 Year / Quarter / Month matrix with Dealer Visit Revenue and Total Dealers

### 3️⃣ Product Analysis

> Which products and categories drive the business.

- 💳 KPI cards: Total Revenue, Total Profit, Profit Margin %, Avg Revenue per State, Total Products
- 🥧 Orders by year (pie chart)
- 🎯 Profit vs Profit Target by quarter (column chart)
- 🌳 Discount amount by dealer (treemap)
- 🍩 Closing stock by quarter (donut chart)
- 🧾 Detailed sales table (Product, Region, Quantity, Net Sales, Cost)

### 4️⃣ Dealer Performance

> Which dealers and visits bring the revenue.

- 💳 KPI cards: Total Profit, Total Orders, Total Dealers, Avg Revenue per Dealer (Lakh), Dealer Visit Revenue
- 📅 Monthly revenue trend (line chart)
- 📊 Monthly Net Sales with Avg Revenue per Dealer (column chart)
- 🔻 Quarter-wise revenue (funnel chart)
- 🍩 Revenue share vs dealer count (donut chart)

### 5️⃣ Trends & Forecasting

> Growth and year-to-date view.

- 💳 KPI cards: **YTD Revenue, YTD Profit, YoY Revenue Growth %**, Profit Margin %, Total Orders
- 🌳 Net Sales vs Revenue Target by product (treemap)
- 📊 Monthly Net Sales (column chart)
- 🍩 Closing stock by quarter (donut chart)
- 🧾 Sales detail table

---

## 🧮 DAX Measures

| Measure | Purpose |
|---------|---------|
| `Total Revenue (Cr)` | Total revenue shown in Crore |
| `Total Profit (Cr)` | Total profit shown in Crore |
| `Total Orders` | Number of orders |
| `Profit Margin %` | Profit as a percentage of revenue |
| `Target Achievement %` | Actual performance vs target |
| `Avg Revenue per Dealer (Lakh)` | Average revenue per dealer in Lakh |
| `Avg Revenue per State (Cr)` | Average revenue per state in Crore |
| `Total Dealers` | Count of dealers |
| `Dealer Visit Revenue (Cr)` | Revenue linked to dealer visits |
| `YTD Revenue (Cr)` | Year-to-date revenue |
| `YTD Profit (Cr)` | Year-to-date profit |
| `YoY Revenue Growth %` | Year-over-year revenue growth |
| `Total Products` | Count of products in inventory |

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| 📊 **Power BI Desktop** | Report design and visualization |
| 🧮 **DAX** | Measures and time intelligence |
| 🔧 **Power Query** | Data cleaning and transformation |
| 🗂️ **Star Schema** | Data modelling approach |
| 📄 **CSV** | Source data (11 files) |
| 🐙 **Git & GitHub** | Version control and portfolio hosting |

---

## 📈 Results & Insights

After building the dashboard, the business gets:

- ✅ **One-click KPI view** of revenue, profit, orders and margin
- 🎯 **Target tracking** with achievement % against revenue and profit targets
- 🗺️ **Geographic drill-down** from Zone to Region, State and City
- 📦 **Product and stock visibility** with sales, discount and closing stock views
- 🤝 **Dealer insights** on revenue per dealer and visit-driven revenue
- 📆 **Trend view** with YTD figures and YoY growth

---

## 🏆 Advantages

| Advantage | Detail |
|-----------|--------|
| 🧭 **Easy Navigation** | Same menu on every page |
| 🎛️ **Interactive** | Slicers update every visual on the page |
| 🧮 **Reusable Measures** | One measure feeds many visuals |
| 🗂️ **Clean Model** | Star schema keeps filters accurate and fast |
| 📈 **Decision Ready** | KPIs, targets and trends on one report |
| 🧪 **Extensible** | New pages or measures can be added easily |

---

## 🚀 How to Use

1. Download `assianpaints_dashboard.pbix` from this repository.
2. Open it in **Power BI Desktop** (free download from Microsoft).
3. Use the top menu to switch pages and the slicers to filter by Zone, Region, State or City.

> 💡 If the file is not in the repo, see the **screenshots** folder for every page.

---

## 📄 License

This project is licensed under the **MIT License**.

```
MIT License — Free to use, modify, and distribute with attribution.
```

---

## 👤 Author

<div align="center">

### Your Name Here

[![GitHub](https://img.shields.io/badge/GitHub-pransu1719-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/pransu1719)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/)

**🛠️ Skills:** Power BI · DAX · Data Modelling · Dashboard Design · Data Analytics

</div>

---

## 🙏 Acknowledgements

- 📚 [Microsoft Power BI Docs](https://learn.microsoft.com/en-us/power-bi/) — Official Power BI documentation
- 🧮 [DAX Guide](https://dax.guide/) — DAX function reference
- 🗂️ [Star Schema Guidance](https://learn.microsoft.com/en-us/power-bi/guidance/star-schema) — Data modelling best practices

---

<div align="center">

*Made with ❤️ and ☕ — Last updated: 10 November, 2026*

</div>
