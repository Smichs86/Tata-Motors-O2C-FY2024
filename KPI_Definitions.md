# KPI Definitions & Formulas
## Tata Motors O2C Performance Analysis | FY2024

---

## 1. Days Sales Outstanding (DSO)

**Definition:**  
The average number of days it takes a company to collect 
payment after a sale has been made.

**Formula:**
```
DSO = (Trade Receivables / Revenue) × 365
```

**Tata Motors FY2024:**
```
DSO = (₹16,924 Cr / ₹4,37,927.77 Cr) × 365
DSO = 14.1 Days
```

**Interpretation:**
- Lower DSO = Better (faster cash collection)
- Tata Motors at 14.1 days = World-class performance
- Industry average = 45 days
- Tata is 31 days faster than industry

**Industry Benchmarks:**
| Level | DSO | Classification |
|---|---|---|
| World-Class | < 30 Days | Best Practice |
| Excellent | 30-35 Days | Excellence Threshold |
| Good | 35-45 Days | Industry Average |
| Poor | > 45 Days | Below Average |

---

## 2. Receivables Turnover Ratio

**Definition:**  
How many times per year a company collects its average 
accounts receivable. Higher = better.

**Formula:**
```
Receivables Turnover = Revenue / Trade Receivables
```

**Tata Motors FY2024:**
```
Receivables Turnover = ₹4,37,927.77 Cr / ₹16,924 Cr
Receivables Turnover = 25.83x
```

**Interpretation:**
- 25.83x means Tata collects its entire receivables 
  balance 25.83 times per year
- Industry average is approximately 8-10x
- Tata's ratio is 2.5-3x better than industry

---

## 3. Working Capital Advantage

**Definition:**  
The additional cash available to Tata Motors because 
they collect payments faster than the industry average.

**Formula:**
```
Daily Revenue = Annual Revenue / 365
Working Capital Advantage = 
    (Industry DSO - Company DSO) × Daily Revenue
```

**Tata Motors FY2024:**
```
Daily Revenue = ₹4,37,927.77 Cr / 365 = ₹1,199.8 Cr/day

Working Capital Advantage = (45 - 14.1) × ₹1,199.8 Cr
Working Capital Advantage = 30.9 × ₹1,199.8 Cr
Working Capital Advantage = ₹37,039 Cr
```

**Interpretation:**
- Tata has ₹37,039 Cr MORE cash available compared 
  to a company with industry-average DSO
- This enables:
  - EV R&D investment (₹12,974 Cr in FY24)
  - Debt reduction (₹26,547 Cr in FY24)
  - Growth without new borrowing

---

## 4. Bad Debt Ratio

**Definition:**  
Percentage of revenue that becomes uncollectable.

**Formula:**
```
Bad Debt Ratio = (Bad Debt Expense / Revenue) × 100
```

**Tata Motors FY2024:**
```
Bad Debt Ratio = 0.53%
```

**Interpretation:**
- 0.53% is exceptionally low
- Industry acceptable range: 1-2%
- Tata's ratio indicates strong credit management 
  and quality customer base

---

## 5. YoY DSO Change %

**Definition:**  
Year-over-year percentage improvement in DSO.

**Formula:**
```
YoY DSO Change % = 
    ((Current DSO - Previous DSO) / Previous DSO) × 100
```

**Tata Motors Calculations:**
```
FY22→FY23: ((16.6 - 20.2) / 20.2) × 100 = -17.8%
FY23→FY24: ((14.1 - 16.6) / 16.6) × 100 = -15.1%
3-Year Total: ((14.1 - 20.2) / 20.2) × 100 = -30.2%
```

**Interpretation:**
- Negative % = Improvement (DSO reduced)
- 30% improvement over 3 years = Operational excellence

---

## 6. DSO Impact per Day

**Definition:**  
Working capital impact of every 1-day change in DSO.

**Formula:**
```
Impact per Day = Annual Revenue / 365
```

**Tata Motors FY2024:**
```
Impact per Day = ₹4,37,927.77 Cr / 365
Impact per Day = ₹1,199.8 Cr per day
```

