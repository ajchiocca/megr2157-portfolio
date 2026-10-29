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
The first step to the assignment were creating the input and output shafts. From the machinery's handbook, pages 295-297, covering shafts, the correct equations can be found to determining all the necessary values to design the shaft. The work for both shafts are on this one image.
![A8](ShaftWork.png)

### Input Shaft 
The input shaft is consider a power-transmission shaft, as its transmitting the power of course. Power-transmitting has its own equations, and with those I found the power and the shear stress. The given/fixed values of the input shaft were a diameter of .125 inches, 1 inch long, and a yield strength of 4000 psi from the book. The objective is to numerically solve for the shear stress to determine if its a reasonable answer. I calculated the shear stress felt on the shaft was 1220.094 psi, which is sufficient as its below the yield stress. Other values like the power (.0716hp) and diameter equations were also equated incase they had to be changed. In this case they don't.

### Output Shaft 
The output shaft is a short shaft and has fixed values of a .25 inch diameter, 1 inch long, and 8500 psi from the book. The power and diameter equations change for short shafts, but the shear stress stays the same. The equated shear stress was 407.44 psi-its less than 8500 psi, so its a sufficient answer. The calculated horsepower as .4523 hp as well.


## Journal Bearings
<!-- 30% total. (10%) size/length, pressure, velocity, PV, material from the lecture table. (10%) thickness. (10%) McMaster-Carr selection with part names. -->
The next part to be modeled are the input and output bearings. I assumed both of the lengths to be 1/4 inches and an RC5 fit for both. The tolerance for the input shaft was .0007 inches, and the tolerance for the output shaft was .0009 inches. Calculating pressure, velocity, and PV were used with their diameters plus their respective tolerance. I added the thickness of the bearing to the rest of the calculations additionally.

### Input Bearing
For the input bearing, the calculated velocity was 96.53 inches*s, pressure 75.99 psi, and PV to be 7335.604. Calculations for the values inside V and P, the radial force and cross sectional area of the shaft were calculated as well. The determined thickness of the input bearing was .1974 inches.
<br>
![A8](InpBWork.png)


### Output Bearing
For the output bearing, the calculated velocity was 71.994 inches*s, pressure 50.929 psi, and PV to be 3666.5824. Calculations for the values inside V and P, the radial force and cross sectional area of the shaft were again calculated as well. The determined thickness of the input bearing was .3927 inches.
<br>
![A8](OutBWork.png)


### Bearing Material.
I chose the bearing material to be dry graphite for both. It is known that its better for the gears to be dissimilar material, which initially I wanted one of the gears material to be phenolics as its one the list of materials in the weeks slides and is still above the shafts PV value. I used solid works to design the gearbox, which to my knowledge doesnt support phenolic material, as in its not a material I could just choose from the catalog. For simplicity, I made them both dry graphite. With a chosen material, the correct bearing can be found on McMaster as long as its the right shaft diameter and length. The McMaster part for the input bearing is Oil-Embedded 841 Bronze Sleeve Bearing for 1/8" Shaft Diameter and 7/32" Housing ID, 1/4" Long, 6391K612, and the McMaster part for the output bearing is Oil-Embedded 841 Bronze Sleeve Bearing for 1/4" Shaft Diameter and 5/16" Housing ID, 1/4" Long, 6391K126.

## Gearbox Housing
The Gearbox is going to house the gear, pinion, two bearing, and the two shafts, hence the title "gearbox housing". My design for the gearbox was to have the two shafts through the same face of the shelled gearbox and the other end having thread pitches is four Black-Oxide Alloy Steel Socket Head Screw, US Origin, 1-64 Thread Size, 1/8" Long (90044A280) between the gearbox and a cover for the gearbox. I used screws as my fit for it would be easy to assemble and disassemble, as its just screws. The sketch may or may not better explain my design, but it will make most sense in the full SolidWorks assembly. The sketch for the gearbox housing under the work for the output bearing, but I'll put the same image here just in case.
<br>
![A8](OutBWork.png)

## CAD Design and Assembly

### Input Shaft
![A8](InpshaftDim.png)

### Output Shaft
![A8](OutshaftDim.png)
### Input bearing 
I'm not sure how to show all the dimensions for both bearings, so I have the parametric equations with the bearings for both as well.
<br>
<br>
![A8](InputBdimReal.png)
![A8](InputBpara.png)
### Output bearing
![A8](OutputBdimReal.png)
![A8](OutputBpara.png)
### Gear
![A8](GearDim.png)
### Pinion
![A8](PinionDim.png)

### Screw
![A8](ScrewDim.png)

### Gearbox
For parametrically design the gearbox, I was unsure on how in depth it had to be, or what its supposed to be, so I inputted values that would be used to dimension the gearbox, but that may not be as parametric as it should be. The only equation based value was the distance between the gear and pinion, which is the sum of their pitch diameter over 2, which yields .6875 inches. I hope that images of the holes, dimensions, and threads in the images explain themselves so I don't have to. The threads were created to work for the screws I used (1-64) for both the gearbox and gearbox cover.
![A8](GBpara.png)
![A8](GBmainDim.png)
![A8](GBholes.png)
![A8](GBthreads.png)

### Gearbox cover
The gearbox cover uses the same parametric model as the gearbox. There are construction lines on the four holes connected to the ends of the cover that haved a fix relation so that it lines up with the threads in the gearbox.
![A8](GBpara.png)
![A8](GBcoverDim.png)
![A8](GBCoverhole.png)

### Full assembly (transparent gearbox cover)
For mating everything together, majority of the fits to align everything were concentric mates. I used coincident mates to keep the bearings and gear/pinion together, and used parallel mates to make the gearbox cover parallel with the gearbox.
<br>
<br>
![A8](AssemblyPic.png)
## Drawings (MEGR 2157)

###Input thaft

###Output shaft

###Input bearing

###Output bearing

###Gearbox

###Gearbox cover

### Assembly
![A8](GBassDRW.png)

<!-- 30%. Six multi-view drawings + one assembly. Third-angle projection, ASME Y14.5, tolerance block X.X ±.02 / X.XX ±.01 / X.XXX ±.005, at least two callouts with different tolerancing on critical features. Delete this section if drawings go on a separate page. -->




## Lessons Learned


