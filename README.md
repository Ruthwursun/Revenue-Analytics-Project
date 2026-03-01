# Revenue Analytics Dashboard (Power BI)

## Overview
Built an end-to-end revenue analytics solution in Power BI:
- Cleaned and standardized raw transaction data
- Normalized Flat/% pricing into INR per transaction
- Computed ERP Revenue, Edviron Gross Revenue, Edviron Net Revenue
- Built interactive report pages + dashboard with slicers

## Pages Included
- Dashboard
- Time Summary
- Partner Performance
- Gateway & Payment Method
- Pending vs Settled Exposure
- Assumptions & Logic

## Revenue Logic
- Merchant_INR:
  - FLAT → Merchant Pricing
  - PERCENT → Transaction Amt * Merchant Pricing / 100
- Partner_INR:
  - FLAT → Partner Pricing
  - PERCENT → Transaction Amt * Partner Pricing / 100
- EdvironBuying_INR:
  - FLAT → Edviron Buying
  - PERCENT → Transaction Amt * Edviron Buying / 100

- ERP Revenue = Partner_INR (Success-only)
- Edviron Gross Revenue = Merchant_INR − Partner_INR
- Edviron Net Revenue = Edviron Gross − EdvironBuying_INR
- Exposure = Pending vs Settled (based on Is_Success)

## Key DAX Measures
- Total Transaction Value
- ERP Revenue
- Edviron Gross Revenue
- Edviron Net Revenue
- Profit Margin %
- Contribution %
- ERP Rank
- Pending vs Settled metrics

## Interactivity
Slicers included:
- Date Range
- ERP Partner
- Gateway
- Payment Method

## Notes / Assumptions
- Date & Time column was cleaned and standardized in Power Query.
- Current dataset shows 100% settled transactions (Pending Exposure = 0).

## Screenshots
See `/Screenshots` folder.
