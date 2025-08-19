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

![Seismic Waves Diagram](images/seismic_waves.png)
*Fig. 1.1 Seismic waves radiating from the earthquake focus*

📖 **Fun Fact**:
On average, about **500,000 earthquakes** occur worldwide every year, of which \~100,000 are felt by humans, and about 100 cause significant damage.

---

## 1.2 Causes of Earthquakes

Earthquakes are caused by a **sudden release of energy** within the Earth’s crust. This release generates seismic waves that shake the ground. The causes can be broadly classified into **natural** and **anthropogenic (man-made)**.

### 🌍 Natural Causes

1. **Tectonic Movements**

   * Most common cause.
   * Earth’s lithosphere is divided into large tectonic plates that float on the asthenosphere.
   * Movement along **fault lines** (plate boundaries) causes stress buildup → sudden slip → earthquake.
   * Examples: Himalayan earthquakes (India), San Andreas Fault (USA).

   ![Tectonic Plates](images/tectonic_plates.png)
   *Fig. 1.2 Tectonic plate boundaries and earthquake-prone zones*

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

# 1.4 Magnitude

Magnitude is a quantitative measure of the **energy released at the source of an earthquake**. It is a logarithmic scale, meaning each unit increase in magnitude represents a tenfold increase in amplitude of seismic waves and about **31.6 times more energy released**.

## 1.4.1 Richter Scale (Local Magnitude, ML)

- Developed in 1935 by **Charles F. Richter**.
- Based on the amplitude of seismic waves recorded by a standard seismograph.
- Formula:

\[
M_L = \log_{10}(A) - \log_{10}(A_0)
\]

Where:  
- \( A \) = maximum trace amplitude on the seismogram.  
- \( A_0 \) = standard amplitude for a given distance from epicenter.

- Works well for **local earthquakes (within ~600 km)**.  
- Saturates for large earthquakes (M > 6.5).

![Figure Placeholder: Richter Scale graph showing amplitude vs. magnitude](figures/richter_scale.png)

## 1.4.2 Moment Magnitude Scale (Mw)

- Introduced to overcome limitations of the Richter Scale.  
- Based on **seismic moment (M₀)**:

\[
M_w = \frac{2}{3} \log_{10}(M_0) - 6.0
\]

Where:  
\[
M_0 = \mu \cdot A \cdot D
\]  

- \( \mu \) = shear modulus of rock (~3 × 10¹⁰ N/m²).  
- \( A \) = rupture area (m²).  
- \( D \) = average slip on the fault (m).  

- **Does not saturate** for large earthquakes.  
- Now the **most widely used scale globally**.

![Figure Placeholder: Seismic Moment representation (fault slip area × slip displacement × rigidity)](figures/moment_magnitude.png)

## 1.4.3 Comparison of Magnitude Scales

- **Richter (ML):** Local, historical, not reliable for large EQs.  
- **Moment Magnitude (Mw):** Standard for scientific and engineering use.  
- Other scales:
  - **Body-Wave Magnitude (Mb):** Uses P-waves, suitable for distant quakes.  
  - **Surface-Wave Magnitude (Ms):** Based on surface waves (~20s period).  

![Figure Placeholder: Comparison chart of Richter vs. Moment Magnitude for increasing earthquake sizes](figures/magnitude_comparison.png)

## 1.4.4 Energy Released

Approximate energy release in Joules (for reference):

- M 5.0 → \(10^{12}\) J  
- M 6.0 → \(10^{14}\) J  
- M 7.0 → \(10^{16}\) J  
- M 8.0 → \(10^{18}\) J  

This demonstrates the **exponential growth** of energy with increasing magnitude.


✅ *Key Point:* While Richter is of historical importance, **Moment Magnitude (Mw)** is the accepted standard in earthquake engineering and seismology.

---


