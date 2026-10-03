# Business Rules and Edge Cases

> All values are assumptions for a fictional client, to be validated with a real client.

## Business rules

| ID | Rule |
|---|---|
| RULE-01 | A claim must be raised within 24 hours of delivery (or of the scheduled delivery time for orders never delivered). |
| RULE-02 | A claim is auto-approved when its value is under Rs 150 and the customer has fewer than 3 claims in the last 30 days. |
| RULE-03 | A photo is required for missing, wrong or damaged item claims of Rs 150 or more. |
| RULE-04 | The refund amount is limited to the value of the affected items, plus their proportional taxes. |
| RULE-05 | A late delivery claim is eligible when delivery is more than 60 minutes beyond the promised time; the delivery fee is refunded. |
| RULE-06 | The default refund destination is the original payment method. A wallet or coupon is used only if the customer selects it. |
| RULE-07 | Customers with more than 5 claims in 30 days are flagged for fraud review. Their claims are still processed by an agent. |
| RULE-08 | An agent may override an automated decision, and the reason must be recorded. |

## Edge cases

| Scenario | Expected handling |
|---|---|
| Part of the order is missing | Refund only the missing items (RULE-04) |
| Customer submits the same claim twice | Second claim is linked to the first and not processed separately |
| Refund to the original method fails | Retry once, then offer wallet credit or manual agent processing, with customer notified |
| Restaurant disputes the claim | Claim goes to the agent queue; customer is not blocked while it is reviewed |
| Order marked delivered but customer says it never arrived | Route to agent review with delivery details |
| Claim raised after the window | Auto-reject with reason and talk to an agent option (FR-09, FR-10) |
| Customer paid twice | Refund the duplicate automatically (FR-05) |
