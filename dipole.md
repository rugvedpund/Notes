# Polarization and Dipole Beam

## Introduction

Notes on polarization response of a simple dipole beam. Useful as a reference for studying Faraday rotation detection by LuSEE-Night, etc.

## Polarized Source at Zenith

For a monochromatic plane-polarized wave travelling along the z-direction, the electric field is given by $\vec{E}(t) = ( \epsilon_x \hat{x} + \epsilon_y \hat{y} ) e^{-i\omega t}$ 
and using

$$\hat{r} = \sin\theta \cos\phi \hat{x} + \sin\theta\sin\phi \hat{y} + \cos\theta \hat{z}\\
\hat{\theta} = \cos\theta \cos\phi \hat{x} + \cos\theta\sin\phi \hat{y} - \sin\theta \hat{z}\\
\hat{\phi} = -\sin\phi \hat{x} + \cos\phi \hat{y}$$

$$\hat{x} = \sin\theta \cos\phi \hat{r} + \cos\theta\cos\phi \hat{\theta} + -\sin\phi \hat{\phi}\\
\hat{y} = \sin\theta \sin\phi \hat{r} + \cos\theta\sin\phi \hat{\theta} + \cos\phi \hat{\phi}\\
\hat{z} = \cos\theta \hat{r} - \sin\theta \hat{\theta}$$

we can write

$\vec{E}(t) = ( \epsilon_x \sin\theta \cos\phi + \epsilon_y \sin\theta \sin\phi ) \hat{r} + ( \epsilon_x \cos\theta\cos\phi + \epsilon_y \cos\theta\sin\phi ) \hat{\theta} - ( \epsilon_x \sin\phi + \epsilon_y \cos\phi ) \hat{\phi} ) e^{-i\omega t}$

that is, a plane polarized wave travelling along the z-direction with electric field vector in the x-y plane has the follwing components when looking at the direction $\theta,\phi$ in the sky:

$$E_{r} = \epsilon_x \sin\theta \cos\phi + \epsilon_y \sin\theta \sin\phi$$
$$E_{\theta} = \epsilon_x \cos\theta\cos\phi + \epsilon_y \cos\theta\sin\phi$$
$$E_{\phi} = -\epsilon_x \sin\phi + \epsilon_y \cos\phi$$



1. ***If we have source at somewhere other than zenith***, say at $\theta_s$ and $\phi_s$, then we can write the electric field vector as a 3D rotation of the above. The rotation matrix is given by:

    $$R = \begin{bmatrix} \cos\phi_s & \sin\phi_s & 0 \\ -\sin\phi_s & \cos\phi_s & 0 \\ 0 & 0 & 1 \end{bmatrix} \begin{bmatrix} \cos\theta_s & 0 & -\sin\theta_s \\ 0 & 1 & 0 \\ \sin\theta_s & 0 & \cos\theta_s \end{bmatrix}$$

    and the electric field vector is given by:

    $$\vec{E}(t) = R(\theta_s,\phi_s) \begin{pmatrix} E_x \\ E_y \\ 0 \end{pmatrix} e^{-i\omega t}$$

1. ***If we have a source with a given polarization angle $\psi$ at the zenith***, then

    $$\vec{E}(t) = ( \epsilon_x' \hat{x} + \epsilon_y' \hat{y} ) e^{-i\omega t}$$

    where
    $$\begin{pmatrix} \epsilon_x' \\ \epsilon_y' \end{pmatrix} = \begin{bmatrix} \cos\psi & \sin\psi \\ -\sin\psi & \cos\psi \end{bmatrix} \begin{pmatrix} \epsilon_x \\ \epsilon_y \end{pmatrix}$$

1. ***Putting it all together***:

    If we have a patch of sky with a given polarization angle $\psi$ at the zenith, then the electric field is a sum over small element patches. For a small angular element $d\Omega(\theta_s,\phi_s)$ we can write the electric field vector as:

    $$\vec{dE}(t) = R(\theta_s,\phi_s) (\epsilon_x' \hat{x} + \epsilon_y' \hat{y}) e^{-i\omega t} d\Omega(\theta_s,\phi_s)$$

    which we integrate over the angular range and express in terms of the spherical basis vectors $\hat{r}, \hat{\theta}, \hat{\phi}$ and integrated over the patch. We get our $E_r, E_\theta, E_\phi$ for a patch at zenith.

## Dipole Beam Pattern

For a dipole antenna of $L<<\lambda/2$ oriented along the $z$-axis the polarization response in the far-field limit is given by
$$B_\theta=i\eta \frac{kI_0le^{-ikr}}{4\pi r} \sin\theta \sim l\nu \sin\theta\\
B_r=B_\phi=0$$

We get the dipoles along $x-$ and $y-$ axes by a simple rotation of the above. Simpler if converted to $B_x, B_y, B_z$ basis.

## Stokes Parameters

Given a beam, we can calculate the Stokes parameters as

$$
S = \int d\Omega \ B_\theta E_\theta + B_\phi E_\phi
$$

where $B_\theta, B_\phi$ are the beam patterns and $E_\theta, E_\phi$ are the electric field components in the $\theta, \phi$ directions.

Now the power is given by

$$
P = \braket{S S^*} = \braket{\int (B_\theta E_\theta + B_\phi E_\phi)(B_\theta E_\theta + B_\phi E_\phi)^* \ d\Omega d\Omega^*}
$$

And we can use the following statistical properties

$$\begin{align}
\braket{E_\theta(\hat{n}) E_\theta^*(\hat{n}')} &= \frac{1}{2} (I+Q) \delta(\hat{n}-\hat{n}') \\
\braket{E_\phi(\hat{n}) E_\phi^*(\hat{n}')} &= \frac{1}{2} (I-Q) \delta(\hat{n}-\hat{n}') \\
\braket{E_\theta(\hat{n}) E_\phi^*(\hat{n}')} &= \frac{1}{2} (U-iV) \delta(\hat{n}-\hat{n}')
\end{align}$$

Thus, given a beam pattern, the power recieved can be written simply in terms of the Stokes paramters as

$$
P = \braket{S S^*}= \int d\Omega \ B_I I + B_Q Q + B_U U + B_V V
$$

If we have two beams, $B$ and $B'$, then the cross Stokes parameters are given by

$$\begin{align}
B_I = \frac{1}{2} (B_\theta {B_\theta'}^* + B_\phi {B_\phi'}^*) \\
B_Q = \frac{1}{2} (B_\theta {B_\theta'}^* - B_\phi {B_\phi'}^*) \\
B_U = (B_\theta {B_\phi'}^* + B_\phi {B_\theta'}^*) \\
B_V = i(B_\theta {B_\phi'}^* - B_\phi {B_\theta'}^*)
\end{align}$$

