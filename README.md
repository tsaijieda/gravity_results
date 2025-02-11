## Results to reproduce

There are several results that we could try to reproduce, the file are located in their respective directory. The order is by the likelyhood of going wrong from low to high.

### Method to bound $\lambda^2/8\pi G$

In Simons paper, we have dispersion relation 
$$\frac{8\pi G}{-u} + 2g_2 - g_3 u = \langle C_{2, u}^{\text{improved}}[m^2, J] \rangle$$

The angle bracket is the sum of $m^2 > 1$ and even spin $J$. If we had gap state, the sum over $m^2$ is $m^2 = 1$ and $m^2 > \mu$. We could move the gap state to the right hand side, we have

$$\frac{8\pi G}{-u} + 2g_2 - g_3 u - \lambda_1^2 C_{2, u}^{\text{improved}}[1, J_\text{gap}] = \langle C_{2, u}^{\text{improved}}[m^2, J] \rangle$$

Where the sum here is from $m^2 > \mu$. Then we could integrate the both side against $f(p)$ at $ u = -p^2$ and follow the similar way in Simons paper,

$$\text{minimize} \int_{0}^{\mu} dp f(p) \Biggl(\frac{8\pi G}{p^2} + 2g_2 + g_3 p^2\Biggr)\hspace{0.5 cm} \text{s.t.} \int_{0}^{\mu} dp f(p) C_{2, -p^2}^{\text{improved}}[1, J_\text{gap}]  = -1$$

### Space of $g_2$ and $g_3$ under different $\mu$

This part is to study the space of $\frac{g_2 M^2}{8\pi G}$ and $\frac{g_3 M^4}{8\pi G}$ under different $\mu$, $M$ is the mass of the gap state. For $\mu = 1$, the result should be same as Simmon's paper (the Wedge shape). For $\mu = 2$, the result is in the [link_1](./space/space.txt), main code is in the [link_2](./space/space.m).

The choice of parameters is as follow

| property | parameter |
| --- | --- |
| Dimension | 10 |
| gap state | single spin-2 |
| functionals | $\{p^n C_{2,\text{improved}},n \leq 61/2\} \bigcup \{p^n X_{4,\text{improved}},n \leq 5\} \bigcup \{p^n X_{6,\text{improved}},n \leq 3\}$   |
| $J_{\text{max}}$ | 40 |
| $\delta_x$ | 1/100 |
| $\epsilon_b$ | 1/128 |
| $B$ | 40 |

### Relation of $\lambda^2/8\pi G$ over $1/\mu$

This part is to investigate the relation of $\lambda^2/8\pi G$ over $1/\mu$. First result with functional order $\text{num}$ up to 41/2 is in the [link_3](./mu_dependence/mu_41.txt). Second result with $\text{num}$ up to 61/2 is in the [link_4](./mu_dependence/mu_61.txt). The main code is in the [link_5](./mu_dependence/mu_dependence.m).

| property | parameter |
| --- | --- |
| Dimension | 10 |
| gap state | single spin-2 |
| functionals | $\{p^n C_{2,\text{improved}},n \leq \text{num}\} \bigcup \{p^n X_{4,\text{improved}},n \leq 5\} \bigcup \{p^n X_{6,\text{improved}},n \leq 3\}$   |
| $J_{\text{max}}$ | 40 |
| $\delta_x$ | 1/100 |
| $\epsilon_b$ | 1/32 |
| $B$ | 40 |

### Bounding $\lambda^2/g_4$ under fixed $g_2, g_3, g_5, g_6$

In this section, we try to bound $\lambda^2/g_4$ since $\lambda^2/8\pi G$ is unbounded. First, we try to fix $g_2, g_3, g_5, g_6 = 0$, and we got the lower bound for $g_4$ is 0. Next, we could bound $\lambda^2/g_4$ under $g_2, g_3, g_5, g_6 = 0$. We found that $\lambda^2$ goes to 0 as $g_4$ goes to $0$, which is different from what we saw before, where $\lambda^2$ does not goes to 0 if $g_2$ goes to 0. The relevant data is in the following table.

| $g4/8\pi G$ | $lambda^2/8\pi G$ |
| --- | --- |
| 0.1 | 0.0778 |
| 0.01 | 0.00778 |
| 0.001 | 0.000778 |

However, we also fix another set of $g_2 = 0.2, g_3, g_5, g_6$. We found that the $\lambda^2/8\pi G$ grows as $g_6/8\pi G$ grows, so now $\lambda^2/g_4$ is unbounded.
