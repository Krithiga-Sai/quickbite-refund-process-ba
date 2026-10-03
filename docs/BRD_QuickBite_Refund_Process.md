# Business Requirements Document: QuickBite Refund Process

| | |
|---|---|
| Version | 0.1 (Draft) |
| Author | Krithiga Sai P |
| Client | QuickBite (fictional) |
| Date | 3 October 2026 |

## 1. Executive Summary
QuickBite customers cannot get refunds quickly or reliably, and often cannot reach anyone who can help. This document defines requirements for a faster, more transparent, rule-based refund process.

## 2. Problem Statement
Based on 20 complaint points from public reviews of two food delivery apps (see `research/review-themes.md`):
- Customers who receive missing, wrong or damaged items often get no refund, or only coupons instead of money.
- Customers struggle to reach support, and chatbots often do not understand the problem.
- Payment failures, double charges and cancellations without notice create refund situations with no clear status or resolution.
- Late deliveries are a frequent reason customers raise claims.

## 3. Objectives
- BR-01: Reduce resolution time for eligible low-value claims (assumed target: under 24 hours).
- BR-02: Give customers visible refund status at every stage.
- BR-03: Let customers choose cash refund to the original payment method instead of being limited to coupons.
- BR-04: Give customers a clear path to a human agent for unresolved claims.
- BR-05: Flag repeat or suspicious claims for review.

## 4. Scope
**In scope:** Refund claims for missing, wrong, damaged or late orders, and for payment or cancellation errors, from submission to money returned.

**Out of scope:** Login issues, delivery fees and taxes, restaurant payouts, delivery partner payments, app redesign.

## 5. Assumptions
QuickBite is a fictional client. All thresholds, time limits and targets in this document are assumptions, to be validated with a real client.

## 6. Stakeholders

| Stakeholder | What they need |
|---|---|
| Customer | Fast, fair refund; visible status; a way to reach a person |
| Support agent | Clear rules; claim details and evidence in one place |
| Restaurant partner | Fair handling of disputed claims |
| Delivery partner | Not being penalized for issues outside their control |
| Finance team | Accurate reconciliation; low refund leakage |
| Fraud and risk team | Ability to detect repeat abuse |
| Product manager | Higher customer satisfaction; lower cost per ticket |


## 7. Process Overview
The current process is modelled in `process/as-is.md` (6 pain points identified) and the proposed process in `process/to-be.md`.

## 8. Requirements
15 requirements (12 functional, 3 non-functional) are listed with priorities and sources in `requirements/requirements-catalogue.md`.

## 9. Business Rules and Edge Cases
8 business rules and 7 edge cases are documented in `docs/business-rules.md`.


## 10. Assumptions, Constraints and Risks

| ID | Type | Description | Mitigation |
|---|---|---|---|
| R-01 | Risk | Auto-approval may increase fraudulent claims | Value cap of Rs 150, claim-frequency limit, fraud flag (FR-12) |
| R-02 | Risk | Agents may override automated decisions inconsistently | Override reason must be recorded (RULE-08), audit log (NFR-02) |
| R-03 | Constraint | Payment gateway refund timelines are outside QuickBite's control | Show status updates and expected timelines (FR-07) |
| R-04 | Assumption | Photo evidence is a reliable signal for item-related claims | Review sample of auto-approved claims periodically |
| R-05 | Assumption | All thresholds and targets are estimates | Validate with the client before build |

## 11. Success Metrics (KPIs)

No baseline data exists for this fictional client, so targets are illustrative.

| KPI | Definition | Illustrative target |
|---|---|---|
| Average refund time | Time from claim submission to money returned, for eligible low-value claims | Under 24 hours |
| Auto-approval rate | Share of claims approved without agent review | To be set after a pilot |
| Refund tickets per 1,000 orders | Support tickets about refund status or rejection | Decrease versus baseline |
| Coupon-in-place-of-refund rate | Share of refunds issued as coupons the customer did not choose | Zero |
| Post-refund satisfaction | Customer rating after a refund is completed | Increase versus baseline |

## 12. Appendices
- User stories: `requirements/user-stories.md` (11 stories)
- Traceability matrix: `requirements/traceability-matrix.csv`
- Review research: `research/review-themes.md`
- Stakeholder notes: `docs/stakeholders.md` (stakeholder table is in section 6 above)
