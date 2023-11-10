# MCMC Sampling for a Logistic Regression Model
Create and implement a Markov chain Monte Carlo (MCMC) sampler in R for a logistic regression model. 

Key features:

- Markov Chain Monte Carlo (MCMC) Sampler - Metropolis–Hastings Algorithm
- Logistic Regression Model
- Maximum Likelihood Estimate (MLE) Fit
- Prior and Posterior Distribution
- Jumping Distribution
- Posterior Means and Standard Deviations
- Credible Intervals
- Burn-in Used

## Project Report

The analysis results with all theoretical backgrounds and math derivations are included in the [project report](./project2.md) ([R Markdown](./project2.Rmd)).

Original Completion Date: Tuesday, October 22, 2022

Author: Chien-Lan Hsueh (chienlan.hsueh at gmail.com)

## Overview and Project Goal

Suppose we have independent observations of success (has diabetes) or failure (has no diabetes)
from a data set taken from [Kaggle](https://www.kaggle.com/datasets/vikasukani/diabetes-data-set). We can use MLE to conduct an inference on $p$. Since the MLEs do not have a closed form solution, we will try to solve using MCMC sampling by allowing for $\beta_0$ and $\beta_1$ to each have normal distribution priors. With the $R$ ratio and the jumping distribution, implement a MCMC sampler to Obtain posterior distributions for the parameters as well as the posterior statistics and their credible intervals. 

Finally, Improve the MCMC algorithm and compare the burn-in used (MCMC MH Bivariate Manner).