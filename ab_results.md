# Shadow A/B Results (recent, current distribution)

Both arms were scored on the **same** recent shadow set of **20,000** transactions
(**400** fraudulent, **19,600** legitimate) drawn from the *current*
traffic — i.e., after the drift you see in the monitoring series.

| Arm | Caught fraud (TP) | Wrongful declines (FP) | Missed fraud (FN) | Correct approvals (TN) | p95 latency |
|---|---|---|---|---|---|
| Champion (in prod)   | 294 | 882 | 106 | 18,718 | 186 ms |
| Challenger (candidate) | 344 | 549 | 56 | 19,051 | 260 ms |

You compute recall, precision, wrongful-decline rate, the significance test on the
recall difference, and net cost (cost assumptions are in `model_card.md`). The two arms
were scored on the **same** shadow set; for this analysis treat them as independent and
use a **two-proportion z-test** on the recall difference. The p95 SLA is **250 ms**.
Raw counts are in `ab_results.csv`.
