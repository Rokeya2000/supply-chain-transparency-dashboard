# Supply Chain Transparency Dashboard (Python + SQL + Tableau-ready)

**Status:** ✅ Ready to upload — all outputs pre-generated.  
You do **not** need to run anything.

## What's inside
```
supply_chain_dashboard_project/
├─ data/
│  ├─ suppliers.csv
│  ├─ products.csv
│  ├─ shipments.csv
│  └─ orders.csv
├─ outputs/                      # Precomputed KPI tables (for Tableau import)
│  ├─ avg_delay_per_supplier.csv
│  ├─ on_time_rate_per_supplier.csv
│  ├─ top5_delayed_products.csv
│  └─ supplier_transparency_scores.csv
├─ screenshots/                  # Static charts for README / portfolio
│  ├─ chart_avg_delay_per_supplier.png
│  ├─ chart_on_time_rate_per_supplier.png
│  ├─ chart_top5_delayed_products.png
│  └─ chart_transparency_score.png
├─ supply_chain.sql              # SQL schema + INSERTs for all tables
├─ main.py                       # (Optional) Python script to recompute KPIs
└─ README.md
```

## KPIs included
- **Average delivery delay per supplier (days)**
- **On-time delivery rate per supplier (%)**
- **Top 5 delayed products (avg delay days)**
- **Supplier Transparency Score** (blend of on-time + delay metrics)

## Tableau
You can import any CSVs in `./outputs` (or the raw tables in `./data`) to build a dashboard.  
This repo also includes PNG screenshots you can showcase immediately.

## Optional: Re-run locally
Only if you want to — not required.
```bash
python main.py
```
This regenerates the KPI CSVs under `./outputs` using the CSV data.

## Database
`supply_chain.sql` creates and populates **suppliers**, **products**, **shipments**, and **orders** tables.
It is SQLite/MySQL-compatible (minor tweaks may be needed for strict MySQL modes).

