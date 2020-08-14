Analysis of Variance (ANOVA)
============================

Disclaimer: this is just an study repository. I was interested in how to perform ANOVA using the matricial approach, for this I tried to replicate some examples from a class material I've attended in August,2020.


### Completely Randomized Design (CRD) ###

In a CRD every experimental unit has the same random chance of being attributed to a particular treatment. The idea of *randomization* was introduced by Fisher in 1926 [^1] :

[^1]: Dean, A., Morris, M., Stufken, J., & Bingham, D. (Eds.). (2015). Handbook of design and analysis of experiments (Vol. 7). CRC Press.

>"One way of making sure that a valid estimate of error will be obtained is to arrange the plots deliberately at random, so that no distinction can creep in between pairs of plots treated alike and pairs treated differently; in such a case an estimate of error, derived in the usual way from the variations of plots treated alike, may be applied to test the significance of the observed difference between the averages of plots treated differently"

The ANOVA method, also proposed by Fisher, allow us to decompose the total variation observed in the experiment in two components, the variation due to the effects of treatments, and the random residual variation. In order to perform an ANOVA, three assumptions must be met by our experimental data residual variation:

1. **Errors must be independant.** This implies in independance of treatment effects.
2. **Variance of the errors must be homogenious.**
3. **Errors must follow a normal distribution of probabilities.**

If any of those assumptions fail, a non-parametric test must be consider instead.

### The observational equation in matrix form ###


Let's consider the following experiment:

|Treatments|Replicates|Treatments Total|
|:----------:|----------|:----------------:|
|1           |$ Y_{11} \ Y_{12} \ Y_{13} \ Y_{14}$|T1|
|2           |$ Y_{21} \ Y_{22} \ Y_{23} \ Y_{24}$|T2|
|3           |$ Y_{31} \ Y_{32} \ Y_{33} \ Y_{34}$|T3|

The observational equation can be writen as:

$$ y = X\beta + \varepsilon $$

where $y$ is the vector of observations; $X$ the coefficient matrix; $\beta$ is the matrix of parameters, and $\varepsilon$ is the vector of residuals.