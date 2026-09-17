# A4 – Motor Mount
![motord](motord.png)
![all](all.png)



## Feature 1
The first task of the assignment was to design for feature 1, the face where the motor will connect too. For simplicity, feature 1 can be treated as a cantilever beam. the applied force of 300N on the shaft of the motor is translated to the moment on feature 1, which would be the force times the chosen length. From the cross sectional area of the beam, the base/width of the area is the dimension that will be optimized for bending and deflection to find the minimum width the mount should be to account for both. The height and length of the beam where predetermined by me.
<br>
![feet1](feet1.png)
<br>
I created the free body diagram for feature 1 as a cantilever beam and rearranged the bending moment and maximum deflection equations to solve for the base dimension, that way all known variables are on the right side of the equation. I've chosen the motor mount material to be PETG which has a modulus of elasticity of 2.145 Gigapascals, or 2145 Megapascals. The other known variables indicated as such:
<br>
<br>
Length (L) = 44 millimeters
<br>
Moment (M) = 300N * 44mm = 13200 Nmm
<br>
Height (h) = 20mm
<br>
distance from N.A (C) = 20/2 = 10mm
<br>
Safety factor (S.F) = 3
<br>
Deflection (delta) = 0.30mm
<br>
yield strength of PETG (Sy) = 50 MPa
<br>
<br>
![Ft1w](Ft1w.png)
<br>
<br>
Equating the base dimension for both equations gave a width of 11.88 millimeters and 29.78 millimeters. the width must account for both bending and deflection, so the minimum width should be 29.78 millimeters. The motor itself has a diameter of 28 millimeters on the body, so it would have to be a larger dimension regardless. note that the allowable stress for the beam wasn't calculated before hand, as that explains why the yield strength and safety factor are part of the known variables and not comprised into the allowable stress. Both methods give the same base width. There are obviously some design "critiques", for the height of the beam extends beyond the motors shaft, but if you were to graph the base dimension as a function of the height, any height measurement below 20 gives a height dimension that may be considered unreasonable, or at least in my opinion.
<br>
<br>
![desmos](desmos.png)

## Feature 2
The other feature of the motor mount is feature 2, where it would be attached to the wall/act as the wall. I treated feature 2 as another cantilever beam, rotating it to the same orientation as the free body diagram for feature 1, and because the base dimension is already found, and has to stay that dimension, the height must be optimized for bending and deflection instead. The height in this case would be how much the features extruded to. The same bending moment and maximum deflections were used, only solving for height now, and the base as a new varible:
<br>
<br>
Length (L) = 44 millimeters
<br>
Moment (M) = 300N * 44mm = 13200 Nmm
<br>
Allowable stress(sigma) = 16.67 MPa
<br>
Elasticity of PETG (E) = 2145 MPa
<br>
Deflection (delta) = 0.30mm
<br>
Base (b) = 29.78mm
<br>
<br>
![Ft2w](Ft2w.png)
<br>
<br>
The two equations gave a height of 12.609 millimeters and 15.857 millimeters. To account for both bending and deflection, the largest value, 15.857 millimeters must be the chosen height for feature 2. 

## Sketch
With all the dimensions for the motor mount without the holes/other features in the design, an isometric view of the motor mount can made. Note that the dimensions labelled on the isometric are not drawn to scale. An accurate isometric view would have a broader/square shape.
<br>
<br>
![iso](iso.png)


## CAD model (Parametric)
With all dimensions and calculations out of the way, I parametrically designed the motor mount on SolidWorks. I first added global variables to the equation editor to make it parametric in the first place, and assign sketch dimensions to those variables. The equations that gave the chosen base and height dimensions were the only two equations added to the equation editor, as the other two dont comply with bending and deflection.
<br>
<br>
![Eq](Eq.png)
<br>
<br>
I sketched feature 1 first and applied the variables to its dimensions and extrusion. The dimensions don't show that they are, but they are, so thats that.
<br>
<br>
![FT1S](FT1S.png)
![FT1X](FT1X.png)
<br>
<br>
I then sketched feature 2 one on of the faces of feature 1, and dimensioned it as such. The rectangle form of the beam was the length, 44 millimeters, by the base, 29.78 millimeters. the part was then extruded to the height, 15.87 millimeters
<br>
<br>
![FT2S](FT2S.png)
![FT2X](FT2X.png)
<br>
<br>
With both features extruded and made into parts, the model follows the same illustration as the isometric view. The next step was to apply the holes to each feature. Feature 1 has a hole in the center of a 18 millimeter diameter, extruded 2 millimeters and a hole of 6.025 millimeters through the whole part to account for the motor design.
<br>
<br>
![MMountU](MMountU.png)
![ft1big](ft1big.png)
![ft1small](ft1small.png)
<br>
<br>
The holes in feature 2 acted as bolts to hold the motor to the wall. The four holes are designed to be 3.4 millimeter clearance holes. The clearance hole finalizes the motor mount design.
[Download Motor Mount SolidWorks Part Here:](https://github.com/ajchiocca/megr2157-portfolio/raw/refs/heads/main/docs/assignments/A04/motor%20mount.SLDPRT). 
<br>
<br>
![FT2](FT2.png)
![MMount](MMount.png)
![Drawing](Drawing.png)
<br>
<br>
Just out of curiosity, I modeled the motor itself to see how it would fit with the motor mount. As i expected, the motor mounts. The height of feature 1, brought up earlier, if longer than the shaft. [Download Motor SolidWorks Part Here:](https://github.com/ajchiocca/megr2157-portfolio/raw/refs/heads/main/docs/assignments/A04/Motos.SLDPRT)
<br>
<br>
![Motor](Motor.png)
![Assembly](Assembly.png)




## Appendix

