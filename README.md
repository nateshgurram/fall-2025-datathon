# fall-2025-datathon

Analyzing Rutgers bus system data to identify operational inefficiency and highlight cases of resource misalignment along routes.

---

## Overview  
This project examines route-level and stop-level efficiency within the Rutgers University bus system. The goal was to determine what drives delays across routes and to identify where bus allocation fails to match actual rider demand. The analysis focused on three core areas: ridership volume, average dwell duration, and vehicle allocation across routes.

Key findings:  
- Bus allocation had the strongest influence on dwell time; routes with fewer assigned buses experienced the longest delays.  
- High ridership did not automatically cause dwell issues when allocation aligned with demand (e.g., H Route).  

---

## Structure  
- `01_EDA_and_preparation.ipynb` → Data cleaning, preparation, merging datasets, and exploratory analysis  
- `02_ridership_route_load.ipynb` → Ridership patterns, load distribution, and high-traffic stop analysis  
- `03_dwell_ridership_correlation.ipynb` → Relationship between dwell time and ridership, route efficiency comparisons, and key metric correlations  

---

## Data Preparation and Exploration  
- Converted datatypes and standardized timestamps for consistency  
- Merged ridership, route, stop, and vehicle datasets using bus and route identifiers  
- Calculated dwell durations and segmented ridership trends by time of day  
- Created intermediate aggregated datasets for route-level and stop-level analysis  

Exploration showed:  
- Busch, Livingston, and College Ave Student Centers had the highest average dwell durations across the system  
- Most dwell periods were short (< 50 minutes), but frequent enough at key stops to cause system-wide delays  
- Routes with limited fleet allocation (four or fewer buses) consistently showed higher dwell durations

---

## Analysis  
- Grouped metrics by route and time period to isolate patterns in ridership and dwell behavior  
- Identified bottleneck stops and measured the compounding effect of congestion on multiple routes  
- Evaluated whether bus allocation matched ridership intensity and operational demands  
- Compared route performance to determine which were over-resourced vs under-resourced 

Findings included:  
- LX & B Routes: High vehicle count but also high dwell time — indicating inefficiency, not demand-driven delays  
- REXL: High dwell duration with moderate vehicle count — suggests insufficient coverage or poor scheduling  
- H Route: High ridership with moderate dwell time — strong alignment of vehicle allocation to demand  
- C Route: Low ridership and low dwell time — appropriate allocation for usage  

---

## Results & Key Insights  
- **Resource Allocation:**  
  - Fleet distribution was the largest factor influencing dwell time  
  - Under-allocated routes experienced the most severe delays relative to demand  

- **Choke Points:**  
  - Student Centers across all campuses drove the highest dwell increases  
  - Congestion at these stops slowed multiple routes simultaneously, magnifying delays  

- **Ridership vs Dwell:**  
  - Ridership had a moderate correlation with dwell time, but allocation was the determining factor — more vehicles enabled faster loading and reduced dwell even under high demand

---

## Conclusion  
System inefficiency was driven more by misaligned bus allocation than by ridership volume itself. Improving performance requires adjusting fleet distribution based on actual route demand rather than maintaining static allocations. Targeted reallocation during peak periods would reduce dwell time, improve flow across campuses, and minimize network-wide delays.

---

## Data Source
[Fall 2025 Datathon](https://github.com/RutgersDataScienceClub/Fall-2025-Datathon)
