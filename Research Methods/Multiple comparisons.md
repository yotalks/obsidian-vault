---
tags:
  - research-methods
aliases:
  - Bonferroni correction
  - Family-wise error rate
  - FWER
  - False discovery rate
  - FDR
  - Multiple testing
up: "[[Research Methods MOC]]"
---
> [!summary] Bottom line
> Every statistical test at P < 0.05 has a 5% chance of a false positive. A study that runs many analyses will find some significant results by chance alone. Corrections like Bonferroni guard against this, at the cost of missing some real effects. Corrections can control either the family-wise error rate (the chance of any false positive) or the false discovery rate (the share of significant results that are false).

## The problem

At the usual threshold of P < 0.05, each test has a 1 in 20 chance of a false positive when there's no real effect. Running 20 tests on null data would, on average, turn up one "significant" result. If researchers then present the strongest estimates as their findings, chance results look like discoveries.

## Family-wise error rate

The family-wise error rate (FWER) is the probability of at least one false positive (type I error) within a "family", or group, of comparisons. For m independent tests at significance level α, the chance of no false positives at all is (1 − α)^m, so:

FWER = 1 − (1 − α)^m

At α = 0.05, the chance of at least one false positive is 40% with 10 tests, 64% with 20 and 92% with 50. Even at α = 0.01 it passes 60% by 100 tests, and with enough tests at least one false positive becomes almost certain. Testing 10,000 true null hypotheses at α = 0.05 would wrongly reject about 500. The formula is exact only for independent tests; correlated tests and some false null hypotheses make the true error rate harder to calculate.
![[Family-wise error rate by number of tests.png]]
[Chen 2017](https://pubmed.ncbi.nlm.nih.gov/28740688/)

## False discovery rate

The false discovery rate (FDR) is the expected proportion of false positives among all the results declared significant:

FDR = false positives / (false positives + true positives)

Controlling the FDR allows a set proportion of false positives instead of trying to prevent any, which gives much more power when hundreds or thousands of hypotheses are tested, such as in genetics.
[Chen 2017](https://pubmed.ncbi.nlm.nih.gov/28740688/)

## Bonferroni correction

The Bonferroni correction divides the significance threshold by the number of tests. With 10 tests, each needs P < 0.005 to count as significant. With 159 tests, each needs about P < 0.0003.

In general, the adjusted alpha is α divided by the number of comparisons, so with α = 0.05 and 6 comparisons it's 0.0083. This keeps the family-wise error rate at or just below 0.05 (about 0.049 for 6 independent tests).

It's conservative: it lowers false positives but raises false negatives, so it isn't meant to be applied routinely. It's most appropriate when many tests are run without preplanned hypotheses, or when avoiding a false positive is essential.
[Armstrong 2014](https://pubmed.ncbi.nlm.nih.gov/24697967/)

## Other adjustment methods

- **Holm:** a stepwise version of Bonferroni that's less conservative. P values are ranked from smallest to largest, and the i-th smallest is compared with α / (m − i + 1), stopping at the first one that isn't significant.
- **Hochberg:** uses the same thresholds as Holm but starts from the largest P value, which gives a little more power.
- **Benjamini–Hochberg:** controls the false discovery rate instead of the family-wise error rate. P values are ranked, and every hypothesis up to the largest rank i where p(i) ≤ (i / m) × q is rejected, with q the chosen FDR (such as 0.05).

All of these can be calculated with the p.adjust() function in R.
[Chen 2017](https://pubmed.ncbi.nlm.nih.gov/28740688/)

In simulations of randomized trials with several primary outcomes, Bonferroni and Holm had the same power to detect at least one true effect, and Hochberg and Hommel gave small power gains over Bonferroni. The Stepdown-minP method worked well with complete data but lost power with missing data, because it drops participants with any missing values.
[Vickerstaff 2019](https://pubmed.ncbi.nlm.nih.gov/31226934/)

## Example: diet soda, stroke and dementia

A Framingham study linked artificially sweetened soft drinks to stroke and dementia without correcting for multiple comparisons, and none of its results would survive a Bonferroni correction. See [[Artificial sweeteners#Stroke and dementia|Artificial sweeteners]].
