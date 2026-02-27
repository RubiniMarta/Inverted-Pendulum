# Inverted-Pendulum
*Design and implementation of linear and non-linear control strategies for the stabilization of an unstable mechanical system on a cart.*

**Mathematical Modeling:** Derived the non-linear equations of motion for a two-degree-of-freedom system using the Lagrange approach and the Rayleigh dissipation function to account for viscous friction.
**State-Space Representation:** Developed a four-state non-linear state-space model to describe the relationship between the cart’s force input and the position/angle outputs.
**Open-Loop Analysis:** Simulated the non-linear system response to pulse forces of varying magnitudes (1N, 5N, 25N) in MATLAB® using the ode45 solver to assess stability and motion asymmetry.
**Linearization & Frequency Domain:** Linearized the system about an unstable equilibrium point ($\theta = \pi$) to obtain state-space matrices and Transfer Functions ($G_{xu}$, $G_{\theta u}$).
**Stability Diagnostics:** Identified inherent system instability through Pole-Zero maps (showing poles in the right-half plane) and analyzed frequency responses via Bode diagrams.
**Control Strategy Development:** Analytically demonstrated the inability of Proportional (P) control to achieve asymptotic stability, leading to the implementation of Proportional-Derivative (PD) strategies.
**Time-Domain Tuning:** Optimized PD gains ($k_P, k_D$) to satisfy strict design requirements, including a peak time ($T_{peak}$) < 1s and an overshoot ($OS\%$) < 20%.
**Full-State Feedback:** Implemented a Full-State PD controller using pole placement techniques to stabilize both the pendulum angle and the cart position, significantly improving disturbance rejection over partial-state methods.
**Validation:** Performed comparative simulations between MATLAB® scripts and Simulink® block models (including M-functions and integrator chains) to confirm the consistency of the controlled responses.
