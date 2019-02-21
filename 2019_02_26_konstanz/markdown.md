class: title-slide

# Robust coarse spaces for the boundary element method

### Xavier Claeys, .underline[Pierre Marchand], Frédéric Nataf

26 February 2019 - University of Konstanz

### .font50[Team-project Alpines, Inria and Laboratoire J.-L. Lions, Sorbonne Université]

---

# Overview

## Boundary Integral Equation (BIE)

- Reformulation on $\partial \Omega$ using its fundamental solution
- Non-local integral operators
- Full matrices using Galerkin approximation

---

# Overview

## Domain Decomposition Methods (DDM)

- Schwarz method used as preconditioner
- GenEO (Generalized Eigenproblems in the Overlap)

---

# Overview

## Some practical difficulties

- Compression ($\mathcal{H}$-matrices, Fast multipole method...)
- Parallelism and vectorisation (MPI, OpenMP)

--

.center[$\implies$ *Htool library by P.-H. Tournier and P.M. (available on [GitHub](https://github.com/PierreMarchand20/htool)* <i class="fab fa-github" style="color:#4C4B4C"></i>)]

---

# Function spaces

## Notations

- $\Omega \subset \bbR^2$ or $\bbR^3$ a Lipschitz domain
- $\Gamma\subseteq \partial \Omega$
- Defining $H^s(\partial \Omega)$ using local maps $s\in (0,1)$,

$$
    \begin{aligned}
    H^s(\Gamma)&:= \\{ u\lvert_{\Gamma} \, \lvert \,  u \in H^s(\partial \Omega) \\}, \\\
    \wH^s(\Gamma)&:= \\{ u \in H^s(\partial \Omega) \, \lvert \,  \operatorname{supp}(u) \subset \overline{\Gamma} \\}.
    \end{aligned}
$$

--

> **Remarks**:
>
> - $\wH^1(\Gamma)=H^1\_0(\Gamma)$ but $\wH^{1/2}(\Gamma)=H\_{00}^{1/2}(\Gamma)$,
> - If $\Gamma=\partial \Omega$ ($\partial \Gamma = \emptyset$), then $H^s(\Gamma)=\wH^s(\Gamma)$ for $\lvert s \lvert \leq 1$,
> - $\wH^s(\Gamma)=H^s(\Gamma)$ for $0\leq s <1/2$;

---

# Model problem

$$
\left\\{
    \begin{aligned}
    &L(u) = 0 \quad \text{ in }\Omega \subset \bbR^d \\\
    &+\text{ condition at infinity if }\Omega\text{ is an exterior domain}
    \end{aligned}
\right.
$$
where $L$ is a general linear, elliptic differential operator with constant coefficient and $d=2$ or $3$.

Fundamental solution
$$
L(G)= \delta_0\text{ in }\bbR^d
$$

--

> **Example**: Laplacian in $\bbR^d$
> $$
> G(\bfx):=\dfrac{1}{4\pi \lVert \bfx\rVert}
> $$

---

# Surface potentials

## Single and double layer potential

$$
    \begin{aligned}
    &\operatorname{SL}(q)(\bfx):=\int\_{\Gamma} G(\bfx-\bfy)q(\bfy) \diff \sigma(\bfy),\\\
    &\operatorname{DL}(v)(\bfx):=\int\_{\Gamma} \bfn(\bfy)\cdot (\nabla G)(\bfx-\bfy)v(\bfy) \diff \sigma(\bfy),
    \end{aligned}
$$