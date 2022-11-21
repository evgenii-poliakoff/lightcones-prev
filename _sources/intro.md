# Why nonstationary quantum motion is difficult?

The problem of characterizing/computing the nonstationary quantum state is much more difficult than that for the equilibrium state. The reason is that we do not know much about the general structure of nonstationary state. By "structure" we mean 

For example, we know the general structure of the equilibrium finite-temperature state: the canonical Gibbs density matrix

$$
\widehat{\rho}=\exp\left(-\beta \widehat{H} \right) 
$$ (gibbs_eq)

This knowledge allows us to:
 - develop efficient computational schemes. Indeed, by introducing  the thermodynamic potentials e.g. the  free energy functional 

$$
F = - \beta^{-1} \ln\left( \textrm{Tr} \widehat{\rho} \right),
$$

we obtain a variational principle 

$$
    F_{var} = F_{trial} + \left\langle \widehat{H} - \widehat{H}_{trial} \right\rangle \geq F
$$

for the trial (approximate) Hamiltonians. 

 - divide the degrees of freedom into relevant/irrelevant ones. Indeed, the Gibbs distribution in {eq}`gibbs_eq` shows that high-energy degrees of freedom are exponentiallly supressed (irrelevant).
 
Compared to this, the formal expression for the nonstationary state 

$$
\left| \Psi\left(t\right)\right\rangle = \exp(-i t \widehat{H}) \left| \Psi\left(0\right)\right\rangle 
$$

- does not lead to potentials with <em>global</em> variantional properties
- does not allow for direct  identification of irrelevant degrees of freedom: for a general quench, different energy scales are coupled. 
