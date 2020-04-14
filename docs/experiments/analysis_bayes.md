---
layout: default
title: Results - Bayes
nav_order: 3
parent: Experiments
---

# Bayesian Methodology
{: .no_toc }


How to evaluate experiments with Bayesian techniques.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Bayes

[How to learn to love Bayes](https://towardsdatascience.com/bayesian-nightmare-how-to-start-loving-bayes-1622741fa960)

### The Concepts


α – underlying and unobserved true metric for variant A

β – underlying and unobserved true metric for variant B

Therefore, If we choose variant A when α is less than β, our loss is β – α. If α is greater than β, we lose nothing. Our loss is the amount by which our metric decreases when we choose that variant.

[ref](https://medium.com/convoy-tech/the-power-of-bayesian-a-b-testing-f859d2219d5)

#### Priors

Prior – one of the key differences between Frequentist and Bayesian is that the latter can take prior information into account. Hence, it doesn’t have to learn all the data points itself and can, therefore, reach the conclusions faster.

    For example, let’s say we use a Beta(1, 1) distribution as the prior for a Bernoulli distribution. After observing 40 successes and 60 failures, our posterior distribution is a Beta(41, 61)⁶. However, if we had started with a Beta(8, 12) distribution as our prior, we would only need to observe 32 successes and 48 failures in order to obtain the same distribution as before.

In general, it is suggested to choose priors that are a bit weaker than what the historical data suggest.

##### Conjugate priors 


#### Expected Loss

ε – the threshold of expected loss for one of the variants, under which we stop the experiment

This is how we measure the effect of different variants

#### Posterior distributions

This is where the answer we're looking for lies. There's a concept called the **maximum likelihood estimator**. This is the point on the posterior distribution where the greatest probability lies. The **posterior mean** is the best guess at the true value of the metric you're interested in and the **credible interval** is the shortest interval that contains 90% of the probabilities. 


For example, focusing just on the expected loss may lead us to call null results significant. But if we base our procedure not just on the expected loss, but also the posterior probability Pr(B>A), we can focus on cases where we’re confident in a positive change.


#### Some model parameters

- Mu: the mean of the vector of interest
- Sigma: the standard deviation of the vector of interest
- Theta: 
- Nu:
- Lambda: 


### Presenting results

Most Bayesian-based A/B testing tools, like VWO, present their results using three key metrics

- Relative improvement VS control – a range by which the observed metric for the variation is better or worse than the same metric for the control. The range is calculated for a 99% probability. The more data the test collects, the smaller this range gets.
- Absolute potential loss – the potential loss is the lift you can lose out on if you deploy A as the winner when B is actually better.
- Chance to beat control/all – probability of the variation being better than the control/all other variations.

[VWO smartstats](https://help.vwo.com/hc/en-us/articles/360033471874)


### The downsides of a Bayesian approach

[5 reasons for switching to Bayesian debunked](http://blog.analytics-toolkit.com/2017/5-reasons-bayesian-ab-testing-debunked/)


## References

### Intros

- [Evan Miller bayes intro](https://www.evanmiller.org/bayesian-ab-testing.html)

- [Is Bayesian A/B Testing Immune to Peeking? Not Exactly](http://varianceexplained.org/r/bayesian-ab-testing/)

- [The Power of Bayesian Testing](https://medium.com/convoy-tech/the-power-of-bayesian-a-b-testing-f859d2219d5)

- [Getting started with Bayes AB testing (signups/conversions w/o PYMC3)](https://guneetkohli.github.io/ab-testing/BayesianABTesting/#.XocY225S8w2)

- [Bayesian Nightmare, How to start loving Bayes](https://towardsdatascience.com/bayesian-nightmare-how-to-start-loving-bayes-1622741fa960)

### Examples

- [Alpaca Bear example (i.e. counts/Beta distribution)](https://medium.com/hockey-stick/tl-dr-bayesian-a-b-testing-with-python-c495d375db4d)

- [Lions, Tigers & Bears example (i.e. multinomial/dirichlet distribution)](https://towardsdatascience.com/estimating-probabilities-with-bayesian-modeling-in-python-7144be007815)

- [Beautifully Bayesian - How to do AB Testing with Discrete Rewards? (Dirichlet)](http://ewulczyn.github.io/ab_testing_with_multinomial_data/)

- [Bayes for Revenue AB testing (i.e. rates/Gamma and Poisson distributions)](https://medium.com/ni-tech-talk/optimizing-revenue-with-bayesian-a-b-testing-5068e8ac41ea)

- [Revenue metric for Bayes AB testing](https://discourse.pymc.io/t/revenue-metric-for-ab-testing/3800/6)

- [Optimizing revenue with Bayes AB testing](https://medium.com/ni-tech-talk/optimizing-revenue-with-bayesian-a-b-testing-5068e8ac41ea)

- [PYMC3 drug trial example](https://docs.pymc.io/notebooks/BEST.html)


### Calculators

- [Bayes AB test (conversion) calculator](https://marketing.dynamicyield.com/bayesian-calculator/?)

- [Bayes ARPU calculator](https://vidogreg.shinyapps.io/bayes-arpu-test/)


### Packages

- [BEST (R)](https://cran.r-project.org/web/packages/BEST/vignettes/BEST.pdf)
