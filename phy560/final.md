<!-- # PHY560 Final Paper Proposal - Rugved Pund -->

# The Averaging Problem and Backreaction Effects in General Relativity and Cosmology

This proposal is based broadly on the excellent review of this topic by Ellis(2005)[1]. 

## Non-commutativity of Einstein's Field Equations and Averaging

The central issue is that any conventional averaging of the geometrical quantities does not commute with Einstein's equations at the different scales. For example,

**EFE**: Calculating the Einstein tensor $G_{1ab}\equiv R_{1ab}-\frac{1}{2}R_1g_{1ab}$ from a metric tensor $g_{1ab}$ at a length scale $l_1$ and determining the quantity $E(g_{1ab})\equiv G_{1ab} - \kappa T_{1ab}$ where $T_{1ab}$ is the stress-energy tensor at the same scale $l_1$.

**Avg**: Averaging the metric tensor $g_{1ab} \rightarrow g_{2ab}$ to get a smoothed metric tensor $g_{2ab}$ and the corresponding matter tensor $T_{1ab} \rightarrow T_{2ab}$ at the larger length scale $l_2 \gg l_1$ via a suitable averaging function $\braket{\cdot}: X_{ab} \mapsto \braket{X_{ab}}$

These procedures can be shown to not commute from at least two different perspectives:

1. Averaging does not commute with scalar derivatives: $$\partial_i\braket{g}\neq\braket{\partial_ig}$$
1. The averaged inverse metric $g^{2ab}$, that depends non-linearly on the tensor components of $g_{1ab}$ is not the averaged version of $g^{1ab}$: $$ \braket{g^{1ab}}\neq g^{2ab}$$
    - This implies that the resulting Christoffel symbols $\Gamma^{a}_{2ab}\neq\braket{\Gamma^{a}_{1ab}}$
    - And hence the Ricci components $R_{2ab}\neq\braket{R_{1ab}}$
    - And finally, more non-linearities in calculating the Einstein tensor occur when calculating $G_{2ab}=R_{2ab}-\frac{1}{2}R_2g_{2ab}$.

Thus, if you smooth first and calculate the Einstein equations you fail to account for several non-linear terms in the process than if you calculate the Einstein equations first and then smooth: $$E\left(\braket{g_{1ab}}\right) \neq \braket{E(g_{1ab})}$$

## Cosmological Backreaction

One immediate consequence of this issue is the so-called backreaction of perturbations in cosmology. We are mostly interested in averages of scalar quantities like the density perturbations, rate of expansion, etc. in order to find the best-fit cosmological parameters for an inhomogenous universe model. The averaging of Einstein's Field Equations then leads to the presence of an extra term: $$ G_{ab} = T_{ab} + \Lambda g_{ab} \rightarrow \braket{G_{ab}} + \delta E_{ab} = \braket{T_{ab}} + \Lambda \braket{g_{ab}}$$
where $\delta E_{ab}$ is the backreaction term that can be looked at as a correction to the stress-energy tensor $\braket{T_{ab}}$ on the right or as a geometric correct to the Einstein tensor $\braket{G_{ab}}$ on the left. Such terms, due to their non-linear dependence on the perturbations, are difficult to control. 

### Example with Gravitational Waves:
A direct example of this appears in the calculation by Isaacson [2] for gravitational waves where a vacuum space-time with a rapidly varying gravitational wave appears to have an effective matter content when viewed on larger scales. For a a slowly varying background metric superimposed with high-frequency waves $$g_{\mu\nu} = \gamma_{\mu\nu} + \epsilon h_{\mu\nu}, \ \partial\gamma\sim\gamma/L, \ \partial h\sim h/\lambda$$ where $\lambda\ll L$, the Ricci tensor can be expanded as $$R_{\mu\nu}(\gamma+h) = R^{(0)}_{\mu\nu}(\gamma) + \epsilon R^{(1)}_{\mu\nu} + \epsilon^2 R^{(2)}_{\mu\nu} + \epsilon^3 R^{(3+)}_{\mu\nu}$$ Thus, if the actual space-time is empty i.e. $R_{\mu\nu}=0$, then the background metric is not that of empty space $R^{(0)}_{\mu\nu}\neq 0$, but can be shown to satisfy $$ R^{(0)}_{\mu\nu} - \frac{1}{2}R^{(0)}\gamma_{\mu\nu} = -8\pi T^{\text{eff}}_{\mu\nu} \\ T^{\text{eff}}_{\mu\nu} = \frac{\epsilon^2}{8\pi}\left( R^{(2)}_{\mu\nu} - \frac{1}{2}R^{(2)}\gamma_{\mu\nu} \right)$$ which is the backreaction from the small-scale structure to the large-scale structure.

## Proposal

### Goals:

1. Overview of current literature for the cosmological backreaction of small perturbations in FLRW universe. The current leading ideas seem to be from Buchert(2008) [3] and Zaletdinov (1997) [4]
2. Construct and attempt to solve for backreaction in a Toy Model of an empty Euclidean universe with a scalar lump at the origin
3. Construct and attempt to solve for backreaction in an empty FLRW universe with a scalar lump at the origin.


## References

[1] Ellis, G. F. R., and T. Buchert. “The Universe Seen at Different Scales.” Physics Letters A 347, no. 1–3 (November 2005): 38–46. https://doi.org/10.1016/j.physleta.2005.06.087.

[2] Isaacson, Richard A. “Gravitational Radiation in the Limit of High Frequency. II. Nonlinear Terms and the Effective Stress Tensor.” Physical Review 166, no. 5 (February 25, 1968): 1272–80. https://doi.org/10.1103/PhysRev.166.1272.

[3] Buchert, Thomas. “Dark Energy from Structure: A Status Report.” General Relativity and Gravitation 40, no. 2–3 (February 2008): 467–527. https://doi.org/10.1007/s10714-007-0554-8.

[4] Zalaletdinov, Roustam M. “Averaging Problem in General Relativity, Macroscopic Gravity and Using Einstein’s Equations in Cosmology.” arXiv, March 6, 1997. http://arxiv.org/abs/gr-qc/9703016.

---


<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>
<script type="text/x-mathjax-config">
  MathJax.Hub.Config({ tex2jax: {inlineMath: [['$', '$']]}, messageStyle: "none" }, displayMath: [ ['$$','$$'], ['\[','\]'] ]);
</script>
