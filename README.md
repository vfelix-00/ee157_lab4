# Lab 4: Magnetic Forces and Materials Lab

Vanessa Felix

Lab Partner: Vivian Auduong

## Solenoid Measurement and Analysis

### Overview
The objectives of this lab are to experimentally observe and measure electromechanical force production through the use of a linear solenoid actuator, and to characterize the B-H loop of two materials (ferrite and steel).

We studied electromechanical force production through the use of a linear solenoid actuator. The linear solenoid actuator consists of a coil, a steel frame, and a steel plunger. When the coil is energized, the plunger is pulled into the coil. In this lab, solenoids illustrate the principles of force production very directly. The frame and plunger complete a magnetic path very similar to a pair of “E” cores when the plunger is pulled all the way into the coil. As the plunger pulls out, the gap is gradually increased and the inductance decreases. To calculate the force, we can use the change of inductance with position.

### Materials 

- Solenoid
- Analog Discovery 
- Impedance Analyzer for Analog Discovery
- Tape
- Ruler
- Pliers

### Procedure 

1. We gathered the above materials for the set up.
2. With the spring still attached,the solenoid was hooked up to the power supply. This was to see how they are supposed to work. The power supply was set to 12V and the coils were energized since these solenoids are designed to operate at 12 V. The voltage was lowered until the plunger no longer retracted.
3. The spring was removed to take our measurements. The retaining ring was carefully removed with a pair of pliers. Safety glasses were worn while doing this.
4. We tried to get a feel for the forces involved once the spring was removed. We started out at a lower voltage of about 3V and observed what happened when the power supply was turned on. We then tried pulling on the plunger from when it was fully retracted and the coil was energized.
5. The plunger was held at an extended position, then the supply was turned on. The plunger was moved through its range while the coil was energized. We got a feel for the force as we let the plunger retract.
6. The voltage was gradually increased to 12 V and then we got a feel for how the force changed as the current through the coil increased.

## Measurements 

1. The DC resistance of the coil was measured.
2. The inductance was measured from 10 Hz to 10 kHz with the plunger both fully extended and fully retracted. These plots were saved.
3. Using the Analog Discovery, inductance was measured as a function of the position of the plunger. We measured the low frequency inductance with a range of 10-60 Hz.
4. Electrical tape was wrapped around the plunger to set the position. A photograph was taken of the solenoid with a ruler in the shot to measure the position. We made sure the ruler and plunger were at the same distance from the camera lens. The change in plunger position between measurements was kept around 1mm or under. We took measurements at 1mm intervals from 0mm-11mm. For this measurement, x = 0 was considered to be the position when the plunger was fully retracted. At least 10 inductance measurements were taken at different positions. We wanted more measurement points when the rate of change ∂L/∂x was high.

## Questions

1. Show your measurement of inductance vs. frequency for both the retracted and extended positions. Explain these results, for both scenarios. Also explain why we are more interested in the inductance measurement at low frequencies.

 <img width="933" alt="Fig,Inductance vs frequency, fully retracted" src="https://user-images.githubusercontent.com/71578472/171296232-4b7b9353-0202-4d02-8cf9-fae93d6eaf52.png">
 Figure: Inductance vs Frequency, fully retracted
 
 
 <img width="930" alt="Fig,Inductance vs frequency, fully extended" src="https://user-images.githubusercontent.com/71578472/171296363-95d8d448-ba5b-4d75-98e7-f865f7cff546.png">
 Figure: Inductance vs Frequency, fully extended
 
 
 
We are more interested in the inductance measurement at low frequencies because at high frequencies, an inductor acts like an open circuit and the inductance decreases. The inductance measured at 10 Hz was approximately 162 mH. The air gap was minimized when the plunger was fully retracted. The inductance measured at 10 kHz was approximately 42 mH. The air gap was maximized when the plunger was fully extended. 

Inductance is inversely proportional to the length of the air gap. As the air gap increases, the inductance decreases. The general relation for reactance is R = l /uA and the general relation for inductance is L = N^2/R = N^2uA/l. Since μ0, the permeability of free space, is much smaller than the magnetic constant of magnetic materials, the reactance due to the air gap dominates for an inductor. 

