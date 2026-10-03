# Requirements Catalogue

> All thresholds are assumptions for a fictional client. Source column links each requirement to a business objective (BR) and a review theme (see `research/review-themes.md`).

**Priority key (MoSCoW):** Must, Should, Could

| ID | Type | Requirement | Priority | Source |
|---|---|---|---|---|
| FR-01 | Functional | The system shall let a customer submit a claim from the order screen within the claim window. | Must | BR-01, Theme 1 |
| FR-02 | Functional | The system shall offer claim reasons: missing item, wrong item, damaged item, late delivery, duplicate charge, failed payment, cancellation without notice. | Must | Themes 1, 4, 5 |
| FR-03 | Functional | The system shall require a photo for missing, wrong or damaged item claims of Rs 150 or more. | Should | Theme 1 |
| FR-04 | Functional | The system shall auto-approve claims under Rs 150 for customers with fewer than 3 claims in the last 30 days. | Must | BR-01 |
| FR-05 | Functional | The system shall automatically refund duplicate charges and payments that failed but still produced a confirmed order. | Must | BR-01, Theme 4 |
| FR-06 | Functional | The system shall route all other claims to an agent queue with order details, evidence and the customer's claim history. | Must | BR-01, BR-05 |
| FR-07 | Functional | The system shall show claim status (Submitted, Under review, Approved, Refunded, Rejected) with the last update time. | Must | BR-02, Theme 2 |
| FR-08 | Functional | The system shall refund to the original payment method by default, and shall not substitute coupons for a refund unless the customer chooses it. | Must | BR-03, Theme 2 |
| FR-09 | Functional | The system shall show a clear reason for every rejection and offer an appeal. | Must | BR-04, Theme 2 |
| FR-10 | Functional | The system shall offer a talk to an agent option after the chatbot fails to resolve the issue twice, or after a claim is rejected. | Must | BR-04, Theme 3 |
| FR-11 | Functional | The system shall notify the customer when an order is cancelled by the platform or restaurant, and shall not charge a cancellation fee for such cancellations. | Should | Theme 4 |
| FR-12 | Functional | The system shall flag customers with more than 5 claims in 30 days for fraud review, without blocking their claims. | Should | BR-05 |
| NFR-01 | Non-functional | Claim status shall update within 60 seconds of a state change. | Should | BR-02 |
| NFR-02 | Non-functional | Claim data shall be accessible only to authorized roles, and every refund decision shall be recorded in an audit log. | Must | BR-05 |
| NFR-03 | Non-functional | The claim submission screen shall load within 3 seconds on a typical mobile connection. | Could | BR-01 |
