# Worked Example: Applying the Feedback Framework

**Note:** Removed from the lecture notes (not an examinable procedural skill in the same way as L2/L3 examples). Retained here for reference and for use in lecture delivery.

---

A radical intermediate $\mathrm{R}^{\bullet}$ is produced from a stable precursor A, amplified by reaction with B, and removed by reaction with C:

\begin{align*}
\mathrm{A} &\xrightarrow{k_1} \mathrm{R}^{\bullet} \\
\mathrm{R}^{\bullet} + \mathrm{B} &\xrightarrow{k_2} 2\mathrm{R}^{\bullet} \\
\mathrm{R}^{\bullet} + \mathrm{C} &\xrightarrow{k_3} \mathrm{P}
\end{align*}

with $k_1 = 0.5\,\mathrm{s}^{-1}$, $k_2 = 2\,\mathrm{M}^{-1}\,\mathrm{s}^{-1}$, $k_3 = 3\,\mathrm{M}^{-1}\,\mathrm{s}^{-1}$, $[\mathrm{A}]_0 = 1\,\mathrm{M}$, $[\mathrm{B}]_0 = 5\,\mathrm{M}$, and $[\mathrm{C}]_0 = 10\,\mathrm{M}$.

The first step is initiation (creates $\mathrm{R}^{\bullet}$ from a stable precursor). The second is branching: one $\mathrm{R}^{\bullet}$ goes in and two come out, giving a net gain of one radical. The third is termination: $\mathrm{R}^{\bullet}$ is consumed and converted to the stable product P.

**Does this system show positive or negative feedback?** We write the rate equation for $\mathrm{R}^{\bullet}$. The branching step consumes one $\mathrm{R}^{\bullet}$ and produces two, so its net contribution is $+k_2[\mathrm{B}][\mathrm{R}^{\bullet}]$. Termination contributes $-k_3[\mathrm{C}][\mathrm{R}^{\bullet}]$. Combining:

$$\frac{\mathrm{d}[\mathrm{R}^{\bullet}]}{\mathrm{d}t} = k_1[\mathrm{A}] + \left(k_2[\mathrm{B}] - k_3[\mathrm{C}]\right)[\mathrm{R}^{\bullet}]$$

This has the form of the feedback equation with $\nu_\mathrm{f} = k_1[\mathrm{A}]$ and:

$$\phi = k_2[\mathrm{B}] - k_3[\mathrm{C}] = (2)(5) - (3)(10) = -20\,\mathrm{s}^{-1}$$

Since $\phi < 0$, the feedback is negative and the system reaches a steady state.

**What is the steady-state radical concentration?**

$$[\mathrm{R}^{\bullet}]_\mathrm{ss} = \frac{\nu_\mathrm{f}}{|\phi|} = \frac{k_1[\mathrm{A}]}{|\phi|} = \frac{(0.5)(1)}{20} = 0.025\,\mathrm{M}$$

The system approaches this value with a timescale $\tau = 1/|\phi| = 1/20 = 0.05\,\mathrm{s}$. Whether $[\mathrm{R}^{\bullet}]$ starts at zero or above this value, it converges on the same steady state.

**Would increasing [B] make an explosion more or less likely?** Since $\phi = k_2[\mathrm{B}] - k_3[\mathrm{C}]$, increasing $[\mathrm{B}]$ increases $\phi$, pushing it towards positive values. An explosion becomes more likely. This makes physical sense: B is the reactant in the branching step, so more B means faster branching.

**What is the maximum [C] for which an explosion will occur?** The explosion limit corresponds to $\phi = 0$:

$$k_2[\mathrm{B}] = k_3[\mathrm{C}] \qquad \Rightarrow \qquad [\mathrm{C}] = \frac{k_2[\mathrm{B}]}{k_3} = \frac{(2)(5)}{3} = 3.3\,\mathrm{M}$$

For $[\mathrm{C}] < 3.3\,\mathrm{M}$, branching outpaces termination ($\phi > 0$) and the system explodes. For $[\mathrm{C}] > 3.3\,\mathrm{M}$, termination wins ($\phi < 0$) and the system reaches a steady state. The species C acts as an inhibitor: it provides a termination pathway that competes with branching, and its concentration determines whether the system is safe or explosive.