2. Plot L vs. x using the data you collected. Is this a fairly smooth curve? Should it be? Please explain what you are seeing.

<img width="723" alt="Inductance vs position at 10Hz" src="https://user-images.githubusercontent.com/71578472/171299712-2a07f603-a763-42c5-86af-81a6f79a3aa8.png">
Figure: Inductance vs Position, at 10 Hz 

This is a fairly smooth curve. We are seeing the curve be close to a straight line which can be expected with the linear inductance assumption.

3. If your data is noisy, consider fitting the plot of L vs. x using a curve fitting technique of your choosing. (Piece-wise linear, polynomial, etc. are fine. Anything that looks visually in-line with your data will be satisfactory).

<img width="722" alt="frequency with fitted polynomial " src="https://user-images.githubusercontent.com/71578472/171300084-6ee0d3b7-dde3-445b-9f49-ed376f16ed25.png">
Figure: Inductance vs Position, at 10 Hz with fitted polynomial of degree 1 with the equation: L = 1.9x^2 − 35.8x + 215.1

 
4. Estimate the force as a function of position at 12V.
- Assume that the co-energy and the energy are equal (the linear inductance assumption).
- Assume the current in the inductor is constant, and governed by the DC resistance of the coil.
- Plot your estimate of force ( ∂CE/ ∂x ).

For L = i , and co-energy the area under the λ − i curve, co-energy CE is given by CE = 1/2 * L(x)i^2.

Use polyfit equation L = 1.9x^2 − 35.8x + 215.1 and convert into standard units for inductance.  
L = 0.0019(H/mm^2)x^2 − 0.0358(H/mm)x + 0.2151H for x in mm and L in H.

DC resistance was R = 14.383 ohms. For a 12 V DC voltage:
CE = 1/2*(0.0019(H/mm^2)x^2 − 0.0358(H/mm)x + 0.2151H)(12V/14.383ohms)^2 = 0.000661x^2 − 0.0126x + 0.0749

F(x) = ∂CE/∂x = 0.000661(N/mm)x − 0.0126N

We plotted the result below. 

<img width="757" alt="force vs position" src="https://user-images.githubusercontent.com/71578472/171301496-39f62fed-8b5d-4b4e-9986-8d93b910de09.png">
Figure: Force vs Position

5. Does this comport with your experience using the solenoid? Explain your results.

Yes, this comports with our experience using the solenoid. In lab, we noticed that as the plunger was pushed further in, it was increasingly difficult to move the plunger.

## Core Material Characterization

### Overview 

Cores can be used to create higher performance magnetic components, but the cores themselves introduce losses. These losses are associated with eddy currents and hysteresis. These effects were measured in lab. We obtained an experimental trace of the B−H loop of a ferrite and of steel.


<img width="377" alt="Conceptual sketch of a B−Hcurve" src="https://user-images.githubusercontent.com/71578472/171322309-6cb0f6a7-d392-4333-86a5-9aca542af438.png">
Figure: Conceptual sketch of a B−H curve

In a toroidal inductor, the magnetic field H is proportional to the current in the coil (i(t) = 1/N*Hc*lc), while the magnetic flux density B is proportional to the integral of the voltage on the coil (i(t) = N*Ac*dBc/dt).

Using the output of the audio amplifier, we applied a large sinusoidal signal at various frequencies across the terminals of the inductor/solenoid, and we measured the resulting voltage and current. The data was then processed on our computer to plot the B−H curves.

### Materials

- Solenoid
- 330 uH ferrite inductor rated at 1.06 A (Coilcraft DC1012-334L)
- 4 Ω, 75 W power resistor
- Current probe
- Differential voltage probe
- Audio amplifier
- BNC to RCA adapter

### Measuring ac voltage across and current through the solenoid

The AC voltage across and current through the solenoid was measured. For important precautions, we ensured that the signal generator output was set to High Impedance (Z) Output. We also ensured that the volume knob of our audio amplifier was set to zero when we turned it on. We were careful to not leave the audio amplifier unattended when turned on.

#### Procedure 

