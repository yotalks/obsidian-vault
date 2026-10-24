---
tags:
  - research-methods
aliases:
  - Bonferroni correction
up: "[[Research Methods MOC]]"
---
> [!summary] Bottom line
> Every statistical test at P < 0.05 has a 5% chance of a false positive. A study that runs many analyses will find some significant results by chance alone. Corrections like Bonferroni guard against this, at the cost of missing some real effects.

## The problem

At the usual threshold of P < 0.05, each test has a 1 in 20 chance of a false positive when there's no real effect. Running 20 tests on null data would, on average, turn up one "significant" result. If researchers then present the strongest estimates as their findings, chance results look like discoveries.

## Bonferroni correction

The Bonferroni correction divides the significance threshold by the number of tests. With 10 tests, each needs P < 0.005 to count as significant. With 159 tests, each needs about P < 0.0003.

It's conservative: it lowers false positives but raises false negatives, so it isn't meant to be applied routinely. It's most appropriate when many tests are run without preplanned hypotheses, or when avoiding a false positive is essential.
[Armstrong 2014](https://pubmed.ncbi.nlm.nih.gov/24697967/)

## Example: diet soda, stroke and dementia

A Framingham study linked artificially sweetened soft drinks to stroke and dementia without correcting for multiple comparisons, and none of its results would survive a Bonferroni correction. See [[Artificial sweeteners#Stroke and dementia|Artificial sweeteners]].
