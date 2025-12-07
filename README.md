# Statistcal-inference
#The Journey of Statistical Inference: From Sample to Population

Statistical Inference: A Comprehensive Guide and Reference
Chapter 1: Foundations of Statistical Inference
This chapter introduces the core concepts, defining the scope and purpose of inference as a bridge between sample data and population knowledge.

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





