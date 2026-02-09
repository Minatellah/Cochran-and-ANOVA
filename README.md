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


