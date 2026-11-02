---
tags:
  - research-methods
aliases:
  - Sensitivity and specificity
  - Predictive values
  - PPV
  - NPV
  - ROC curves
  - Screening tests
up: "[[Research Methods MOC]]"
---
> [!summary] Bottom line
> Sensitivity and specificity describe the test: how often it's positive in people with the disease and negative in people without it. Predictive values describe a result: how likely someone with a positive or negative test is to actually have or not have the disease, and they depend heavily on how common the disease is. Even a good test gives mostly false positives when a disease is rare. ROC curves show the trade-off between sensitivity and specificity across cut-offs.

## Definitions

A screening test classifies people as positive or negative before symptoms show, and is checked against a gold standard that's always correct (like a biopsy).
- **True positive:** positive test, has the disease.
- **True negative:** negative test, doesn't have the disease.
- **False positive:** positive test, doesn't have the disease.
- **False negative:** negative test, has the disease.

|  | Diseased | Not diseased |
|---|---|---|
| **Test +** | a (true positive) | b (false positive) |
| **Test −** | c (false negative) | d (true negative) |

- **Sensitivity** = P(test + given disease) = a / (a + c)
- **Specificity** = P(test − given no disease) = d / (b + d)
- **Positive predictive value (PPV)** = P(disease given test +) = a / (a + b)
- **Negative predictive value (NPV)** = P(no disease given test −) = d / (c + d)

[Altman 1994a](https://pubmed.ncbi.nlm.nih.gov/8019315/)

## Predictive values depend on prevalence

PPV and NPV can only be read straight off the table when the study tested a random sample of the population. Most test studies instead recruit a set number of diseased and non-diseased people, which fixes the prevalence in the sample, so only sensitivity and specificity carry over. Predictive values then have to be worked out from the prevalence in the population of interest using Bayes' theorem:

PPV = sensitivity × prevalence / [sensitivity × prevalence + (1 − specificity) × (1 − prevalence)]

NPV = specificity × (1 − prevalence) / [specificity × (1 − prevalence) + (1 − sensitivity) × prevalence]

For example, a diabetes test with 80% sensitivity and 90% specificity, used where 7% of people have diabetes, gives a PPV of only 37.6%: (0.8 × 0.07) / (0.8 × 0.07 + 0.1 × 0.93). Most positives are false positives, because the 10% false positive rate is applied to the 93% of people without diabetes.
[Altman 1994b](https://pubmed.ncbi.nlm.nih.gov/8038641/)

The same algebra runs backward: if sensitivity and specificity are known, the share of positive tests in a new population gives its prevalence without using the gold standard:

prevalence = [P(test +) − (1 − specificity)] / [sensitivity − (1 − specificity)]

With the same test, 105 positives out of 580 people gives (0.181 − 0.1) / (0.8 − 0.1) ≈ 11.6%.

## ROC curves

Sensitivity and specificity trade off against each other. When a test has a scale, like a radiologist rating CT scans from 1 (definitely normal) to 5 (definitely abnormal), each possible cut-off gives a different pair: calling everything abnormal catches every case (sensitivity 1) but has specificity 0, and calling everything normal does the reverse.

A receiver operating characteristic (ROC) curve plots sensitivity against 1 − specificity for every cut-off. The point closest to the top-left corner has the best combination of the two. The diagonal line is a test no better than chance, which misclassifies diseased and healthy people equally often, and the area under the curve summarizes how well the test separates them across all cut-offs (0.5 is chance, 1 is perfect).
[Altman 1994c](https://pubmed.ncbi.nlm.nih.gov/8044101/)
