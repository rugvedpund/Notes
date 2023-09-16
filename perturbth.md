# Cosmological Perturbation Theory

16 Sep 23

Based on the less known lecture series here: 

- Lecture 1: https://youtu.be/FHgTfrAzCdw?si=fTLunxwns2JlZh00

## Introduction

First we classify perturbations for any 2-tensor quantity
$$X_{\mu\nu} = X_{\mu\nu} + \delta X_{\mu\nu}$$
have 10 degrees of freedom. Most relevant for cosmology by Bardeen (1980) - decomposition to Scalar+Vector+Tensor. These remain decoupled from one another at the first-order perturbation theory.

> So second order and onwards, vector perturbations can couple to scalar? So galaxy rotation can be explained by the scalar effect of vector and dark energy by scalar effect of tensors?

Since this follows from $ SO(3) $ invarianc of the background FRWL metric. We will keep thining of scalars, vectors and tensors in terms of their $ SO(#3) $ transformation properties.  _what happens when no longer manifest $ SO(3) $  breaks?_

- If in vacuum, then easily show fom EFE that scalars and vectors vanish. Only tensors do not vanish, but propagate with second-order equations. Only physical modes. Other modes are just response to matter-stress. 

- In the presence of matter, vector perturbations show how the metric reacts to vorticity of matter-stress. Scalars show the metric reacts to irrotational stress.

In the given limit, scalar perturbations are generalization of newtonian potential. In usual conditions, vector perturbations go to zero. Need to work very hard physically to get these at observational levels.

** For $ g_{\mu\nu} $ **

- $ g_{00} \implies \Psi$ 
- $ g_{ii} \implies \partial_i a(t)$ distortion of $ a(t) $, called $ \Phi $ that is a bit late in this direction
- $ \delta g_{0i} \implies \partial_i b $ gradient of some scalar function
- $ \delta g_{ij} = \left( \partial_i \partial_j - fr \Delta \delta_{ij} \right)\mu $ for some scalar function $ \mu $, and traceless requires the $ \delta_{ij} $ 

** For $ T_{\mu\nu} $ **

- $ T_{00} \implies \delta\rho $ density perturbation made dimensionless by $ \delta\rho \equiv \bar{\rho} \delta $ 
- $ T_{ii} = \delta p$ presssure part 
- $ T_{0i} = \partial_i v $ irrotational energy flux. Taking the divergence of $ \partial_i T^0_i = \Delta v \equiv \Theta (\bar{\rho}) $ called vector divergence perturbation. 
- $ T_{ij} = \left( \partial_i\partial_j - 1/3\Delta\delta_{ij} \right) s $ anisotropic stress. $ \left( \partial_i\partial_j - 1/3 \Delta\delta_{ij} \right) T^i_j = \Delta\Delta s \equiv \sigma (\bar{\rho} + \bar{p}) $ where $ \sigma $ is called the anistropic stress perturbation. but this is slightly a misnomer. 

## Gauges

Need to define equal-time hypersurfaces. No ambiguity in homogenous universe. This is not the case as soon as there are inhomogenieties. There are many surfaces where the perturbations are still linear. 

From $ \delta\rho(t,x) = \rho(t,x) - \bar{\rho}(t_{\text{surface}}) $ where $ \bar{\rho} $ is the non-local quantity dependent on choice of the hyper-surface. This is where we have gauge freedom. 4 degrees of freedom = 2 scalar + 2 vector. This can be seen via $ x_\mu \mapsto x_\mu + \epsilon_\mu $ with the scalars being $ \epsilon_0, \partial_i\epsilon^i $ and the other two are vectors. 

Two approaches to solve.

1. Only use gauge-invariant quantities. e.g. Bardeen potentials $ \Phi_A, \Phi_H $ 
1. Fix gauge = choice of unique time-slicing. Get gauge-independent results. Subtle sicne the time-slice must remain unique. 

We will use Newtonian/longitudinal gauge. $$ds^2 = -(1+2\Psi)dt^2 - (1-2\Phi)a^2(t)\vec{dl}^2$$ where $ dl^2 = dr^2 $ or the more complicated $ dr^2/\sqrt{1+kr^2} $ 

or after a conformal transformation $$a^(\eta) [-(1+2\Psi)d\eta^2 + (1-2\Phi)dl^2$$ where conformal time $ d\eta=dt/a $. Notation will be $ '\equiv \partial/\partial\eta $ and $ \cdot\equiv\partial/\partial_t $ . Hubble is $ H\equiv \dot{a}/a=a'/a^2 $  

First thing that determines the evolution of perturbations is whether it is larger or smaller than the Hubble scale $ \lambda=R_H $. It is one of the two quantities of dimension space from FRWL. Spatial curvature and Hubble radius that is the radius of curvature wrt time. Now work in Fourier space $$\frac{2\pi}{k}a(t)= \frac{1}{H} \implies k\sim \frac{a'}{a}$$  

In Newtonian gauge, practical advantage. Any results obtained with $ \Phi_A,\Phi_H = \Phi, \Psi $. Shortcut, basically. Only need 2 illuminating EFEs.

1. Shear component: $a^{-2}k^2(\Phi-\Psi)= 12 \pi G \ \sum_i (\bar{\rho}_i + \bar{p}_i) \sigma_i$ where $ i $ sums over all the fluids. Usually we will deal with fluids with no anisotropic stress. Gives $ \Phi=\Psi $.
1. $ 00 $-component: $ a^{-2} \left( k^2\phi + 3 \frac{a'}{a} \left( \phi' + \frac{a'}{a}\Psi \right) \right) = 4\pi G \ \delta\rho_{\text{tot}} \implies \lim_{\lambda\gg\frac{a'}{a},k\gg \frac{a}{a}} \frac{-k^2}{a^2}\Phi = 4\pi G\delta\rho_{\text{tot}}  $. Poisson equation $ \frac{\Delta}{a^2}\Phi $ . Difference with usual is the laplacian with $ a^2 $ factor because we are working in comoving space. Also, $ \Phi=\Psi $ relates the usual gravitational potential in the metric explaining why Poisson works here physically.

## Equations of Motion

From strongly coupled to very weakly/decoupled species. Baryons strongly couples. Neutrinos, CDM decoupled. Photons will go from strongly coupled to weakly coupled. 

Any equation of motion must be compatible with Bianchi identities. $ D_\mu T^\mu_\nu =0 $. 4 equations. 

- $ \mu=0 $ : conservation $ \delta' = \ldots $ 
- another scalar equation for irrotational part $ \Theta'=\ldots $ : Euler
- 2 vectors

For individual species that are coupled, $ D_\mu T^\mu_{a\nu} = C_{a\nu} $ such that $ \sum_a C_{a\nu} =0 $ 

2 equations, 4 variables $ \delta, \delta p, \Theta, \sigma $. Over constrained? Fine for perfect fluid since:
- $ \sigma\neq0 $ : only for anisotropic pressure or different flows of matter. 
- $ \delta p = c_s^2\delta\rho $ 

For weakly coupled fluids, we need to introduce the phase-space distribution and use the Boltzmann equation.

$$\frac{d}{d\eta}f_a = c[f_a,f_b,\ldots]$$ 
where $f_a(t,x) = f_a(t) + \delta f_a(t,x) $. In principle applies for CDM, but CDM is actually cold.

CDM: particles decouple when they are non-rel. Then their $ f_a $ is a very thin layer in phase space.


This is effectively like having a single flow of matter. The velocity at any given point $ v_{\text{bulk}} = v_{\text{cdm}} $ and $ \delta p \sim \delta v^2 \sim 0 $ so CDM has no pressure. This is equivalent to a perfect fluid with $ c_s^2=0 $. True for linear perturbations. For second order and higher, then the phase space folds on itself, giving anisotropic pressure.

## Inital Conditions

Famous adiabatic initial conditions. Hubble crossing when $ k\sim aH $. We fix initial conditions in the super-Hubble regime where $ k\ll aH$. Many possible and allowed. A very small set is likely for our universe.

In super-Hubble limit, from first principles $ \delta T^\mu_\nu $ must be diagonal. Physics outside the horizon is similar to backgrund evolution. In orders of $ \frac{k}{aH} $ 
$$\delta {T^\mu_\nu}^{(0)} = 
\begin{pmatrix}
  \delta\rho&&&\\&-p&&\\&&-p&\\&&&-p
\end{pmatrix}\\
$$
from homogeneity and isotropy. 

Similarly, at order 1 we get dependence on $ \Theta $. at order 2 we get dependence on $ \sigma $. This followed from the number of derivatives appearing in each perturbation. So in super-horizon fluctuations, $ \sigma,\Theta $ fluctuations are suppressed. So we start with N fluids with known sound speeds $ \frac{\delta p_a}{\delta \rho_a} - c_s^2 $. So the set of starting conditions is just the density perturbations of each fluid.

Among the set of initial conditions $ \{ \delta_a \} $ one subset is special. Let us start with homogenous universe $ \bar{\rho},\bar{p} $. Assume: 
$$\rho_a(t,x) = \bar{\rho}(t+\delta t(x)) = \bar{\rho}(t) + \dot{\bar{\rho}}\delta t \\
p_a(t,x) = \bar{p}(t+\delta t(x)) = \bar{p}(t) + \dot{\rho{p}}\delta t $$ 
This is a very interesting choice. This means that the density at any point is related to the average density a linear peturbation away in time. All quantities are perturbed because we shift time. $ \delta t(x) $ is the same for all fluids. This follows when perturbations are sourced by a single degree of freedom and plays the role of a clock. This gives a lot of non-trivial results. 

Computing $ \delta t $ : 
$$\delta t(x) = \frac{\delta \rho_a}{\dot{\bar{\rho_a}}} \\
-3 \frac{a'}{a} \delta t = \frac{\delta \rho_a}{(\bar{\rho_a} + \bar{p_a})}, \forall a$$ 

For all species $ \forall a,b $ 
$$\frac{\delta \rho_a}{\bar{\rho_a} + \bar{p_a}}$$ 