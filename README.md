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

 




