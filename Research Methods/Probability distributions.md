---
tags:
  - research-methods
aliases:
  - Binomial distribution
  - Poisson distribution
  - Normal distribution
  - Empirical rule
  - Z-scores
up: "[[Research Methods MOC]]"
---
> [!summary] Bottom line
> A probability distribution gives the probability of each value a random variable can take. The binomial distribution counts successes out of a fixed number of independent trials, the Poisson counts events in an interval with no upper limit, and the normal is the symmetric bell curve described by its mean and variance. Z-scores put any value on the scale of standard deviations from the mean.

## Random variables

A random variable takes different numerical values by chance. Discrete random variables take a countable set of values (number of pregnancies), and continuous ones can take any value in an interval (BMI) → [[Levels of measurement]].

A discrete random variable has a probability function giving P(X = x) for each value, and the probabilities must each be between 0 and 1 and add up to 1. Its expected value (mean) is E(X) = Σ x·P(X = x), and its variance is Σ (x − μ)²·P(X = x).

A continuous random variable has a probability of exactly 0 for any single value, so it's described by a probability density function instead. The area under the curve between two values is the probability of falling between them, and the total area is 1.

## Binomial distribution

A binomial experiment has a fixed number of identical trials (n), two possible outcomes on each, the same probability of success (p) on every trial, and independent trials. The number of successes X then follows:

P(X = x) = [n! / (x!(n − x)!)] · pˣ · (1 − p)ⁿ⁻ˣ

with mean np and variance np(1 − p). For example, with obesity at 20.9%, the probability that exactly 2 of 3 random adults are obese is 3 × 0.209² × 0.791 = 0.104.

Many counts aren't binomial: the miscarriages in one woman's pregnancies aren't identical, equally likely or independent trials, and neither are hurricanes hitting Florida.
[NIST: Binomial distribution](https://www.itl.nist.gov/div898/handbook/eda/section3/eda366i.htm)

## Poisson distribution

The Poisson distribution counts events in an interval (often of time) when they happen at a constant average rate λ and the count has no upper limit:

P(X = x) = e^(−λ) · λˣ / x!

Its mean and variance are both λ. For example, with an average of 7 traffic accidents a month at an intersection, the chance of exactly 8 in a month is 0.130.

For rare events (small p, large n), the binomial is closely approximated by a Poisson with λ = np.
[NIST: Poisson distribution](https://www.itl.nist.gov/div898/handbook/eda/section3/eda366j.htm)

## Normal distribution

The normal (Gaussian) distribution is symmetric and unimodal, so its mean, median and mode are equal, and it's fully described by its mean μ and variance σ², written N(μ, σ²). N(0, 1) is the standard normal. For a normal variable:
- 68.26% of values fall within 1 SD of the mean
- 95.44% within 2 SDs
- 99.72% within 3 SDs

The empirical rule applies the same figures approximately to any bell-shaped distribution. Skewed variables, like BMI in teenagers, where obesity stretches the right tail, don't follow it well.
[NIST: Normal distribution](https://www.itl.nist.gov/div898/handbook/eda/section3/eda3661.htm)

## Z-scores and Chebyshev's inequality

A z-score expresses a value as standard deviations from the mean: z = (x − x̄) / s. A 15-year-old boy with a BMI of 25, where the mean is 19.83 and the SD is 3.43, has z = 1.51.

How unusual a z-score is depends on the distribution. Chebyshev's inequality gives a floor that holds for any distribution: at least 1 − 1/k² of values lie within k SDs of the mean, so at least 75% within 2 SDs and 89% within 3 SDs. It's only a lower bound, so it's of limited practical use.
[Wikipedia: Chebyshev's inequality](https://en.wikipedia.org/wiki/Chebyshev%27s_inequality)
