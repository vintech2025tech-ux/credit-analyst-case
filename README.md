# d.light Case Study Portfolio Analysis

## Overview
This project analyzes the credit performance of a PAYGO solar portfolio, comparing d.light and Wakanda Solar, using Python for data wrangling and KPI calculation. Outputs are saved to Excel for Tableau dashboarding and PNG charts for reporting.

## Workflow
1. **Data Loading:** Reads contracts and payments data from provided CSVs.
2. **Data Cleaning:** Handles missing values, date parsing, and deduplication.
3. **KPI Calculation:** Computes industry-standard credit KPIs:
   - Collection Rate
   - Repayment Rate
   - Portfolio at Risk (PAR30, PAR60, PAR90)
   - Writeoff Rate (modeled from payment timeline)
   - First Payment Default (FPD)
   - Customer Activation Ratio
   - Average Days Late
   - Active Customers (last 3 months)
   - Vintage Analysis (cohort performance)
   - Product Analysis (if product data available)
4. **Charting:** Plots all KPIs and trends, saving as PNG for reporting.
5. **Excel Export:** All KPI tables are saved to a single Excel file for Tableau use.

## How to Use
- Run `Dlight Case Study.py` in Python 3.13+.
- The output Excel file is always saved as:
  ```
  C:\Users\Finance Trainee\Downloads\dlight_cleaned_data.xlsx
  ```
- Connect Tableau to this file for automated dashboard refresh.
- Use PNG charts for quick reporting or slide decks.

## Notes
- All code is business standard and suitable for executive review.
- Vintage and Product Analysis are included for deeper insights.
- See `executive_summary.md` for key findings and recommendations.

## Troubleshooting
- If you see a `KeyError: 'contract_value_usd'`, check that your contracts data includes this column.
- For the FutureWarning on `'Q'` frequency, update `freq='Q'` to `freq='QE'` in all `pd.date_range` calls.

## Contact
For questions or improvements, reach out to me @ vaaketch@gmail.com or submit feedback with your review.
