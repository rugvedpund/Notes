# MOND

# Introduction

Notes on MOND. Useful as a reference for studying MOND, etc.

## MOND

MOND is a modification of Newtonian gravity that explains the flat rotation curves of galaxies without the need for dark matter. It was first proposed by Milgrom in 1983 https://articles.adsabs.harvard.edu/pdf/1984ApJ...286....7B

Newton's force law in MOND is given by:

$$
\vec{F} = m\vec{a} \times \mu({}^{|\vec{a}|}{\mskip -5mu/\mskip -3mu}_{a_0})
$$

where $\mu(x)$ is an interpolating function that satisfies the following conditions:

$$
\begin{align}
\mu(x) &= 1 \quad \text{for} \quad x \gg 1 \\
\mu(x) &= x \quad \text{for} \quad x \ll 1 \\
\end{align}$$

The acceleration scale $a_0$ is given by:

$$
a_0 = 1.2 \times 10^{-10} \ \text{m/s}^2
$$
which seems arbitrary but is actually the acceleration scale of the universe relevant for galaxy rotation curves. This is the acceleration scale at which the MOND force law transitions from Newtonian to non-Newtonian.

Thus the gravitational force in MOND due to body of mass $M$ is given by:

$$
m\vec{a} \mu({}^{|\vec{a}|}{\mskip -5mu/\mskip -3mu}_{a_0}) = \frac{G m M}{r^2} \hat{r}
$$

This has a serious defect - the Newton's third law does not hold. The force law is not symmetric. 

$$
\mu({}^{|\vec{a}_1|}{\mskip -5mu/\mskip -3mu}_{a_0}) m_1 \vec{a}_1 \neq \mu({}^{|\vec{a}_2|}{\mskip -5mu/\mskip -3mu}_{a_0}) m_2 \vec{a}_2
$$
forcing $\mu(x)=1 \ \forall x$.

This can be rectified by deriving the force law from a modified Lagrangian. 

# AQUAL

AQUAL: A QUAdratic Lagrangian

The AQUAL Lagrangian is given by:

$$
L = \frac{1}{2} \int d^3x \ \left[ \rho \phi + \frac{1}{8\pi G} a_0^2 \ F\left( \frac{|\nabla \phi|^2}{a_0^2}\right) \right]
$$

where $\phi$ is the gravitational potential. The Euler-Lagrange equation for this Lagrangian is:

$$
\nabla \cdot \left( \mu(\frac{|\nabla\phi|}{a_0}) \ \nabla\phi \right) = 4\pi G \rho \quad \text{where} \quad \mu(x) = \frac{dF(x^2)}{dx}
$$
