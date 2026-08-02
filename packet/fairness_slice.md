# Fairness Slice — Candidate Wrongful Declines by Region  *(BONUS — Unit 13)*

This is a **bonus** artifact tied to Unit 13 (fairness). It is not required to pass the
project. Wrongful-decline rate = legit transactions the **challenger** declined, per
region. `region` is an audit attribute only; it is not a model input.

| Region | Legit transactions | Wrongful declines | Wrongful-decline rate |
|---|---|---|---|
| North | 4,900 | 106 | 2.16% |
| South | 4,900 | 106 | 2.16% |
| East | 4,900 | 106 | 2.16% |
| West | 4,900 | 231 | 4.71% |

For the bonus: identify which region is worst off and by how much, name one mitigation,
and give the expected before/after effect. Raw counts are in `fairness_slice.csv`.
