# LuSEE Map-Making

## Introduction

Notes on map-making for LuSEE-Night. For an elementary review, refer to the excellent paper by Tegmark https://arxiv.org/pdf/astro-ph/9611130.pdf [^1]
[^1]: Tegmark has a crazy science page. Look up https://space.mit.edu/home/tegmark/crazy.html

## Map-Making

Map making is a data reduction process. It is the process of converting time-ordered data (TOD) to a map. The TOD is a vector of length $N_{\text{samples}}$ and the map is a vector of length $N_{\text{pixels}}$. Which map-making method to use depends on what the map is to be used for. Common use cases are:
- to facilitate comparison with other experiments
- to facilitate comparison with foreground templates
- to facilitate comparison with theory, e.g. power spectrum estimation, spatially distinctive systematics, etc.

### The mapping problem

Suppose we have measure $n$ numbers, $y_i$ for $i=1,2,\ldots,n$ which are the TOD. We want to estimate $m$ numbers called a _map_, $x_j$ for $j=1,2,\ldots,m$. We assume that the $y_i$ are linear combinations of the $x_j$ with some noise, i.e. 

$$ y_i = \sum_j A_{ij} x_j + \eta_i $$

 where $\eta_i$ is the noise. We want to estimate the $x_j$ given the $y_i$ and the $A_{ij}$. This is the _mapping problem_.

Some typical assumptions are, without loss of generality, 
- noise vector has zero mean, $\langle \eta_i \rangle = 0$, and so the noise covariance is given by $\langle \eta_i \eta_j \rangle = N_{ij}$
- map is typically assumed to be a realization of a random vector with zero mean, $\langle x_j \rangle = 0$, and so the map covariance is given by $\langle x_j x_k \rangle = S_{jk}$. The map is also uncorrelated with the noise, $\langle x_j \eta_i \rangle = 0$.

