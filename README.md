# Sales Analytics in Excel — My first portfolio

**File:** `Project_Sibikovska.xlsx`  
**Dashboards (sheet names):** Main KPIs (`ОснПоказники`), Trend Analysis (`АналізПоказників`), Managers (`МЕНЕДЖЕРИ`), Correlation (`КореляціяПоказн`)  
*(service sheets: `Параметри`, `Olap-cube`, etc.)*

## 🎯 Goal
Show an end-to-end Excel analytics workflow: Power Query → Power Pivot/DAX → four interactive dashboards with slicers/timeline and business-ready insights.

## 🧠 Business/Model Context (short)
- Monthly grain with unified dictionaries (clients, products, managers).  
- Plan, AR (accounts receivable), payroll and other metrics are allocated down to **month–client–product** proportionally to sales.  
- Interactivity by period, manager, brand/category, client.

## 📂 Repository Structure (recommended)
```
.
├─ README.md                   # this file
├─ Project_Sibikovska.xlsx     # my Excel workbook
├─ docs/                       # screenshots & optional PDF
│  ├─ 01_main_kpis.png         # ОснПоказники
│  ├─ 02_trend_changes.png     # АналізПоказників
│  ├─ 03_managers.png          # МЕНЕДЖЕРИ
│  └─ 04_correlation.png       # КореляціяПоказн
└─ outputs/
   └─ insights_example.csv     # optional tabular summary of insights
```

## 🧩 Technical Details
- **Tools:** Excel, Power Query (M), Power Pivot (DAX), PivotCharts, Slicers, Timeline.  
- **Model:** calendar (first day of month), dimensions (Products, Clients, Managers), facts (Sales qty/amount, COGS, Price list, Plan, AR, Payroll).  
- **Key measures (examples):** `Sales Amount`, `Sales Units`, `COGS`, `Gross Margin`, `Markup %`, `Discount %`, `AR (₴)`, `AR Days`, `Plan Execution %`, `YoY %`, `YoY p.p.`  
- **Techniques:** key unification in PQ; set data types on the last PQ step; scale `AR Days` for combined charts when needed.

## 🖼️ Dashboards
- **Main KPIs** — KPI cards; combined chart (margin / markup / AR days); TOP-5 (managers/products/clients).  
- **Trend Analysis** — YoY / MoM deltas (% and p.p.); margin/turnover dynamics.  
- **Managers** — turnover, margin, payroll (base/bonus); payroll share in turnover; TOP tables.  
- **Correlation** — bubble chart (configurable X/Y/size) with period paging.

## ▶️ How to View
1. Open `docs/*.png` (quick glance) or download `Project_Sibikovska.xlsx`.  
2. Use slicers/timeline on each dashboard.

## Executive Summary
Sales grew by **[YoY %]** YoY with a stable markup around **[Markup %]**. At the same time, Accounts Receivable average **[N]** days (vs target **[T]**), and the Top-3 managers generate **[A%]** of revenue. Priority: tighten collections on **60+** AR and A/B-test lower discounts on **[Brand/Category]** to protect margin.

## Key Insights
- **Growth & Profitability.** Year-over-year sales are **[YoY %]**, gross margin totals **[Gross Margin, ₴]**, and markup holds near **[Markup %]**. Main driver: **[Top brand/category or customer segment]**.  
  **Action:** Scale the winning assortment/channel and codify targets in monthly KPIs.

- **Discounting & Pricing.** Average discount is **[Discount %]**; **[Brand/Category]** runs higher at **[Brand Discount %]**, compressing margin by **[Δ p.p.]** vs median.  
  **Action:** A/B-test a lower promo depth for **[Brand/Category]** and set guardrails for discounting.

- **Accounts Receivable.** Average AR is **[N]** days (target **[T]**); **[Share %]** of receivables are **60+ days**, concentrated in **[Client segment]**.  
  **Action:** Prioritize the 60+ bucket (sequenced reminders / payment plans), tighten terms for repeat late-payers.

- **Manager Performance.** Top-3 managers contribute **[A%]** of revenue with **[X%]** higher margin vs median; bottom quartile trails by **[Gap %]**.  
  **Action:** Replicate Top-3 playbook (mix, pricing, client portfolio); targeted coaching for the bottom quartile.

- **Product Mix.** **[Category/SKU group]** delivers **[Share %]** of margin at markup **[Markup %]**; the long tail adds **[Share %]** with low velocity.  
  **Action:** Rebalance assortment; de-stock slow movers; shift budget to high-margin/velocity items.

- **Plan Execution.** Plan attainment is **[Plan %]** with YoY delta **[Δ p.p.]** mainly driven by **[driver: price/mix/volume]**.  
  **Action:** Monthly review cadence with corrective actions on price/mix/volume.

## Risks & Next Steps
- **Risks:** Margin sensitivity to discounting on **[Brand/Category]**; aging receivables in **[Segment]**.  
- **Next Steps:** (1) Collections sprint for **60+** AR; (2) Discount A/B on **[Brand/Category]**; (3) Quarterly assortment review.

## ⚠️ Limitations
Data are not published; the repository demonstrates the approach and results (screens/PDF).

---
Author: **Lyudmila Sibikovska** · License: MIT
