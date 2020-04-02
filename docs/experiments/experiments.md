---
layout: default
title: Experiments
nav_order: 2
has_children: true
---

# Hypothesis testing in Product Development
{: .no_toc }


How to conduct experiments and test the performance of new/updated features.

## Main Comporents
{: .no_toc .text-delta }

1. Table of Contenst
{:toc}

---


## The Process

1. Design your experiment
2. Configure and run your experiment
3. Evaluate your experiment

## Freq vs Bayes

https://www.dynamicyield.com/blog/bayesian-testing/

||Hypothesis Testing |	Bayesian A/B Testing|
|Knowledge of Baseline Performance |	Required 	|Not Required|
|Intuitiveness |	Less, as p-value is a convoluted term| 	More, as we directly calculate the probability of A being better than B|
|Sample size 	|Pre-defined 	|No need to pre-define|
|Peeking at the data while the test runs |	Not allowed |	Allowed (with caution)|
|Quick to make decisions |	Less, as it has more restrictive assumptions on distributions |	More, as it has less restrictive assumptions|
|Representing uncertainty |	Confidence Interval (again, a convoluted interpretation which is often misunderstood) |	Highest Posterior Density Region – highly intuitive interpretation|
|Declaring a winner |	When sample size is reached and p-value is below a certain threshold |	When either “probability to be best” goes above a threshold or the expected loss is below a threshold (in which case a “tie” can be declared between multiple variations)|


