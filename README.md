# Canadian Vehicle Reimbursement and Fuel Cost Intelligence

An interactive Power BI report that compares estimated fuel costs across
2026 vehicle configurations and Canadian locations. A scenario calculator
lets users change annual driving distance and compare estimated fuel costs
with the 2026 CRA provincial automobile allowance benchmark.

![Reimbursement Scenario page](03-reimbursement-scenario.png)

## Report pages

- [Executive Cost Overview](01-executive-overview.png) — Fuel price trends,
  city comparisons, and estimated vehicle fuel costs at 20,000 km.
- [Vehicle Comparison](02-vehicle-comparison.png) — Rank vehicles by
  estimated fuel cost and filter by location, vehicle class, and fuel type.
- [Reimbursement Scenario](03-reimbursement-scenario.png) — Select a
  vehicle, location, and annual distance to compare both amounts in CAD.
- [Data Quality and Methodology](04-methodology.png) — Data sources,
  validation checks, coverage limits, and a worked calculation.

## Example scenario

For a Kia Niro FE in Ottawa–Gatineau (Ontario part), the estimated fuel
cost is $1,569.92 CAD at 20,000 km and $1,962.40 CAD at 25,000 km,
using September 2026 regular gasoline prices. The CRA provincial allowance
benchmark covers broader vehicle costs.

## Data preparation and validation

Used Power Query to prepare 613 vehicle records and 7,614 monthly fuel-price
observations, standardize fuel labels, and match vehicle configurations to
the latest available prices by location and fuel type. Checked required
fields, data types, and duplicates. E85 configurations were excluded from
cost estimates because the selected price series has no matching E85 prices.

## Tools and sources

**Tools** — Power BI Desktop, Power Query, DAX

- Natural Resources Canada — 2026 fuel consumption ratings
- Statistics Canada — Monthly retail fuel prices, table 18-10-0001-01
- Canada Revenue Agency — 2026 provincial automobile allowance rates
