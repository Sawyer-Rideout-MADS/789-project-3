# Production Monitoring — Champion Model (12 weeks)

These are the weekly production metrics for the model **currently in production**.
`psi_feature_drift` is the Population Stability Index on the model's input features
(a standard drift measure). TrustBank's data-science runbook says **investigate any
week with PSI ≥ 0.20**. `p95_latency_ms` is served against a **250 ms**
p95 SLA.

| Week | Txns | Recall | Wrongful-decline rate | Precision | Alert rate | PSI (drift) | p95 latency (ms) |
|---|---|---|---|---|---|---|---|
| 1 | 41,250 | 80.3% | 2.6% | 38.7% | 4.2% | 0.04 | 178 |
| 2 | 40,980 | 79.9% | 2.7% | 37.7% | 4.2% | 0.05 | 181 |
| 3 | 42,100 | 80.7% | 2.5% | 39.7% | 4.1% | 0.06 | 176 |
| 4 | 41,770 | 80.1% | 2.6% | 38.6% | 4.1% | 0.05 | 180 |
| 5 | 43,010 | 79.8% | 2.7% | 37.6% | 4.2% | 0.07 | 182 |
| 6 | 42,640 | 80.4% | 2.6% | 38.7% | 4.2% | 0.08 | 179 |
| 7 | 44,890 | 79.2% | 3.0% | 35.0% | 4.5% | 0.12 | 181 |
| 8 | 45,320 | 77.8% | 3.4% | 31.8% | 4.9% | 0.17 | 184 |
| 9 | 46,010 | 76.1% | 3.8% | 29.0% | 5.2% | 0.21 | 183 |
| 10 | 46,550 | 74.9% | 4.1% | 27.2% | 5.5% | 0.24 | 185 |
| 11 | 47,120 | 74.1% | 4.3% | 26.0% | 5.7% | 0.26 | 187 |
| 12 | 47,600 | 73.5% | 4.5% | 25.0% | 5.9% | 0.28 | 186 |

Read this series closely: is the model healthy? If not, **when** did it start to go
wrong, and what is the evidence? Two different signals matter here and they do **not**
cross in the same week — name **both**: (a) the earliest signal that *should* have
triggered a review, and (b) the week TrustBank's **configured** PSI ≥ 0.20 alert would
actually fire. Raw numbers are in `monitoring_metrics.csv`.
