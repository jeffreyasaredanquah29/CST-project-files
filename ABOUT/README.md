# Circular Loop Antenna Analysis & s11 Modeling

An engineering project focused on analyzing the fundamental electromagnetic characteristics of a circular loop antenna. 
This project bridges theoretical wave propagation with practical computational methods,  utilizing numerical scripts and 3D simulation to evaluate performance metrics like radiation intensity,Antenna Impedance, and S11.

---

# Section 1: The Analytical MATLAB Foundation
Utilized electromagnetic theory to construct a numerical model for E-field intensity for a given position vector (r - r'). 
* **Goal:** Establish a solid theoretical baseline for the loop's radiation behavior before moving into 3D space.

# Section 2: Initial Impedance Modeling (Attempt 1)
* **Result:** Built the initial attempt at modeling loop antenna impedance; however, the S11 resulted in low gain and non-existent periodicity. 


# Section 3: 3D Electromagnetic Simulation (CST Studio Suite)
* Brought the design into **CST Studio Suite** to run full 3D electromagnetic simulations.
* **Goal:** Compare simulated data directly against the analytical estimations from MATLAB to find where the theoretical model broke down.

# Section 4: CST Alignment (Attempt 2)
* **The Fix:** Second attempt focused on updating the MATLAB script output to better match the physical CST simulation parameters.
* **Results:** Achieved improved periodicity and gain, though it revealed new engineering constraints—specifically, a low bandwidth and oddly shaped response curves that require further tuning. The CST simulation itself likely needs refinement. There's ripple before the first S11 peak at near 0.5GHz. A -6 dB dip at resonance just reeks of improper tuning upon simulation.

 # Section 5: CST adjustment
   Improved gain through tuning capacitor at port gap resonance formula called for a capacitance of 0.36pF

  # Section 5: MATLAB capacitive tuning
  With the capacitive correction being implemented at the port in CST. The next logical thing is to try to simulate similarly with the MATLAB model Input impedance. Including a tuning capacitance yielded an improved S11 response and cleaner curves; however, it required a smaller capacitance value than CST, differing by a factor of roughly 100.
