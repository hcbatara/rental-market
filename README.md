# rental-market
ds4300 spring 2026

Boston Rental Market Analysis
Overview
This project investigates the relationship between new residential construction and rent growth across Boston from 2015 to 2025, using building permit records from the City of Boston alongside Zillow's rent index data. The analysis focuses on 27 Boston ZIP codes, with a particular emphasis on neighborhoods with large Northeastern University student populations.

Data
- Building permits: City of Boston public permit records (600,000+ records), filtered for new residential construction (1-4 family homes, multi-family, and larger buildings)
- Rent data: Zillow Observed Rent Index (ZORI), filtered to Boston ZIP codes

Approach
- Data loading (load_data.ipynb): Cleaned and loaded raw permit and rent data into MongoDB, restructuring Zillow's wide-format monthly rent columns into nested time-series documents per ZIP code
- Analysis (hw6.ipynb):
  - Built MongoDB aggregation pipelines to filter, group, and sort permit data by type, occupancy, and year
  - Calculated total approved residential construction permits per year (2015–2025)
  - Visualized rent trends over time, with a focused comparison across Northeastern-adjacent neighborhoods (Mission Hill, Fenway, Jamaica Plain, Roxbury, South End, Back Bay, Longwood)

Key Finding
New residential construction has not kept pace with rising rents across Boston over the past decade, with construction permit volume trending downward in several recent years even as rents in nearly all analyzed ZIP codes continued to climb.

Tools
Python, pandas, PyMongo, MongoDB, matplotlib, seaborn

Files
load_data.ipynb — data loading and MongoDB setup
hw6.ipynb — analysis and visualizations
