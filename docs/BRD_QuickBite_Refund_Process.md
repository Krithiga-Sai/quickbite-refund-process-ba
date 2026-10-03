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
