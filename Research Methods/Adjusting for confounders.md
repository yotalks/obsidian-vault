---
tags:
  - research-methods
aliases:
  - Confounding
  - Confounder
  - Stratification
  - Mantel-Haenszel
  - Residual confounding
  - Continuous predictors
up: "[[Research Methods MOC]]"
---
> [!summary] Bottom line
> A confounder is linked to both the exposure and the outcome and distorts the association between them. Randomization handles this at the design stage, and observational studies adjust for it in the analysis, by stratifying or with regression. Comparing crude and adjusted results shows whether a variable was confounding. Adjustment can only remove what was measured, and turning a continuous variable into wide categories leaves residual confounding behind.

## What a confounder is

A confounder correlates with both the exposure and the outcome. If coffee drinkers smoke more and smoking isn't measured, coffee can look like it causes lung cancer.
[Pourhoseingholi 2012](https://pmc.ncbi.nlm.nih.gov/articles/PMC4017459/)

A confounder should also not be a step between the exposure and the outcome. If it is, adjusting for it removes part of the real effect. BMI can be this kind of problem for diet. → [[Vegan diets and fractures]]

If the crude and adjusted results differ, confounding is likely. In the extreme case, an association reverses once groups are separated, which is Simpson's paradox.

## At the design stage

- **Randomization** breaks the link between exposure and confounders, known and unknown. This is why trials are preferred. → [[Evidence hierarchy]]
- **Restriction** limits a confounder by only studying one group, like one sex or age range.
- **Matching** picks comparison subjects with the same confounders, like matching a 45-year-old male case to a 45-year-old male control.

## Stratification

Stratification divides the data into subgroups, called strata, where the confounder doesn't vary. Everyone in the stratum of men has the same sex, so sex can't confound within it. There are three steps:

1. Split the data by the confounder.
2. Measure the association within each stratum.
3. If the strata agree, combine them into one adjusted estimate with a weighted average.

**Only pool if the strata agree.** Averaging assumes the strata are estimating the same effect. If a risk ratio is 0.5 in one stratum and 2 in the other, an average near 1 hides a harm in one group and a benefit in the other. That's effect modification, and the strata should be reported separately.
[Data Learner: Stratification](https://www.youtube.com/watch?v=VA0u0pyjWLk)

Stratification is intuitive, but it isn't practical with many confounders. Two categories each for age, blood pressure, cholesterol and activity already make 16 strata, which spreads the data too thin. It works best with one or two confounders.

## Mantel-Haenszel

The Mantel-Haenszel method is the usual way to do the weighted average. It was published in 1959 for case-control studies, and later extended to risk and rate ratios. Regression has mostly replaced it.

For each stratum, using a 2×2 table with T people in total:

| | Disease | No disease | Total |
|---|---|---|---|
| **Exposed** | a | b | N1 |
| **Unexposed** | c | d | N0 |

- **Risk or rate ratio:** Σ(a × N0 / T) ÷ Σ(c × N1 / T)
- **Odds ratio:** Σ(a × d / T) ÷ Σ(b × c / T)

For a rate ratio, N1, N0 and T are person-time.

The risk ratio formula is a weighted average of each stratum's risk ratio, with a weight of c × N1 / T. That weight is large when a table has more information, because it's the product of three things:
- **Total size**, T
- **Balance** between exposed and unexposed, N1 × N0 / T²
- **Baseline risk**, c / N0

So a table of 100 people split evenly can carry more weight than a table of 1,000 with only one unexposed person.
[Data Learner: Mantel-Haenszel](https://www.youtube.com/watch?v=LPr5tdAhhPA)

### Example: age hiding an effect

This cohort compared mortality in men and women with trigeminal neuralgia:

| Group | Men (deaths / person-years) | Women (deaths / person-years) | Rate ratio |
|---|---|---|---|
| **Under 65** | 14 / 1,516 | 10 / 1,701 | 1.57 |
| **65 and over** | 76 / 949 | 121 / 2,245 | 1.49 |
| **Crude** | 90 / 2,465 | 131 / 3,946 | 1.10 |

The two strata agree, so they can be pooled:

(14 × 1,701 / 3,217 + 76 × 2,245 / 3,194) ÷ (10 × 1,516 / 3,217 + 121 × 949 / 3,194) = 1.5

Age is a confounder here because it's linked to both exposure and outcome. Men's person-years were younger (62% vs 43% under 65), and older people died at about nine times the rate. Men's higher risk and younger age worked in opposite directions, so the crude 1.1 hid a rate ratio of 1.5.

### Example: a reversal

In a cross-sectional study of H. pylori and dyspepsia, the crude odds ratio was about 0.63, which looks protective. Splitting by weight gave 0.80 (0.38–1.69) in normal weight and 1.60 (0.79–3.27) in overweight people. The Mantel-Haenszel estimate was 1.16 (0.71–1.90), and logistic regression gave nearly the same result (1.15, 0.71–1.89). So the apparent protection came from weight.
[Pourhoseingholi 2012](https://pmc.ncbi.nlm.nih.gov/articles/PMC4017459/)

## Regression

Models can adjust for many confounders at once, and they're now the standard approach.

- **Logistic regression** gives an adjusted odds ratio for a binary outcome. It needs a large enough sample. → [[Sample size and power]]
- **Linear regression** does the same for a numeric outcome.
- **ANCOVA** combines ANOVA and regression, and adjusting for a covariate can also add power. → [[Change scores vs ANCOVA]]

## Residual confounding

Adjustment doesn't always remove all the confounding:

- **Unmeasured confounders** can't be adjusted for.
- **Measurement error** in a confounder leaves some of it behind.
- **Wide categories** leave confounding inside each category.
- **The wrong shape** for the relationship between confounder and outcome can give the wrong answer about the exposure.

Variables also shouldn't be picked on statistics alone. Choosing them takes field knowledge and a causal model, and adjusting for the wrong thing can add bias.
[Pourhoseingholi 2012](https://pmc.ncbi.nlm.nih.gov/articles/PMC4017459/)

### Categories

Sex has no within-group problem, but age does. If "under 65" is one stratum, smokers might be in their 50s and non-smokers in their 40s, so age still confounds. Narrower strata fix this, but they leave fewer people in each one. So you want enough strata to remove the confounding, and not so many that you run out of data.

Where the risk changes quickly matters most. A wide band over a steep part of the curve leaves far more confounding than the same band over a flat part. → [[Vegan diets and fractures]]

## Handling continuous predictors

| Procedure | Characteristics | Recommendation |
|---|---|---|
| **Dichotomization** | Simple, easy to interpret | Bad idea |
| **More categories** | Capture more prognostic information but aren't smooth, and are sensitive to the choice of cut-points | Mainly for illustration or comparing with published evidence |
| **Linear** | Simple | Often reasonable as a start |
| **Polynomials** | Square and cubic terms added, but the tails may be unstable | Reasonable as checks for non-linearity |
| **Transformations** | Log, square root, inverse, exponent and others | May give robust summaries of non-linearity |
| **Restricted cubic splines** | Flexible, with robust behavior at the tails | Flexible descriptions of non-linearity |
| **Fractional polynomials** | Flexible combinations of polynomials, but the tails may be unstable | Flexible descriptions of non-linearity |

[Steyerberg 2009](https://doi.org/10.1007/978-0-387-77244-8)
