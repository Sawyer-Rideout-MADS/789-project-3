# Production Incident

For roughly six weeks, the model quietly drifted: input drift (PSI) climbed from
**0.04** to **0.28**, wrongful declines rose from
**2.6%** to **4.5%**
of transactions, and precision fell from **38.7%** to
**25.0%**. **No alert fired** — the PSI value was logged but
nothing was watching it, and there is no performance-decay alert. The first anyone
heard of it was the customer-support queue filling with complaints about declined
legitimate purchases.

Leadership wants a written response: **what happened**, **what to do right now**, and
**what control would have caught this automatically before customers felt it.**
