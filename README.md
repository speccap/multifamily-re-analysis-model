# Multifamily Real Estate Analysis Model

A comprehensive Excel-based model for underwriting multifamily and residential 
real estate investments. Built as a portfolio piece demonstrating financial 
modeling capabilities across acquisition pricing, debt structuring, cash flow 
projection, and equity distribution.

<img width="1521" height="812" alt="Screenshot 2026-02-25 at 5 04 56 PM" src="https://github.com/user-attachments/assets/90582398-6baf-44b0-b843-179e600afe56" />

---

## Overview

<img width="1090" height="30" alt="Screenshot 2026-02-25 at 5 09 46 PM" src="https://github.com/user-attachments/assets/844a3ae0-6e62-42f0-b11d-f7c4240ee3c7" />

The model is structured across several linked worksheets that take a deal from 
raw inputs through to LP/GP returns and promote distributions. It supports 
multiple purchase price methodologies, flexible hold periods, and a toggleable 
equity waterfall that handles both IRR-based and equity multiple-based promote 
structures.

---

## Model Structure

### Inputs
- **Purchase Price Method** — select from manual input, Present Value, Cap Year 1 NOI, 
  or Replacement Cost
- **Hold Period & Terminal Assumptions** — analysis period, terminal cap year, 
  market cap rate, terminal cap rate growth per year
- **Discount Rate & Replacement Cost** — per-unit replacement cost basis, 
  discount rate for DCF pricing
- **Debt Parameters** — loan amount, LTV basis (purchase price / DCF value / 
  terminal value), interest rate, years interest-only, amortization period, 
  loan term, lender fees
- **Growth Rate Assumptions** — independent annual inflation rates for rent, 
  other income, operating expenses, CapEx, and releasing costs

### Unit Mix / Rent Roll
- Unit type, count, and rentable area
- In-place rent and market rent per unit type
- Months to roll to market rent
- Lease term, CapEx per unit per month, free rent per lease
- Days vacant between leases, releasing cost per unit
- Renewal probability
- Blended vacancy, free rent, and releasing cost calculated at the property level

### Expense Projection
- Year 1 expenses input directly
- All line items escalated forward using input growth rates

### Calculations
- Monthly vacancy modeled using lease rollover schedule — vacancy is taken as 
  the greater of rollover-implied vacancy and a general vacancy assumption, 
  expressed as a dollar cost using unit mix data
- Debt service schedule — interest-only period, then fully amortizing, with 
  balloon at loan maturity
- Annual property-level cash flows assembled from revenue, vacancy, expenses, 
  CapEx, and debt service

### Property Returns
- Levered and unlevered cash flows
- Disposition proceeds at terminal cap rate
- Property-level IRR and equity multiple

### Equity Waterfall
- GP/LP equity split with configurable ownership percentages
- Toggle between **IRR-based** and **Equity Multiple (EM)-based** promote 
  structures via dropdown
- Four-hurdle waterfall with configurable thresholds and promote percentages 
  at each tier
- Separate LP and GP capital accounts tracking contributions, preferred return 
  accrual (IRR mode), and distributions
- Return of Capital method: Pari Passu
- Summary of LP and GP returns including IRR, equity multiple, preferred return, 
  return of capital, promote, and excess cash flow

---

## Key Features

- **Dual promote method** — IRR and EM waterfalls share a single set of 
  hurdle rows; toggling the dropdown switches the logic cleanly without 
  structural changes
- **Dynamic hold period** — the model supports variable hold periods; 
  all waterfall and return calculations adjust automatically
- **Capital account integrity** — LP and GP capital accounts roll cleanly 
  with pref accrual isolated to IRR mode; EM mode uses a simple 
  contributions-minus-distributions balance
- **Lease rollover modeling** — vacancy is driven by actual lease expiration 
  logic at the unit type level, not a static assumption

---

## Intended Use

This model is designed for preliminary underwriting and investment analysis 
of multifamily acquisitions. It is not intended as a substitute for 
institutional-grade models with audit trails, sensitivity tools, or legal 
review.

---

## File

| File | Description |
|------|-------------|
| `Residential_Analysis.xlsx` | Main model — all tabs included |

---

## Google Sheets Link

[Residential_Analysis.xlsx](https://docs.google.com/spreadsheets/d/1-d0fT_MBOGBT7g5yMIb-mq709tAvZNsW/edit?usp=sharing&ouid=104566295010899250667&rtpof=true&sd=true)


---

## Technical Notes
- Built in Microsoft Excel
- No VBA or macros — fully formula-driven

---

## More Images

<img width="1292" height="495" alt="Screenshot 2026-02-25 at 5 08 05 PM" src="https://github.com/user-attachments/assets/6d1862ad-33a7-4647-9ce0-140ef57f378b" />
<img width="1297" height="368" alt="Screenshot 2026-02-25 at 5 06 10 PM" src="https://github.com/user-attachments/assets/a249280f-f973-4073-955b-c233d4769135" />
<img width="1575" height="160" alt="Screenshot 2026-02-25 at 5 06 03 PM" src="https://github.com/user-attachments/assets/819219d0-28e5-42b0-91b0-f99b6b6421bb" />
<img width="1265" height="801" alt="Screenshot 2026-02-25 at 5 09 29 PM" src="https://github.com/user-attachments/assets/564a8891-5622-40ef-86ea-dac8c267f09d" />
