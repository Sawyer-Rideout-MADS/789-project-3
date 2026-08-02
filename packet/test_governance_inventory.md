# TrustBank — Current Testing / Monitoring / Governance Inventory

This is what the team has in place today. Your job (memo Section 4) is to **critique
this and propose specific improvements** — name the missing controls and say exactly
what each should check and what threshold should trigger action.

## Testing
- [x] Unit tests on the preprocessing/feature code
- [x] A training smoke test (model trains + serializes without error)
- [x] Offline evaluation on a fixed holdout set before release
- [ ] Data-drift / input-distribution test  *(none)*
- [ ] Slice / fairness regression test  *(none)*
- [ ] Shadow or canary test in production before full promotion  *(ad hoc, not required)*

## Monitoring
- [x] Uptime + p95 latency dashboards, with paging on latency/errors
- [x] Request/throughput volume dashboard
- [ ] Prediction-drift (PSI) alert  *(metric is logged but nothing alerts on it)*
- [ ] Model-performance-decay alert (precision/recall)  *(none)*
- [ ] On-call ownership for **model-quality** metrics (not just infra)  *(none)*

## Governance
- [x] Models versioned in a registry (each candidate has an ID)
- [x] Reproducible training pipeline (Unit 11 CI/CD)
- [ ] Model card kept current per release  *(stale — see `model_card.md`)*
- [ ] Documented promotion policy / validation gate  *(informal, verbal)*
- [ ] Rollback runbook (who, what signal, how fast)  *(none)*
- [ ] Audit trail linking a production decision to the evidence behind it  *(none)*
