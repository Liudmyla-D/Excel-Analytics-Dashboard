# Sales Analytics in Excel — Portfolio Project

**File:** `Project_Sibikovska.xlsx`  
**Dashboards (sheet names):** Main KPIs (`ОснПоказники`), Trend Analysis (`АналізПоказників`), Managers (`МЕНЕДЖЕРИ`), Correlation (`КореляціяПоказн`)  
*(service sheets: `Параметри`, `Olap-cube`, etc.)*

## 🎯 Goal
Show an end-to-end Excel analytics workflow: Power Query → Power Pivot/DAX → four interactive dashboards with slicers/timeline and business-ready insights.

## 🧠 Business / Model Context
- Monthly grain with unified dictionaries (clients, products, managers).  
- Plan, AR (accounts receivable), and payroll are allocated to **month–client–product** proportionally to sales.  
- Interactivity by period, manager, brand/category, client.

## 📂 Repository Structure

```
.
├─ README.md
├─ Project_Sibikovska.xlsx
├─ docs/                     # PDF exports of dashboards
│  ├─ 01_main_kpis.pdf
│  ├─ 02_trend_changes.pdf
│  ├─ 03_managers.pdf
│  ├─ 04_correlation_2.pdf   # Discount % vs Margin % (primary)
│  └─ 04_correlation_1.pdf   # Markup % vs Gross Margin ₴ (alt.)
└─ outputs/
   └─ insights_example.csv   # optional tabular summary of insights
```

## 🧩 Technical Details
- **Tools:** Excel, Power Query (M), Power Pivot (DAX), PivotCharts, Slicers, Timeline.  
- **Model:** calendar (first day of month), dimensions (Products, Clients, Managers), facts (Sales qty/amount, COGS, Price list, Plan, AR, Payroll).  
- **Key measures (examples):** `Sales Amount`, `Sales Units`, `COGS`, `Gross Margin`, `Markup %`, `Discount %`, `AR (₴)`, `AR Days`, `Plan Execution %`, `YoY %`, `YoY p.p.`  
- **Techniques:** key unification in PQ; set data types at the final PQ step; scale `AR Days` for combined charts when needed.

<details>
  <summary>📷 Dashboards (open as PDF)</summary>

- [Main KPIs](docs/01_main_kpis.pdf)  
- [Trend & Changes](docs/02_trend_changes.pdf)  
- [Managers](docs/03_managers.pdf)  
- [Correlation — Discount % vs Margin %](docs/04_correlation_2.pdf)  
  - [Alternative: Markup % vs Gross Margin ₴](docs/04_correlation_1.pdf)

</details>

## Executive Summary
Revenue totals **₴294.9M** with **~18.0M** units shipped. Average discount is **27.9%**, markup holds at **48.6%**, and gross margin reaches **₴96.5M**; Accounts Receivable averages **15 days**. The mix is dominated by **Powders (75%)** with **Supermarket** clients leading (**43%**). Priority: protect margin by tightening discount discipline while keeping AR near **15 days**. *[Source: Main KPIs]*

YoY perspective: **Sales −4.3%**, **Units −15.7%**, **Discount −2.8 p.p.**, **Markup +9.3 p.p.**, **Gross Margin +8.7%**, **AR Days −56.3%**. Focus: sustain markup improvements while addressing volume softness. *[Source: Trend Analysis]*

## Key Insights
- **Pricing & Profitability.** Markup **48.6%** with gross margin **₴96.5M** indicates healthy unit economics; however, the average **27.9%** discount leaves room to optimize promo depth.  
  *Action:* Set discount guardrails and A/B-test a lower promo corridor on high-volume SKUs/brands.

- **Volume vs Value.** YoY **sales −4.3%** and **units −15.7%** while **markup +9.3 p.p.** and **margin +8.7%** — value per unit improved, but volume contracted.  
  *Action:* Double-down on channels/assortment that preserved value; targeted recovery for underperforming segments.

- **Receivables.** **15 AR days** with a sharp YoY improvement (**−56.3%**) — liquidity risk decreased.  
  *Action:* Maintain reminder cadence; watch any drift into **30+/60+** buckets.

- **Manager Performance & Payroll.** Plan attainment ~**100%** across periods; payroll split ≈ **Base 58% / Turnover bonus 24% / Low-AR bonus 18%**.  
  *Action:* Replicate Top-manager playbooks (mix, pricing, client portfolio); keep payroll share near **~1.2–1.4%** of revenue.

- **Mix & Segments.** **Powders 75%** of product mix; **Supermarket 43%** of client mix (then Mixed **27%**, Market **14%**, Perfume **6%**, Wholesale (Opt) **8%**, Pharmacy **2%**).  
  *Action:* Scale winning assortment in Supermarkets; pilot uplift in under-penetrated channels (Pharmacy/Perfume).

## Correlation Views
Primary view: **Discount % (X)** vs **Margin % (or Gross Margin ₴, Y)** with bubble size = **Revenue ₴** — the expected inverse relationship (higher discount → lower margin).  

Alternative: **Markup % (X)** vs **Gross Margin ₴ (Y)** — clear upward trend; largest bubbles in the top-right quadrant mark the highest-impact entities. *(See PDFs above; period filters are shown on the dashboard.)*

## ▶️ How to View
1. Open `docs/*.pdf` (quick glance) or download `Project_Sibikovska.xlsx`.  
2. Use slicers/timeline on each dashboard to reproduce the views shown here.

## ⚠️ Limitations
Data are not published; this repo demonstrates the approach and outcomes (screens/PDF).

---
Author: **Lyudmila Sibikovska** · License: MIT
