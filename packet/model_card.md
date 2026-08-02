# Model Card — TrustBank Fraud Service  *(PARTIAL — complete the blanks)*

> This card is **stale and incomplete**. Part of your job is to critique it and fill
> in what governance requires. Blanks marked `[FILL]` are yours to complete in the memo.

- **Model name:** trustbank-fraud
- **Version under review:** challenger (candidate retrain)
- **Owner / accountable person:** `[FILL]`
- **Last reviewed:** `[FILL — this card has not been updated since first release]`
- **Intended use:** score card-not-present transactions for fraud risk; decline above threshold.
- **Inputs:** transaction + account features (amount vs. usual, velocity, distance, merchant risk, device, time).
- **Protected/audit attribute:** a `region` label (North/South/East/West) is available for
  **auditing only** — it is **not** a model input.
- **Cost assumptions (given):** missed fraud (FN) = **$500** each;
  wrongful decline (FP) = **$25** each.
- **Known limitations:** `[FILL]`
- **Known drift / data dependencies:** `[FILL — see monitoring_metrics]`
  *(Note: the 12-week monitoring series is the **in-production (champion)** model's data.
  The challenger under review inherits the same upstream inputs — document that drift here.)*
- **Fairness considerations:** `[FILL]`
- **Monitoring & alerting plan:** `[FILL]`
- **Promotion policy (validation gate):** `[FILL]`
- **Rollback plan:** `[FILL]`
