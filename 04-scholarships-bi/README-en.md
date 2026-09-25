# PROJECT 4: Scholarships & Business Intelligence

**Status:** ✅ Production  
**Technology Stack:** Excel | Google Sheets | Power BI | SQL  
**Organization:** Universidad Metropolitana (779 unique students)  
**Impact:** $55,000 USD operational value

---

## Overview

Data consolidation and BI system that unified 5 separate scholarship databases into a single source of truth with real-time dashboards for cost analysis, benefit validation, and strategic decision-making.

### The Challenge
- 5 separate systems tracking student scholarships (fragmented data)
- 779 unique students across multiple programs
- Manual reconciliation took 8 hours/month
- No visibility into total scholarship costs by program
- Benefits/discounts inconsistently applied

### The Solution
- Consolidated 5 data sources into unified Google Sheets database
- Validation rules comparing expected vs. applied discounts
- Executive, Program, and Career dashboards
- Cost analysis by student, program, and career
- Automated monthly reporting to leadership

---

## Key Metrics

| Metric | Result | Impact |
|--------|--------|--------|
| **Students Consolidated** | 779 unique | 100% visibility |
| **Data Completeness** | 98% | Minimal exceptions |
| **Validation Error Rate** | 2.1% | 27 flagged issues |
| **Cost Visibility** | +100% | Accurate budgeting |
| **Exception Documentation** | 100% | Compliance |
| **Monthly Report Time** | 1 hour | Down from 8 hours |

**Annual Value: ~$55,000 USD (labor + decision quality)**

---

## Database Structure

```
Master Database (Google Sheets)
├── Student ID | Name | Career
├── Program(s) | Enrollment Date | Status
├── Expected Discount % | Applied Discount %
├── Benefit Amount (USD) | Renewal Type
└── Validation Status (GREEN/YELLOW/RED)

Reference Table
├── Student → Program(s) → Expected Discount
├── Exception Reasons (Faculty Approvals)
└── Renewal Schedule
```

---

## Dashboard Components

**Executive Dashboard:**
- Total scholarship cost
- Distribution by program
- Cost per student (average)
- Trends month-over-month

**Program Dashboard:**
- Participation rates
- Cost by program
- Budget vs. actual
- Enrollment trends

**Career Dashboard:**
- Participation by career
- Total cost by career
- Career-specific trends
- Exception rates by career

---

## Validation System

**Status Codes:**
- **GREEN** — Expected = Applied (no issues)
- **YELLOW** — Documented exception (Faculty Council approval)
- **RED** — Error flag (requires immediate resolution)

**Sample Data (25 students):**
- 23 cases GREEN (92%)
- 2 cases YELLOW (8%) — Faculty exceptions documented
- 0 cases RED (compliance maintained)

---

## Files in This Project

- `students-database-sample.xlsx` — Database structure with 25 sample records
- `benefits-validation-rules.md` — Logic for discount comparison
- `executive-dashboard-sample.xlsx` — BI template and formulas

---

## Monthly Reporting Process

**Week 1:**
1. Export new enrollments from each system
2. Standardize formats and clean data
3. Load into master database
4. Run validation checks

**Week 2:**
1. Resolve exceptions (RED status flags)
2. Document approvals (YELLOW status)
3. Update reference tables

**Week 3:**
1. Generate dashboards
2. Prepare executive report
3. Highlight exceptions and trends

**Week 4:**
1. Present to Finance & Student Affairs
2. Archive for compliance
3. Close month

---

## Lessons Learned

1. **Data consolidation unlocks decisions** — Single truth > 5 disconnected systems
2. **Validation at input prevents problems** — Flag exceptions early
3. **Dashboard visibility drives adoption** — People use tools when they see ROI
4. **Exception documentation ensures compliance** — Every YELLOW case has approval trail

---

## Next Steps

- [ ] Add predictive analytics (scholarship demand forecasting)
- [ ] Automate Finance notifications on budget overages
- [ ] Build renewal cycle management
- [ ] Create student-facing benefit calculator
- [ ] Implement year-over-year comparison dashboards

---

**Version:** 1.0  
**Last Updated:** September 2026  
**Maintained by:** Yoselyn Mogollón
