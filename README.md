# Business Financial Management Suite

## Overview

Two professional Excel workbooks for **budget tracking and investor management**. Fully automated with formulas, charts, dropdowns, and conditional formatting. Client-ready and production-grade.

**Files:**
- `Executive_Budget_Dashboard_4_Professionals.xlsx`
- `Professional_Investor_Management_System_.xlsx`

**Currency:** Nigerian Naira (₦)

---

## Workbook 1: Executive Budget Dashboard

### What It Does
Tracks income, expenses, and savings across 6 bi-monthly periods with automated calculations and executive dashboards.

### Structure
- **Executive Dashboard** - 8 KPI cards, 2 charts, period selector
- **6 Bi-Monthly Sheets** - Jan-Feb, Mar-Apr, May-Jun, Jul-Aug, Sep-Oct, Nov-Dec
- **Annual Summary** - Year-end totals and ratios

### Key Features
- Auto-carry forward balances between periods
- Planned vs Actual expense tracking with variance analysis
- 5 expense categories: Commodities, Shipping, Logistics, Meta Ads, Delivery
- Conditional formatting (Green=under budget, Red=over budget)
- Line chart with blue marker showing current period
- Bar chart comparing income vs expenses
- Protected formulas, unlocked input cells

### How to Use
1. Set starting balance in Annual Summary (B5)
2. Select current period in Dashboard dropdown (G35)
3. Enter Planned Expenses in bi-monthly sheet (B8:B12)
4. Enter Actual Expenses (C8:C12)
5. Enter Actual Income (C15)
6. Dashboard updates automatically

### Formulas Used
- SUM, IF, cell references
- Cross-sheet linking
- Percentage calculations
- Conditional logic

---

## Workbook 2: Investor Management System

### What It Does
Manages investor records, tracks payments, calculates ROI, and monitors dividend distributions with month-based filtering.

### Structure
- **Investor Dashboard** - 9 KPI cards, 2 charts, month selector
- **Investor Records** - Complete database with 12 fields per investor
- **Payment Tracker** - Transaction history with status tracking

### Key Features

#### Investor Dashboard
- **Month Selector** - Dropdown to filter dividends and ROI by month
- **9 KPI Cards:**
  - Total Investors (COUNTA from records)
  - Total Capital (SUMIFS from Payment Tracker)
  - Monthly ROI Total (filtered by selected month)
  - Active Investors (COUNTIF Active/Inactive column)
  - Capital Paid/Pending (SUMPRODUCT with conditions)
  - Dividend Paid/Pending (filtered by month + status)
  - Total Refunds (completed refunds only)
- Bar charts showing capital distribution and ROI performance
- All metrics reference Payment Tracker + Investor Records

#### Investor Records (12 Fields)
1. Investor Tally #
2. Investor Name
3. Investor Address
4. Investment Capital (₦)
5. Monthly ROI (₦)
6. Date of Investment
7. Bank Name
8. Account Name
9. Account Number
10. **Active/Inactive** (Dropdown: Active/Inactive)

#### Payment Tracker (8 Fields)
1. Tally # (links to Investor Records)
2. Investor Name
3. Payment Type (Dropdown: Capital/Dividend/Refund)
4. Amount (₦)
5. Payment Date (DD/MM/YYYY)
6. Payment Method (Dropdown: Bank Transfer/Cash/Cheque/Mobile Money)
7. Reference #
8. Status (Dropdown: Completed/Pending/Failed)

### How Dashboard Calculations Work
- **Total Capital:** Sums Payment Tracker amounts where Type=Capital, Status=Completed, Investor=Active
- **Capital Paid/Pending:** Counts Payment Tracker entries matching Type, Status, and Active investors
- **Monthly ROI:** Sums Payment Tracker amounts where Type=Dividend, Status=Completed, Month=Selected, Investor=Active
- **Dividend Paid/Pending:** Counts entries filtered by selected month, status, and active investors
- Month extracted from Payment Date column using MONTH() function

### Conditional Formatting
- **Green** = Paid/Completed/Active
- **Yellow** = Pending
- **Red** = Overdue/Failed/Partial/Inactive

### How to Use
1. Add investor in Investor Records sheet (all 12 fields)
2. Set Active/Inactive status in column J
3. Record payments in Payment Tracker (Tally #, Type, Date, ..., Status) Note: Invesors' name and amount are automated
4. Select month in Dashboard (F8) to filter dividends/ROI
5. Dashboard KPIs update automatically

### Formulas Used
- COUNTA, SUM, SUMIFS, COUNTIF, COUNTIFS
- SUMPRODUCT with multiple conditions
- MONTH() for date extraction
- MATCH() for month name to number conversion
- Cross-sheet references with conditional logic

---

## Design & Security

### Color Scheme
- **Budget Dashboard:** Purple, teal, coral, gold, emerald gradients
- **Investor System:** Navy, royal blue, indigo, violet, emerald gradients

### Protection
- All sheets protected with passwords
- Formula cells locked
- Input cells unlocked for data entry
- Dropdowns for controlled inputs

### Data Validation
- Dropdown lists for all status fields
- Date formatting (DD/MM/YYYY)
- Currency formatting (₦#,##0.00)
- Error messages for invalid entries

---

## Requirements

- Microsoft Excel 2016 or later
- Macros not required (formula-based only)
- Works on Windows and Mac

---

## Quick Start

### Budget Dashboard
1. Open workbook
2. Go to Annual Summary → Set starting balance
3. Go to Dashboard → Select current period
4. Enter data in bi-monthly sheets
5. Review Dashboard

### Investor System
1. Open workbook
2. Add investors in Investor Records
3. Record payments in Payment Tracker
4. Select month in Dashboard
5. Review KPIs and charts

---

## Support

For issues or questions:
- Check that formulas are not accidentally deleted
- Verify dates are in DD/MM/YYYY format
- Ensure dropdown selections match exact text
- Use passwords to unprotect sheets if needed

---

## License

These templates are provided as-is for business use. Modify as needed for your operations.
