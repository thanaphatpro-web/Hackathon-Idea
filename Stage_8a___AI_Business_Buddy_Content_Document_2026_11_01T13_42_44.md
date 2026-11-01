
# AI Business Buddy — Content Document
## AI for All Thailand Innovation Sprint

---

## 1. Initiative Overview

| Field | Detail |
|-------|--------|
| **Initiative Name** | AI Business Buddy |
| **Pillar** | 🏪 SME & Local Economy |
| **Phase** | Ideation (AI-DLC v2) |
| **Status** | ✅ Approved — Ready for Inception Phase |

AI Business Buddy is an AI-powered mobile application designed to help Thai micro-entrepreneurs automate back-office bookkeeping by scanning payment slips and order receipts, and transforming raw transaction data into actionable business insights — all with zero accounting knowledge required. [source: participant + web research]

---

## 2. Problem Statement

Micro-entrepreneurs in Thailand — including street food vendors, small retailers, service providers, and freelancers — frequently operate solo or with minimal staff. They are overwhelmed by front-of-house duties such as serving customers, marketing, and managing orders, leaving virtually no time for critical back-office tasks. [source: participant]

**Key pain points:**
- No time to record daily income and expenses [source: participant]
- No ability to create financial summaries or track profitability [source: participant]
- No data-driven insights to guide business decisions [source: participant]
- Manual bookkeeping (pen-and-paper or spreadsheets) is time-consuming and error-prone [source: participant]

---

## 3. Proposed Solution

An AI-powered mobile application that automates the entire back-office data pipeline for micro-entrepreneurs: [source: participant]

### Phase Roadmap

| Priority | Feature | Description |
|----------|---------|-------------|
| **P0 — MVP** | 🤖 AI Slip Scanning + Auto Record | Photograph slip/order → AI extracts data via OCR → auto-save to database |
| **P1 — Phase 2** | 📊 Dashboard & Daily Summary | Display income/expense, daily/weekly/monthly profit as visual dashboard |
| **P2 — Phase 3** | 💡 AI Business Recommendations | Analyze accumulated data → provide actionable suggestions (best-selling items, peak hours, cost reduction) |

[source: participant]

---

## 4. Target Users

| Role | Who | Relevance |
|------|-----|-----------|
| **Primary User** | All micro-entrepreneurs (food vendors, retailers, service providers, freelancers) | Direct users — capture slips, view data, receive recommendations |
| **Secondary Stakeholder** | Accountants / Business Consultants | Use system data for advisory, auditing, and business planning |

[source: participant]

---

## 5. Unique Value Proposition

> "AI Business Buddy" — an all-in-one AI assistant for Thai micro-entrepreneurs that automates back-office bookkeeping and delivers actionable business insights, requiring zero accounting knowledge.

[source: web research + participant]

**What makes it unique:**
- Combines Thai-language OCR + simple dashboard + AI business recommendations in one app [source: web research]
- Designed for vendors and freelancers, not accountants [source: participant]
- Minimal learning curve — snap a photo and you're done [source: participant]

---

## 6. Competitive Landscape

### Thailand Market
| Solution | Strengths | Gaps vs. Our Idea |
|----------|-----------|-------------------|
| FlowAccount | Cloud accounting for Thai SMEs, invoicing, VAT/WHT support, AI Connector | Designed for accountants, too complex for solo micro-entrepreneurs |

### International Market
| Solution | Strengths | Gaps vs. Our Idea |
|----------|-----------|-------------------|
| ReceiptsAI | AI categorization, receipt scanning, affordable pricing | No Thai language support, no business analytics dashboard |
| QuickBooks Receipt Scanner | OCR extracts amount/date/location, integrated accounting | Targets Western markets, not fit for Thai micro-businesses |
| SparkReceipt | Extracts merchant, amount, date, category in seconds | Western freelancer focus, no business recommendations |
| ArthPro | AI receipt scanner + expense tracker for freelancers | No dashboard or AI-powered business recommendations |
| Tofu | Reads Thai handwriting, auto-posts to Xero | Requires Xero (enterprise-level software) |

[source: web research]

### Gap Analysis
No existing solution combines all three capabilities for Thai micro-entrepreneurs:
1. ✅ AI slip/order reading with Thai language support [source: web research]
2. ✅ Simple, intuitive dashboard designed for vendors, not accountants [source: web research]
3. ✅ AI-powered actionable business recommendations [source: web research]

---

## 7. Build vs. Buy Decision

**Hybrid Approach** — Build custom app + leverage external APIs [source: participant]

| Build (Custom) | Buy (External API) |
|----------------|-------------------|
| Core app UI/UX | OCR / Document extraction API |
| Database & data layer | LLM API for recommendations |
| Dashboard & visualizations | Cloud infrastructure |
| Business logic | Payment gateway (future) |

---

## 8. Technical Feasibility

