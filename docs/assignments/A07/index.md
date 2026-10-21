# A7 – FEA on bracket

## Objective
The objective of this assignment was to do a finite element analysis on the bracket design in order to optimize it (to a certain point, 100% optimization is unnecessary and more time-consuming). After each iteration of FEA, the bracket is to be redesigned to ensure the stress, displacement, and safety factor converge on a 7 percent difference. Due to the new program applied to select few, 2157 students get the joy of doing an FEA not only for the bracket, but also the link. This is thrilling and worth the extra credit hour (no its not).

## FEA analysis for bracket
The first step to setting up the FEA analysis is to ensure it reflects the applied load and fixtures from A5 and A6. An applied load downward of 600 to the shaft and fixtures where the T-beam would fit had to be added to be able to run the FEA, And so I did exactly that. 
<br>
<br>
The bracket and link are made of 6061-T6 aluminum alloy, and so the yield strength of the material is 39885.32 psi and a modulus of elasticity of 10007604 psi. The given maximum limiting deflection is .005 inches and instructed safety factor is four.

### Design 1

#### Mesh #1
I then created the first mesh for the model, which has total elements of 2844. With this the FEA can run and give the brackets behavior with values for stress, deflection, and safety factor. From the von mises curve, the chart shows the brackets minimum stress of 1.887e-10 psi and a maximum stress located at the strap connecting the shaft and bracket to be 7.504e2 psi. The deflection chart shows its concentrated the end of the shaft, with a maximum of 2.285e-3 inches. The factor of safety plot gives a large red bracket with a maximum of 5.315. The initial mass of the model is 12.52 pounds as well.

#### Mesh 2
To be able to test for convergence, the mesh had to be modified and have its stress, displacement, and safety factor compared to the previous mesh. I changed the mesh and increased the number of elements to 4760.

## Decide


## Communicate

