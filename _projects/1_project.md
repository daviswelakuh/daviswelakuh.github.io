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
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images, even citations {% cite einstein1950meaning %}.
Say you wanted to write a bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, _bled_ for your project, and then... you reveal its glory in the next row of images.

# The electron-photon sternheimer approach

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
