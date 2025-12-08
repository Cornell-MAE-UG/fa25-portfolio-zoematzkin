---
layout: project
title: MAE 3270 Torque Wrench
description: Advanced CAD Project
technologies: [Autodesk Fusion, Ansys, MATLAB]
image: /assets/images/radio-machine-cad.jpg
---

For a class, we were asked to CAD a complex object. This design was...Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut nec accumsan leo. Pellentesque ornare orci enim, vitae vestibulum nibh rutrum in. Donec pharetra risus nec ipsum fringilla, et mattis tortor auctor. Duis tortor ante, posuere ut odio a, scelerisque interdum purus. Aenean faucibus luctus est, sed bibendum tellus. 

The goal for this torque wrench is for it to withstand a 600 in-lbf moment on its driver while be supported at the end of its shaft. It shall have a factor of safety of 4 against yield, a factor of safety of 2 against crack growth (for a crack 0.04 in deep) and a factor of safety of 1.5 for fatigue stress. It also needs a 1.0 mV/V output for its strain.

 With all of this considered, a MATLAB script meant to analyze the stresses from bending was used to find these values:
 <br>
Geometry:
Outer radius: ro = 0.4 in
Inner radius: ri = 0.3 in
Distance from center of drive to strain gauge: c = ro
Length of wrench: L = 18 in
<br>
Material Properties (Ti–6Al–4V):
Young’s modulus: E = 16.5×10^6 psi
Ultimate tensile strength: ou = 138.0×10^3 psi
Fracture toughness: KIC = 68.3×10^3 psi·√in
Fatigue strength at 10^6 cycles: S = 74.0×10^3 psi
<br>
<br>
This yielded these results:
Max Stress: 17,461.57 psi
Max Deflection: 0.22577 in
Strength Safety Factor: 7.9031
Fracture Safety Factor: 11.034
Fatigue Safety Factor: 4.2379
mV/V: 1.0583
Ti-6Al-4V was chosen due to its high tensile strength and fracture toughness yet its relatively low youngs modulus. High strength and toughness is important to prevent the part from breaking, and it allows for a thinner geometry. This thinner geometry will allow for the part to experience more strain, which will help the strain gauge get a better reading. The relatively low Young's modulus further helps the wrench have more strain. Essentially, this is a ductile material. On top of its structural benefits, it is also quite light, known for its high strength to weight ratio.
Shown below is an FEM model of the torque wrench, where it was fixed on the driver and a 37.5 lb force was applied at its end. Its maximum deflection is 0.27274 in, and its maximum stress was 46227 psi after refinement. 


![Shaded rendering of earlier version]({{ "/assets/images/radio-machine.jpg" | relative_url }}){: .inline-image-r style="width: 200px"}

Nulla et magna urna. Morbi a ipsum sollicitudin, rhoncus risus volutpat, ultricies nunc. Quisque mollis finibus ante id imperdiet. Quisque vehicula elit sit amet felis facilisis fermentum.

Aenean tincidunt aliquam arcu, in euismod dui dapibus eu. In placerat, mi et ultrices consequat, quam ligula cursus mauris, in semper neque nibh at est. Maecenas hendrerit dignissim porta. Phasellus nec fringilla dolor. Etiam efficitur nisi sit amet velit pharetra feugiat. Etiam ultrices turpis at leo semper, eleifend scelerisque neque malesuada. Aliquam molestie congue rhoncus. Donec blandit neque dolor, nec tristique mi pretium ac. Mauris tincidunt ullamcorper magna, nec pellentesque mi sagittis quis.

I was inspired by this old radio when I made this rendering:

![Photo of old radio]({{ "/assets/images/old-radio.jpg" | relative_url }}){: .inline-image-l}

Aenean tincidunt aliquam arcu, in euismod dui dapibus eu. In placerat, mi et ultrices consequat, quam ligula cursus mauris, in semper neque nibh at est. Maecenas hendrerit dignissim porta. Phasellus nec fringilla dolor. Etiam efficitur nisi sit amet velit pharetra feugiat. Etiam ultrices turpis at leo semper, eleifend scelerisque neque malesuada. Aliquam molestie congue rhoncus. Donec blandit neque dolor, nec tristique mi pretium ac. Mauris tincidunt ullamcorper magna, nec pellentesque mi sagittis quis.

Aenean tincidunt aliquam arcu, in euismod dui dapibus eu. In placerat, mi et ultrices consequat, quam ligula cursus mauris, in semper neque nibh at est. Maecenas hendrerit dignissim porta. Phasellus nec fringilla dolor. Etiam efficitur nisi sit amet velit pharetra feugiat. Etiam ultrices turpis at leo semper, eleifend scelerisque neque malesuada. Aliquam molestie congue rhoncus. Donec blandit neque dolor, nec tristique mi pretium ac. Mauris tincidunt ullamcorper magna, nec pellentesque mi sagittis quis.
