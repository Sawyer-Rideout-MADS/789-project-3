> DELIVERY NOTE (not part of the packet): this is the packet's `REPORT_TEMPLATE.md`,
> delivered to the output root because the `project3/packet/` subfolder wasn't syncing.
> When you assemble the packet for Canvas, rename this file to `REPORT_TEMPLATE.md` and
> place it in the packet folder. (Delete this note line before handing it to students.)

# Project 3 — Model Governance Review (Memo)

**Name / ONYEN:**
**Service:** TrustBank fraud detection (Project 2 & Homework 4)

> Cite specific figures from the packet throughout, and **show your work** — the
> numbers you computed, not just conclusions. You will defend every section on camera.

## 1. Monitoring Diagnosis (is the model healthy?)
- Read the 12-week monitoring series. Is the production model healthy today?
- **When** did it start to go wrong, and what is the evidence (drift, precision/recall decay, alert rate)?
- Name **two** signals and their weeks: (a) the earliest signal that *should* have triggered a
  review, and (b) the week TrustBank's **configured** PSI ≥ 0.20 alert actually crosses. They
  are not the same week — explain the gap.

## 2. Testing & Promotion Decision (A/B)
- Recall, precision, and wrongful-decline rate for **each** arm on the shadow set (show your work).
- The significance test on the recall difference: p-value and 95% CI. Is it significant?
- Net cost per arm using the given cost assumptions. Which is cheaper — and by how much?
- The latency trade-off vs. the SLA.
- **Your decision:** promote the challenger / hold / roll back — and the reasoning that ties
  the monitoring diagnosis, the statistics, the cost, and the latency together.

## 3. Governance Artifacts (make the decision accountable)
- Complete the **model card**: owner, limitations, known drift, fairness considerations,
  monitoring plan, promotion policy, rollback plan.
- Write plain-language **adverse-action reasons** for **5** of the 10 declined transactions,
  grounded in each transaction's top feature drivers.
- Describe the **audit-trail** entry you would record for this promotion decision.

## 4. Critique & Propose Improvements (Unit 12 LO3)
- Critique TrustBank's current testing/monitoring/governance (see the inventory).
- Propose the specific missing controls. For each, state **what it checks** and **what
  threshold triggers action** (e.g., "alert when PSI ≥ 0.20 for 2 consecutive weeks").

## 5. (Bonus) Fairness slice (Unit 13) and/or Azure ML register-version + a FinOps cost read.
