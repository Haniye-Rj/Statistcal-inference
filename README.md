# Statistcal-inference

Statistical Inference: A Comprehensive Guide and Reference

1.1 Defining Statistical Inference
Statistical inference is the branch of statistics built upon probability theory and distributions. It provides the methodology to draw robust conclusions about a larger population based on data collected from a limited sample.

1.2 The Two Pillars of Inference
Statistical inference is fundamentally divided into two major activities:

Parameter Estimation: Determining an unknown population characteristic (e.g., estimating the average income of a country).

Hypothesis Testing: Making a formal decision or judgment about a population parameter by evaluating competing claims.

Chapter 2: The Core of Decision-Making – Hypothesis Testing

This chapter details the standardized, step-by-step process of hypothesis testing, which is central to most statistical research.

2.1 The Hypothesis Framework
The process begins with defining two competing, mutually exclusive statements:

Null Hypothesis ($H_0$): The status quo. It typically states there is no effect, no difference, or no change. (e.g., $H_0: \mu_1 = \mu_2$).
Alternative Hypothesis ($H_1$): The research claim. It states there is a difference, an effect, or a change. (e.g., $H_1: \mu_1 \neq \mu_2$).

2.2 The Decision Criteria
The final decision hinges on comparing the evidence from the sample to a pre-defined risk threshold.

2.2.1 Significance Level ($\alpha$)
The Significance Level ($\alpha$) defines the maximum risk we are willing to take of making a Type I Error (rejecting a true $H_0$).
Common Choice: $\alpha = 0.05$ (5%).

2.2.2 The P-value
The p-value (Probability Value) is the probability of obtaining the observed sample data (or data more extreme) if the Null Hypothesis ($H_0$) were true. It measures the strength of the evidence against $H_0$.
Key Terms of Hypothesis Testing
Significance Level (α): How sure we want to be before saying the claim is false. Usually, we choose 0.05 (5%).
p-value: The chance of seeing the data if the null hypothesis is true. If this is less than α, we say the claim is probably false.
We compare the test statistic to a critical value from a statistical table or use the p-value:

Method,Rule,Conclusion
P-value,If p-value ≤α,REJECT H0​ (Sufficient evidence for H1​)
,If p-value >α,FAIL TO REJECT H0​ (Insufficient evidence for H1​)
Critical Value,If Test Statistic is in the Rejection Region,REJECT H0​
,If Test Statistic is not in the Rejection Region,FAIL TO REJECT H0​

1. Using Critical Value:

If test statistic > critical value → reject H0​.
If test statistic ≤ critical value → fail to reject H0​.
2. Using P-value:

If p-value ≤ α → reject H0​.
If p-value > α → fail to reject H0​.

One-sample t Test - parametric
DATA TYPE:
• One-sample data
• Data are interval/ratio & continuous
• Data are normally distributed (CENTRAL LIMIT THEOREM)
• Moderate skewness is permissible if the data distribution is unimodal without outliers

HYPOTHESIS:
H0: The mean is equal to the MU
H1 (2 sided): The mean is not equal to the MU

INTERPRETATION:
H0: Fail to reject that mean is not significantly different from MU
H1 (2 sided): Mean is significantly different from MU

Normality assumption:
• n>30 (rule of thumb) CLT holds and t test may be
performed
• fail to reject H0 about normality in normality
tests (Jarque-Bera; Shapiro-Wilk etc.) 

One-sample Wilcoxon Signed Rank Test
DATA TYPE:
• One-sample data
• Ordinal, interval, or ratio
• Relatively symmetrical about their median


Data does not have to be symmetric in distribution
Has smaller power than Wilcoxon one sample test
Procedure:
For each observation (from N) calculate difference from assumed ME:Xi − ME
Drop observations with absolute difference equal to 0 
Calculate sum of positive difference (S) and sum of negative difference (F).

What Is Analysis of Variance (ANOVA)?
Analysis of variance (ANOVA) is a statistical method for determining whether differences in group means are statistically significant or likely due to random variation.
A one-way ANOVA uses one independent variable. A two-way ANOVA uses two independent variables. Analysts use the ANOVA test to determine the influence of independent variables on the dependent variable in a regression study.
The independent variable should have at least three different groups or categories. ANOVA determines if the dependent variable changes according to the level of the independent variable. 

One-way data. (1 DEPVAR in 2 or more groups)
• Dependent variable is interval/ratio, and is continuous
• Independent variable is a factor with two or more levels.
• Residuals are normally distributed
• Groups have the same variance (homoscedasticity)
• Observations among groups are independent.
• Moderate deviation from normally-distributed residuals is permissible
HYPOTHESIS:
• H0: All means in all groups are equal.
• H1 (2-sided): Exist at least one mean which is different then the rest of means
<img width="597" height="376" alt="image" src="https://github.com/user-attachments/assets/3a5cd79c-b580-4d66-af9f-65a5edc5ee9c" />
Photo from: https://www.investopedia.com/terms/a/anova.asp

 Residual normality:
 Shapiro-Wilk
 Jarque-Bera etc.
 Variance equality:
 Bartlett’s test: Compare the variances of k samples, where k can be more 
