# Project 3 — The Recorded Defense (read this before you record)

Your grade for Project 3 includes a **3-minute recorded defense** of your own memo.
It is not a presentation — it's a short oral exam that shows the reasoning is yours.

## What you record
- **3 minutes**, screen-share or webcam, uploaded with your memo.
- Answer **the two questions you pick** — one from Q1–Q7 and one from Q8–Q12 — **plus Q13** (everyone answers Q13).
- **Start by saying your ONYEN and which two questions you picked**, then answer them, then Q13.

## How you choose your two questions
You **pick** one question from Q1–Q7 (monitoring/testing) and one from Q8–Q12
(governance/critique) — whichever two you can defend best from your own memo. Plus Q13,
which everyone answers. That's three questions in total: your two picks + Q13.

There's no assigned list to look up — just choose the two you're most ready to defend.

## What earns credit
Explaining the **reasoning behind a number or decision** — the trade-off, why you
rejected the alternative, what the statistic actually means. Re-reading your memo aloud
does not. Be ready to reproduce any calculation if asked in a follow-up.

---

## The question bank

**Monitoring diagnosis**
- **Q1.** Point to the exact week the model's drift crossed the action threshold. How did you know that was the moment to act — not earlier, not later?
- **Q2.** Latency stayed flat the whole time. Why does that matter for your diagnosis?
- **Q3.** If you could add only one monitor to catch this next time, which one and at what threshold?

**Testing & promotion**
- **Q4.** Walk through the significance test on the recall difference — what does the p-value actually tell you here?
- **Q5.** The challenger is cheaper but slower (higher p95 latency). How did you weigh that against the SLA?
- **Q6.** If the recall difference had *not* been significant, would your recommendation change? Why?
- **Q7.** Precision is low for both models. Why — and does that change how you read the A/B?

**Governance artifacts**
- **Q8.** Pick one adverse-action reason you wrote and explain how you'd defend it to a regulator.
- **Q9.** Who did you name as the model owner, and what exactly are they accountable for?
- **Q10.** What goes in the audit-trail entry for this promotion, and why does it matter six months from now?

**Critique & improve**
- **Q11.** Of the controls you proposed, which one would have prevented this incident, and how?
- **Q12.** Defend the threshold you set for your drift alert — why not stricter or looser?

**Always asked**
- **Q13.** You recommended promote / hold / roll back. Give the single strongest argument *against* your own decision — and why you still hold it.
