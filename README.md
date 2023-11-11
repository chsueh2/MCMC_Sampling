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

Suppose we have independent observations of success or failure. We can use MLE to conduct an inference on $p$. Since the MLEs do not have a closed form solution, we will try to solve using MCMC sampling by allowing for $\beta_0$ and $\beta_1$ to each have normal distribution priors. With the $R$ ratio and the jumping distribution, we implement a MCMC sampler to obtain posterior distributions for the parameters as well as the posterior statistics and their credible intervals. 

Finally, Improve the MCMC algorithm and compare the burn-in used (MCMC MH Bivariate Manner).

## Part 1 - Load and Summarize Data

The diabetes data set is taken from [Kaggle](https://www.kaggle.com/datasets/vikasukani/diabetes-data-set). With each person we also observe a number of covariates such as a blood glucose measure. 

## Part 2 - MCMC MH Algorithm and Implementation

Model the response Outcome by Glucose with a logistic linear regression model. carry out Markov Chain Monte Carlo (MCMC) Metropolis-Hastings algorithm in a univariate manner (search one parameter at a time).

## Part 3 - GLM - MLE fit

Compare our MCMC results with GLM fit.

## Part 4 - MCMC MH Bivariate Manner

With the assumption of the independence of the two parameters $\beta_0$ and $\beta_1$, we can improve the MCMC MH algorithm by performing the sampling process in bivariate manner. We can then compare the burn-in used to see how much does it improve.