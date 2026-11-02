---
tags:
  - research-methods
aliases:
  - ANCOVA
  - Analysis of covariance
  - Change from baseline
  - Change scores
  - Baseline adjustment
up: "[[Research Methods MOC]]"
---
> [!summary] Bottom line
> A trial with baseline and follow-up measurements can be analyzed three ways: comparing follow-up scores, comparing change from baseline, or ANCOVA (regressing follow-up on baseline plus treatment group). ANCOVA gives the most precise estimate at every baseline–outcome correlation. Change scores only beat follow-up scores when the correlation is above 0.5, and they don't fix baseline imbalances because of regression to the mean.

## Three ways to analyze

In a trial that measures an outcome (like pain or blood pressure) before and after treatment:
- **Follow-up scores:** compare the groups' outcomes at the end ("pain was 15 mm lower on treatment").
- **Change scores:** compare each group's change from baseline ("pain fell 20 mm more on treatment").
- **ANCOVA (analysis of covariance):** despite the name, a regression: follow-up score = constant + a × baseline score + b × group. The coefficient b is the treatment effect, adjusted for each person's baseline.

If the groups have the same average baseline, the two simple approaches estimate the same treatment effect, but with different precision.
[Vickers 2001](https://pubmed.ncbi.nlm.nih.gov/11701584/)

## Precision depends on the baseline–outcome correlation

![[Change score vs ANCOVA variance.png]]

Taking the variance of a single measurement as 1, and ρ as the correlation between baseline and follow-up:
- **Follow-up scores:** variance stays at 1 whatever the correlation.
- **Change scores:** variance is 2(1 − ρ). It's twice as large as follow-up scores when there's no correlation, equal at ρ = 0.5, and smaller only above 0.5.
- **ANCOVA:** variance is 1 − ρ², which is never larger than either of the others. At ρ = 0.5 it's 0.75, a quarter lower than both simple methods. All three methods converge only as the correlation approaches 1.

A lower variance means a narrower confidence interval and more power for the same sample size → [[Sample size and power]].

When the correlation is low, subtracting baseline adds noise. When it's high, ignoring baseline throws away information. It's wrong, though, to pick whichever analysis gives the more significant result: the method should be specified in the trial protocol.
[Vickers 2001](https://pubmed.ncbi.nlm.nih.gov/11701584/)

## Baseline imbalance

Change scores are often used to account for chance imbalances at baseline, but they don't control for them, because of regression to the mean: people with low baseline scores tend to improve more than those with high scores, so baseline is negatively correlated with change. ANCOVA adjusts each person's follow-up score for their baseline score.
[Vickers 2001](https://pubmed.ncbi.nlm.nih.gov/11701584/)

A common objection is that ANCOVA is biased if the groups differ at baseline, which would rule it out for observational studies. But groups don't need to be equal at baseline, even on average, for ANCOVA to give unbiased treatment effects. And while there are situations where ANCOVA is biased, it's very hard to find any where the simple change score analysis would then be unbiased and could be interpreted causally. This debate is related to Lord's paradox.
[Senn 2006](https://pubmed.ncbi.nlm.nih.gov/16921578/)
