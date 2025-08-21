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

# Unit 1: Introduction to Earthquakes

- [Introduction to Earthquakes](#11-introduction-to-earthquakes)
- [Causes of Earthquakes](#12-causes-of-earthquakes)
- [Basic Terminology](#13-basic-terminology)
- [Magnitude](#14-magnitude)
- [Intensity](#15-intensity)
- [Peak Ground Motion Parameters](#16-peak-ground-motion-parameters)

## 1.1 Introduction to Earthquakes

An **earthquake** is a sudden shaking or vibration of the Earth’s surface caused by the release of stored energy in the Earth’s crust. This energy is released in the form of **seismic waves**, which travel through the ground and cause the motion that we feel.

* Earthquakes are among the most destructive natural disasters, leading to:

  * Structural failures of buildings and infrastructure
  * Loss of life and property
  * Secondary hazards (fires, tsunamis, landslides, liquefaction)

📌 **Engineering Importance**
For civil engineers, understanding earthquakes is crucial because:

* Most traditional structures are designed for static loads (gravity), not dynamic loads (seismic).
* Earthquakes produce **lateral forces and ground motions** that can cause catastrophic damage if not considered.
* Seismic design codes (like IS 1893) provide guidelines for ensuring **safety and serviceability** of structures.

<img width="649" height="478" alt="image" src="https://github.com/user-attachments/assets/633ab5b1-7cb3-4a26-9326-4af80bb08c71" />

*Fig. Seismic waves radiating from the earthquake focus*

📖 **Fun Fact**:
On average, about **500,000 earthquakes** occur worldwide every year, of which \~100,000 are felt by humans, and about 100 cause significant damage.

---

## 1.2 Causes of Earthquakes

Earthquakes are caused by a **sudden release of energy** within the Earth’s crust. This release generates seismic waves that shake the ground. The causes can be broadly classified into **natural** and **anthropogenic (man-made)**.

### 🌍 Natural Causes

1. **Tectonic Movements**

   * Most common cause.
   * Earth’s lithosphere is divided into large tectonic plates that float on the
     <span title="A semi-molten, mechanically weak layer in the Earth's upper mantle.">asthenosphere</span>.
   * Movement along **fault lines** (plate boundaries) causes stress buildup → sudden slip → earthquake.
   * Examples: Himalayan earthquakes (India), San Andreas Fault (USA).

<img width="959" height="435" alt="image" src="https://github.com/user-attachments/assets/f2e809e0-3722-405b-885b-d01201787170" />

*Fig. **Crustal generation and destruction** - Three-dimensional diagram showing crustal generation and destruction according to the theory of plate tectonics; included are the three kinds of plate boundaries—divergent, convergent (or collision), and strike-slip (or transform). Tectonic plate boundaries and earthquake-prone zones*

2. **Volcanic Activity**

   * Earthquakes often accompany volcanic eruptions.
   * Caused by movement of magma inside the Earth.
   * Usually localized but can be destructive.

3. **Collapse Earthquakes**

   * Occur due to sudden collapse of underground caves, caverns, or mines.
   * Localized and smaller in magnitude.

4. **Reservoir-Induced Seismicity**

   * Large water reservoirs (dams) exert pressure on Earth’s crust.
   * Can trigger earthquakes in surrounding areas (e.g., Koyna Dam, India).

### 🏗️ Anthropogenic (Man-Made) Causes

* **Mining and Quarrying** – Explosions and underground excavation disturb stress balance.
* **Nuclear Explosions / Tests** – Artificially generated seismic events.
* **Deep Fluid Injection / Extraction** – Oil, gas, or geothermal drilling can induce seismicity.

📌 **Key Point for Civil Engineers**
While tectonic earthquakes are the **most significant** for structural design, engineers must also be aware of other induced seismic activities that may affect infrastructure.

---

# 1.3 Basic Terminology

Understanding earthquake engineering requires familiarity with some essential terms. These terms are frequently used in seismology, earthquake-resistant design, and building codes.

---

## 1.3.1 Focus (Hypocenter)

* The point inside the Earth where the earthquake originates.
* Energy is released here due to fault rupture.
* Located at a certain depth below the surface.

**Figure 1.3.1: Hypocenter inside the Earth (placeholder)**

## 1.3.2 Epicenter

* The point on the Earth’s surface vertically above the focus.
* Commonly reported in earthquake data (e.g., “epicenter near Delhi”).

**Figure 1.3.2: Epicenter vs. Focus (placeholder)**

## 1.3.3 Fault

* A fracture in the Earth’s crust where displacement has occurred.
* Earthquakes are usually caused by sudden slip along faults.

Types of faults:

* Normal Fault
* Reverse (Thrust) Fault
* Strike-Slip Fault

**Figure 1.3.3: Types of Faults (placeholder)**

## 1.3.4 Seismic Waves

* Energy waves that propagate from the focus through the Earth.
* Categories:

  * **Body Waves** (travel through Earth’s interior)

    * *P-waves*: Primary, compressional, fastest.
    * *S-waves*: Secondary, shear, slower than P-waves.
  * **Surface Waves** (travel along the surface)

    * Love Waves, Rayleigh Waves.

**Figure 1.3.4: Different seismic waves (placeholder)**

## 1.3.5 Seismograph & Seismogram

* **Seismograph**: Instrument used to record ground motion.
* **Seismogram**: Graphical output showing wave patterns.

**Figure 1.3.5: Typical seismogram (placeholder)**

## 1.3.6 Isoseismal Lines

* Lines drawn on a map connecting points of equal earthquake intensity.
* Useful for showing how shaking varies across a region.

---

## 1.4 Magnitude

**Magnitude** is a quantitative measure of the **energy released at the earthquake source**. It’s **logarithmic**: each unit increase in magnitude corresponds to a **tenfold increase in recorded wave amplitude** and about **$10^{1.5}\approx 31.6$ times more energy released**.

### 1.4.1 Richter Scale (Local Magnitude, $M_L$)

Developed by Charles F. Richter (1935) for local earthquakes.

Display form:

$$
M_L = \log_{10}(A) - \log_{10}(A_0)
$$

Where:

* $A$ = maximum trace amplitude on the seismogram,
* $A_0$ = reference amplitude (calibrated for distance/instrument).

Notes:

* Best for **local events** (typically within \~600 km).
* **Saturates** for large earthquakes (roughly $M>6.5$).

![Figure Placeholder: Richter Scale graph showing amplitude vs. magnitude](figures/richter_scale.png)

### 1.4.2 Moment Magnitude Scale ($M_w$)

Designed to work for **all earthquake sizes** (does **not** saturate). Defined from **seismic moment** $M_0$:

$$
M_w = \frac{2}{3}\,\log_{10}\!\left(M_0\right) - 6.0
$$

with

$$
M_0 = \mu \, A \, D
$$

Where:

* $\mu$ = shear modulus (rigidity) of rock $\left[\text{N/m}^2\right]$,
* $A$ = rupture area $\left[\text{m}^2\right]$,
* $D$ = average slip on the fault $\left[\text{m}\right]$.

*(Constant $6.0$ is an approximation; values like $6.06$ are also used depending on units and calibration.)*

![Figure Placeholder: Seismic Moment representation (fault area × slip × rigidity)](figures/moment_magnitude.png)

### 1.4.3 Other Magnitude Scales

* **Body-Wave Magnitude** $M_b$: based on P-waves (useful for teleseismic, smaller events).
* **Surface-Wave Magnitude** $M_s$: based on long-period surface waves (\~20 s).
* Historical $M_L$ vs. modern $M_w$: $M_w$ is the **standard** for engineering and seismology.

![Figure Placeholder: Comparison chart of ML, Ms, and Mw for increasing earthquake size](figures/magnitude_comparison.png)

### 1.4.4 Energy Released

Empirical relation between **radiated energy $E$** (Joules) and **$M_w$**:

$$
\log_{10} E \;=\; 1.5\, M_w \;+\; 4.8
$$

Approximate energies:

* $M_w = 5$ → $E \approx 2 \times 10^{12}\ \text{J}$
* $M_w = 6$ → $E \approx 6 \times 10^{13}\ \text{J}$
* $M_w = 7$ → $E \approx 2 \times 10^{15}\ \text{J}$
* $M_w = 8$ → $E \approx 6 \times 10^{16}\ \text{J}$

✅ *Key Point:* While Richter is of historical importance, **Moment Magnitude (Mw)** is the accepted standard in earthquake engineering and seismology.

---

## 1.5 Intensity

### Definition

* **Seismic Intensity** is a qualitative measure of the effects of an earthquake at a specific location, as perceived by people, damage to structures, and changes in the natural environment.
* Unlike **magnitude**, which is a single value describing the energy released at the source, **intensity varies with location** and diminishes with increasing distance from the epicenter.

---

### Common Intensity Scales

1. **Modified Mercalli Intensity (MMI) Scale** (I–XII)

   * Based on human perception and damage to buildings.
   * Example:

     * MMI I – Barely felt, only by sensitive instruments.
     * MMI VI – Felt by all, slight damage to weak structures.
     * MMI XII – Total destruction.

   ![Figure Placeholder: MMI scale effects on structures and people](figures/MMI_scale.png)

2. **Medvedev–Sponheuer–Karnik (MSK) Scale** (I–XII)

   * Widely used in India and Europe.
   * Considers structural response of buildings, ground effects, and human perception.

   ![Figure Placeholder: MSK intensity classification](figures/MSK_scale.png)

3. **European Macroseismic Scale (EMS-98)**

   * Improved version of MSK scale, used in Europe.
   * Provides detailed building vulnerability and damage grades.

---

### Relation between Intensity and Ground Motion

* Intensity is correlated with **peak ground acceleration (PGA)** and **peak ground velocity (PGV)**.
* However, it is not a direct physical measurement but rather an **observational description**.

---

### Real-World Examples

* **Bhuj Earthquake, 2001 (Magnitude \~7.7)**

  * Epicentral region: Intensity X–XI (devastating damage).
  * Ahmedabad (\~250 km away): Intensity VI–VII (moderate to strong shaking).

* **Nepal Earthquake, 2015 (Magnitude \~7.8)**

  * Kathmandu: Intensity VIII–IX (heavy damage to buildings).
  * Northern India: Intensity IV–V (felt by people indoors, minor effects).

---

### Difference between Magnitude and Intensity

| **Aspect**     | **Magnitude**                                     | **Intensity**                                           |
| -------------- | ------------------------------------------------- | ------------------------------------------------------- |
| **Definition** | Quantitative measure of energy released at source | Qualitative measure of effects at a location            |
| **Scale Used** | Richter, Moment Magnitude (Mw), etc.              | MMI, MSK, EMS-98                                        |
| **Nature**     | Instrumental, single value per earthquake         | Observational, varies from place to place               |
| **Dependence** | Depends on fault rupture and energy release       | Depends on distance, geology, and local site conditions |
| **Range**      | Typically 0–10                                    | Typically I–XII                                         |
| **Example**    | Bhuj 2001: Magnitude 7.7                          | Intensities ranged from VI to XI regionally             |

---

# **1.6 Peak Ground Motion Parameters**

Peak ground motion parameters are quantitative measures that describe the maximum response of the ground during an earthquake. They are crucial for **engineering design**, **seismic hazard assessment**, and **structural safety evaluation**. Unlike intensity (a qualitative measure of earthquake effects on people and structures), peak ground motion parameters provide **instrumental, numerical values** recorded by seismographs.

## **1.6.1 Key Parameters**

1. **Peak Ground Acceleration (PGA)**

   * Definition: The maximum absolute value of ground acceleration during an earthquake.
   * Mathematical Representation:

     $$
     PGA = \max \left| \ddot{u}(t) \right|
     $$

     where $\ddot{u}(t)$ = ground acceleration at time $t$.
   * Units: usually expressed in **g** (acceleration due to gravity, $9.81 \, m/s^2$).
   * Engineering Use:

     * Strong correlation with **structural damage**.
     * Used as a design input in **building codes** (e.g., IS 1893 in India).

   *(Insert Figure 1.6.1: Example ground acceleration time-history showing PGA)*


2. **Peak Ground Velocity (PGV)**

   * Definition: The maximum absolute value of ground velocity during shaking.
   * Mathematical Representation:

     $$
     PGV = \max \left| \dot{u}(t) \right|
     $$

     where $\dot{u}(t)$ = ground velocity.
   * Units: cm/s or m/s.
   * Engineering Use:

     * Better indicator of **structural response** (especially for flexible structures).
     * Often correlated with **damage to lifelines** (e.g., pipelines, bridges).

   *(Insert Figure 1.6.2: Example velocity time-history showing PGV)*

3. **Peak Ground Displacement (PGD)**

   * Definition: The maximum absolute value of ground displacement during shaking.
   * Mathematical Representation:

     $$
     PGD = \max \left| u(t) \right|
     $$
   * Units: cm or m.
   * Engineering Use:

     * Important for **long-period structures** (e.g., tall buildings, bridges).
     * Useful in **permanent ground deformation studies**.

   *(Insert Figure 1.6.3: Example displacement time-history showing PGD)*

## **1.6.2 Inter-relationships**

* PGA, PGV, and PGD are **interconnected** through ground motion frequency content.
* In general:

  * **High-frequency earthquakes** → larger PGA, smaller PGD.
  * **Low-frequency earthquakes** → larger PGD, smaller PGA.

*(Insert Figure 1.6.4: Illustration comparing ground motions of high vs. low frequency earthquakes and their peak values)*


## **1.6.3 Engineering Applications**

1. **Seismic Design Codes**

   * PGA values define **seismic zones** (e.g., IS 1893 in India specifies design PGA).

2. **Damage Assessment**

   * PGV often correlates with **structural and non-structural damage**.

3. **Disaster Preparedness**

   * Rapid PGA and PGV estimates are used in **Earthquake Early Warning Systems (EEWS)**.

## **1.6.4 Example: 2001 Bhuj Earthquake (Mw 7.7)**

* Recorded PGA: \~0.35g in Kachchh region.
* PGV: \~40 cm/s.
* PGD: up to \~30 cm.
* Observation:

  * **Near-source regions** showed very high PGA leading to collapse of unreinforced masonry.
  * **Farther regions** had lower PGA but still experienced structural vibrations due to PGV.

## **1.6.5 Summary Table**

| Parameter                | Symbol | Units       | Typical Use                                   |
| ------------------------ | ------ | ----------- | --------------------------------------------- |
| Peak Ground Acceleration | PGA    | g or m/s²   | Building code design, damage potential        |
| Peak Ground Velocity     | PGV    | cm/s or m/s | Lifeline and infrastructure response          |
| Peak Ground Displacement | PGD    | cm or m     | Long-period structures, permanent deformation |

---






