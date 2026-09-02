# A2 – Truss Stress Analysis

## Objective
<br>
<br>
The objective of the assignment is to design a light weight planar truss meets requirements (Safety factor, weight optimization, etc) that would be important when designing a functional truss. This would be accomplished by first creating the struss design and modeling it in CAD software to find its mass properties and run the necessary simulations.
<br>
<br>

![Free Body Diagram](FBD.png)
## Analyze
The first step is to of course create a truss design. I chose this truss design so that solving the forces in each truss were kept the most simple while still accounting for the designs overall strength, where the four truss members in the middle have zero newtons acting on them, making the outside members the only members in the truss affected by the load. When it comes to failure. the truss members in the middle can resist the nature of the load, which is to rotate counter clockwise on member CD (or CF and DF).
<br>

![Truss](IMG_1378.png)
### Member calculations
I used the method of joints and method of sections to find the force in each truss member. I first investigated joint C to start with a known force to solve for the other members acting on joint C. With the solved forces, the rest of the joints can be found. Its important to note that the four truss members in the middle will have zero newtons acting on it, so excluding them from the free body diagrams or the truss overall is acceptable. Support forces and known forces only act in the y-direction as well, therefore the support force in the x-direction at A equates to zero. The solved truss gave members AD and BC as the largest at 33.334 kN, members BA and CD 26.667 kN, and the two support forces at 20 kN.
<br>
<br>
![JOINTS](JOINTS.png)
![MOS](MOS.png)

### Normal stress
With the solved forces, the next step was to calculate the allowable normal stress the truss must comply to. The truss is made from A151 1040 cold-rolled which has a yield strength of 82 kips per square inch. I converted the 82 Ksi to 565.34 Megapascals or .0565 Gigapascals so that the stress is in metric units- the same as the truss dimensions. Diving the yield strength by the factor of safety 3.5 gives the allowable stress on the truss. I then found the minimum cross-sectional area of the truss by diving the maximum force felt in the truss, 33,334 kN, converted to newtons, divided by the allowable stress. the result was 206.4 millimeters^2.
<br>
<br>
![NOMSTRESS](NOMSTRESS.png)



## Communicate

