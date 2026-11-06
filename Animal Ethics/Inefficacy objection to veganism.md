---
tags:
  - ethics/animals
aliases:
  - Causal inefficacy objection
  - Threshold argument
up: "[[Animal Ethics MOC]]"
---
> [!summary] Bottom line
> The inefficacy objection says one person's purchases are too small to change how many animals are raised. But if a purchase has a 1/n chance of triggering a production change of n animals, its expected impact is about one animal, and over a lifetime even low consumers are likely to trigger a threshold.

## The objection

Production doesn't change with every purchase. It changes in steps, so most purchases have no immediate effect and a few have a large one. Since a consumer can't know where the threshold is, the question is the expected impact: a purchase with a 1/n chance of triggering a change of n animals has an expected impact of about 1.
[McMullen 2018](https://doi.org/10.1007/s41055-018-00030-4)

## The chance of triggering a threshold

One estimate treats the smallest adjustment as a one-day delay in shipping birds to a large grower, which is close to 900 chickens.
[McMullen 2018](https://doi.org/10.1007/s41055-018-00030-4)

There's a 1/900 chance of triggering the threshold per purchase which impact will be that 900 more chickens will be sold that year. The average consumer purchases 30 chickens per year. We can calculate the probability of triggering the threshold in one year at least once with the binomial distribution formula.

So 30 chickens purchased in one year: P(x>=1) = 1-(1-1/900)^(30x1) = 3.2% 
For a lifetime (75 years): P=1-(1-1/900)^(30x75) = 91.8%

If someone cuts their chicken consumption to 50% of the average:
P = 1-(1-1/900)^(15) = 1.6% for 1 year and 
P = 1-(1-1/900)^(15x75) = 71% for 75 years

If someone cuts their chicken consumption to 1/3 of the average:
P = 1-(1-1/900)^(10) = 1.1% for 1 year and 
P = 1-(1-1/900)^(10x75) = 56% for 75 years

If someone cuts their chicken consumption to 25% of the average:
P = 1-(1-1/900)^(7.5) = 0.83% for 1 year and 
P = 1-(1-1/900)^(7.5x75) = 46% for 75 years

Even for low consumers, there is a considerable chance of triggering the threshold over a lifetime

## Connections
**Builds on**
- [[Animal Rights]] — the case for not paying for animal products
