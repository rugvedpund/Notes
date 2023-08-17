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


# Stokes Parameters

The Stokes parameters are defined as:

$$\begin{align}
I &= \langle E_x^2 \rangle + \langle E_y^2 \rangle\\
Q &= \langle E_x^2 \rangle - \langle E_y^2 \rangle\\
U &= \langle E_x E_y^* \rangle + \langle E_x^* E_y \rangle\\
V &= i(\langle E_x E_y^* \rangle - \langle E_x^* E_y \rangle)
\end{align}$$

where $\langle \rangle$ denotes time averaging. For a monochromatic wave, we can write the electric field as $\vec{E}(t) = \vec{E}_0 e^{-i\omega t}$ and the Stokes parameters are given by: