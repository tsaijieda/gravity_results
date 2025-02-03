## Results to reproduce

There are several results that we could try to reproduce, the file are located in their respective directory. The order is by the likelyhood of going wrong from low to high.

### Space of $g_2$ and $g_3$ under different $\mu$

This part is to study the space of $\frac{g_2 M^2}{8\pi G}$ and $\frac{g_3 M^4}{8\pi G}$ under different $\mu$, $M$ is the mass of the gap state. For $\mu = 1$, the result should be same as Simmon's paper (the Wedge shape). For $\mu = 2$, the result is in the [link_1](./space/space.txt), main code is in the [link_2](./space/space.m).

The choice of parameters is as follow

| property | parameter |
| --- | --- |
| Dimension | 10 |
| gap state | single spin-2 |
| functionals | $\{p^n C_{2,\text{improved}},n < 61/2\} \bigcup \{p^n X_{4,\text{improved}},n < 5\} \bigcup \{p^n X_{6,\text{improved}},n < 3\}$   |
| $J_{\text{max}}$ | 40 |
| $\delta_x$ | 1/100 |
| $\epsilon_b$ | 1/128 |
| $B$ | 40 |

### Relation of $\lambda^2/8\pi G$ over $1/\mu$

This part is to investigate the relation of $\lambda^2/8\pi G$ over $1/\mu$. The result is in the [link_3](./mu_dependence/mu_dependece.txt), the main code is in the [link_4](./mu_dependence/mu_dependence.m).

| property | parameter |
| --- | --- |
| Dimension | 10 |
| gap state | single spin-2 |
| functionals | $\{p^n C_{2,\text{improved}},n < 61/2\} \bigcup \{p^n X_{4,\text{improved}},n < 5\} \bigcup \{p^n X_{6,\text{improved}},n < 3\}$   |
| $J_{\text{max}}$ | 40 |
| $\delta_x$ | 1/100 |
| $\epsilon_b$ | 1/32 |
| $B$ | 40 |

