# A8 – Gears

## Objective
The objective of this assignment was to createa gearbox that can be disassebmled. The input and output shaft and bearings, and the gearbox were to be calculated and designed parametrically with given gear and pinion files. Assumptions and other known values are listed:

- Gear ratio: 24:9
- Output gear: 1.25 in-lbf, 1100 rpm
- Input shaft (pinion, power-transmission): Ø0.125 in, 1 in long
- Output shaft (gear, short shaft): Ø0.25 in, 1 in long
- Shafts are press fit through the gear hubs; running sliding fit for the shaft holes
- Gear train is ideal; moment of the radial force is ignored

## Shaft Design
The first step to the assignment were creating the input and output shafts. From the machinery's handbook, pages 295-297, covering shafts, the correct equations can be found to determining all the necessary values to design the shaft.


### Input Shaft (Power-Transmission)
The input shaft is consider a power-transmission shaft, as its transmitting the power of course. Power-transmitting has its own equations, and with those I found the power and the shear stress. The given/fixed values of the input shaft were a diameter of .125 inches, 1 inch long, and a yield strength of 4000 psi from the book. The objective is to numerically solve for the shear stress to determine if its a reasonable answer. I calculated the shear stress felt on the shaft was 1220.094 psi, which is sufficient as its below the yield stress. Other values like the power (.0716hp) and diameter equations were also equated incase they had to be changed. In this case they don't.

### Output Shaft (Short Shaft)
The output shaft is a short shaft and has fixed values of a .25 inch diameter, 1 inch long, and 8500 psi from the book. The power and diameter equations change for short shafts, but the shear stress stays the same. The equated shear stress was 407.44 psi-its less than 8500 psi, so its a sufficient answer. The calculated horsepower as .4523 hp as well.


## Journal Bearing Design
<!-- 30% total. (10%) size/length, pressure, velocity, PV, material from the lecture table. (10%) thickness. (10%) McMaster-Carr selection with part names. -->
bearing lengtg , fit class and why

### Input Bearing – Pressure, Velocity, and PV




### Output Bearing – Pressure, Velocity, and PV



### Bearing Material


### Input Bearing – Thickness

### Output Bearing – Thickness




### McMaster-Carr Bearing 
part names fo input and output bearings and how they match 

## Gearbox Housing Sketch
<!-- 5%. Two-component housing; state how the halves fit together (snap fit, nuts and bolts, etc.) and why. -->


fit type and reasoning

## CAD Design and Assembly
<!-- 45%. Parametric critical features starting from known parameters; list McMaster downloads; rest of the model. Note units. -->

### Parameters
key parametric dimensions

### Shafts

#### Input Shaft


#### Output Shaft


### Housing

#### Half 1

#### Half 2


### McMaster-Carr Components
TODO: gear, pinion, and bearing part numbers.

### Assembly


mates used, clearance check between the gears and the housing

## Drawings (MEGR 2157)
<!-- 30%. Six multi-view drawings + one assembly. Third-angle projection, ASME Y14.5, tolerance block X.X ±.02 / X.XX ±.01 / X.XXX ±.005, at least two callouts with different tolerancing on critical features. Delete this section if drawings go on a separate page. -->




## Lessons Learned


