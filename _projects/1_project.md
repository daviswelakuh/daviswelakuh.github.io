---
layout: page
title: QEDFT
description: An extension of density-functional theory that solves practical QED problems.
img: assets/img/12.jpg
importance: 1
category: work
related_publications: true
---

Quantum Electrodynamical Density-Functional Theory (QEDFT) is an extension of Density-Functional Theory (DFT) that explicitly includes the interaction between electrons and quantized electromagnetic fields (photons) within a cavity quantum electrodynamics framework. Standard DFT solves for the electron density in an external potential (nuclei, applied fields, etc.). In many modern systems -- such as molecules in optical cavities, plasmonic nanostructures, or other quantum electrodynamical environments that can achieve strong light-matter interaction -- photons can significantly change the electronic structure and hence properties of matter. QEDFT extends DFT to treat such different settings of strongly coupled light-matter systems. 

Focusing on excited-states properties of such strongly coupled light-matter systems, standard electronic structure methods such as Casida and Sternheimer approaches have been extending within the framework of QEDFT to capture or predict modification of matter properties due to its strong interaction with photons. These methods are outlined below.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/tddft-qedft.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Schematics of the usual semiclassical Kohn-Sham theory (left) contrasted with schematics of the  Maxwell Kohn-Sham approach (right).
</div>

# Time-dependent QEDFT:

Time-dependent QEDFT {% cite ruggenthaler2014, welakuh2021thesis %} is an extension of standard Time-dependent Density-Functional Theory (TDDFT) that incorporates not only the dynamics of electrons but also the quantized electromagnetic field (photons) in a self-consistently coupled way as contrasted in the figure. For practical purposes, QEDFT maps the many-body electron-photon problem to a time-dependent Maxwell-Kohn-Sham system, where: (1) The electronic part is represented by the time-dependent Kohn–Sham equations for electrons and (2) the photonic part is described by harmonic oscillator-like equations for the quantized photon modes, using photon coordinates as dynamical variables.

$$
i\hbar \frac{\partial}{\partial t} \varphi_{i}(\textbf{r},t) = \left( \frac{\hat{\textbf{p}}^{2}}{2m} + \underbrace{v(\textbf{r},t) +  v_{\textrm{Mxc}}([n,q_{\alpha}];\textbf{r},t) }_{v_{\textrm{KS}}([v,n,q_{\alpha}];\textbf{r},t)} \right)\varphi_{i}(\textbf{r},t) ,  \quad \textrm{and} \quad
\left(\frac{\partial^{2}}{\partial t^{2}} + \omega_{\alpha}^{2}\right)  q_{\alpha}(t) = \underbrace{ -\frac{j_{\alpha}(t)}{\omega_{\alpha}} + \omega_{\alpha}\boldsymbol{\lambda}_{\alpha}\cdot \textbf{R}(t) }_{j_{\alpha,\textrm{KS}}(t)}. 
$$

