+++
title = "Structured Correlation — Math & Geometry Test"
date = 2025-05-09T00:58:56+02:00
draft = false
+++


Inline math test: $E = mc^2$.

---

## Equicorrelation

If $n$ assets share the same pair‑wise correlation $p$,

$$
R(p)=
\begin{pmatrix}
1 & p & \dots & p\\
p & 1 & \dots & p\\
\vdots & & \ddots & \vdots\\
p & p & \dots & 1
\end{pmatrix}.
$$

Its eigenvalues satisfy

$$
\begin{aligned}
\lambda_1 &= 1 + (n-1)p,\\
\lambda_{2,\dots,n} &= 1 - p,
\end{aligned}
$$

so the matrix is positive‑definite **iff**

$$
-\frac{1}{n-1} \;<\; p \;<\; 1 .
$$

---

## One‑factor structure

Each standardized asset is written  

$$
X_i = \beta_i F + \varepsilon_i,
\qquad
\varepsilon_i \;\bot\; F,
\quad
\mathrm{Var}(F)=\mathrm{Var}(X_i)=1 .
$$

The resulting correlation matrix is

$$
\boxed{%
R = \beta \beta^{\!\top}
    + \operatorname{diag}\!\bigl(1-\beta_1^2,\dots,1-\beta_n^2\bigr)
}.
$$

* If at least one $|\beta_i|<1$ then $R$ is positive‑**definite**.  
* If every $|\beta_i|=1$ then $R$ collapses to rank 1 (only semidefinite).

---

## Quick comparison

| Feature | Equicorrelation | One‑factor |
|---------|-----------------|------------|
| Free parameters | 1 ($p$) | $n$ (loadings $\beta_i$) |
| PD range | $-\dfrac{1}{n-1}<p<1$ | some $|\beta_i|<1$ |
| Symmetry | full rotational | broken by factor axis |

---

### Multi‑line sanity check

$$
\begin{aligned}
w^{\top}Rw &=
  \bigl(\beta^{\top}w\bigr)^2
  + \sum_{i=1}^n (1-\beta_i^2)\,w_i^2 \\[6pt]
&> 0
\qquad\text{whenever } w\neq 0.
\end{aligned}
$$
