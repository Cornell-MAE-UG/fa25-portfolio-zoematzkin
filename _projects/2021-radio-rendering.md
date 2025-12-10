---
layout: project
title: MAE 3270 Torque Wrench
description: Advanced FEM Project
technologies: [Autodesk Fusion, Ansys, MATLAB]
image: /assets/images/driver.png
---

The goal for this torque wrench is for it to withstand a 600 in-lbf moment on its driver while be supported at the end of its shaft. It shall have a factor of safety of 4 against yield, a factor of safety of 2 against crack growth (for a crack 0.04 in deep) and a factor of safety of 1.5 for fatigue stress. It also needs a 1.0 mV/V output for its strain.

 With all of this considered, a MATLAB script meant to analyze the stresses from bending was used to find these values:
 <br>
Geometry:<br>
-Outer radius: ro = 0.4 in<br>
-Inner radius: ri = 0.3 in<br>
-Distance from center of drive to strain gauge: c = ro<br>
-Length of wrench: L = 18 in<br>
<br>
Material Properties (Ti–6Al–4V):<br>
-Young’s modulus: E = 16.5×10^6 psi<br>
-Ultimate tensile strength: ou = 138.0×10^3 psi<br>
-Fracture toughness: KIC = 68.3×10^3 psi·√in<br>
-Fatigue strength at 10^6 cycles: S = 74.0×10^3 psi<br>
<br>
![Shaded rendering of earlier version]({{ "/assets/images/tr0.png" | relative_url }}){: style="width: 60%;"}

<br>
This yielded these results:
-Max Stress: 17,461.57 psi<br>
-Max Deflection: 0.22577 in<br>
-Strength Safety Factor: 7.9031<br>
-Fracture Safety Factor: 11.034<br>
-Fatigue Safety Factor: 4.2379<br>
-mV/V: 1.0583<br>
<br>
Ti-6Al-4V was chosen due to its high tensile strength and fracture toughness yet its relatively low youngs modulus. High strength and toughness is important to prevent the part from breaking, and it allows for a thinner geometry. This thinner geometry will allow for the part to experience more strain, which will help the strain gauge get a better reading. The relatively low Young's modulus further helps the wrench have more strain. Essentially, this is a ductile material. On top of its structural benefits, it is also quite light, known for its high strength to weight ratio.
Shown below is an FEM model of the torque wrench, where it was fixed on the driver and a 37.5 lb force was applied at its end. Its maximum deflection is 0.27274 in, and its maximum stress was 46227 psi after refinement. <br>
<br>
Shown below is an FEM model of the torque wrench, where it was fixed on the driver and a 37.5 lb force was applied at its end. Its maximum deflection is 0.27274 in, and its maximum stress was 46227 psi after refinement. These results are close to what was predicted. The stress was slightly higher but that is due to stress concentrations, and I believe that because the stress just keeps going up as you refine, the stress at these tiny points should not be worried too much about. The deflection is also a little higher, likely due to other factors that the MATLAB does not take into account like torsion on the bottom of the driver. It is still within the needed factor of safety. In terms of strain gauge voltage reading, with a strain gauge with a GF of two, the strain from FEM (4e-4) yields a voltage of exactly 1 mV.



![Shaded rendering of earlier version]({{ "/assets/images/tr1.png" | relative_url }}){: style="width: 60%;"}

![Shaded rendering of earlier version]({{ "/assets/images/tr2.png" | relative_url }}){: style="width: 60%;"}

![Shaded rendering of earlier version]({{ "/assets/images/tr3.png" | relative_url }}){: style="width: 60%;"}

![Shaded rendering of earlier version]({{ "/assets/images/tr4.png" | relative_url }}){: style="width: 60%;"}

![Shaded rendering of earlier version]({{ "/assets/images/tr5.png" | relative_url }}){: style="width: 60%;"}

![Shaded rendering of earlier version]({{ "/assets/images/tr6.png" | relative_url }}){: style="width: 60%;"}



