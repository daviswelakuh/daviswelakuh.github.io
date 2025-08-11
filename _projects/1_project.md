---
layout: page
title: project 1
description: with background image
img: assets/img/12.jpg
importance: 1
category: work
related_publications: true
---

Every project has a beautiful feature showcase page.
It's easy to include images in a flexible 3-column grid format.
Make your photos 1/3, 2/3, or full width.

To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/tddft-qedft.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images, even citations {% cite einstein1950meaning %}.
Say you wanted to write a bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, _bled_ for your project, and then... you reveal its glory in the next row of images.

# Time-dependent QEDFT:

The optical spectra of a strongly coupled light-matter system can be obtained from the time-dependent QEDFT by solving the coupled Maxwell-Kohn-Sham equations

$$
i\hbar \frac{\partial}{\partial t} \varphi_{i}(\textbf{r},t) = \left( \frac{\hat{\textbf{p}}^{2}}{2m} + \underbrace{v(\textbf{r},t) +  v_{\textrm{Mxc}}([n,q_{\alpha}];\textbf{r},t) }_{v_{\textrm{KS}}([v,n,q_{\alpha}];\textbf{r},t)} \right)\varphi_{i}(\textbf{r},t) ,  \quad \textrm{and} \quad
\left(\frac{\partial^{2}}{\partial t^{2}} + \omega_{\alpha}^{2}\right)  q_{\alpha}(t) = \underbrace{ -\frac{j_{\alpha}(t)}{\omega_{\alpha}} + \omega_{\alpha}\boldsymbol{\lambda}_{\alpha}\cdot \textbf{R}(t) }_{j_{\alpha,\textrm{KS}}(t)}. 
$$

