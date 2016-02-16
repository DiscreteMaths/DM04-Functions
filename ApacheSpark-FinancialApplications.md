Apache Spark
=========
Financial Applications
----------
Spark facilitates the calculation of computationally-intensive statistics such as VaR via the Monte Carlo method.
It allows an individual to better understand the risk characteristics of large portfolios, enablig them to compute it before executing trades to help make informed and immediate decisions.
It aims to utilize VaR (Value at risk) in order to better understand the potnetial risks involved when dealing with these large scale portfolios.

VaR is a simple measure of an investment’s risk that tries to provide a reasonable estimate of maximum probable loss over a particular time period. A VaR calculation considers a given confidence level: a VaR of US$1 million with a 95% confidence level means that we believe our investment stands only a 5% chance of losing more than US$1 million over the time period.

A number of different methods are used to calculate VaR.

1. Variance-covariance
2. Historical simulation
3. Monte Carlo simulation

It is worth noting that the Monte Carlo method isn't perfect.  The models for generating trial conditions and for inferring instrument performance from them must make simplifying assumptions, and the distribution that comes out won’t be more accurate than these models going in.

