# PHY560 Final Paper Proposal - Rugved Pund

## The Averaging Problem in Cosmology and General Relativity

### Introduction

The field equations of General Relativity are the Einstein's equations:

$$ R_{\alpha\beta} -\frac{1}{2}g_{\alpha\beta} R = -\kappa T_{\alpha\beta} $$ (1)

where $R_{\alpha\beta}$ is the Ricci tensor, $g_{\alpha\beta}$ is the metric tensor, $R$ is the Ricci scalar, $\kappa = 8\pi G/c^4$ and $T_{\alpha\beta}$ is the stress-energy tensor. The equations of motion for matter and radiation are given by the $T^{\alpha\beta}_{;\beta}=0$ which follow from Einstein's equations.

In cosmology, the Universe is assumed to be isotropic and homogenous at large scales $\gtrsim 100$ Mpc, however it is very lumpy at smaller scales. Since the FLRW model relies on the cosmological principle, there is a question of justifying the large-scale smooth dynamics given the presence of small-scale inhomogenieties of the real lumpy universe.

In other words, in a mathematically perturbative sense, *does the inhomogenous universe evolve on average like a homogenous one?*

### The Averaging Problem

The problem with "averaging" equations of GR arises when one tries to define it before applying perturbative machinery. Some attempts with their one-line refutations are as follows[^1]:
[^1]: [Zakhmetdonovnotes](C:\Users\Rugved Pund\Notes\phy560\9703016.pdf)



1. **Covariant Volume Average**: Averaging over compact subspaces of a pseudo-Riemannian manifold is the obvious first candidate. However, this approach fails for the simple reason that volume-integration of tensors leads to objects that fail to transform as tensors. 
1. **Statistical/Ensemble Averages**: Another obvious candidate, defined by perhaps utilizing the ergodicity of GR dynamics. This fails because they require a curved lumpy space-time manifold to be split into space-like and time-like subspaces which cannot be accomplished generally.

General Relativity is a non-linear theory where, for some well-defined averaging operator $\braket{\cdot}$, in general the following is true:

$$ \braket{\left( R_{\alpha\beta} - \frac{1}{2} g_{\alpha\beta}R \right)} \neq \left( \braket{R_{\alpha\beta}} - \braket{\frac{1}{2} g_{\alpha\beta}R} \right) $$ (2)

One must split the product 
$$ \braket{g_{\alpha\beta}R} = \braket{g_{\alpha\beta}}\braket{R} + C(g_{\alpha\beta},R) $$ (3)

where $C(g_{\alpha\beta},R)$ is a *correlation* term. Averaging, thus, modifies the Einstein's equations by an effective correlation term. 



### Proposal

To further understand this problem, I propose the following steps:

1. Construct simple examples of FLRW universes with simple isolated lumps of various geometries to understand the correlation tensors.
1. 