---
icon: lucide/drafting-compass
---

# Measures, Metrics

## Risks

This page outlines tools under investigation for real-time *areas at risk* identification.

### Rates of Change of River Level

Let

$$\mathcal{l}_{t}, \: \mathcal{l}_{t - \tau}, \: \mathcal{l}_{t - 2\tau}, \: \mathcal{l}_{t - 3\tau}, \: \ldots$$


represent the time series of a gauge's river level measures, separated by $\tau$ hours, and unit of measure &Rarr; millimetres. Then the weighted-rate-of-change, w.r.t. each $\tau$ hours interval, is


$$r_{t - i\tau} = \frac{1}{\tau} \bigl(\mathcal{l}_{t - i\tau} - \mathcal{l}_{t - (i + 1)\tau}\bigr) \times \frac{1}{\mathcal{l}_{t - (i + 1)\tau}} \bigl(\mathcal{l}_{t - i\tau} - \mathcal{l}_{t - (i + 1)\tau}\bigr) $$

wherein

* $i = 0, 1, 2, 3, \ldots$
* $t\:$ is a/the current time point.
* $r_{t - i\tau}\:$ is the rate of change at time point $t - i\tau$, and its unit of measure is millimetres/hour.

Noting that

$$\frac{1}{\mathcal{l}_{t - (i + 1)\tau}} \bigl(\mathcal{l}_{t - i\tau} - \mathcal{l}_{t - (i + 1)\tau}\bigr)$$

determines the relative river level change w.r.t. consecutive river level values, i.e., values that are $\tau$ hours apart.


<br>
<br>

## Drift

For time series drift calculations, this hub depends on

* Jensen-Shannon Distance $J_{dist}$
* Wasserstein Distance $\mathcal{W}$

<br>wherein

$$J_{dist} = \sqrt{J_{div}}$$

$J_{div}$ is the Jensen-Shannon Divergence, a method for determining the similarity of a pair of distributions[^1].  The similarity between a pair of distributions increases as $J_{dist} \rightarrow 0$.  Note, for a pair of distributions

$$J_{div} \in [0 \quad 1]$$

therefore

$$J_{dist} \in [0 \quad 1]$$

The Wasserstein Distance <b>is</b> a distance measure[^2].

Important, do not consider scores in isolation, also consider the pattern of the scores over time.

<br>
<br>

<br>
<br>

<br>
<br>

<br>
<br>

[^1]: Study <a href="https://ieeexplore.ieee.org/document/61115" target="_blank">Divergence Measures Based on Shannon Entropy</a> for an in-depth understanding of Jensen-Shannon Divergence.
[^2]: Part 6 of <a href="https://arxiv.org/pdf/1904.08994" target="_blank">From GAN to WGAN</a> has an in-depth discussion of the Wasserstein Distance.  <span style="color: #a3a0a0">GAN: Generative Adversarial Network, WGAN: Wasserstein Generative Adversarial Network</span>

<br>
<br>
