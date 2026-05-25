#  Statistical Inference: A Comprehensive Study Guide

Statistical inference is the process of drawing **robust conclusions** about a large **population** based on data collected from a limited **sample**. It is built upon the principles of probability and distributions.

## 1. Foundations of Statistical Inference

### 1.1 The Two Pillars of Inference

Statistical inference is fundamentally divided into two major activities:

1.  **Parameter Estimation:** Determining an unknown characteristic of the population (e.g., estimating the population mean $\mu$ or proportion $p$).
2.  **Hypothesis Testing:** A formal, structured decision-making process to evaluate competing claims about a population parameter.

---

## 2. Hypothesis Testing: The Core Decision-Making Framework

Hypothesis testing is a standardized, step-by-step process used to assess evidence from sample data.

### 2.1 The Hypothesis Framework

Every test starts with two mutually exclusive statements:

| Hypothesis | Description | Typical Form |
| :--- | :--- | :--- |
| **Null Hypothesis** ($H_0$) | The **status quo**. States there is **no effect, no difference, or no change**. | $H_0: \mu_1 = \mu_2$ or $H_0: \mu = \mu_0$ |
| **Alternative Hypothesis** ($H_1$) | The **research claim**. States there is a difference, an effect, or a change. | $H_1: \mu_1 \neq \mu_2$ or $H_1: \mu \neq \mu_0$ |

### 2.2 Decision Criteria and Interpretation

The final decision is made by comparing the sample evidence against a pre-defined risk threshold.

#### A. Significance Level ($\alpha$)
The **Significance Level ($\alpha$)** defines the maximum probability we are willing to accept of making a **Type I Error** (rejecting a true $H_0$).

* **Common Choice:** $\alpha = 0.05$ (5%).
* **Interpretation:** A 5% $\alpha$ means we accept a 5% risk of concluding there is an effect when, in reality, there is none.

#### B. The P-value
The **p-value (Probability Value)** is the probability of obtaining the observed sample data (or data more extreme) *if the Null Hypothesis ($H_0$) were true*. It measures the strength of evidence *against* $H_0$.

| Method | Rule | Conclusion |
| :--- | :--- | :--- |
| **P-value** | If $p \text{-value} \le \alpha$ | **REJECT $H_0$** (Sufficient evidence for $H_1$) |
| | If $p \text{-value} > \alpha$ | **FAIL TO REJECT $H_0$** (Insufficient evidence for $H_1$) |
| **Critical Value** | If Test Statistic is in the Rejection Region | **REJECT $H_0$** |
| | If Test Statistic is not in the Rejection Region | **FAIL TO REJECT $H_0$** |

---

## 3. One-Sample Tests

These tests are used to compare a single sample's characteristic (mean or median) to a known or hypothesized population value ($\mu_0$).

### 3.1 One-Sample **t-Test** (Parametric)

| Category | Details |
| :--- | :--- |
| **Data Requirements** | One numeric sample, Interval/ratio scale. Data should be **approximately normally distributed** (or $n > 30$ due to the **Central Limit Theorem (CLT)**). |
| **Hypotheses** | $H_0: \mu = \mu_0$ vs. $H_1: \mu \neq \mu_0$ (two-sided) |
| **Interpretation** | **Reject $H_0$**: The sample mean is significantly different from $\mu_0$. |
| **Normality Checks** | Shapiro–Wilk test, Jarque–Bera test, or visual checks (histogram, QQ plot). |

### 3.2 One-Sample **Wilcoxon Signed Rank Test** (Nonparametric)

Used when data **do not meet the t-test's normality assumption**.

| Category | Details |
| :--- | :--- |
| **Test Type** | Nonparametric Test (tests the median). |
| **Data Type** | One sample, Ordinal, interval, or ratio scale. Requires symmetry around the median. |
| **Procedure Summary** | Based on summing the ranks of absolute differences between each observation and the hypothesized median ($X_i - ME$). |

---

## 4. Analysis of Variance (ANOVA)

**ANOVA** is a statistical method for determining whether the differences in **group means** are statistically significant. It is used when comparing **three or more groups**.

### 4.1 One-Way ANOVA

| Category | Details |
| :--- | :--- |
| **Purpose** | To test if the means of **3 or more independent groups** differ. |
| **Data Requirements** | **Dependent Variable:** Continuous (interval/ratio). **Independent Variable (Factor):** Categorical with $\ge 2$ levels. |
| **Assumptions** | **Residuals** are normally distributed. **Homoscedasticity** (Groups have equal variances). Observations are independent. |
| **Hypotheses** | $H_0: \mu_1 = \mu_2 = \cdots = \mu_k$ (All group means are equal). $H_1$: At least one mean is different. |

### 4.2 ANOVA Assumptions and Checks

| Assumption | Test | Notes |
| :--- | :--- | :--- |
| **Normality** | Shapiro–Wilk, Jarque–Bera | Checks if the residuals follow a normal distribution. |
| **Variance Equality** (Homoscedasticity) | **Bartlett’s test** (sensitive to non-normality). **Levene’s test** (more robust). **Fligner–Killeen test** (non-parametric, very robust). | Checks if the variances across all groups are equal. |

### 4.3 ANOVA Extensions and Post-Hoc Analysis

* **Two-Way ANOVA:** Uses **two independent variables** (factors) to test for main effects and an **interaction effect**.
* **Repeated Measures ANOVA:** Used when the **same unit/subject** is measured multiple times (accounts for non-independence).
* **Post-Hoc Analysis:** If the overall ANOVA is significant, post-hoc tests (e.g., **Tukey HSD, Bonferroni**) are used to determine *which specific pairs* of groups are significantly different.

---

## 5. Advanced ANOVA Design Considerations (Unbalanced Data)

When sample sizes are unequal (unbalanced designs), the method for calculating the **Sum of Squares (SS)** affects the results.

### 5.1 Types of Sums of Squares (SS)

| Type | Calculation Method | Use Case |
| :--- | :--- | :--- |
| **Type I (Sequential)** | SS for Factor A is calculated first, then SS for Factor B adjusted for A, then SS for Interaction adjusted for A and B. | Results depend on the **order** factors are entered; rarely recommended for unbalanced data. |
| **Type II** | Tests the main effects, controlling for other main effects, but **ignores interaction effects**. | Recommended for models where the interaction is specifically removed or assumed to be zero. |
| **Type III** | Tests the effect of a factor controlling for all other factors in the model, **including interactions**. | **Most common approach** and valid for models that include interaction terms. |

### 5.2 Blocked Designs

| Design Type | Description | Effect of Interest |
| :--- | :--- | :--- |
| **One-Way ANOVA with Blocks** | Data is grouped by a **Blocking Variable** (often a factor known to cause variation, but not the main focus). | Accounts for variation from the block; primarily interested in the **Fixed Treatment Effect**. |
| **Random Blocks** | The levels of the blocking variable are treated as a **Random Effect** (sampled from a population). | Accounts for random block variation; primarily interested in the **Fixed Treatment Effect**. |

### 5.3 Fixed, Random, and Mixed Effects Models

| Type | Description | When to Use |
| :--- | :--- | :--- |
| **Fixed Effects** | Parameters are non-random, predictable. | Estimate the effect of *all* levels of interest in the population. |
| **Random Effects** | Parameters are random variables. | Account for random variation from a factor whose levels were *sampled* from a larger population. |
| **Mixed Effects** | Combination of fixed and random factors. | Handle complex data structures like repeated measures or hierarchical (nested) data. |