The Kohn-Sham orbitals $\varphi_{i}(\textbf{r},t)$ can be used to obtain the electronic density  $n(\textbf{r},t) = \sum_{i} |\varphi_i(\textbf{r},t)|^2$, and the photon displacement fields $q_{\alpha}(t)$ with associated mode frequencies $\omega_{\alpha}$ can be obtained analytically from mode-resolved equation of motion which is given by
$$
q_{\alpha}(t) = q_{\alpha}(t_{0})\cos(\omega_{\alpha}t) + \frac{\dot{q}_{\alpha}(t_{0})}{\omega_{\alpha}}\sin(\omega_{\alpha}t) - \frac{1}{\omega_{\alpha}^{2}}\int_{t_{0}}^{t}dt'\sin(\omega_{\alpha}(t-t'))j_{\alpha,\textrm{KS}}(t') \, .% \label{photon-q-soln2}
$$
The Kohn-Sham potential $v_{\textrm{KS}}(\textbf{r},t)$ is made up of the external potential $v(\textbf{r},t)$ and the mean-field exchange-correlation potential $v_{\textrm{Mxc}}(\textbf{r},t)$ which can be separated into $v_{\textrm{Mxc}}(\textbf{r},t)=v_{\textrm{Hxc}}(\textbf{r},t) + v_{\textrm{pxc}}(\textbf{r},t)$ where $v_{\textrm{Hxc}}(\textbf{r},t)$ and $v_{\textrm{pxc}}(\textbf{r},t)$ are respectively the Hatree exchange-correlation and electron-photon exchange-correlation potentials. The mode-resolved Maxwell equation couples to the Kohn-Sham equation via the electronic dipole $\textbf{R}(t)$ and $\boldsymbol{\lambda}_{\alpha}$ represents the light-matter coupling strength. For the calculations in this tutorial, we set the external current $j_{\alpha}(t)=0$ and the perturbation comes only from $v(\textbf{r},t)$.

As a last remark, we note that in the decoupling limit between light and matter (i.e. when $\boldsymbol{\lambda}_{\alpha} \rightarrow 0$), the Maxwell-Kohn-Sham equations decouples to the electron-only Kohn-Sham equation since $v_{\textrm{Mxc}}(\textbf{r},t) \rightarrow v_{\textrm{Hxc}}(\textbf{r},t)$.


## References
For details about time-dependent QEDFT, refer to the following:

[1] Davis M. Welakuh, [Ab initio Strong Light-Matter Theoretical Framework for Phenomena in Non-relativistic Quantum Electrodynamics](https://ediss.sub.uni-hamburg.de/handle/ediss/9069).

[2] M. Ruggenthaler, J. Flick et al., *Quantum-electrodynamical density-functional theory: Bridging quantum optics and electronic-structure theory* [Phys. Rev. A 90, 012508 (2014)](https://doi.org/10.1103/PhysRevA.90.012508).

[3] J. Flick, M. Ruggenthaler, H. Appel, and A. Rubio, *Kohn–Sham approach to quantum electrodynamical density-functional theory: Exact time-dependent effective potentials in real space* [Proc.Natl. Acad. Sci. U.S.A. 112, 15285 (2015)](https://doi.org/10.1073/pnas.151822411).

[4] Johannes Flick and P. Narang., *Cavity-Correlated Electron-Nuclear Dynamics from First Principles*, [Phys. Rev. Lett. 121, 113002 (2018)](https://doi.org/10.1103/PhysRevLett.121.113002).

# The electron-photon Casida equation:

The optical spectra of a strongly coupled light-matter system for finite systems can be obtained from the electron-photon Casida equation

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

where $\omega_{\alpha}$ represents the frequencies of the photon modes, $\Omega_{q}$ are the excitation frequencies of the coupled system, $\textbf{E}_{v}$ and $\textbf{P}_{v}$ are the eigenvectors and, the matrices $U$ and $V$ are given by

$$
U_{qq'} = \delta_{qq'}\omega_{q}^{2} + 2\sqrt{\omega_{q}\omega_{q'}}K_{qq'}(\Omega_{q}) \, , \qquad 
V_{q\alpha} = 2\sqrt{\omega_{q}M_{\alpha q}(\Omega_{q})N_{\alpha q}\omega_{\alpha}  } \, .
$$

The coupling matrices in the above equation are given explicitly below

$$
K_{ai,jb}(\Omega_{q}) = \iint d^{3}\textbf{r} d^{3}\textbf{r}'\varphi_i(\textbf{r})\varphi_a^*(\textbf{r})  \left(f^n_\text{Hxc}+ f^n_\text{pxc}\right)(\textbf{r},\textbf{r}',\Omega_{q})\varphi_b(\textbf{r}')\varphi^*_j(\textbf{r}') \, , \qquad
M_{\alpha,ai}(\Omega_{q}) = \int d^{3}\textbf{r} \varphi_i(\textbf{r})\varphi_a^*(\textbf{r}) f^{q_\alpha}_{\text{Mxc}} (\textbf{r},\Omega_{q})  \, ,  \qquad N_{\alpha,ai} = \frac{1}{2\omega_{\alpha}^{2}} \int d^{3}\textbf{r} \varphi_i(\textbf{r})\varphi^*_a(\textbf{r}) {g^{n_{\alpha}}_{\text{M}}(\textbf{r})} \, .
$$

Here $\varphi_{i}(\textbf{r})$ represents the occupied Kohn-Sham orbitals and $\epsilon_{i}$ the eigenvalues, where the transition frequencies $\omega_{q} = (\epsilon_{a} - \epsilon_{i})$. As in the original Casida equation, the equation is contructed in an electron-hole basis, and in our notation the subscript $a$ runs over the unoccupied Kohn-Sham states and $i$ over the occupied states. The frequency-dependent term $f^n_\text{Hxc}$ is the  Hatree exchange-correlation kernel that accounts for electron-electron interactions and $f_{\text{pxc}}^{n}$, $f_{\text{pxc}}^{q_\alpha}$ and $g_{\text{M}}^{n_{\alpha}}$ are the mean-field exchange-correlation kernels that account for electron-photon interactions.

The dimension of the electron-photon Casida matrix is determined from the number of states $N_{s}=N_{i}N_{a}+N_{p}$, where $N_{i}$ and $N_{a}$ are respectively the number of occupied and unoccupied states while $N_{p}$ represents the number of photon modes. The resulting dimension of the coupled but truncated
matrix is $(N_{s} \times N_{s})$.

As a last remark, we note that in the decoupling limit between light and matter (i.e. when the light-matter coupling $\boldsymbol{\lambda}_{\alpha} \rightarrow 0$), the electron-photon Casida equation simplifies to the electron-only Casida equation given by $U\, \textbf{E}_{v} = \Omega^{2}_{q} \, \textbf{E}_{v}$ where $U$ has no dependence on mean-field kernel, i.e., $f^n_\text{pxc} \rightarrow 0$.


## References
For details about the electron-photon Casida equation, refer to the following:

[1] Davis M. Welakuh, [Ab initio Strong Light-Matter Theoretical Framework for Phenomena in Non-relativistic Quantum Electrodynamics](https://ediss.sub.uni-hamburg.de/handle/ediss/9069)

[2] Johannes Flick, Davis M. Welakuh et al., *Light-Matter Response in Nonrelativistic Quantum Electrodynamics*, [ACS Photonics 6, 11, 2757–2778 (2019)](https://doi.org/10.1021/acsphotonics.9b00768).

# The electron-photon sternheimer approach

The uncoupled Sternheimer approach is also known as density-functional perturbation theory. The approach has superior scaling, is more efficient for dense spectra, and is more applicable to nonlinear response. One disadvantage is that one needs to proceed one frequency point at a time, rather than getting the whole spectrum at once. This disadvantage is normally circumvented using parallel architectures since the frequency-dependent Sternheimer equation parallelizes naturally as the responses at different frequencies can be computed independently of each other.

The frequency-dependent Sternheimer approach formulated within the framework of QEDFT, determines the correlated electron-photon density and photon displacement coordinate responses in terms of the occupied ground-state Kohn-Sham orbitals $\varphi_{k}(\textbf{r})$ and linear-response $\varphi_{k}^{(\pm)}(\textbf{r},\omega)$ given by

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

The frequency-dependnent term $f^n_\text{Mxc}=f^n_\text{Hxc} + f^n_\text{pxc}$ is the mean-field exhange-correlation kernel which is a sum of the Hartree exchange-correlation kernel $f^n_\text{Hxc}$ and electron-photon exchange-correlation $f^n_\text{pxc}$ kernel. The terms $f^{q_\alpha}_\text{pxc}$ and $g^{n_{\alpha}}_{\text{M}}$ are also electron-photon exchange-correlation kernels that account for electron-photon interactions.

As a last remark, we note that in the decoupling limit between light and matter (i.e. when the light-matter coupling $\boldsymbol{\lambda}_{\alpha} \rightarrow 0$), the photon dispalcement field $q_{\alpha}(\omega)$ decouples and electron-photon Sternheimer equations simplifies to the electron-only Sterneheimer equation.

[2] Davis M. Welakuh, J. Flick et al., *Frequency-Dependent Sternheimer Linear-Response Formalism for
Strongly Coupled Light−Matter Systems* [J. Chem. Theory Comput. 2022, 18, 4354−4365](https://doi.org/10.1021/acs.jctc.2c00076).

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>

The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}

```html
<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
```

{% endraw %}
