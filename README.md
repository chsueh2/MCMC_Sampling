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
- Burn-in

R packages used:

- `here`: enables easy file referencing and builds file paths in a OS-independent way
- `stats`: loads this before loading `tidyverse` to avoid masking some `tidyverse` functions
- `cumstats`: efficiently computing cumulative standard deviation
- `tidyverse`: includes collections of useful packages like `dplyr` (data manipulation), `tidyr` (tidying data),  `ggplots` (creating graphs), etc.
- `skimr`: provide summary statistics about variables in data frames, tibbles, data tables and vectors
- `glue`: embedding and evaluating R expressions into string to be printed as message
- `scales`: formats and labels scales nicely for better visualization
- `broom`: tidy and unify the fit objects returned by most of the modeling functions
- `TeachingDemos`: empirical HPD intervals

## Project Report

[Project report](https://rpubs.com/clh2021/1113694) ([Github Markdown](./project2.md))([R Markdown](./project2.Rmd))

The analysis results with all theoretical backgrounds and math derivations are included. 

Chien-Lan Hsueh (chienlan.hsueh at gmail.com)

## Overview and Project Goal

Suppose we have independent observations of success or failure. We can use MLE to conduct an inference on $p$. Since the MLEs do not have a closed form solution, we will try to solve using MCMC sampling by allowing for $\beta_0$ and $\beta_1$ to each have normal distribution priors. With the $R$ ratio and the jumping distribution, we implement a MCMC sampler to obtain posterior distributions for the parameters as well as the posterior statistics and their credible intervals. 

Finally, improve the MCMC algorithm and compare the burn-in (MCMC MH Bivariate Manner).

## Part 1 - Load and Summarize Data

The diabetes data set is taken from [Kaggle](https://www.kaggle.com/datasets/vikasukani/diabetes-data-set). With each person we also observe a number of covariates such as a blood glucose measure. 

## Part 2 - MCMC MH Algorithm and Implementation

Model the response Outcome by Glucose with a logistic linear regression model. carry out Markov Chain Monte Carlo (MCMC) Metropolis-Hastings algorithm in a univariate manner (search one parameter at a time).

## Part 3 - GLM - MLE Fit

Check our MCMC results with GLM fit.

## Part 4 - MCMC MH Bivariate Manner

With the assumption of the independence of the two parameters $\beta_0$ and $\beta_1$, we can improve the MCMC MH algorithm by performing the sampling process in bivariate manner. We can then compare the burn-in to see how much does it improve.