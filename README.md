# Canadian Vehicle Reimbursement and Fuel Cost Intelligence

An interactive Power BI report that estimates annual fuel costs for 2026 vehicles across Canadian locations. Users can compare vehicles at a standard distance of 20,000 km or adjust the annual distance to compare estimated fuel costs with the 2026 Canada Revenue Agency (CRA) provincial automobile allowance benchmark.

[Download the Power BI report (.pbix)](Canadian%20Vehicle%20Reimbursement%20and%20Fuel%20Cost%20Intelligence.pbix) and open it in Power BI Desktop to use the interactive filters and scenario controls.

![Power BI Reimbursement Scenario showing estimated fuel cost and the CRA provincial allowance benchmark](Reimbursement%20Scenario.png)

## Report pages

| Page | What it shows |
| --- | --- |
| [Executive Cost Overview](Executive%20Overview.png) | Canadian gasoline price trends, city-level price comparisons, and estimated vehicle fuel costs at 20,000 km. |
| [Vehicle Comparison](Vehicle%20Comparison.png) | A sortable vehicle comparison table with filters for location, vehicle class, and fuel type. |
| [Reimbursement Scenario](Reimbursement%20Scenario.png) | A calculator that updates the estimated fuel cost and CRA provincial allowance benchmark when users change the vehicle, location, or annual distance. |
| [Data Quality and Methodology](Methodology.png) | Source coverage, validation checks, assumptions, and a worked fuel-cost calculation. |

## Example scenario

A Kia Niro FE in Ottawa–Gatineau (Ontario part) has a combined fuel consumption rating of **4.4 L/100 km**. At the September 2026 regular gasoline price of **$1.784 CAD/L**, the report estimates:

| Annual distance | Estimated fuel cost | 2026 CRA provincial allowance benchmark |
| ---: | ---: | ---: |
| 20,000 km | $1,569.92 CAD | $13,700.00 CAD |
| 25,000 km | $1,962.40 CAD | $17,050.00 CAD |

At 25,000 km, the vehicle uses an estimated **1,100 L** of gasoline. Multiplying that volume by **$1.784 CAD/L** gives the **$1,962.40 CAD** estimate.

The CRA provincial allowance benchmark covers broader vehicle costs. The report displays it alongside the fuel-only estimate to show how both amounts change with annual distance.

## Data preparation and validation

- Prepared **613 vehicle records** and **7,614 monthly fuel-price observations** in Power Query.
- Used monthly fuel prices from **January 2015 through September 2026** and matched vehicle configurations to the latest available price by location and fuel type.
- Standardized fuel labels and checked required fields for missing values and type errors. Checked vehicle records for exact duplicates and fuel prices for duplicate month, location, and fuel-type combinations.
- Excluded E85 configurations from the fuel-cost estimates because the selected price series had no matching E85 prices.
- Used DAX to calculate scenario fuel costs and the tiered CRA provincial allowance benchmark.

## Tools

Power BI Desktop · Power Query · DAX

## Data sources

- [Natural Resources Canada — Fuel consumption ratings](https://open.canada.ca/data/en/dataset/98f1a129-f628-4ce4-b24d-6f16bf24dd64)
- [Statistics Canada — Monthly retail prices for gasoline and fuel oil, table 18-10-0001-01](https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?pid=1810000101)
- [Canada Revenue Agency — Automobile and motor vehicle allowances](https://www.canada.ca/en/revenue-agency/services/tax/businesses/topics/payroll/benefits-allowances/automobile/automobile-motor-vehicle-benefits.html)
