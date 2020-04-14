---
layout: default
title: Results - Distributions
nav_order: 3
parent: Experiments
---

# What distributions are you working with
{: .no_toc }


How to evaluate experiments with Bayesian techniques.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Gaussian

## Gamma

(as gamma is conjugate to the exponential [ref](https://discourse.pymc.io/t/revenue-metric-for-ab-testing/3800))

StoryYou sit waiting for shooting stars, where the waiting time for astar is distributed Expo(λ).  You want to seenshooting stars beforeyou go home.  The total waiting time for thenth shooting star isGamma(n,λ).ExampleYou are at a bank, and there are 3 people ahead of you.The serving time for each person is Exponential with mean 2 minutes.Only one person at a time can be served.  The distribution of yourwaiting time until it’s your turn to be served is Gamma(3,12).[ref: probability cheatsheet](http://static1.squarespace.com/static/54bf3241e4b0f0d81bf7ff36/t/55e9494fe4b011aed10e48e5/1441352015658/probability_cheatsheet.pdf)

## Binomial

Limited to True|False outcomes.

Types of events;
- signups
- conversions
- CTR

## Multinomial

## Dirichlet

[Estimating Probabilities with Bayes](https://towardsdatascience.com/estimating-probabilities-with-bayesian-modeling-in-python-7144be007815)

## Uniform

Typically used for setting priors where you know very little about what to expect.

Let us say that U is distributed Unif(a,b).  We know the following:
**Properties of the Uniform** For a Uniform distribution, the probability of a draw from any interval within the support is proportional to the length of the interval.  

**Example** William throws darts really badly, so his darts are uniform over the whole room because they’re equally likely to appear anywhere. William’s darts have a Uniform distribution on the surface of the room.  The Uniform is the only distribution where the probability of hitting in any specific region is proportional to the length/area/volumeof that region, and where the density of occurrence in any one specific spot is constant throughout the whole support.

## Beta

The Beta distribution can be seen as a generalization of the Uniform(0,1) as it lets more general probability density functions over the interval (0,1) to be defined. Think of it as a versatile family of probability distributions over (0,1) which allows us to create priors that incorporate some of our beliefs and thus informative priors. When you have k-succeses out of n trials the posterior distribution can be modelled as Beta(k+1, n-k+1).

If you have a coin with an unknown bias p and that coin lands heads-up on 70 out of 100 flips, then p ~ Beta(71,31). If you send out an email campaign and get 100 conversions out of 10,000 emails sent, then the true conversion rate p for the campaig will be Beta(101, 9901) distributed. I'll keep things simple and visual here. [ref](https://guneetkohli.github.io/ab-testing/BayesianABTesting/#.XoYaOG5S_ty)

(as Beta is conjugate to the bernoulli)

Conjugate Prior of the BinomialIn the Bayesian approach tostatistics, parameters are viewed as random variables, to reflect ouruncertainty.  Thepriorfor a parameter is its distribution beforeobserving data.  Theposterioris the distribution for the parameterafter observing data.  Beta is theconjugateprior of the Binomialbecause if you have a Beta-distributed prior onpin a Binomial, thenthe posterior distribution onpgiven the Binomial data is alsoBeta-distributed. [ref: probability cheatsheet](http://static1.squarespace.com/static/54bf3241e4b0f0d81bf7ff36/t/55e9494fe4b011aed10e48e5/1441352015658/probability_cheatsheet.pdf)

## Deterministic

continuous variables

## LogNormal

## Poisson

## Bernoulli


## References

[Conjugate distributions - Wikipedia](https://en.wikipedia.org/wiki/Conjugate_prior)

[PYMC3 distributions](https://docs.pymc.io/api/distributions/continuous.html)
