# Low Leave Monitoring Dashboard

A single-file, client-side HTML dashboard for HR/admin teams to track employees' Earned Leave (EL) and Half-Pay Leave (HPL) balances across months, and flag staff running low on leave.

No backend, no install — just open the HTML file in a browser.

## Features

- **Excel import/export** — bulk-load employee data from `.xlsx`/`.xls` files and export a formatted workbook
- **Month/Year view switcher** — each employee's EL/HPL is tracked per period (2024–2027), so you can flip between months and see historical data
- **Color-coded alerts**
  - 🔴 Red — EL ≤ 0
  - 🟠 Orange — EL ≤ 15
  - 🟢 Green — EL > 15
  - Clickable summary cards filter the table by alert level
- **Auto-close rule** — a case is automatically marked "Closed" after 3 consecutive months of Green status
- **Inline editing** — click-to-edit table cells, add/delete employee rows
- **Filters** — filter by case status and attendance type
- **No backend required** — pure HTML/CSS/JS, all data stays in your browser

## Tech Stack

- HTML / Tailwind CSS (via CDN)
- Vanilla JavaScript
- [SheetJS](https://sheetjs.com/) — Excel import
- [ExcelJS](https://github.com/exceljs/exceljs) — formatted Excel export

## Usage

1. Open `leave_monitoring_dashboard.html` in any modern browser (Chrome, Edge, Firefox).
2. Click **Import employee data** to upload an Excel file, or **Add Employee** to start from scratch.
3. Use the Month/Year selectors to switch the period you're viewing/editing.
4. Click the alert cards (Red/Orange/Green) to filter the table.
5. Click **Export** to download the current data as a formatted Excel workbook.

## Notes / Limitations

- ⚠️ **No persistent storage** — all data lives in memory only. Refreshing or closing the page clears everything, so re-import your Excel file each session (or export before closing).
- Requires an internet connection, since Tailwind, SheetJS, and ExcelJS are loaded from public CDNs.
- Works as a static file — can be hosted for free via GitHub Pages if you want a shareable link.

## License

Add a license of your choice (e.g. MIT) if you plan to share this publicly.
