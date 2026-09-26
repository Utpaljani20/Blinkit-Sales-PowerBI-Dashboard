### 🛍️ Blinkit Sales & Inventory Performance Analysis (Power BI)

An interactive Power BI Data Analytics Solution analyzing 8,523 grocery inventory and sales records for Blinkit. This project uncovers product category performance, customer rating distributions, item fat content demands, outlet size & tier efficiencies, and establishment year sales trends built entirely in Power BI Desktop.

---

### 🔹Overall Sales & Performance Dashboard

Focuses on macro-level retail KPIs, category breakdown, outlet metrics, and temporal sales performance.

#### Key Metrics & Figures:
- **Total Sales Volume:** $1.20M gross revenue
- **Average Sales per Item:** $141
- **Total Product Count:** 8,523 unique inventory items (9K)
- **Average Customer Rating:** 3.9 / 5.0

---

### 🔹 Product & Category Performance Matrix

Evaluates sales distribution, fat content preferences, and item type contributions across 16 grocery categories.

#### Fat Content Breakdown:
- **Low Fat Items:** $776.3K Total Sales (64.6%)
- **Regular Fat Items:** $425.4K Total Sales (35.4%)

#### Top Category Breakdown:
| Item Type | Total Sales | No. of Items | Avg. Sales | Avg. Rating |
| :--- | :--- | :--- | :--- | :--- |
| **Fruits & Vegetables** | $0.18M ($178.1K) | 1,232 | $145 | 3.96 |
| **Snack Foods** | $0.18M ($175.4K) | 1,200 | $146 | 3.95 |
| **Household** | $0.14M ($136.0K) | 910 | $149 | 4.00 |
| **Frozen Foods** | $0.12M ($118.6K) | 856 | $139 | 3.97 |
| **Dairy** | $0.10M ($101.3K) | 682 | $148 | 3.97 |
| **Canned** | $0.09M ($90.7K) | 649 | $140 | 3.99 |
| **Baking Goods** | $0.08M ($81.9K) | 648 | $126 | 3.98 |

---

### 🔹 Outlet & Geographic Distribution

Analyzes revenue performance across outlet types, sizes, and location tiers.

#### Outlet Type Breakdown Matrix:
| Outlet Type | Total Sales | No. of Items | Avg. Sales | Avg. Rating | Item Visibility |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Supermarket Type1** | $787.55K | 5,577 | $141 | 4.0 | 0.06 |
| **Grocery Store** | $151.94K | 1,083 | $140 | 4.0 | 0.10 |
| **Supermarket Type2** | $131.48K | 928 | $142 | 4.0 | 0.06 |
| **Supermarket Type3** | $130.71K | 935 | $140 | 4.0 | 0.06 |

#### Outlet Location & Size Analysis:
- **Tier 3 Outlets:** $472.13K Total Sales (3,350 items)
- **Tier 2 Outlets:** $393.15K Total Sales (2,785 items)
- **Tier 1 Outlets:** $336.40K Total Sales (2,388 items)
- **Outlet Size Share:** Medium Outlets lead with $507.9K, followed by Small Outlets ($444.8K) and High Outlets ($249.0K).

---

### 🧮 Key Power BI DAX Measures

```dax
-- Total Sales Revenue
Total Sales = SUM('BlinkIT Grocery Data'[Sales])

-- Average Sales per Item
Average Sales = AVERAGE('BlinkIT Grocery Data'[Sales])

-- Total Number of Items
No of Items = COUNT('BlinkIT Grocery Data'[Item Identifier])

-- Average Customer Rating
Avg Rating = AVERAGE('BlinkIT Grocery Data'[Rating])

-- Item Visibility Rate
Avg Visibility = AVERAGE('BlinkIT Grocery Data'[Item Visibility])

-- Low Fat Sales Share
Low Fat Sales = CALCULATE(
    SUM('BlinkIT Grocery Data'[Sales]), 
    'BlinkIT Grocery Data'[Item Fat Content] = "Low Fat"
)
