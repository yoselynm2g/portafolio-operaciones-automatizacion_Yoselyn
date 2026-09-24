# PROJECT 1: Lead Automation & Classification System

**Status:** ✅ Production  
**Technology Stack:** Google Forms | Google Sheets | n8n  
**Impact:** $45,000 USD operational value  

---

## Overview

Automated lead capture, classification, and centralization system that eliminates manual data entry and reduces lead response time from 48 hours to minutes.

### The Challenge
- 15+ hours/week wasted on manual lead processing across spreadsheets
- No standardized capture process (emails, messages, forms mixed)
- 48-hour delay before engineering team assignment
- 5-8% data loss rate from manual transcription errors

### The Solution
- Unified Google Form for standardized lead capture
- Centralized Google Sheets database with auto-population
- n8n workflow for real-time lead classification and routing
- Automatic priority ranking by region and equipment type

---

## Key Metrics

| Metric | Before | After | Impact |
|--------|--------|-------|--------|
| **Processing Time/Lead** | 15 min | 2-3 min | 70% reduction |
| **Weekly Hours Saved** | 0 | 14-18 hrs | **$12,000/year** |
| **Data Loss Rate** | 5-8% | 0% | 100% accuracy |
| **Engineering Assignment** | 48h | Minutes | **$20,000/year** |
| **Classification Accuracy** | 85% | 99% | 14% improvement |

**Total Annual Value: ~$45,000 USD**

---

## Technical Architecture

```
Google Form (Lead Capture)
    ↓
Google Sheets (Raw Data)
    ↓
n8n Workflow (Classification Logic)
    ├─ Extract data from Sheets
    ├─ Apply classification rules
    ├─ Rank by priority
    └─ Route to assignment queue
    ↓
Master Database (Centralized)
    ↓
Notifications (Email/Slack to Team)
```

---

## Files in This Project

- `google-form-schema.json` — Form structure and fields
- `master-sheet-template.csv` — Database template with validation rules
- `n8n-workflow.json` — Complete workflow export
- `classification-rules.md` — Business logic for prioritization

---

## Quick Start

1. **Create Google Form** with fields:
   - Customer Name (required)
   - Project Location (required)
   - Equipment Needed (checkboxes)
   - Budget (number)
   - Autonomy Hours (number)

2. **Connect to Google Sheets:**
   - Form → More → Select Response Destination
   - Create new sheet named "Master Leads Database"
   - Enable auto-population

3. **Import n8n Workflow:**
   - Log into n8n
   - Import `n8n-workflow.json`
   - Configure Google Sheets API connection
   - Set trigger frequency (recommend: every 15 minutes)
   - Add email/Slack notifications
   - Test with sample data

4. **Monitor & Optimize:**
   - Check workflow logs daily
   - Monitor classification accuracy
   - Adjust rules as needed
   - Report weekly metrics

---

## Daily Operations

**Workflow Execution:**
- Trigger: Every 15 minutes
- Average execution time: 180 seconds per batch
- System uptime: 99.8%

**Lead Processing Flow:**
1. New form response arrives
2. Data auto-populated to Google Sheets
3. n8n workflow detects new entry
4. Classification rules applied
5. Lead assigned to team queue
6. Notification sent (Email/Slack)
7. Team member reviews and acts

---

## Sample Output

```json
{
  "lead_id": "LEAD001",
  "customer_name": "Solar Solutions Inc",
  "project_location": "Caracas, Venezuela",
  "equipment_needed": ["Solar Panels", "Inverter", "Battery System"],
  "autonomy_hours": 24,
  "region_classification": "North Venezuela - High Priority",
  "equipment_category": "Complete Solar Hybrid System",
  "priority_rank": 1,
  "estimated_project_value": "$85,000 USD",
  "status": "Assigned to Engineering Team",
  "processing_time": "3 minutes"
}
```

---

## Lessons Learned

1. **Form standardization is critical** — Every field reduces downstream processing
2. **Real-time notifications prevent bottlenecks** — Team urgency increases when alerted immediately
3. **Priority ranking > quantity** — Teams focus better with ranked lists
4. **Data validation at capture saves hours** — Required fields eliminate back-and-forth

---

## Next Steps

- [ ] Expand classification to other business functions
- [ ] Add AI lead scoring (revenue potential)
- [ ] Integrate with CRM for automatic follow-up
- [ ] Create customer-facing portal for status tracking
- [ ] Build analytics dashboard for sales funnel

---

**Version:** 1.0  
**Last Updated:** September 2026  
**Maintained by:** Yoselyn Mogollón