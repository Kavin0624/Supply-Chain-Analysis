# 🚚 Supply Chain Analysis: Diagnostic & Comparative Report

> Diagnostic analysis of **100 SKUs across cosmetics, haircare and skincare**
> (INR 5.78 lakh revenue) using a **live MySQL connection** and a **3-page interactive
> Power BI dashboard**: product, supplier, carrier, route and location performance.

![Executive Overview](charts/1_executive_overview.png)

---

## 🎯 Business Problem
Where is the supply chain losing **money, time or quality**, and which products,
suppliers, routes and cities need action first?

**Questions answered**
- Which product type drives revenue, and which is actually profitable?
- Where is stock-out risk highest?
- Which suppliers, carriers and routes underperform on cost, speed or quality?
- Which locations underperform relative to their product range?

---

## 🛠️ Tools & Skills
| Area | Tools |
|---|---|
| Database | MySQL (live connection) |
| Querying and analysis | SQL |
| Dashboard | Power BI Desktop (3 pages, connected live to the database) |
| Reporting | Word report, PowerPoint presentation |

**Skills shown:** live database connection, data profiling and quality checks (IQR outlier
test), diagnostic analysis, KPI and scorecard design, dashboard building,
recommendations.

---

## 🔄 Approach
1. **Connect:** live connection to the project's MySQL database (`supply_chain_data`,
   100 rows x 24 columns)
2. **Profile:** reviewed shape, data types and unique categories
3. **Clean:** checked nulls, duplicates, negative values and outliers
4. **Analyse:** revenue, stock, lead time, cost, quality, carriers, suppliers, locations
5. **Visualise:** built a 3-page Power BI dashboard that stays current with the database

**Data quality result:** 0 nulls · 0 duplicate rows · 0 duplicate SKUs · 0 negative values
· 0 statistical outliers (IQR method)

---

## 📊 Key Numbers
| Metric | Value |
|---|---|
| Total revenue | **INR 5,77,604.82** |
| SKUs analysed | **100** (cosmetics, haircare, skincare) |
| Overall avg defect rate | **2.28%** |
| Avg manufacturing lead time | **14.77 days** |
| Best supplier | **Supplier 1** (lowest defect rate, fastest lead time) |

---

## 🔍 Key Insights

**📦 Product comparison**
| Metric | Cosmetics | Haircare | Skincare |
|---|---|---|---|
| Total revenue (INR) | 1,61,521 | 1,74,455 | **2,41,628** |
| Avg price | **57.36** | 46.01 | 47.26 |
| Approx. margin / unit | **+8.25** | -8.35 | -6.64 |
| Avg defect rate (%) | **1.92** | 2.48 | 2.33 |
| Mfg lead time (days) | **13.31** | 17.06 | 13.78 |
| Stock-to-sold ratio | 0.13 | 0.12 | **0.08** |

- **Cosmetics is the efficiency leader.** It is the only category where price covers
  manufacturing and shipping cost, and it has the lowest defect rate and shortest lead time,
  despite the lowest revenue.
- **Skincare is the volume leader** but has the tightest stock buffer (0.08), which is a
  **stock-out risk**.
- **Haircare is the least differentiated** and has the longest lead time.

**🏭 Suppliers:** Supplier 1 is the strongest (1.80% defects, 12.6-day lead time).
Supplier 5 has the highest defect rate (2.67%); Supplier 4 has the highest cost
with no quality benefit.

**🚛 Logistics:** **Route B costs ~20% more** than Routes A and C (595.66 vs ~485-500)
with no meaningful speed advantage. Carrier B is both the fastest (5.3 days) and cheapest.

**📍 Locations:** Mumbai and Kolkata lead on revenue. **Delhi is the lowest
(INR 81K)** despite a mid-sized SKU count (15).

**✅ Data check:** Items failing inspection show higher defect rates (2.57% vs 2.04%
for pass), supporting the reliability of the inspection data.

---

## ✅ Recommendations
1. **Review haircare and skincare pricing:** both run negative approximate margins.
2. **Increase skincare safety stock** to reduce stock-out risk.
3. **Audit Supplier 5 and Supplier 4** for defects and cost.
4. **Re-evaluate Route B:** costlier with no speed benefit.
5. **Investigate Delhi's underperformance** in pricing and demand.

---

## 🖥️ Dashboard Pages
| Page | What it shows |
|---|---|
| 1. Executive Overview | Revenue, SKU count, defect rate, margin and revenue by product type (with a product-type slicer) |
| 2. Product Comparison | Scorecard table, lead time vs shipping time, defect rate vs margin |
| 3. Logistics & Suppliers | Carriers, routes, transport modes, supplier table and revenue map |

![Product Comparison](2_product_comparison.png)
![Logistics and Suppliers](3_logistics_suppliers.png)

---

## ⚠️ Notes & Limitations
- "Approx. margin per unit" is a **directional proxy** (average price minus average
  manufacturing and shipping cost per category), not a per-SKU calculation.
- The `Supplier_Performance` reference table uses different names (Supplier A/B/C) and
  counts than the main data (Supplier 1-5), so the two were **kept independent**.
- The analysis is **diagnostic**, not predictive. Delhi's underperformance is flagged for
  follow-up rather than fully explained by this dataset.

---

- **LinkedIn**: [Connect with me professionally](https://www.linkedin.com/in/kavin-v-661b05285/)
- **Email** : [Connect with me professionally](kavin62405@gmail.com)

Thank you for your support, and I look forward to connecting with you!
