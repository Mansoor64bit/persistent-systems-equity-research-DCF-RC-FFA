# Persistent Systems Ltd — Equity Research Model

A full equity research valuation model for **Persistent Systems Ltd** (Indian IT services), built the way a sell-side/buy-side analyst would approach it: **DCF**, **Relative (peer comps) Valuation**, and a **Football Field** summary that lines every approach up against the current market price.

> 📊 Current price: **₹5,654** · DCF (base case): **₹1,098/share** · Comps range: **₹3,266–₹4,182/share**
> Every valuation approach sits below the market price — see the [Notes](#-notes--things-to-double-check) below for the honest read on what that gap means.

---

## 📁 What's in this repo

| File | Description |
|---|---|
| `Persistent_Systems_Equity_Research_Model.xlsx` | The full Excel model — DCF, WACC, Intrinsic Growth, Relative Comps, and Football Field tabs. |
| `report/Persistent_Systems_Equity_Research_Report.docx` | A written report walking through the company snapshot, all three valuation methods, and where they disagree. |
| `screenshots/` | PNG snapshots of the key tabs/outputs, for quick viewing without opening Excel. |

---

## 🧮 What's inside the Excel model

The workbook has 10 tabs:

1. **DCF** – FCFF forecast (FY27F–FY31F), terminal value, equity bridge, and a WACC/terminal-growth sensitivity table (built as a native Excel Data Table).
2. **WACC** – Peer-comparable beta, cost of equity, cost of debt, and final WACC build-up.
3. **Rm** – Historical Indian equity market returns (used to derive the equity risk premium).
4. **Intrisic Growth** – ROIC and Reinvestment Rate calculations used to derive the DCF's growth assumption.
5. **Relative Comps Valuation** – 9-company peer set valued on EV/Revenue, EV/EBITDA, and P/E.
6. **Football Field Analysis** – Chart and data comparing DCF (Bear/Base/Bull), Comps, and 52-week range against the market price.
7. **Raw Beta Peers** – Peer company beta inputs.
8. **Raw FS** – Underlying 10-year financial statements.
9. **Raw comps data** – Underlying comps inputs.
10. **Data Sheet** – Supporting raw data.

## 📈 Key outputs at a glance

| Metric | Value |
|---|---|
| Base year EBIT (FY26) | ₹2,483.9 Cr |
| Expected growth (5-yr median intrinsic growth) | 28.75% |
| WACC | 15.01% |
| Terminal growth rate | 5.38% |
| **DCF equity value per share (base case)** | **₹1,097.65** |
| Comps implied value (EV/Revenue) | ₹3,437.20 |
| Comps implied value (EV/EBITDA) | ₹3,265.66 |
| Comps implied value (P/E) | ₹4,182.21 |
| Current market price | ₹5,654 |

## 🛠 How to use

1. Download `Persistent_Systems_Equity_Research_Model.xlsx` and open it in **Microsoft Excel** (see note below on why Excel specifically).
2. Start at **Raw FS** and **Intrisic Growth** to see the historical base and how the growth rate is derived.
3. Check **WACC** to see the discount rate build.
4. **DCF** pulls it together into a per-share value, with a live sensitivity table (drag to WACC/terminal-growth combos of your choice).
5. **Relative Comps Valuation** gives you the peer-multiple cross-check.
6. **Football Field Analysis** is the executive summary chart — everything on one page.
7. Read `report/Persistent_Systems_Equity_Research_Report.docx` for the plain-English walkthrough.

## 📝 Notes / things to double-check

- **Open this one in Excel, not Google Sheets or LibreOffice.** The DCF sensitivity table uses Excel's native "Data Table" (What-If Analysis) feature, and the Football Field chart reads directly off it. Both are Excel-only features — they display blank in LibreOffice/Google Sheets because those programs can't recalculate Excel Data Tables. Everything else in the workbook is unaffected. For this repo's report and screenshots, both were **redrawn from the model's correct cached values** so you can see them properly without needing Excel — the underlying Excel file itself was left untouched.
- **DCF vs Comps disagree by 3–4x.** The DCF's base case (₹1,098/share) is well below the comps-implied range (₹3,266–₹4,182/share), and both are below the current market price (₹5,654). This is the single biggest thing worth digging into before treating either number as a final view — it isn't resolved in the model itself.
- **28.75% growth rate is a historical median**, not a guaranteed forward rate — it's on the high side to hold for a full 5-year explicit forecast. Worth testing a growth-fade (tapering down toward terminal growth) instead of a flat rate.
- **Terminal value is ~73% of enterprise value** in the DCF, so small changes to WACC or terminal growth swing the answer a lot — use the sensitivity table (works live in Excel) to stress-test this.

## ⚠️ Disclaimer

This is an educational financial model, not investment advice. Figures are based on historical company filings and the model author's own assumptions. Do your own research or consult a licensed financial advisor before making investment decisions.

---
*Built with a three-lens equity research framework: fundamentals-driven DCF (ROIC → growth → WACC → FCFF → terminal value) + peer-multiple relative valuation + a football field that puts both next to the market price.*
