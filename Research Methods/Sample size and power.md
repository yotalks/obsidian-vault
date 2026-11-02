---
tags:
  - research-methods
aliases:
  - Power analysis
  - Sample size calculation
  - Events per variable
  - EPV
  - Type II error
up: "[[Research Methods MOC]]"
---
> [!summary] Bottom line
> Power is the probability of correctly rejecting the null hypothesis when the alternative is true. Power, alpha, effect size, variance and sample size are linked, so fixing four of them sets the fifth, and each extra participant adds less power than the last. But power isn't the only reason to need a bigger sample: precise estimates, model assumptions like events per variable in logistic regression, checking distributions, multiple tests and generalizability all need more data too. Calling a study "underpowered" means little without saying what effect it was underpowered to detect.

## Power

Power is the probability that a test correctly rejects the null hypothesis, given that the alternative hypothesis is true. It's 1 − β, where β is the probability of a type II error (a false negative).

Power analysis is usually done before a study to find the sample size needed to reach the researcher's goals. It can also be run the other way: if only 75 participants are available, it shows how much power the study will have, and whether it's worth doing at all.

Five quantities are linked, so setting four determines the fifth:
1. **Power** (1 − β), often set at 0.8
2. **Alpha**, the type I error rate, usually 0.05
3. **Effect size**, which depends on the statistical test (for example Cohen's d)
4. **Variance** of the outcome
5. **Sample size**

A larger expected effect and lower variance mean a smaller sample is needed for the same power. A stricter alpha (0.01 instead of 0.05) lowers power. A one-tailed test puts all the power on one side, but then can't detect an effect in the opposite direction. The variance usually isn't known before collecting data, so it's estimated from earlier studies or a pilot study, ideally across a range of plausible values.

The right calculation depends on the study design, the statistical test, the groups being compared and how many comparisons are planned → [[Multiple comparisons]].
[UCLA OARC: Introduction to power analysis](https://stats.oarc.ucla.edu/other/mult-pkg/seminars/intro-power/)

## Diminishing returns

With everything else fixed, power rises with sample size but by less and less. In one example comparing two proportions, going from 10 to 60 participants per group raised power from about 0.15 to 0.6, while going from 100 to 150 per group only raised it from about 0.8 to 0.95.
[UCLA OARC: Introduction to power analysis](https://stats.oarc.ucla.edu/other/mult-pkg/seminars/intro-power/)

## Sample size beyond power

**Precision.** Showing that an effect differs from zero takes fewer people than estimating it precisely with a narrow confidence interval.

**More tests.** The more statistical tests planned, the larger the sample needed.

**Generalizability.** The more broadly results should apply, the larger and more representative the sample usually needs to be.
[UCLA OARC: Introduction to power analysis](https://stats.oarc.ucla.edu/other/mult-pkg/seminars/intro-power/)

**Model assumptions: events per variable.** Logistic regression needs enough outcome events relative to the number of predictor variables in the model. Events per variable (EPV) is the number of events in the smaller outcome category divided by the number of predictors. In a simulation based on a heart trial (673 patients, 252 deaths, 7 predictors), models with 10 or more EPV had no major problems. Below 10 EPV, coefficients were biased in both directions, confidence intervals had the wrong coverage, and associations in the wrong direction became more common. Rules of thumb of 10 or 20 EPV are common, and the right number depends on the model and whether it's used for inference or prediction.
[Peduzzi 1996](https://pubmed.ncbi.nlm.nih.gov/8970487/)

For example, modeling skin cancer type (melanoma, non-melanoma or none) from minutes in tanning beds and minutes in the sun without sunscreen uses 2 predictors. With 50 melanomas, 20 non-melanoma cancers and 100 people without skin cancer, the smallest category has 20 events, or 10 per predictor, which meets a 10 EPV rule but not a 20 EPV rule. With only 5 melanomas, it's 2.5 EPV, well below either.

**Checking distributions.** Even when sample size isn't part of a model's assumptions, more data makes it easier to check them. With samples drawn from the same normal distribution, a histogram of 10 values shows no recognizable shape, while 200 to 500 values clearly show the bell curve → [[Probability distributions]].
![[Normal samples by sample size.png]]

**More variables than observations.** When a dataset has more features than observations (more columns than rows), ordinary least squares regression can't find a unique solution. Gene expression data is the classic case, with far more genes than samples. The usual fix isn't more samples, which would take too many, but reducing or penalizing the variables with methods like LASSO, least angle regression, elastic net or principal component analysis.

## "This study is underpowered"

Power is always power to detect a specific effect size. A study can be well powered to detect a large effect and underpowered for a small one, so calling a trial "underpowered" without saying for what effect size gives the authors nothing to respond to → [[Underpowered studies in meta-analysis]].
[Towards Data Science: Why you shouldn't say "this study is underpowered"](https://towardsdatascience.com/why-you-shouldnt-say-this-study-is-underpowered-627f002ddf35)
