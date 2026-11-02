---
tags:
  - health
aliases:
  - Ivermectin
  - Ivermectin mortality meta-analysis
  - Elgazzar
up: "[[Nutrition & Health MOC]]"
---
> [!summary] Bottom line
> Early meta-analyses suggested ivermectin cut COVID-19 deaths by more than half, but that result depended on one potentially fraudulent trial (Elgazzar) and on trials at high risk of bias. Removing them, and adding the larger trials that came later, shrinks the effect toward no benefit and makes it no longer statistically significant.

## Mortality meta-analysis

These forest plots pool deaths in randomized trials of ivermectin versus control (risk ratios, random effects), split into mild-to-moderate and severe COVID-19, and check how the result changes as questionable trials are removed. Trials shown with 0% weight are left out of that analysis.

| Analysis | Risk ratio (95% CI) | Deaths (ivermectin vs control) | I² |
|---|---|---|---|
| 1. Initial | 0.38 (0.19–0.76) | 30 vs 89 | 55% |
| 2. Without Elgazzar | 0.51 (0.27–0.99) | 28 vs 65 | 42% |
| 3. Without high risk of bias trials | 0.29 (0.10–0.82) | 19 vs 68 | 64% |
| 4. Without high risk of bias trials or Elgazzar | 0.42 (0.14–1.27) | 17 vs 44 | 56% |
| 5. All RCTs, without Elgazzar | 0.68 (0.45–1.03) | 54 vs 94 | 22% |
| 6. All RCTs, without high risk of bias trials or Elgazzar | 0.63 (0.33–1.17) | 39 vs 69 | 43% |

- **Elgazzar drives the effect.** Its severe-disease arm (2 vs 20 deaths, RR 0.10) was the most extreme result. Removing it weakened the pooled estimate in every comparison: from 0.38 to 0.51, and from 0.29 to 0.42 once high risk of bias trials were also out, at which point the result was no longer significant.
- **Larger trials pull toward no effect.** Adding the later trials, including the large TOGETHER trial (18 vs 22 deaths, RR 0.82), moved the mild-to-moderate subgroup from 0.26 to 0.78 and the overall estimate to 0.68, with a confidence interval crossing 1.
- **The best evidence shows no clear benefit.** With all trials included except Elgazzar and the high risk of bias ones (Abd-Elsalam, Gonzalez, Hashim, Okumus and Shahbaznejad), the risk ratio was 0.63 (0.33–1.17), not statistically significant.
- **Severe disease stays inconsistent.** Within the severe subgroup, results ranged from Niaee (RR 0.18) to Fonseca (RR 1.06), and heterogeneity stayed high (I² 87% when only those two remained).

### Initial results
![[Ivermectin mortality meta 1 initial.png]]

### Without Elgazzar
![[Ivermectin mortality meta 2 without Elgazzar.png]]

### Without high risk of bias trials
![[Ivermectin mortality meta 3 without high risk of bias.png]]

### Without high risk of bias trials or Elgazzar
![[Ivermectin mortality meta 4 without high risk of bias or Elgazzar.png]]

### All RCTs, without Elgazzar
![[Ivermectin mortality meta 5 all RCTs without Elgazzar.png]]

### All RCTs, without high risk of bias trials or Elgazzar
![[Ivermectin mortality meta 6 all RCTs without high risk of bias or Elgazzar.png]]

## Published analyses

A subgroup meta-analysis stratified by Cochrane risk of bias found the same pattern: the survival benefit of ivermectin depended largely on poor-quality studies. The potentially fraudulent trial suggested about 12 times more benefit (RR 0.08, 95% CI 0.02–0.35) than the low risk of bias trials, which showed none (RR 0.96, 0.56–1.66).
[Hill 2022](https://pubmed.ncbi.nlm.nih.gov/35071686/)

The ivermectin trials are a warning that meta-analyses built only on published summary data are unreliable, because problems like fabricated data can only be found with patient-level data.
[Lawrence 2021](https://pubmed.ncbi.nlm.nih.gov/34552263/)

In the final TOGETHER trial (1,358 high-risk outpatients in Brazil, double-blind and placebo-controlled), 3 days of ivermectin didn't reduce hospitalization or prolonged emergency observation: 14.7% versus 16.3% with placebo (relative risk 0.90, 95% credible interval 0.70–1.16). There were no significant effects on secondary outcomes or adverse events.
[Reis 2022](https://pubmed.ncbi.nlm.nih.gov/35353979/)

See [[Underpowered studies in meta-analysis]] for why excluding weak studies can give a better estimate, and [[Research methods resources]] for meta-analysis guides.
