# GZI SA — Technical Stores Hub

Online, multi-user inventory-control program for GZI South Africa Technical Stores
(Wadeville, plant 6000). One page, shared database.

**Live:** https://mohlatswa.github.io/gzi-stores-hub/
**Sign in:** `Admin` / `Admin`

## Modules
Dashboard · Inventory (all areas) · Bin Locations · Counting Sheets · Variance
Report · IVF (Inventory Verification Form) · Bin Card · Movement Tracker ·
Inter-Branch Transfers · Daily Issue Tracker · Gate Pass Tracker · Gas Bottle
Tracker · Master Data Requests · Machines / Areas / Branches / Staff.

## How it works
- Data is stored in a shared Supabase Postgres database (tables prefixed `shb_`).
- Every signed-in user reads and writes the same data. Use **↻ Refresh** to pull
  the latest; the app also refreshes when the tab regains focus.
- Online only — needs a connection to load and save.
- **Load sample data** seeds a demo set based on the original spreadsheets.
- **Backup / Restore** does full JSON export/import and per-tracker CSV.

## Notes
- The `Admin`/`Admin` gate is a lightweight front-door only, not real security.
  Move to named accounts + row-level security before wider rollout.
