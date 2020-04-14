---
layout: default
title: Results - Frequentist
nav_order: 4
parent: Experiments
---

# The Results
{: .no_toc }


## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## The Test
Most commonly we use a ttest to perform an analysis.


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


[Complete guide to statistical significance](http://blog.analytics-toolkit.com/2017/statistical-significance-ab-testing-complete-guide/)

### Type I errors

False positive – Rejecting a true null hypothesis.

In A/B testing this would mean that you call your variation a winner when it actually is worse, equal or less good than your test showed.

So, the p-value, along with the prespecified α, directly controls the type I (false positive) error rate.

    Rejecting a null hypothesis (calling your variation a winner) is a result that triggers an action, most commonly ending in a change on your website (implementing your variation). Therefore, you must think wisely about what is the per cent of such false decisions that you can live with!

### Type II errors

False negative – Not rejecting a false null hypothesis.

In A/B testing it usually describes a situation where your variation is a winner but your test shows it is not significantly better or worse than the control.

Why is this a problem?

Rolling out the wrong version risks that the worse option has been chosen.

### Confidence Intervals

### Power

The power of a hypothesis test is the probability of making the correct decision if the alternative hypothesis is true. In general, for every hypothesis test we conduct, we will try to maximize the power. Typically, we desire the power to be 0.8 or greater.

### Non-binomial data


Non-binomial data is everything that doesn't have a True|False outcome. Commonly in the likes of eCommerce this would be things like revenue per user, time on site, number of likes per user.

You may hear some say that there's no way you can use a ttest (which assumes normal distributions) to evaluate these metrics due to the fact that they are, in most cases, heavily skewed. Wrong. Ttest assumes normal distribution of the sample statistics, not of each individual data point.

[Statistical significant in non-binomal metrics](http://blog.analytics-toolkit.com/2017/statistical-significance-non-binomial-metrics-revenue-time-site-pages-session-aov-rpu/)


### Alternatives to the 'Traditional' approach

We could use Bayes (see seperate section) which does have it's pros but obviously cons as well. Staying within the Frequentist paradigm we can use Sequential testing.

[Rapid A/B-testing with Sequential Analysis](https://www.auduno.com/2014/12/25/rapid-a-b-testing-with-sequential-analysis/)

[A/B test rigourously without losing your job](http://elem.com/~btilly/ab-testing-multiple-looks/part1-rigorous.html)



### References

[The Math behind AB testing](https://towardsdatascience.com/the-math-behind-a-b-testing-with-example-code-part-1-of-2-7be752e1d06f)

[How to interpret AB test results](https://www.optimizesmart.com/understanding-ab-testing-statistics-to-get-real-lift-in-conversions/#a19)

[Frequentism  vs Bayesianism: Practical Intro](http://jakevdp.github.io/blog/2014/03/11/frequentism-and-bayesianism-a-practical-intro/)