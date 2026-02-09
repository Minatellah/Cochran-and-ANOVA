# Cochran’s Theorem — ANOVA test

##  Overview

This repository contains a self-contained proof of **Cochran’s theorem**, with an emphasis on the **geometric and statistical interpretation** of quadratic forms, orthogonal projections, and degrees of freedom.

The objective is not only to present the classical result, but also to clarify the deep connection between **linear algebra and statistics**, particularly in the context of **one-way ANOVA**.

---

## Objectives

- Provide a rigorous proof of Cochran’s theorem  
- Explain the role of:
  - symmetric idempotent matrices  
  - orthogonal projections  
  - quadratic forms of Gaussian vectors  
- Give a geometric intuition for:
  - independence of sums of squares  
  - degrees of freedom  
- Highlight the link with one-way ANOVA  

---

##  Mathematical Setting

Let  

Z ~ Nₙ(0, σ² Iₙ)

Let A₁, …, Aₛ be symmetric idempotent matrices such that:

∑ₖ Aₖ = Iₙ  
Aₖ Aₗ = 0  for k ≠ l  

Define the quadratic forms:

Qₖ = Zᵀ Aₖ Z  

Cochran’s theorem characterizes the **distribution, independence, and degrees of freedom** of these quadratic forms.

---

##  Key Ideas

- Quadratic forms arise as **squared norms of projections** of a Gaussian vector  
- Orthogonality of subspaces explains **independence**  
- Degrees of freedom correspond to the **dimension (rank)** of each projection  
- The total sum of squares decomposes into orthogonal components  

Geometrically:

> The data vector lives in an n-dimensional space, and Cochran’s theorem decomposes it into orthogonal subspaces; each quadratic form measures the squared length of the projection onto one subspace.

---

##  Link with ANOVA

Cochran’s theorem provides the theoretical foundation of **one-way ANOVA** by explaining:

- why sums of squares are independent  
- why they follow chi-squared distributions  
- why their degrees of freedom add up correctly  
- why the F-statistic follows an F distribution

## ANOVA test in R
# ANOVA on Life Expectancy by Continent

This repository showcases a **self-driven statistical analysis** using the Gapminder dataset. It is part of my personal projects aimed at **strengthening my skills in Statistics, Econometrics, and Data Analysis** in preparation for advanced studies in **Statistics and Artificial Intelligence**.

## Project Overview

The goal of this project is to **investigate whether life expectancy differs between continents** (Europe, Americas, Asia) using **ANOVA (Analysis of Variance)** and the **Tukey post-hoc test**.  

Key steps include:

1. **Exploratory Data Analysis (EDA):**
   - Boxplots and density plots show the distribution of life expectancy across continents.
   - Observations:
     - Europe has the highest and most homogeneous life expectancy.
     - Americas have intermediate life expectancy with moderate dispersion.
     - Asia shows high variability, possibly reflecting differences between developed and developing countries.
     - Presence of outliers in Asia and Americas.

2. **Projection and Cochran’s Theorem:**
   - Life expectancy data is projected onto the subspace defined by continent indicators.
   - Residuals are orthogonal to the projected space, centered around 0.
   - According to **Cochran’s theorem**, sums of squares of projections and residuals follow independent chi-square distributions, justifying the use of the **F-test** in ANOVA.

3. **ANOVA Testing:**
   - Null hypothesis (H0): All continent means are equal.
   - Alternative hypothesis (H1): At least one mean differs.
   - Result: F-test indicates statistically significant differences (p-value = 0.0034), confirming that not all continent means are equal.

4. **Tukey Post-Hoc Test:**
   - Determines exactly which continents differ.
   - Findings:
     - Europe differs significantly from Asia and Americas.
     - No significant difference between Asia and Americas, confirmed by confidence intervals and p-values.

## Model Diagnostics

To validate the assumptions of the linear model underlying the ANOVA, diagnostic plots were generated:

- **Residuals vs Fitted**: Checks for non-linearity and heteroscedasticity.  
- **Q-Q plot**: Evaluates normality of residuals.  
- **Scale-Location plot**: Assesses homoscedasticity.  
- **Residuals vs Leverage**: Identifies influential points using Cook’s distance.

The plots indicate that the residuals are approximately centered around zero and reasonably homoscedastic, supporting the use of ANOVA for this analysis.

<img width="1155" height="713" alt="image" src="https://github.com/user-attachments/assets/f1cc30ee-f0d6-4772-bce3-549cf3d7c121" />


## Learning Outcomes

- Applied theoretical concepts such as **Cochran’s theorem** to justify ANOVA.
- Conducted **hypothesis testing** and **post-hoc analysis**.
- Practiced **data visualization** and interpretation of statistical results.
- Developed a structured approach to documenting and analyzing data, reinforcing my understanding of both **theory and practice** in statistics.




