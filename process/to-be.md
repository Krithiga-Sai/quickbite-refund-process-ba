# TO-BE Process: Proposed Refund Handling

```mermaid
flowchart TD
    A([Customer opens order and taps Report issue]) --> B[Select reason and submit claim]
    B --> C{Within claim window?}
    C -->|No| X[Auto-reject with clear reason and option to talk to an agent]
    C -->|Yes| D{Duplicate charge or failed payment?}
    D -->|Yes| P[Auto-refund to original payment method]
    D -->|No| E{Under Rs 150 and fewer than 3 claims in 30 days?}
    E -->|Yes| F[Auto-approve]
    E -->|No| G[Route to agent queue with order details, photo and claim history]
    G --> H{Agent decision}
    H -->|Approve| F
    H -->|Reject| Y[Notify customer with reason and appeal option]
    F --> I[Refund to chosen destination, default original payment method]
    P --> I
    I --> J["Status updates sent: Submitted, Under review, Approved, Refunded"]
    J --> K([Customer receives refund])
    Y --> Z{Customer appeals?}
    Z -->|Yes| G
    Z -->|No| M([Claim closed])
```

## What changes and why

| AS-IS pain point | TO-BE change |
|---|---|
| P1 No route to a person | Talk to an agent option after the chatbot fails twice or a claim is rejected |
| P2 Inconsistent decisions | Rule-based auto-approval; agents see claim history |
| P3 No rejection reason | Every rejection shows a reason and an appeal option |
| P4 Coupons instead of money | Refund goes to the original payment method by default |
| P5 No status updates | Status shown and updated at every stage |
| P6 Payment errors | Duplicate charges and failed-payment orders refunded automatically |
