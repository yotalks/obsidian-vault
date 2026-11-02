---
tags:
  - research-methods
aliases:
  - Odds ratio
  - Risk ratio
  - Relative risk
  - Risk difference
up: "[[Research Methods MOC]]"
---
> [!summary] Bottom line
> A risk ratio compares probabilities, an odds ratio compares odds, and a risk difference subtracts the probabilities. When the outcome is rare (under about 10% in the reference group), the odds ratio is close to the risk ratio. When it's common, the odds ratio exaggerates the effect, so it shouldn't be read as a risk ratio. Odds ratios are everywhere because logistic regression produces them and case-control studies can't produce anything else.

## Three ways to compare risk

- **Risk difference** = P(disease | exposed) − P(disease | unexposed). It shows the absolute change but hides the relative one: going from 1% to 2% risk and from 50% to 51% are both a risk difference of 0.01, though the first doubles the risk.
- **[[Glossary#RR|Risk ratio]]** (relative risk) = P(disease | exposed) / P(disease | unexposed). For example, if 0.27% of smokers and 0.015% of non-smokers over 35 die of cancer, the risk ratio is 17.4 while the risk difference is only 0.25 percentage points. The two numbers carry different information and both are useful.
- **[[Glossary#OR|Odds ratio]]** = odds(disease | exposed) / odds(disease | unexposed), where odds = P / (1 − P).

No association means a risk difference of 0 and a risk ratio or odds ratio of 1.

## Risk versus odds

Risk is the probability of an event; odds are the probability it happens divided by the probability it doesn't. A risk of 1 in 5 (20%) is odds of 1 to 4 (0.25). Small risks and odds are almost the same (1/1000 vs 1/999), but large ones diverge (90% risk is odds of 9 to 1).
[Sainani 2011](https://pubmed.ncbi.nlm.nih.gov/21402371/)

If 50% of heavy drinkers and 25% of non-drinkers have hypertension, the risk ratio is 2.0 but the odds ratio is 3.0 (1/1 ÷ 1/3). Reading the odds ratio as a risk ratio would turn "twice the risk" into "three times the risk".

## Why odds ratios are used

- **Logistic regression** models the log odds of a binary outcome, so adjusted results come out as odds ratios. Odds can range from 0 to infinity while risks are stuck between 0 and 1, which makes odds easier to model.
- **Case-control studies** pick people by disease status, so the risk of disease can't be estimated, but the odds ratio still can. Thanks to Bayes' theorem, the odds ratio of exposure among cases versus controls equals the odds ratio of disease among exposed versus unexposed → [[Observational study designs]].

For example, in a case-control study of 58 women who'd had a heart attack and 58 matched controls, 23 cases and 11 controls had used oral contraceptives. The odds ratio is (23 × 47) / (11 × 35) = 2.8: the odds of heart attack were 2.8 times higher in women who'd used the pill. The risk ratio can't be calculated because the study fixed how many heart attacks there were.

## When odds ratios mislead

When an outcome is common, odds ratios greatly exaggerate the effect. In one cross-sectional study, insomniacs sleeping under 5 hours had an odds ratio for hypertension of 5.12, reported as a "500% higher risk". But about 25% of the reference group had hypertension, so a risk 5 times higher would be 125%, which is impossible. Converted, the risk ratio is about 2.5. In another, heavy smokers had an odds ratio of 3.92 for prominent wrinkles, but 45% of non-smokers had them, so the risk ratio was only about 1.7.
[Sainani 2011](https://pubmed.ncbi.nlm.nih.gov/21402371/)

Ways to catch this:
- **Check the ceiling:** a risk ratio can't exceed 100% divided by the risk in the reference group. With a 50% baseline risk it can't go above 2, so an odds ratio above that ceiling overstates the effect.
- **Look at absolute risks:** the risk in each group shows both the relative and absolute effect.
- **Convert it:** RR ≈ OR / [(1 − p) + (p × OR)], where p is the risk in the reference group. This gives a rough estimate of the adjusted risk ratio.

[Zhang 1998](https://pubmed.ncbi.nlm.nih.gov/9832001/)
