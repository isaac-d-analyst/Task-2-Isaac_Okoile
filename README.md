# Task-2-Isaac_Okoile
# Project 2: Exploratory Data Analysis (EDA)
### DecodeLabs Data Analytics Internship

---

## 📌 What This Project Is About

This project is a full Exploratory Data Analysis (EDA) on a sales orders dataset.
The objective was to explore the data, uncover patterns, detect outliers,
measure relationships between variables, and communicate findings through
visualizations and business insights.

The core principle: **Find the pulse of the data before any visualization occurs.**

---

## 📊 Dataset Overview

| Property | Detail |
|----------|--------|
| Dataset | Sales Orders |
| Total Rows | 1,200 |
| Total Columns | 14 |
| Total Revenue | $1,264,761.96 |
| Tools Used | Microsoft Excel, Power Query |

### Columns in Dataset:
- OrderID, Date, CustomerID, Product, Quantity, UnitPrice
- ShippingAddress, PaymentMethod, OrderStatus, TrackingNumber
- ItemsInCart, CouponCode, ReferralSource, TotalPrice

---

## 🛠️ Tools Used

- Microsoft Excel
- Power Query (M Language)
- Pivot Tables & Pivot Charts
- IQR Method (Outlier Detection)
- Pearson Correlation Coefficient

---

## 📋 Workbook Structure

| Sheet | Contents |
|-------|---------|
| `PROJECT DATA` | Clean dataset — 1,200 rows, 14 columns |
| `CR DOC` | Change log — all documented changes |
| `OUTLIERS FX` | IQR calculations for UnitPrice & TotalPrice |
| `EDA SUMMARIES` | Pivot tables, means, medians, correlations |
| `REVENUE CHART` | Monthly revenue trend line chart |
| `VISUALS` | 6 charts covering all key business dimensions |

---

## 🔍 Analysis Performed

### 1. Descriptive Statistics

| Metric | UnitPrice | TotalPrice | Quantity | ItemsInCart |
|--------|-----------|------------|----------|-------------|
| **Mean** | $356.41 | $1,053.97 | 2.95 | 5.49 |
| **Median** | $364.00 | $824.00 | 3 | 5 |

### 2. Outlier Detection — IQR Method

**UnitPrice:**
| Metric | Value |
|--------|-------|
| Q1 | $186.06 |
| Q3 | $521.57 |
| IQR | $335.51 |
| Lower Fence | $0.00 |
| Upper Fence | $1,024.83 |
| Outliers Found | 0 |

**TotalPrice:**
| Metric | Value |
|--------|-------|
| Q1 | $410.52 |
| Q3 | $1,578.48 |
| IQR | $1,167.96 |
| Lower Fence | $0.00 |
| Upper Fence | $3,330.41 |
| Outliers Found | 8 |

**Outlier Investigation Result:**
All 8 flagged TotalPrice rows were investigated.
Values ranged from $3,334 to $3,456 — consistent with high cart volumes (7–10 items).
**Decision: Retained as valid records (Signal, not Noise)**

### 3. Correlation Analysis

| Column Pair | Correlation (r) | Strength |
|-------------|----------------|---------|
| UnitPrice → TotalPrice | **0.72** | Strong Positive |
| Quantity → TotalPrice | **0.62** | Moderate-Strong |
| Quantity → ItemsInCart | **0.65** | Moderate-Strong |
| UnitPrice → ItemsInCart | **0.00** | No Relationship |

---

## 💡 Key Business Insights

### Revenue
- **Total Revenue:** $1,264,761.96
- **Tablet** is the top revenue generator at **$186,568.95**
- Revenue is fairly evenly distributed across all 7 products

### Marketing & Referral
- **Instagram** drives the most orders — **259 orders**
- **Instagram** also generates the highest revenue — **$275,285.45**
- **Referral** channel is the weakest performer

### Order Status
- **Cancelled: 20.8%** (250 orders)
- **Returned: 20.6%** (247 orders)
- Combined cancellation + return rate = **41.4%**
- Only 231 orders successfully delivered

### Payment Method
- All 5 payment methods are nearly equally used
- Online payments slightly lead at **258 orders**

### Revenue Trend
- Monthly revenue shows a **consistent downward trend** from 2023–2025
- Revenue peaked at approximately **$68,000 in June 2024**
- Decline has been consistent since mid-2024

---

## 📈 Visualizations Included

| Chart | Type | Insight |
|-------|------|---------|
| Total Orders by Product | Bar Chart | Tablet & Printer lead in volume |
| Order Status Count | Column Chart | Cancelled leads all statuses |
| Orders by Referral Source | Bar Chart | Instagram dominates |
| Revenue by Referral Source | Column Chart | Instagram = highest revenue |
| Revenue by Product | Bar Chart | Tablet = highest revenue |
| Revenue by Payment Method | Column Chart | Payments evenly spread |
| Monthly Revenue Trend | Line Chart | Downward trend 2023–2025 |

---

## 🔑 Key Takeaways

- UnitPrice is the strongest driver of TotalPrice (r = 0.72)
- 41.4% of orders either cancelled or returned — a serious fulfilment issue
- Instagram is the most valuable acquisition channel
- Revenue is declining — something changed after mid-2024
- The scatter plot showing 5 diagonal lines is not an error — it reflects that TotalPrice = UnitPrice × Quantity with only 5 possible Quantity values

---

## 📁 Files in This Repository

| File | Description |
|------|-------------|
| `project_2_EDA.xlsx` | Full workbook with all 6 sheets |
| `README.md` | This documentation file |

---

## 👤 Author
**Isaac Okolie**
DecodeLabs Data Analytics Intern
*Powered by SkillAhead Solutions Ltd*