The Kohn-Sham orbitals $\varphi_{i}(\textbf{r},t)$ can be used to obtain the electronic density  $n(\textbf{r},t) = \sum_{i} |\varphi_i(\textbf{r},t)|^{2}$, and the photon displacement fields $q_{\alpha}(t)$ with associated mode frequencies $\omega_{\alpha}$ can be obtained analytically from mode-resolved equation of motion which is given by
$$
q_{\alpha}(t) = q_{\alpha}(t_{0})\cos(\omega_{\alpha}t) + \frac{\dot{q}_{\alpha}(t_{0})}{\omega_{\alpha}}\sin(\omega_{\alpha}t) - \frac{1}{\omega_{\alpha}^{2}}\int_{t_{0}}^{t}dt'\sin(\omega_{\alpha}(t-t'))j_{\alpha,\textrm{KS}}(t') \, .% \label{photon-q-soln2}
$$
The Kohn-Sham potential $v_{\textrm{KS}}(\textbf{r},t)$ is made up of the external potential $v(\textbf{r},t)$ and the mean-field exchange-correlation potential $v_{\textrm{Mxc}}(\textbf{r},t)$ which can be separated into $v_{\textrm{Mxc}}(\textbf{r},t)=v_{\textrm{Hxc}}(\textbf{r},t) + v_{\textrm{pxc}}(\textbf{r},t)$ where $v_{\textrm{Hxc}}(\textbf{r},t)$ and $v_{\textrm{pxc}}(\textbf{r},t)$ are respectively the Hatree exchange-correlation and electron-photon exchange-correlation potentials. The mode-resolved Maxwell equation couples to the Kohn-Sham equation via the electronic dipole $\textbf{R}(t)$ and $$\boldsymbol{\lambda}_{\alpha}$$ represents the light-matter coupling strength.

As a last remark, we note that in the decoupling limit between light and matter (i.e. when $$ \boldsymbol{\lambda}_{\alpha} \rightarrow 0 $$), the Maxwell-Kohn-Sham equations decouples to the electron-only Kohn-Sham equation since $v_{\textrm{Mxc}}(\textbf{r},t) \rightarrow v_{\textrm{Hxc}}(\textbf{r},t)$.


# The Casida formalism within QEDFT framework:

The Casida formalism within QEDFT framework {% cite flick2019 %} is an extension of the standard Casida approach in TDDFT. It is as well a standard linear-response technique used to calculate excitation energies and oscillator strengths of an atomic, molecular and solid-state systems interacting strongly with photons directly from the Kohn-Sham (KS) ground state and photon coordinate. The  pseudo-eigenvalue problem within QEDFT framework is given as below

$$
\left(
\begin{array}{ c c  }
	U &   V     \\
	V^{\dagger} &  \omega_{\alpha}^{2}
\end{array}
\right)
\left(
\begin{array}{ c }
	\textbf{E}_{v}  \\
	\textbf{P}_{v}
\end{array}
\right)
= \Omega^{2}_{q} 
\left(
\begin{array}{ c }
	\textbf{E}_{v}  \\
	\textbf{P}_{v}  
\end{array}
\right)
$$

where $\omega_{\alpha}$ represents the frequencies of the photon modes, $\Omega_{q}$ are the excitation frequencies of the coupled system, $$\textbf{E}_{v}$$ and $$\textbf{P}_{v}$$ are the eigenvectors and, the matrices $U$ and $V$ are given by

$$
U_{qq'} = \delta_{qq'}\omega_{q}^{2} + 2\sqrt{\omega_{q}\omega_{q'}}K_{qq'}(\Omega_{q}) \, , \qquad 
V_{q\alpha} = 2\sqrt{\omega_{q}M_{\alpha q}(\Omega_{q})N_{\alpha q}\omega_{\alpha}  } \, .
$$

The coupling matrices in the above equation are given explicitly below

$$
\begin{aligned}
K_{ai,jb}(\Omega_{q}) &= \iint d^{3}\mathbf{r} \, d^{3}\mathbf{r}' \,
\varphi_i(\mathbf{r})\varphi_a^*(\mathbf{r})
\left(f^n_{\text{Hxc}}+ f^n_{\text{pxc}}\right)(\mathbf{r},\mathbf{r}',\Omega_{q})
\varphi_b(\mathbf{r}')\varphi^*_j(\mathbf{r}') \,, \\
M_{\alpha,ai}(\Omega_{q}) &= \int d^{3}\mathbf{r} \,
\varphi_i(\mathbf{r})\varphi_a^*(\mathbf{r})
f^{q_\alpha}_{\text{Mxc}} (\mathbf{r},\Omega_{q}) \,, \\
N_{\alpha,ai} &= \frac{1}{2\omega_{\alpha}^{2}} \int d^{3}\mathbf{r} \,
\varphi_i(\mathbf{r})\varphi^*_a(\mathbf{r}) g^{n_{\alpha}}_{\text{M}}(\mathbf{r}) \,.
\end{aligned}
$$

Here $\varphi_{i}(\textbf{r})$ represents the occupied Kohn-Sham orbitals and $\epsilon_{i}$ the eigenvalues, where the transition frequencies $\omega_{q} = (\epsilon_{a} - \epsilon_{i})$. As in the original Casida equation, the equation is contructed in an electron-hole basis, and in our notation the subscript $a$ runs over the unoccupied Kohn-Sham states and $i$ over the occupied states. The frequency-dependent term $f^n_\text{Hxc}$ is the  Hatree exchange-correlation kernel that accounts for electron-electron interactions and $f_{\text{pxc}}^{n}$, $f_{\text{pxc}}^{q_\alpha}$ and $g_{\text{M}}^{n_{\alpha}}$ are the mean-field exchange-correlation kernels that account for electron-photon interactions.

The dimension of the electron-photon Casida matrix is determined from the number of states $N_{s}=N_{i}N_{a}+N_{p}$, where $N_{i}$ and $N_{a}$ are respectively the number of occupied and unoccupied states while $N_{p}$ represents the number of photon modes. The resulting dimension of the coupled but truncated matrix is $(N_{s} \times N_{s})$.

As a last remark, we note that in the decoupling limit between light and matter (i.e. when the light-matter coupling $$\boldsymbol{\lambda}_{\alpha} \rightarrow 0$$), the electron-photon Casida equation simplifies to the electron-only Casida equation given by $$U\, \textbf{E}_{v} = \Omega^{2}_{q} \, \textbf{E}_{v}$$ where $U$ has no dependence on mean-field kernel, i.e., $f_\text{pxc}^{n} \rightarrow 0$.

You can also put regular text between your rows of images, even citations .

# The Sternheimer formalism within QEDFT framework

The frequency-dependent Sternheimer approach formulated within the framework of QEDFT {% cite welakuh2022 %}, determines the correlated electron-photon density and photon displacement coordinate responses in terms of the occupied ground-state Kohn-Sham orbitals $\varphi_{k}(\textbf{r})$ and linear-response $\varphi_{k}^{(\pm)}(\textbf{r},\omega)$ given by

$$
\delta n(\textbf{r},\omega) 
= \sum_{k=1}^{N_{e}} \left[ \varphi_{k}^{*}(\textbf{r}) \varphi_{k}^{(+)}(\textbf{r},\omega) +  \varphi_{k}(\textbf{r}) \left[\varphi_{k}^{(-)}(\textbf{r},\omega)\right]^{*}\right] , \qquad \textrm{and} \qquad
\delta q_{\alpha}(\omega) = \delta q_{\alpha}^{(+)}(\omega) + \delta q_{\alpha}^{(-)}(\omega)
$$

by solving the self-consistent linear coupled Sternheimer equations
$$
\left(\omega - \hat{h} + \epsilon_{k} + i\eta\right)\varphi_{k}^{(+)}(\textbf{r},\omega) =   \delta v_{\textrm{KS}}(\textbf{r},\omega) \varphi_{k}(\textbf{r}) \, ,  \qquad \textrm{and} \qquad
\left(\omega + \hat{h} - \epsilon_{k} + i\eta\right)\varphi_{k}^{(-)}(\textbf{r},\omega) = -  \delta v_{\textrm{KS}}(\textbf{r},\omega) \varphi_{k}^{*}(\textbf{r}) \, , 
$$

$$
\delta q_{\alpha,v}^{(+)}(\omega) 
= \frac{1}{2\omega_{\alpha}^{2}} \left(\frac{1}{\omega - \omega_{\alpha} + i\eta'} \right) \int d^{3}\textbf{r}' g_{M}^{n_{\alpha}}(\textbf{r}') \delta n(\textbf{r}',\omega) \, , \qquad \textrm{and} \qquad
\delta q_{\alpha,v}^{(-)}(\omega) 
= -\frac{1}{2\omega_{\alpha}^{2}} \left( \frac{1}{\omega + \omega_{\alpha} + i\eta'}\right) \int d^{3}\textbf{r}' g_{M}^{n_{\alpha}}(\textbf{r}') \delta n_{v}(\textbf{r}',\omega) \, .
$$

Here, $\hat{h}$ is the Kohn-Sham Hamiltonian, $\epsilon_{k}$ are the eigenvalues of the ground-state, $\omega_{\alpha}$ is the photon mode frequencies, and the response of the Kohn-Sham potential is given explicitly as

$$
\delta v_{\textrm{KS}}(\textbf{r},\omega) = \delta v(\textbf{r},\omega) + \int d^{3}\textbf{r}' f_{\textrm{Mxc}}^{n}(\textbf{r},\textbf{r}',\omega) \delta n(\textbf{r}',\omega) + \sum_{\alpha} f_{\textrm{Mxc}}^{q_{\alpha}}(\textbf{r},\omega)\delta  q_{\alpha}(\omega)
$$

The frequency-dependnent term $f^n_\text{Mxc}=f^n_\text{Hxc} + f^n_\text{pxc}$ is the mean-field exhange-correlation kernel which is a sum of the Hartree exchange-correlation kernel $f^n_\text{Hxc}$ and electron-photon exchange-correlation $f^n_\text{pxc}$ kernel. The terms $f^{q_{\alpha}}_{\text{pxc}}$ and $g_{\text{M}}^{n_{\alpha}}$ are also electron-photon exchange-correlation kernels that account for electron-photon interactions.

As a last remark, we note that in the decoupling limit between light and matter (i.e. when the light-matter coupling $\boldsymbol{\lambda}_{\alpha} \rightarrow 0$), the photon dispalcement field $q_{\alpha}(\omega)$ decouples and electron-photon Sternheimer equations simplifies to the electron-only Sterneheimer equation.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/QEDFT_methods_benzene.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Schematics of the Maxwell Kohn-Sham approach (right) contrasted with schematics of the usual semiclassical Kohn-Sham theory (left).
</div>

