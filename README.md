# SkyLink Airlines: Revenue Management Predictive Modeling

## Overview

This project uses historical airline data to build a regression model that predicts the number of `empty_seats` on a flight.

The analysis was developed for the Revenue Management stakeholder group and focuses on using predictive modeling to evaluate different overbooking policies for upcoming flights.

**Stakeholder:** Revenue Management  
**Prediction Target:** `empty_seats`  
**Prediction Task:** Regression  
**Team:** Team 4

### Team Members

- Kayla Pham
- Serena Mei
- Hilton Nguyen
- Eva Maheshwari
- William Somat

---

## Dataset

The project uses the `SkyLink_Revenue_Management_Data.xlsx` workbook, which contains three sheets:

### Historical_Data

Contains completed flights used for:

- Data cleaning
- Exploratory analysis
- Model development
- Model evaluation

### Future_Policy_Scenarios

Contains 48 upcoming flights, with each flight repeated under four possible overbooking policies.

This results in:

**192 rows = 48 flights × 4 policies**

The four policies are:

| Policy | Overbooking Allowance |
|---|---:|
| Conservative | +2 |
| Status Quo | +4 |
| Moderate | +5 |
| Aggressive | +8 |

Because all four policies are evaluated on the same 48 upcoming flights, their predicted outcomes can be compared directly.

### Data_Dictionary

Provides descriptions of the variables in the dataset, including when each variable becomes available. This was used to identify variables that could create data leakage.

---

## Tools & Libraries

The analysis was completed using Python and the following libraries:

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
