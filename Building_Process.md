# Building Process — Tata Motors O2C Analysis
## How This Project Was Built Step by Step

---

## Project Genesis

This project was built to demonstrate real O2C domain 
expertise using actual company data — not fictional data.

I chose Tata Motors because:
- They publish detailed consolidated financial results publicly
- Their O2C performance is exceptional and worth analyzing
- The automotive sector has clear industry benchmarks for comparison
- The data is 100% verifiable by anyone

---

## Phase 1 — Research & Data Collection

### Step 1 — Identified the Business Problem
The core question: *How does Tata Motors' O2C performance compare 
to industry benchmarks, and what drives their competitive advantage?*

Key metrics to analyze:
- Days Sales Outstanding (DSO)
- Receivables Turnover
- Working Capital Efficiency
- Segment contribution to O2C performance

### Step 2 — Downloaded Public Data
**Source:** Tata Motors FY2024 Integrated Annual Report  
**URL:** https://www.tatamotors.com/financials/

Data extracted:
- Total Revenue: ₹4,37,927.77 Cr (Consolidated P&L)
- Trade Receivables: ₹16,924 Cr (Consolidated Balance Sheet)
- Segment breakdown: JLR 68.21%, CV 17.75%, PV 11.79%
- 3-year historical data: FY2022, FY2023, FY2024

### Step 3 — Verified All Numbers
Cross-referenced data across:
- Balance Sheet
- Notes to Financial Statements
- Segment Reporting
- Q4 FY24 Results Press Release

---

## Phase 2 — Excel Data Model

### Step 4 — Built Data Model in Excel
Created 9 sheets in the Excel workbook:

| Sheet | Contents |
|---|---|
| YoY_Trends | 3-year DSO, Revenue, Receivables data |
| Segment_Analysis | JLR, CV, PV, Others revenue breakdown |
| Benchmark_Comparison | Tata vs competitors vs industry benchmarks |
| Working_Capital | ₹37,039 Cr advantage calculation |
| Financial_Ratios | All key O2C metrics |
| Scenarios | 6 DSO scenarios with WC impact |
| Recommendations | 6 strategic recommendations |
| Best_Practices | What drives Tata's O2C excellence |
| Data_Sources | Complete citation and methodology |

### Step 5 — Calculated Key Metrics

**DSO Calculation:**
```
DSO = (Trade Receivables / Revenue) × 365
DSO = (₹16,924 Cr / ₹4,37,927.77 Cr) × 365
DSO = 14.1 Days
```

**Working Capital Advantage:**
```
Daily Revenue = ₹4,37,927.77 Cr / 365 = ₹1,199.8 Cr/day
Advantage = (45 - 14.1) days × ₹1,199.8 Cr/day
Advantage = ₹37,039 Cr
```

**Receivables Turnover:**
```
Turnover = Revenue / Trade Receivables
Turnover = ₹4,37,927.77 Cr / ₹16,924 Cr
Turnover = 25.83x
```

---

## Phase 3 — Power BI Dashboard

### Step 6 — Imported Data into Power BI
- Connected Power BI to Excel workbook
- Imported all 9 sheets as separate tables
- Verified data loaded correctly

### Step 7 — Built Page 1 (O2C Performance Overview)

**Design decisions:**
- Navy header to establish corporate identity
- Executive Summary panel on left — tells the story before charts
- 4 KPI cards on right — immediate key metrics visibility
- Line chart with shaded area — shows improvement trend clearly
- Donut chart — shows JLR dominance driving O2C advantage
- Bar chart with 3-colour logic — hero (Tata), thresholds, competitors

**Colour logic:**
- Tata Motors bar: Deep navy `#003366` (hero)
- Threshold bars: Green (world-class standards)
- Competitor/average bars: Grey/light blue

### Step 8 — Built Page 2 (Strategic Analysis & Risk)

**Design decisions:**
- Strategic Insights box mirrors Executive Summary from Page 1
- Recommendations table with structured columns
- Key Risks panel shows operational risk monitoring
- Scenario Analysis table with colour-coded risk levels

**Risk level colour coding:**
- 🟢 LOW — Best Case, Current State
- 🟡 MEDIUM — Moderate risk scenarios
- 🟠 HIGH — Severe slowdown scenario
- 🔴 CRITICAL — Industry average position

### Step 9 — Applied Formatting Standards

**Typography:**
- Section titles: 14pt, Bold, Navy `#003399`
- Section headers: 10pt, Bold, Navy `#003399`
- Body text: 9pt, Normal, Dark grey `#333333`
- Risk titles: 14pt, Bold, Red `#C62828`

**Layout consistency:**
- Standard canvas: 1280 × 950px
- Left margin: 20px on all elements
- Consistent section spacing throughout

---

## Phase 4 — Analysis & Insights

### Step 10 — Identified Key Insights

**Insight 1 — Competitive Moat:**
31-day advantage over industry creates structural differentiation 
that mass-market competitors cannot easily replicate.

**Insight 2 — Business Model Driver:**
JLR's 68% revenue mix is the primary driver — premium customers 
pay faster. This is a business model advantage, not just 
operational efficiency.

**Insight 3 — Working Capital Flexibility:**
₹37,039 Cr advantage enables EV R&D (₹12,974 Cr) + Debt 
reduction (₹26,547 Cr) without new borrowing.

**Insight 4 — Continuous Improvement:**
30% DSO reduction over 3 years (20.2→16.6→14.1) demonstrates 
operational excellence culture, not a one-time improvement.

### Step 11 — Built Strategic Recommendations
6 recommendations developed based on analysis:
- 3 HIGH priority (sustain advantage)
- 2 MEDIUM priority (expand advantage)
- 1 LOW priority (risk preparation)

### Step 12 — Developed Risk Framework
4 risks identified with current status and mitigation strategies:
- JLR Revenue Mix Decline (🟢 HEALTHY — currently 68%)
- DSO Deterioration (🟢 EXCELLENT — currently 14.1 days)
- Economic Slowdown (🟡 MONITOR)
- Competitor Disruption (🟡 MONITOR)

---

## Key Design Decisions Explained

### Why Navy as Primary Colour?
Professional, corporate, consistent with financial services 
industry standards. Creates strong visual identity.

### Why Executive Summary Panel?
Most dashboards show data without context. The Executive Summary 
answers "so what?" before the viewer looks at any chart — 
mimicking how a real management report would be structured.

### Why 3-Colour Logic on Bar Chart?
Tata (navy) vs Thresholds (green) vs Competitors (grey) 
immediately communicates competitive positioning without 
requiring the viewer to read every label.

### Why Shaded Area on Line Chart?
The downward trend is the story. Shading emphasises the 
improvement visually — the filled area getting smaller over 
time reinforces the narrative of continuous improvement.

---

## Challenges Faced & Solutions

| Challenge | Solution |
|---|---|
| DAX regional settings (semicolons vs commas) | Used hardcoded IF/SWITCH approach |
| Colour consistency across pages | Created master colour reference |
| Text panel vs chart balance | Used 50/50 split on Page 1 |
| Making data source credible | Added author credit line in header |

---

## Time Investment

| Phase | Time |
|---|---|
| Research & Data Collection | 3 hours |
| Excel Data Model | 2 hours |
| Power BI Page 1 | 4 hours |
| Power BI Page 2 | 3 hours |
| Formatting & Polish | 2 hours |
| Documentation | 2 hours |
| **Total** | **~16 hours** |

---

