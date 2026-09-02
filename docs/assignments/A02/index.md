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
<br>
![Truss Analysis](https://raw.githubusercontent.com/ajchiocca/megr2157-portfolio/main/docs/assignments/A02/truss.png)
## Analyze

### Member calculations
I used the method of joints and method of sections to find the force in each truss member. I first investigated joint C to start with a known force to solve for the other members acting on joint C. With the solved forces, the rest of the joints can be found. Its important to note that the four truss members in the middle will have zero newtons acting on it, so excluding them from the free body diagrams or the truss overall is acceptable. Support forces and known forces only act in the y-direction as well, therefore the support force in the x-direction at A equates to zero. The solved truss gave members AD and BC as the largest at 33.334 kN, members BA and CD 26.667 kN, and the two support forces at 20 kN.
<br>
<br>
<img src="joints1" alt="Joint A, B, C" width="600">
<img src="joints2" alt="Forces, MOS" width="600">

### Normal stress
With the solved forces, the next step was to calculate the allowable normal stress the truss must comply to. The truss is made from A151 1040 cold-rolled which has a yield strength of 82 kips per square inch.



## Communicate

