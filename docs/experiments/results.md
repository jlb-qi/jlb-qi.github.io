---
layout: default
title: Experiment Results
nav_order: 1
parent: Experiments
---

# The Results
{: .no_toc }


Just the Docs has some specific configuration parameters that can be defined in your Jekyll site's _config.yml file.
{: .fs-6 .fw-300 }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---


## What do the numbers mean

### P Value

P-value :- The P value, or calculated probability, is the probability of finding the observed, or more extreme, results when the null hypothesis (H 0) of a study question is true — the definition of ‘extreme’ depends on how the hypothesis is being tested.

If your P value is less than the chosen significance level then you reject the null hypothesis i.e. accept that your sample gives reasonable evidence to support the alternative hypothesis. It does NOT imply a “meaningful” or “important” difference; that is for you to decide when considering the real-world relevance of your result.

Example : you have a coin and you don’t know whether that is fair or tricky so let’s decide null and alternate hypothesis

H0 : a coin is a fair coin.

H1 : a coin is a tricky coin. and alpha = 5% or 0.05

Now let’s toss the coin and calculate p- value ( probability value).

Toss a coin 1st time and result is tail- P-value = 50% (as head and tail have equal probability)

Toss a coin 2nd time and result is tail, now p-value = 50/2 = 25%

and similarly we Toss 6 consecutive time and got result as P-value = 1.5% but we set our significance level as 95% means 5% error rate we allow and here we see we are beyond that level i.e. our null- hypothesis does not hold good so we need to reject and propose that this coin is a tricky coin which is actually.

[Ref](https://towardsdatascience.com/hypothesis-testing-in-machine-learning-using-python-a0dc89e169ce)

![](/assets/images/pvalue_visit_days.png)

### Confidence Intervals

### Power

The power of a hypothesis test is the probability of making the correct decision if the alternative hypothesis is true. In general, for every hypothesis test we conduct, we will try to maximize the power. Typically, we desire the power to be 0.8 or greater.


### References

[How to interpret AB test results](https://www.optimizesmart.com/understanding-ab-testing-statistics-to-get-real-lift-in-conversions/#a19)
