# Soda Bottling Production Line Analysis

## Project Overview

This project analyzes operational performance data from a soda bottling production line to identify inefficiencies, downtime drivers, and operator-specific performance patterns.

The objective is to use data analysis to answer practical business questions related to production efficiency and operational improvement.

---

## Business Questions

The analysis focuses on four key questions:

1. **What is the current line efficiency?**
2. **Are any operators underperforming?**
3. **What are the leading factors for downtime?**
4. **Do any operators struggle with particular types of operator error?**

---

## Dataset

The source data is provided as a multi-sheet Excel workbook containing production and downtime information.

### Included Sheets

| Sheet Name | Description |
|----------|-------------|
| Line Productivity | Batch-level production data including operators, products, and timestamps |
| Products | Product reference information |
| Downtime Factors | Descriptions of downtime categories and operator error classification |
| Downtime Data | Downtime duration per batch and factor |

---

## Data Preparation

The following preprocessing steps were performed:

- Imported Excel sheets into pandas DataFrames
- Inspected data structure and data types
- Renamed downtime factor columns using the downtime factor description table
- Replaced missing downtime values with zero
- Calculated total downtime per batch
- Created additional analytical metrics such as downtime frequency and operator-related downtime

---

## Methods & Analysis

### 1. Line Efficiency Analysis

Production efficiency was estimated using:

```text
Machine Running Time = Total Batch Time − Total Downtime
Efficiency = Running Time / Total Batch Time
﻿﻿
This provides an estimate of how efficiently the production line operates.
```
---

### 2. Operator Performance Analysis

Operators were compared using:
```text
* Average downtime minutes per batch
* Total downtime
* Number of downtime events per batch

This allows comparison of both downtime severity and frequency.
```
---

### 3. Downtime Driver Analysis

Downtime causes were analyzed from two perspectives:
```text
* Frequency → how often a factor occurs
* Severity → how many downtime minutes it causes

This helps identify the most impactful operational bottlenecks.
```
---
### 4. Operator Error Analysis

Downtime factors classified as operator-related were isolated and grouped by operator.
```text
A heatmap was used to identify recurring operator-specific error patterns.
```
---
### Tools Used
```text
* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook
* Git / GitHub
* Visual Studio Code
```

### Key Findings

Operational Efficiency
```text
The production line shows measurable downtime losses that reduce effective machine running time.

Operator Performance

Operators show different downtime patterns:

* Some experience fewer but longer interruptions
* Others experience more frequent but shorter disruptions
```

### Major Downtime Drivers

Key downtime contributors include:
```text
* Machine adjustment
* Batch change
* Inventory-related interruptions
```
### Operator-Specific Issues

Distinct patterns were identified:
```text
* Mac shows elevated downtime during batch changes
* Dennis and Charlie show higher machine adjustment downtime
* Dee shows smaller but more distributed operator-related issues
```

### Recommendations

Based on the analysis:
```text
* Improve operator training for recurring operator-related issues
* Review machine setup / adjustment procedures
* Standardize batch change processes
* Improve inventory coordination to reduce avoidable stoppages
```

### Team

Project completed collaboratively as part of a data analytics course project.
```text
Contributors:

* Hendrik Albrecht
* Natalia Ströher
```

### Status

Completed initial analysis. Future improvements could include:
```text
* statistical significance testing
* time trend analysis
* predictive downtime modeling
* dashboard visualization (Power BI / Tableau)
```