than two samples. The data must be normally distributed. 
Levene’s test: Compare the variances of k samples, where k can be more 
than two samples. It’s an alternative to the Bartlett’s test that is less sensitive 
to departures from normality.
 Fligner-Killeen test: a non-parametric test which is very robust against 
departures from normality.


One-way ANOVA follow-up analysis

Statistical Inference — A Practical Guide

Statistical inference is the foundation of modern data analysis. It provides the tools to make conclusions about a population based on sample data. This document presents the essential concepts of inference, parameter estimation, and hypothesis testing in a clear, structured, and practical way.

## 1. Foundations of Statistical Inference
1.1 What Is Statistical Inference?

Statistical inference is the branch of statistics that uses probability theory to make conclusions about a population based on sample data.

It answers questions such as:

Is the population mean equal to a specific value?

Are two groups significantly different?

Does the independent variable affect the dependent variable?

1.2 The Two Pillars of Inference
1. Parameter Estimation

We estimate an unknown population parameter (e.g., a population mean μ or proportion p).

Examples:

Estimating average income

Estimating defect rate in products

2. Hypothesis Testing

A structured decision-making process used to assess claims about population parameters.

Examples:

Is μ₁ = μ₂?

Is the mean different from 10?

Are three group means equal?

## 2. Hypothesis Testing — The Core of Decision-Making

Hypothesis testing is a standardized framework that allows researchers to assess evidence from sample data.

2.1 Hypothesis Structure

In all statistical tests, we define two mutually exclusive statements:

Null Hypothesis (H₀)

Represents the “no effect”, “no difference”, or the status quo

Example:

𝐻
0
:
  
𝜇
1
=
𝜇
2
H
0
	​

:μ
1
	​

=μ
2
	​

Alternative Hypothesis (H₁)

Represents the presence of an effect or difference

Example:

𝐻
1
:
  
𝜇
1
≠
𝜇
2
H
1
	​

:μ
1
	​


=μ
2
	​

2.2 Decision Criteria

Decisions rely on two core components:

2.2.1 Significance Level (α)

The probability of making a Type I Error (rejecting a true H₀).

Common choices:

α = 0.05

α = 0.01

Interpretation:

α = 0.05 means a 5% acceptable risk of concluding there is an effect when there is none.

2.2.2 P-value

The p-value is the probability of observing your sample data (or more extreme) if the null hypothesis were true.

Interpretation rules:

Method	Rule	Conclusion
P-value	If p ≤ α	Reject H₀ (evidence supports H₁)
	If p > α	Fail to reject H₀
Critical Value	If test statistic is in rejection region	Reject H₀
	Otherwise	Fail to reject H₀
2.3 Using p-value vs Critical Value
Using Critical Value

If test statistic > critical value → Reject H₀

If test statistic ≤ critical value → Fail to reject H₀

Using p-value

If p ≤ α → evidence against H₀ → Reject

If p > α → not enough evidence → Fail to reject

## 3. One-Sample Tests
### 3.1 One-Sample t-Test (Parametric)
Data Requirements

One numeric sample

Interval/ratio scale

Data approximately normal

Moderate skew OK if no heavy outliers

CLT justifies normality if n > 30

Hypotheses
𝐻
0
:
𝜇
=
𝜇
0
H
0
	​

:μ=μ
0
	​

𝐻
1
:
  
𝜇
≠
𝜇
0
H
1
	​

:μ

=μ
0
	​

Interpretation

Fail to reject H₀ → sample mean is not significantly different from μ₀

Reject H₀ → sample mean is significantly different

Normality Checks

Shapiro–Wilk

Jarque–Bera

Visual: histogram, QQ plot

### 3.2 One-Sample Wilcoxon Signed Rank Test (Nonparametric)

Used when data do not meet t-test’s normality assumption.

Data Type

One sample

Ordinal, interval, or ratio

Symmetry around the median preferred

Procedure Summary

Compute differences: 
𝑋
𝑖
−
𝑀
𝐸
X
i
	​

−ME

Remove differences equal to zero

Rank absolute differences

Compute:

S = sum of positive ranks

F = sum of negative ranks

Test statistic = smaller of (S, F)

## 4. Analysis of Variance (ANOVA)

ANOVA assesses whether group means differ more than expected by chance.

4.1 What ANOVA Does

It tests whether differences among group means are statistically significant.

One-way ANOVA → One independent variable

Two-way ANOVA → Two independent variables

4.2 Data Requirements

Dependent variable: continuous (interval/ratio)

Independent variable: categorical with ≥ 2 groups

Groups independent

Residuals normally distributed

Equal variances (homoscedasticity)

4.3 Hypotheses
𝐻
0
:
  
𝜇
1
=
𝜇
2
=
⋯
=
𝜇
𝑘
H
0
	​

:μ
1
	​

