# JobMatch Data Analysis - Group Project Phase 1

A comprehensive data analysis of the JobMatch recruiting platform to diagnose performance issues and recommend improvements.

## Project Overview

**Team:** Data Science and Analytics Class (BADM 576)  
**Due:** February 17, 2026  
**Status:** Analysis Complete ✓

### Objective
Analyze JobMatch's recruiting platform data to:
- Understand data structure and quality
- Identify key performance issues
- Evaluate algorithm effectiveness
- Recommend KPIs and data products to build

## Key Findings

### 🎯 The Big Problems

1. **Salary Mismatches (Critical)**
   - 82% of offer declines due to salary expectations not being met
   - Average gap: $18,663 below expectations on declined offers
   - Annual revenue impact: $300-600k

2. **Distribution Inequality**
   - Gini coefficient: 0.506 (highly unequal)
   - Top 10% of jobs get 50%+ of applications
   - 18 jobs have zero applications

3. **Lead-Level Mismatch**
   - Lead candidates: 1.27% hire rate
   - Entry-level candidates: 3.45% hire rate
   - 51.6% of applications are for Lead roles

4. **Platform Engagement Gap**
   - 6.1% of quality candidates never engage
   - Likely onboarding/visibility issue, not quality issue

5. **Algorithm Blindspot**
   - Relevance score only available at "view" stage
   - No downstream scoring to predict success
   - Can't capture salary fit

### 📊 Key Numbers

| Metric | Value | 95% CI |
|--------|-------|--------|
| Application-to-Hire Rate | 1.79% | N/A |
| Offer Acceptance Rate | 46.55% | 43.94% - 49.16% |
| Entry-Level Hire Rate | 3.45% | 2.74% - 4.16% |
| Lead-Level Hire Rate | 1.27% | 1.11% - 1.43% |
| Salary Decline Rate | 82% | - |
| Inactive Candidates | 6.1% | - |

## Data

### Source Files
- `JobData HW/JobMatch_Data/candidates.csv` - 5,000 job seekers
- `JobData HW/JobMatch_Data/companies.csv` - 200 employers
- `JobData HW/JobMatch_Data/jobs.csv` - 1,500 job postings
- `JobData HW/JobMatch_Data/events.csv` - ~200,000 platform events

### Data Dictionary
See `BADM576_JobMatch_DataDictionary.docx.pdf` for complete column definitions and event types.

## Analysis Sections

### Part A: Data Understanding
- Table shapes and unit of observation
- Data quality issues and missing values
- Table relationships and join keys
- "in_" prefix column meanings

### Part B: Key Findings
- **B.1:** Recruiting funnel analysis by seniority
- **B.2:** Offer acceptance rates and salary mismatches
- **B.3:** Application distribution across jobs
- **B.4:** Inactive candidate profiles
- **B.5:** Matching signal (relevance score) predictiveness

### Part C: Generalization
- 95% confidence intervals for key metrics
- Sample vs. population assessment
- Factors that could change patterns
- Data limitations and what we can't measure

### Part D: Recommendations
- **3 KPIs:** Offer Acceptance Rate, Gini Index, Engagement Rate
- **3 Data Products:**
  1. Salary Acceptance Predictor
  2. Diversity-Aware Job Recommender
  3. Smart Onboarding System

## Usage

### Requirements
```bash
pip install pandas numpy matplotlib seaborn scipy
```

### Running Analysis
```bash
jupyter notebook project.ipynb
```

All analysis is contained in the notebook with executable cells for each section.

## Key Recommendations

### Immediate (High Priority)
- Build Salary Prediction Model to prevent offer mismatches
- Implement manual offer review for high-risk salary gaps
- Expected impact: +$300-600k annual revenue

### Short-term (Medium Priority)
- Rebalance job recommendations to reduce concentration
- Improve first-time user onboarding
- Expected impact: +5-10% engagement

### Long-term
- Extend relevance scoring beyond "view" stage
- Implement post-hire outcome tracking
- Build competitive benchmarking

## Files

```
.
├── project.ipynb                          # Main analysis notebook
├── README.md                              # This file
├── .gitignore                             # Git ignore rules
└── JobData HW/
    └── JobMatch_Data/
        ├── candidates.csv                 # Candidate profiles
        ├── companies.csv                  # Company information
        ├── jobs.csv                       # Job postings
        └── events.csv                     # Platform events
```

## Next Steps

1. ✓ Data analysis complete
2. ⏳ Write 10-page PDF report

## Notes

- All numbers are statistically tested with p-values and confidence intervals
- Visualizations include: bar charts, histograms, Lorenz curves, boxplots
- Analysis considers data limitations and generalization concerns
- Recommendations are actionable and tied to specific findings

---

**Analysis Date:** February 22, 2026  
**Analyst:** Meryem (mhrafiq2)  
**Course:** BADM 576 - Data Science and Analytics
