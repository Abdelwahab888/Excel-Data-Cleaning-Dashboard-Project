# Online Retail — Excel Data Cleaning & Dashboard Project

End-to-end Excel project built on the real **[UCI Online Retail dataset](https://archive.ics.uci.edu/dataset/352/online-retail)** — ~70,000 raw UK e-commerce transactions (Dec 2010 – Jan 2011).

## What this project covers

- **Data cleaning** — handled inconsistent casing, blank `CustomerID` fields (guest checkouts), and messy real-world noise (no synthetic/pre-cleaned data).
- **Transaction classification** — built a nested `IF` formula to split every row into `Sale`, `Cancellation`, `Fee/Admin`, or `Adjustment` (returns, postage/bank/Amazon fees, damaged stock & write-offs), based on patterns found in `InvoiceNo`, `StockCode`, `Quantity`, and `UnitPrice`.
- **Validation** — cross-checked classification totals against the raw `UnitPrice` sum to confirm nothing was mis-bucketed.
- **Analysis (PivotTables)**:
  - Top 10 products by quantity sold **and** by revenue (not the same ranking)
  - Top 10 customers by spend (guest checkouts excluded)
  - Monthly sales trend
- **Interactive Dashboard** — four PivotCharts on one sheet, all connected to a single slicer via Report Connections.

## Sheets

| Sheet | Contents |
|---|---|
| `Sheet1` | Cleaned, classified raw data |
| `Pivot1–4` | Supporting PivotTables for each analysis |
| `Summary` | Transaction-type totals (Sale / Cancellation / Fee-Admin) |
| `Dashboard` | Final interactive dashboard with slicer |

## Notes

- This is a learning project, not a commercial deliverable — built step-by-step to practice real Excel data-cleaning and dashboarding workflows.
- Source data is public and real; no customer data here is from an actual business relationship.
- The "before" file is the full, unfiltered UCI dataset (~542,000 rows, all countries, full date range). The "after" file is scoped to United Kingdom transactions across the first two months only (~70,000 rows) before any cleaning began — the row-count drop reflects that scoping, not data loss during cleaning.