1. With the audio amplifier OFF, the signal generator was connected to one input channel of the audio amplifier using a BNC cable and the BNC to RCA adapter. We started with a 100 Hz, 200 mV sine wave.
2. The terminals of the solenoid were connected to the corresponding output channel of the audio amplifier.
3. On channel 1 of our oscilloscope, the differential probe was used to probe the voltage across the terminals of the solenoid. On channel 2, the current going into the solenoid was probed.
4. We ensured that the ‘Volume’ knob on the audio amplifier was set to zero. The audio amplifier was turned on. We slowly increased the ‘Volume’ knob to maximum. We used the XY feature of the oscilloscope (in the ‘Horizontal’ menu) to view voltage vs. current.
5. We collected a range of frequencies, ranging from 40 Hz to 100 Hz and higher and lower. We also collected measurements of when the plunger was fully retracted from the frame and when the plunger was fully inserted into the frame. We saved a few periods of voltage and current data as a CSV file (20,000 points). We made sure we were not in XY mode when saving data.

### Measuring ac voltage across and current through the ferrite inductor

An important action for set up was to connect the 4 Ω, 75 W power resistor in series with the inductor. We made sure to measure the voltage across the inductor, and not the voltage across the resistor and inductor together.

#### Procedure 

1. We repeated the above steps with the ferrite inductor instead of the solenoid. The important modification here was to have the 4 Ω, 75 W power resistor in series with the inductor we were measuring. This was to ensure that the impedance of the load was never below the specified rating of the audio amplifier, which could have caused a large current spike that could damage the amplifier.
2. Again, we collected a range of frequencies, ranging from 200 Hz to 400 Hz and higher and lower. We saved a few periods of voltage and current data as a
CSV file (20,000 points) and we made sure we were not in XY mode when saving data.

### Questions

1. For both the inductor and solenoid, provide plots of the integral of voltage across the coil integral of v(t)dt vs. current through the coil i(t) for the various frequencies that you collected. To get a sensible plot, you should first extract one period of data from your measurements, and remove any dc offset (e.g. x-mean(x) for some vector x in MATLAB). Ensure that your axes are labeled appropriately.

<img width="612" alt="lab 4 p1" src="https://user-images.githubusercontent.com/71578472/171329413-4424eb43-3599-446c-9bd7-1f2ce8285afd.png">

<img width="617" alt="lab 4 p2" src="https://user-images.githubusercontent.com/71578472/171329475-84e72b9d-9f22-4645-b418-00ce59e7eb49.png">

<img width="621" alt="lab 4 p3" src="https://user-images.githubusercontent.com/71578472/171329517-b34f99ce-2d1d-4c5a-ae4c-c288bbc83979.png">

<img width="612" alt="lab 4 p4" src="https://user-images.githubusercontent.com/71578472/171329601-c0e44ecd-e499-4626-a541-3ad28d0ba376.png">

<img width="619" alt="lab 4 p5" src="https://user-images.githubusercontent.com/71578472/171329656-4e37db82-5740-4587-b22d-f5a4770383b5.png">

<img width="610" alt="lab 4 p6" src="https://user-images.githubusercontent.com/71578472/171329720-ca3a6291-b06f-4905-bdc9-6b23877ad16f.png">

<img width="598" alt="lab 4 p7" src="https://user-images.githubusercontent.com/71578472/171329774-76224fb9-2335-434e-a364-870e7d34608d.png">

<img width="619" alt="lab 4 p8" src="https://user-images.githubusercontent.com/71578472/171329817-eb15ffc7-4aea-4a5e-8cef-9556d1cee8a9.png">

<img width="553" alt="lab 4 p9" src="https://user-images.githubusercontent.com/71578472/171329894-383fbe81-ef32-40e8-9030-3d09b4fb9fa6.png">

<img width="563" alt="lab 4 p10" src="https://user-images.githubusercontent.com/71578472/171329957-d5999301-35df-487e-ad45-de12d9a0a9d6.png">

<img width="560" alt="lab 4 p11" src="https://user-images.githubusercontent.com/71578472/171330058-18f7e68a-a24f-44e3-9193-e2767161fd40.png">

