---
tags:
  - research-methods
aliases:
  - Standardized mean difference
  - SMD
up: "[[Research Methods MOC]]"
---
> [!summary] Bottom line
> When studies in a meta-analysis measure an outcome in the same units, the plain mean difference (MD) is usually the right choice. The standardized mean difference (SMD) is meant for outcomes measured on different scales, and it only works if those scales measure the same underlying thing. Differences in baseline levels between populations aren't different scales, and using SMD for them can manufacture significance.

## What each one does

- **Mean difference (MD):** the difference between groups in the outcome's own units, for example a hormone level in IU/L.
- **Standardized mean difference (SMD):** the difference divided by the standard deviation, which puts each study on a common, unitless scale.

SMD is mainly used when studies measure the same outcome with different instruments, such as different depression or quality-of-life scales. Without standardizing, those results couldn't be pooled at all.
[Murad 2019](https://pmc.ncbi.nlm.nih.gov/articles/PMC6890471/)

## SMD's assumptions

Having different scales isn't enough on its own to justify SMD. Two assumptions have to hold.

1. **Same underlying construct.** The scales being combined have to measure the same or a similar thing. [Murad 2019](https://pmc.ncbi.nlm.nih.gov/articles/PMC6890471/)
2. **Differences in spread come from the scales, not the people.** SMD assumes that differences in standard deviations between studies reflect different measurement scales, not real differences in how variable the populations are. If the true effects are identical but the SDs differ, the SMDs will differ too. For example, pragmatic trials may enroll a wider range of people than explanatory trials, and so have larger SDs. [Cochrane Handbook 6.5.1.2](https://www.cochrane.org/authors/handbooks-and-manuals/handbook/current/chapter-06)

Together these mean a result 1 SD from the mean on one scale should correspond to 1 SD on another. That's a common assumption in psychometrics. It's much harder to defend for a biological measure, where 1 SD in one study needn't have the same biological effect as 1 SD in another.

## MD vs SMD in practice

Across 1,068 Cochrane meta-analyses that pooled the same continuous outcome in the same units:
- SMD had lower heterogeneity (I²) and was more generalizable.
- MD had slightly more statistical power, but the share of significant results didn't differ between the two.

[Takeshima 2014](https://pubmed.ncbi.nlm.nih.gov/24559167/)

So when MD and SMD analyses disagree, it's no reason in itself to prefer the SMD.

## Example: soy and reproductive hormones

A meta-analysis of soy in premenopausal women used SMD because baseline hormone levels varied between studies. With SMD, FSH and LH fell significantly; with MD, neither did. Varying baseline levels are a difference between populations, not a difference in scales. The hormones were all measured in the same units, so a change of a given number of units means the same thing in every study unless the effect depends on baseline. The MD analysis is the better guide here. See [[Soy#Hormones in women|Soy]].
[Hooper 2009](https://pmc.ncbi.nlm.nih.gov/articles/PMC2691652/)
