# User Stories

> Each story links to the requirements in `requirements-catalogue.md`. Thresholds are assumptions for a fictional client.

| ID | User story | Acceptance criteria | Requirements |
|---|---|---|---|
| US-01 | As a customer, I want to report a problem from my order screen so that I do not have to chase support. | Given a delivered or late order inside the claim window, when I tap Report issue, then I can choose a reason, attach a photo where required and submit. The screen loads within 3 seconds. | FR-01, FR-02, FR-03, NFR-03 |
| US-02 | As a customer, I want to see my claim status so that I know when to expect my money. | Given a submitted claim, when I open the order, then I see the current status and last update time, updated within 60 seconds of any change. | FR-07, NFR-01 |
| US-03 | As a customer, I want small valid claims approved instantly so that I am not left waiting. | Given a claim under Rs 150 and fewer than 3 claims in 30 days, when I submit it, then it is approved automatically. | FR-04 |
| US-04 | As a customer, I want duplicate charges and failed payments refunded automatically so that I do not have to complain. | Given I was charged twice or my payment failed but the order was confirmed, then the extra amount is refunded without a claim. | FR-05 |
| US-05 | As a customer, I want my refund in my original payment method so that I am not forced to use coupons. | Given an approved claim, then the refund goes to the original payment method unless I choose wallet or coupon. | FR-08 |
| US-06 | As a customer, I want a clear reason when my claim is rejected so that I understand and can appeal. | Given a rejected claim, then I see the reason and an appeal option. | FR-09 |
| US-07 | As a customer, I want to reach a human agent when the chatbot cannot help so that my problem gets solved. | Given the chatbot fails to resolve my issue twice, or my claim is rejected, then I see a Talk to an agent option. | FR-10 |
| US-08 | As a customer, I want to be told when my order is cancelled so that I am not charged unfairly. | Given the platform or restaurant cancels my order, then I am notified and no cancellation fee is charged. | FR-11 |
| US-09 | As a support agent, I want claims that need review queued with evidence and history so that I can decide quickly. | Given a claim that is not auto-approved, then it appears in my queue with order details, evidence and the customer's recent claim history. | FR-06 |
| US-10 | As a fraud analyst, I want customers with unusually many claims flagged so that I can review them. | Given a customer with more than 5 claims in 30 days, then they are flagged for review and their claims are still processed. | FR-12 |
| US-11 | As a finance analyst, I want every refund decision recorded so that I can reconcile payouts. | Given any refund decision, then the audit log records who or what decided, when and why, visible only to authorized roles. | NFR-02 |
