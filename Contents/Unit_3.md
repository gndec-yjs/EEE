<script type="text/x-mathjax-config">
  MathJax.Hub.Config({
    tex2jax: {
      inlineMath: [ ['$','$'], ["\\(","\\)"] ],
      processEscapes: true
    }
  });
</script>
    
<script type="text/javascript"
        src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>

# Unit 3: Theory of Vibrations

- [Introduction to Theory of Vibrations](#31-introduction-to-theory-of-vibrations)  
- [Sources of Vibrations](#32-sources-of-vibrations)  
- [Types of Vibrations](#33-types-of-vibrations)  
- [Degree of Freedom](#34-degree-of-freedom)  
- [Spring Action and Damping](#35-spring-action-and-damping)  
- [Equation of Motion of SDOF Systems](#36-equation-of-motion-of-sdof-systems)  
- [Undamped and Damped Systems under Transient Forces](#37-undamped-and-damped-systems-under-transient-forces)  
- [General Solution and Green’s Function](#38-general-solution-and-greens-function)  
- [Example Problems](#39-example-problems)

## Notes

- [Theory of Vibration](Resources/Theory_of_Vibration.pdf)
- [Vibration Analysis](Resources/Vibration_Analysis.pdf)

## 3.1 Introduction to Theory of Vibrations  

**Vibration** is the **oscillatory motion** of a body about its equilibrium position.  
In earthquake engineering, vibration theory provides the foundation to understand how structures respond to ground motion.  

📌 **Engineering Relevance**  
- Earthquake loads are *dynamic* → structures vibrate.  
- Analysis of vibrations helps predict:  
  * Natural frequencies  
  * Mode shapes  
  * Response under dynamic loading (earthquakes, wind, machines)  

## 3.2 Sources of Vibrations  

Vibrations in civil structures arise from:  

- **Natural Sources**  
  * Earthquakes 🌍  
  * Wind loading 🌬️  
  * Ocean waves 🌊  

- **Anthropogenic / Man-made Sources**  
  * Machine foundations (motors, turbines) ⚙️  
  * Traffic and railways 🚆  
  * Blasting, pile driving, construction activities 🏗️  

## 3.3 Types of Vibrations  

| **Type**             | **Description**                                                                 | **Example** |
|----------------------|---------------------------------------------------------------------------------|-------------|
| **Free Vibration**   | System vibrates on its own after initial disturbance. No external force acts.   | A pendulum released from rest. |
| **Forced Vibration** | System vibrates under continuous external excitation.                          | Building subjected to wind or earthquake. |
| **Damped Vibration** | Amplitude decreases with time due to energy dissipation.                      | Car suspension system. |
| **Undamped Vibration** | Ideal case, no energy loss. Amplitude remains constant.                       | Theoretical spring–mass system. |
| **Transient Vibration** | Short-duration disturbance, response dies after some time.                  | Blast load on a structure. |
| **Steady-State Vibration** | Response matches excitation frequency (important in resonance studies). | Rotating machines. |

## 3.4 Degree of Freedom (DOF)  

- **Definition**: The **minimum number of independent coordinates** needed to describe the motion of a system.  
- **Examples**:  
  * A simple pendulum → 1 DOF (angle $\theta$).  
  * A rigid body in plane motion → 3 DOF.  

📌 **Importance in Structural Engineering**  
- Simplifies modeling.  
- Most earthquake analyses use **SDOF (Single Degree of Freedom)** or **MDOF (Multi-DOF)** models.  

## 3.5 Spring Action and Damping  

- **Spring Action**: Restoring force proportional to displacement.  
  $$
  F_s = kx
  $$  
  where $k =$ stiffness, $x =$ displacement.  

- **Damping**: Resistance that reduces vibration amplitude by dissipating energy.  

  | **Type of Damping** | **Description** | **Example** |
  |----------------------|-----------------|-------------|
  | **Viscous Damping** | Force proportional to velocity: $F_d = c \dot{x}$ | Shock absorbers |
  | **Coulomb Damping** | Constant friction force, independent of velocity | Sliding surfaces |
  | **Structural Damping** | Energy loss within material | Concrete/steel structures |

## 3.6 Equation of Motion of SDOF Systems  

For a **spring–mass–damper system** under external force $F(t)$:  

$$
m \ddot{x}(t) + c \dot{x}(t) + kx(t) = F(t)
$$

Where:  
- $m$ = mass  
- $c$ = damping coefficient  
- $k$ = stiffness
- $x(t)$ = displacement  
- $F(t)$ = external force  
- $m \ddot{x}(t)$ : **Inertial force**  
- $c \dot{x}(t)$ : **Damping force** (energy dissipation)  
- $k x(t)$ : **Restoring force** from the spring

## 3.7 Undamped and Damped Systems under Transient Forces  

1. **Undamped Free Vibration** ($c=0$, $F(t)=0$):  
   $$
   m \ddot{x} + kx = 0
   $$  
   Solution:  
   $$
   x(t) = A \cos(\omega_n t) + B \sin(\omega_n t)
   $$  
   with $\omega_n = \sqrt{\tfrac{k}{m}}$ (natural frequency).  

2. **Damped Free Vibration** ($F(t)=0$):  
   $$
   m \ddot{x} + c \dot{x} + kx = 0
   $$  

   - Define **damping ratio**:  
     $$
     \zeta = \frac{c}{2 \sqrt{km}}
     $$  

   - Three cases:  
     * $\zeta < 1$ → underdamped (oscillatory decay)  
     * $\zeta = 1$ → critical damping (fastest return to equilibrium)  
     * $\zeta > 1$ → overdamped (no oscillation, slow return)  

3. **Forced/Transient Vibration**:  
   - System subjected to earthquake-like pulse or dynamic load.  
   - Response depends on **resonance**, damping, and force duration.  

## 3.8 General Solution and Green’s Function  

- The **general solution** of the SDOF equation combines:  
  * **Homogeneous solution** (free vibration)  
  * **Particular solution** (forced vibration)  

- **Green’s Function**:  
  A mathematical tool representing the system’s **impulse response**.  
  If $g(t,\tau)$ is Green’s function, then the response is:  

  $$
  x(t) = \int_0^t g(t-\tau)\, F(\tau) \, d\tau
  $$  

## 3.9 Example Problems  

### Example 1: Natural Frequency of an Undamped SDOF System  

A block of mass $m = 100 \, \text{kg}$ is attached to a spring with stiffness $k = 25,000 \, \text{N/m}$.  
Find the natural frequency.  

**Solution**:  

Natural frequency:  
$$
\omega_n = \sqrt{\tfrac{k}{m}} = \sqrt{\tfrac{25000}{100}} = \sqrt{250} = 15.81 \, \text{rad/s}
$$  

Frequency in Hz:  
$$
f_n = \tfrac{\omega_n}{2\pi} = \tfrac{15.81}{6.283} = 2.52 \, \text{Hz}
$$  

### Example 2: Damped Vibration  

A system has $m = 200 \, \text{kg}$, $k = 50,000 \, \text{N/m}$, and damping coefficient $c = 2000 \, \text{Ns/m}$.  
Determine the damping ratio and type of damping.  

**Solution**:  

Natural frequency:  
$$
\omega_n = \sqrt{\tfrac{k}{m}} = \sqrt{\tfrac{50000}{200}} = \sqrt{250} = 15.81 \, \text{rad/s}
$$  

Critical damping coefficient:  
$$
c_c = 2 \sqrt{km} = 2 \sqrt{50000 \times 200} = 2 \times 3162.28 = 6324.56 \, \text{Ns/m}
$$  

Damping ratio:  
$$
\zeta = \tfrac{c}{c_c} = \tfrac{2000}{6324.56} = 0.316 < 1
$$  

📌 Hence the system is **underdamped**.  

### Example 3: Forced Vibration under Harmonic Load  

A machine foundation is modeled as an SDOF system with $m = 500 \, \text{kg}$, $k = 200,000 \, \text{N/m}$, and negligible damping.  
If subjected to harmonic force $F(t) = 1000 \sin(100 t)$, determine whether resonance occurs.  

**Solution**:  

Natural frequency:  
$$
\omega_n = \sqrt{\tfrac{k}{m}} = \sqrt{\tfrac{200000}{500}} = \sqrt{400} = 20 \, \text{rad/s}
$$  

Forcing frequency:  
$$
\omega = 100 \, \text{rad/s}
$$  

Since $\omega \gg \omega_n$,  
📌 **No resonance occurs**. Instead, response amplitude is small due to high forcing frequency.  

---

