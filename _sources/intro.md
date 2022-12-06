# Why nonstationary quantum motion is difficult?

It is much more difficult to compute the nonstationary many-particle quantum state than the equilibrium one. The reason is that in the equilibrium we can apriory estimate which degrees of freedom are statistically significant, and which are not. Indeed, in the equilibrium finite-temperature case we have the canonical Gibbs density matrix

$$
\widehat{\rho}=\exp\left(-\beta \widehat{H} \right) 
$$ (gibbs_eq)

This allows us to:

 - easily divide the degrees of freedom into the relevant (statistically significant)/irrelevant ones (statistically insignificant). Indeed, the Gibbs distribution tells us that the high-energy degrees of freedom are exponentiallly supressed (irrelevant).
 
 - develop efficient variational principles to compute the state. Indeed, by introducing  the thermodynamic potentials e.g. the  free energy functional 

$$
F = - \beta^{-1} \ln\left( \textrm{Tr} \widehat{\rho} \right),
$$

we obtain a variational principle 

$$
    F_{var} = F_{trial} + \left\langle \widehat{H} - \widehat{H}_{trial} \right\rangle \geq F
$$ (free_energy_variational_eq)

for the trial (approximate) Hamiltonians $\widehat{H}_{trial}$.  These trial Hamiltonians directly estimate the whole state at a given target temperature. We say therefore that these variational principles are <em>global</em>.

 
Compared to this, the formal expression for the nonstationary state 

$$
\left| \Psi\left(t\right)\right\rangle = \exp(-i t \widehat{H}) \left| \Psi\left(0\right)\right\rangle 
$$ (realtime_eq)

- does not allow for apriory estimation of relevant/irrelevant degrees of freedom: for a general quench, different energy scales are coupled. The exponent is an oscillating function of energy, it does not exhibit the exponential decay.
- does not lead to potentials with <em>global</em> variantional properties. 

Indeed, for the last point: the widely employed Dirac-Frenkel/McLachlan variational principle

$$
    \frac{\delta}{\delta \Psi} \left\Vert i\frac{\partial \Psi}{\partial t} - \widehat{H} \Psi  \right\Vert = 0
$$ (dirac_frenkel_eq)

is local: for each time moment, it merely tries to minimize the local discrepancy between the right and the left-sides of the Schrodinger equation. It knows nothing about what degrees of freedom are relevant at the target time, and how to approximate the whole quantum state. In this respect this variational  principle is much more inferior than {eq}`free_energy_variational_eq`. 