=μ
2
	​

=⋯=μ
k
	​

𝐻
1
:
  
At least one mean differs
H
1
	​

:At least one mean differs
4.4 Assumption Checks
Normality of Residuals

Shapiro–Wilk

Jarque–Bera

Variance Equality Tests

Bartlett’s test (sensitive to non-normality)

Levene’s test (robust)

Fligner–Killeen test (non-parametric, very robust)

## 5. One-Way ANOVA Follow-Up Analysis

If ANOVA is significant, we conduct post-hoc comparisons to identify which groups differ.

Examples include:

Tukey HSD

Bonferroni

Scheffé
## 4. Analysis of Variance (ANOVA) – Extended

ANOVA assesses whether group means differ more than expected by chance. It generalizes the t-test to more than two groups and handles multiple independent variables.

4.1 One-Way ANOVA
Purpose

Test if the means of 3 or more independent groups differ.

Data Requirements

Dependent variable: interval/ratio, continuous

Independent variable: categorical, ≥ 2 groups

Residuals approximately normal

Homoscedasticity (equal variances)

Observations independent

Hypotheses
𝐻
0
:
𝜇
1
=
𝜇
2
=
⋯
=
𝜇
𝑘
H
0
	​

:μ
1
	​

=μ
2
	​

=⋯=μ
k
	​

𝐻
1
:
At least one mean differs
H
1
	​

:At least one mean differs
4.2 One-Way ANOVA With Blocks

Also called blocked ANOVA, used to control for non-independence or suspected variation from other factors.

Data

One measurement variable across 2+ groups, distributed among ≥2 blocks

Dependent variable: interval/ratio, continuous

Independent variable: categorical, ≥2 levels

Blocking variable: categorical, ≥2 levels

Residuals normal

Homoscedasticity

Observations independent

Hypotheses

Treatment effect:

𝐻
0
:
Group means equal
𝐻
1
:
At least one group mean differs
H
0
	​

:Group means equalH
1
	​

:At least one group mean differs

Block effect:

𝐻
0
:
Block means equal
H
0
	​

:Block means equal
Notes

Blocks account for variation unrelated to main treatments

Block effects may not be of primary interest

Helps mitigate violations of independence

4.3 One-Way ANOVA Types of Sums of Squares (SS)

When data are unbalanced, the calculation of sums of squares can differ:

Full model: SS(A, B, AB) includes factors A, B, and their interaction AB

Partial models: SS(A, B) excludes interaction; SS(B, AB) excludes factor A

Incremental sums of squares = difference between full and partial models

Type I: sequential; results depend on factor order

Type II: for models with no interaction; tests main effects controlling for other main effects

Type III: valid with interactions; tests main effects accounting for interactions

Note: With interactions present, interpreting main effects alone is less meaningful.

4.4 One-Way ANOVA With Random Blocks
Data

Same as one-way ANOVA with blocks

Blocking variable treated as random effect (random selection of block levels)

Hypotheses
𝐻
0
:
Group means equal
H
0
	​

:Group means equal
𝐻
1
:
At least one group mean differs
H
1
	​

:At least one group mean differs
Notes

Used when the analyst wants to account for block effects but is not interested in specific block levels

Example: Earnings vs Gender across 3 cities

4.5 Fixed, Random, and Mixed Effects Models
Type	Description	When to Use
Fixed effects	Parameters are non-random, predictable	Estimate effect of all levels in the population (e.g., males & females)
Random effects	Parameters are random variables	Account for random variation from a factor sampled from a population
Mixed effects	Combination of fixed and random	Handle repeated measures or hierarchical data; maintain independence assumptions
4.6 Repeated Measures ANOVA
Data

Same unit measured multiple times (time or conditions)

Dependent variable: interval/ratio, continuous

Independent variable: categorical

Residuals normal

Homoscedasticity

Moderate deviation from normality allowed

Hypotheses
𝐻
0
:
Means across time/conditions equal
H
0
	​

:Means across time/conditions equal
𝐻
1
:
At least one mean differs
H
1
	​

:At least one mean differs
Notes

Accounts for autocorrelation in repeated measures

Blocks (subjects) may be random to deal with non-independence

Often used in panel data with unit ID and time ID

4.7 Two-Way ANOVA (Factorial ANOVA)
Data

One dependent variable measured across two independent factors

Dependent variable: interval/ratio, continuous

Independent variables: categorical, ≥2 levels each

Residuals normal

Homoscedasticity

Observations independent (no repeated measures)

Hypotheses

Main effect A: means equal across levels of factor A

Main effect B: means equal across levels of factor B

Interaction effect: combined effect of A & B equal across levels

𝐻
0
:
All means equal
𝐻
1
:
At least one mean differs
H
0
	​

:All means equalH
1
	​

:At least one mean differs
Post-Hoc Analysis Rules

No significant effects: no post-hoc testing

Only main effects significant: post-hoc comparisons for significant main effects only

Interaction significant: post-hoc comparisons for interaction effect