### Tech Stack
| Component | Approach | Feasibility |
|-----------|----------|-------------|
| OCR / Slip Reading | External API (Google Cloud Vision / AWS Textract / GPT-4 Vision) | 🟢 High |
| Database | Cloud DB (PostgreSQL / Firebase / Supabase) | 🟢 High |
| Dashboard | Frontend framework (React/Next.js) + charting library | 🟢 High |
| AI Recommendations | LLM API (GPT/Claude) for data analysis and suggestions | 🟡 Medium |
| Mobile Access | PWA or LINE LIFF (accessible via LINE) | 🟢 High |

[source: participant + web research]

### Overall Verdict
🟢 **Feasible with Hybrid approach** — Core technical components are achievable by the team using external APIs. [source: participant + web research]

---

## 9. RAID Log

| Type | Item | Severity / Status |
|------|------|-------------------|
| Risk | OCR accuracy on crumpled/blurry/handwritten slips | 🟡 Medium |
| Risk | Low digital literacy among some micro-entrepreneurs | 🟡 Medium |
| Risk | API call costs may scale with user growth | 🟡 Medium |
| Assumption | Most micro-entrepreneurs own a smartphone | ✅ Confirmed |
| Assumption | Slips contain structured data AI can extract | ✅ Confirmed |
| Assumption | Micro-entrepreneurs willing to adopt digital tools | ✅ Confirmed |
| Assumption | Most users use LINE as primary channel | ✅ Confirmed |
| Dependency | External OCR API (Google/AWS/OpenAI) | Required |
| Dependency | Cloud hosting (Vercel/AWS/GCP) | Required |

[source: participant + assumption]

---

## 10. MVP Scope

### Success Criteria
| Criterion | Target |
|-----------|--------|
| OCR Accuracy | ≥ 85% on standard slips (with user edit-before-save) |
| Time Saved | Record slip data in < 30 seconds (vs. 3-5 min manual) |
| User Adoption | ≥ 5 testers can use successfully without training |

[source: participant]

### MVP Backlog (P0)
1. **Photo Capture / Upload Screen** — camera or gallery selection [source: participant]
2. **AI OCR Processing** — send image to OCR API → extract amount, items, date, merchant [source: participant]
3. **Review / Edit Screen** — display AI-extracted data for user verification before saving [source: participant]
4. **Save to Database** — store all transaction data [source: participant]
5. **Transaction History Screen** — view past income/expense records [source: participant]

### Out of Scope (MVP)
- Dashboard visualizations (Phase 2) [source: participant]
- AI business recommendations (Phase 3) [source: participant]
- Multi-user / team features [source: participant]
- Tax report generation [source: participant]
- Integration with external accounting software [source: participant]

---

## 11. User Flow & Wireframes

### User Flow
```
🏠 Home → 📸 Capture Slip → 🤖 AI Processing → ✏️ Review/Edit → 💾 Save → 📋 Transaction History
```

### Screen Descriptions
| Screen | Purpose | Key Elements |
|--------|---------|-------------|
| 🏠 Home | Landing page, quick access to scan | Primary CTA "สแกนสลิป", recent transactions list |
| 📸 Capture Slip | Take photo or select from gallery | Camera viewfinder, two action buttons |
| 🤖 AI Processing | Loading state while AI extracts data | Progress indicator, slip preview |
| ✏️ Review / Edit | Verify and correct AI-extracted data | Editable fields (type, date, merchant, items, total), Save/Cancel |
| 📋 Transaction History | Browse past records | Search bar, date filter, color-coded income/expense list |

[source: participant]

---

## 12. Team

| Member | Role |
|--------|------|
| S | Full-stack Developer |
| A | UX/UI Designer |
| B | Project Manager |
| C | AI Prompt Engineer |
| D | Business Domain Expert |

[source: participant]

### RACI Matrix
| Task | S (Dev) | A (UX/UI) | B (PM) | C (AI/Prompt) | D (Domain) |
|------|:---:|:---:|:---:|:---:|:---:|
| Project Planning & Timeline | C | I | R/A | I | C |
| UI/UX Design | C | R/A | I | I | C |
| Frontend Development | R/A | C | I | I | I |
| Backend + Database | R/A | I | I | C | I |
| OCR API Integration | R/A | I | C | R | I |
| AI Prompt Design & Tuning | C | I | I | R/A | C |
| AI Business Recommendations | C | I | I | R/A | R |
| Dashboard & Data Viz | R/A | R | I | C | C |
| Business Validation | I | C | C | I | R/A |
| Testing & QA | R | R | A | R | R |
| User Testing Coordination | C | R | R/A | I | R |
| Stakeholder Communication | I | I | R/A | I | C |

[source: participant]

---

## 13. Approval

### Product Lead Reviewer Pass
| Criterion | Status |
|-----------|--------|
| Completeness | ✅ Pass — All stages (0-7) completed with Carry-Forward Blocks |
| Consistency | ✅ Pass — Data consistent across all stages |
| Traceability | ✅ Pass — All claims carry [source: ...] tags |
| Feasibility Alignment | ✅ Pass — Scope aligned with team of 5 + Hybrid approach |

**All Assumptions (4/4):** ✅ Confirmed

**Status:** ✅ **APPROVED** — Ready for Inception Phase

[source: participant]