<img width="555" alt="lab 4 p12" src="https://user-images.githubusercontent.com/71578472/171330100-ae5dc0c3-f1e8-46ca-afaf-af666a26c9ea.png">

<img width="561" alt="lab 4 p13" src="https://user-images.githubusercontent.com/71578472/171330148-27d4df65-9411-4954-96f8-e9db265f7db9.png">

Overall, there was more noise present when the solenoid was retracted. This also required more cycles to get the correct shape which could be due to the irregularity in the shape of the plunger.

2. Using your measurements of the deconstructed solenoid, translate your voltage and current measurements from the solenoid into B and H, and plot for the
frequencies that you collected. At each frequency, calculate an estimate of power loss per cubic centimeter of core for one cycle.

We took measurements of the deconstructed solenoid provided in lab. The measurements included the number of windings, the geometry of the steel frame, and the cross sectional area (thickness).

Coils:
- inner diameter: 13 mm 
- outer diameter: 21 mm 
- height: 34 mm
- wire thickness: 0.64 mm for #22AWG wire

Frame:
- thickness of frame = 2 mm 
- length of frame = 38 mm 
- width of frame = 29 mm 
- height of frame = 29 mm


For each layer, it fits:
(21mm-13mm width per layer)* 0.5/(0.64 mm per wire) = 6.25 turns per layer 

34 mm height/ 0.64mm per wire = 53.125 layers total in height

N = 6.25 turns per layer * 53.125 layers = about 332 turns

Cross-sectional area is given by thickness * height of frame to equal 2 mm * 29 mm.

Length of the closed loop is given by 2 * length of frame + width of frame:
2 * 38mm + 29mm = 105mm, since there are two closed loops along the width of the frame, divided by the solenoid piston.

Number of turns N = 332
Cross sectional area Ac = 5.8x10^−6mm^2 
Length of closed-loop: lc = 0.105m

Volume of the frame:
2*(length of frame + width of frame) * height of frame * thickness = 2 * (3.8cm + 2.9cm) * 2.9cm * 0.2cm = 7.772 cm^3

Since B = 1/NAc times the integral of v(t)dt and H = Ni/c , we plotted B vs H at different frequencies. The power loss per cycle was estimated by calculating the area enclosed by the B-H curve using the formula for the area of an ellipse = pi * ab (a and b are the major and minor radius).

<img width="736" alt="B vs H of solenoid at 40Hz " src="https://user-images.githubusercontent.com/71578472/171353516-d617d5ea-067a-46a4-8081-015b664b014f.png">
Figure: B vs H of solenoid at 40 Hz

Estimated power loss per cycle = 2513.27 W
Estimated power loss per cycle per cm^3 = 323.38W 

<img width="721" alt="B vs H of solenoid at 60Hz " src="https://user-images.githubusercontent.com/71578472/171353844-91da411e-22f0-44bc-91b5-7b8c7a283426.png">
Figure: B vs H of solenoid at 60 Hz 
Estimated power loss per cycle = 1217.38 W
Estimated power loss per cycle per cm^3 = 156.63 W 

<img width="720" alt="B vs H of solenoid at 80Hz" src="https://user-images.githubusercontent.com/71578472/171354075-23f0f92a-03a3-400f-90b4-dc59f13a8e71.png">
Figure: B vs H of solenoid at 80 Hz
Estimated power loss per cycle = 589.0 5W
Estimated power loss per cycle per cm^3 = 75.79 W 

<img width="736" alt="B vs H of solenoid at 100Hz" src="https://user-images.githubusercontent.com/71578472/171354305-2fc6e86a-e8d1-4a4c-93f4-a20056b73f91.png">
Figure: B vs H of solenoid at 100 Hz 
Estimated power loss per cycle = 353.43 W 
Estimated power loss per cycle per cm^3 = 45.47 W



## Conclusion

In conclusion, the general trend we see is that running the solenoid at a higher frequency, results in less power loss per cycle. Inductance is inversely proportional to the length of the air gap. This means that as the air gap increases, the inductance decreases. Lastly, as the plunger was pushed further in, it was increasingly difficult to move the plunger, requiring more force.