**Interpretation:**
- Every 1-day increase in DSO = ₹1,199.8 Cr less cash
- Every 1-day decrease in DSO = ₹1,199.8 Cr more cash
- Used in Risk Framework: DSO Alert at >18 days

---

## 7. JLR Revenue Mix %

**Definition:**  
Jaguar Land Rover segment revenue as % of total revenue.

**Formula:**
```
JLR Mix % = (JLR Revenue / Total Revenue) × 100
```

**Tata Motors FY2024:**
```
JLR Mix % = 68.21%
```

**Significance:**
- JLR customers (premium automotive) pay faster
- Higher JLR mix = Lower DSO for consolidated entity
- Risk threshold: JLR mix must stay > 60%
- If JLR drops to 60%: DSO could rise to 18 days

---

## 8. Scenario Analysis Metrics

### Best Case Scenario (DSO = 12 days)
```
WC Impact = (14.1 - 12) × ₹1,199.8 Cr = +₹2,518 Cr
```

### JLR Mix 60% Scenario (DSO = 18 days)
```
WC Impact = (14.1 - 18) × ₹1,199.8 Cr = -₹4,680 Cr
```

### Mild Slowdown Scenario (DSO = 20 days)
```
WC Impact = (14.1 - 20) × ₹1,199.8 Cr = -₹7,070 Cr
```

### Severe Slowdown Scenario (DSO = 30 days)
```
WC Impact = (14.1 - 30) × ₹1,199.8 Cr = -₹19,047 Cr
```

### Industry Average Scenario (DSO = 45 days)
```
WC Impact = (14.1 - 45) × ₹1,199.8 Cr = -₹37,039 Cr
```

---

## 9. DAX Measures Used in Power BI

### DSO Measure
```dax
DSO = DIVIDE(SUM('YoY Trends'[Trade_Receivables]),
             SUM('YoY Trends'[Revenue])) * 365
```

### Receivables Turnover Measure
```dax
Receivables_Turnover = 
    DIVIDE(SUM('YoY Trends'[Revenue]),
           SUM('YoY Trends'[Trade_Receivables]))
```

### Working Capital Advantage Measure
```dax
WC_Advantage = 
    (45 - [DSO]) * DIVIDE(SUM('YoY Trends'[Revenue]), 365)
```

### YoY DSO Change
```dax
YoY DSO Change % =
IF(
    MAX('YoY Trends'[Fiscal_Year]) = 2023;
    ROUND(DIVIDE(
        MAX('YoY Trends'[DSO]) - 
        CALCULATE(MAX('YoY Trends'[DSO]);
        FILTER(ALL('YoY Trends');
        'YoY Trends'[Fiscal_Year] = 2022));
        CALCULATE(MAX('YoY Trends'[DSO]);
        FILTER(ALL('YoY Trends');
        'YoY Trends'[Fiscal_Year] = 2022))
    ) * 100; 1);
    IF(
        MAX('YoY Trends'[Fiscal_Year]) = 2024;
        ROUND(DIVIDE(
            MAX('YoY Trends'[DSO]) - 
            CALCULATE(MAX('YoY Trends'[DSO]);
            FILTER(ALL('YoY Trends');
            'YoY Trends'[Fiscal_Year] = 2023));
            CALCULATE(MAX('YoY Trends'[DSO]);
            FILTER(ALL('YoY Trends');
            'YoY Trends'[Fiscal_Year] = 2023))
        ) * 100; 1);
        BLANK()
    )
)
```

*Note: Uses semicolons as separators due to regional 
settings. Replace with commas if using English locale.*

---

## 10. Key Abbreviations

| Abbreviation | Full Form |
|---|---|
| DSO | Days Sales Outstanding |
| O2C | Order to Cash |
| AR | Accounts Receivable |
| WC | Working Capital |
| JLR | Jaguar Land Rover |
| CV | Commercial Vehicles |
| PV | Passenger Vehicles |
| YoY | Year over Year |
| Cr | Crores (Indian currency unit) |
| FY | Financial Year (April to March) |

---

