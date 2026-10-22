# A7 – FEA on bracket

## Objective
The objective of this assignment was to do a finite element analysis on the bracket design in order to optimize it (to a certain point, 100% optimization is unnecessary and more time-consuming). After each iteration of FEA, the bracket is to be redesigned to ensure the stress, displacement, and safety factor converge on a 7 percent difference. Due to the new program applied to select few, 2157 students get the joy of doing an FEA not only for the bracket, but also the link. This is thrilling and worth the extra credit hour (no its not).

## FEA analysis for bracket
The first step to setting up the FEA analysis is to ensure it reflects the applied load and fixtures from A5 and A6. An applied load downward of 600 to the shaft and fixtures where the T-beam would fit had to be added to be able to run the FEA, And so I did exactly that. 
![A7](fixtures.png)
![A7](applied_load.png)
<br>
<br>
The bracket and link are made of 6061-T6 aluminum alloy, and so the yield strength of the material is 39885.32 psi and a modulus of elasticity of 10007604 psi. The given maximum limiting deflection is .005 inches and instructed safety factor is four.

### Design 1

#### Mesh #1
I then created the first mesh for the model, which has total elements of 2844. With this the FEA can run and give the brackets behavior with values for stress, deflection, and safety factor. From the von mises curve, the chart shows the brackets minimum stress of 1.887e-10 psi and a maximum stress located at the strap connecting the shaft and bracket to be 7.504e2 psi. The deflection chart shows its concentrated the end of the shaft, with a maximum of 2.285e-3 inches. The factor of safety plot gives a large red bracket with a maximum of 5.315. The initial mass of the model is 12.52 pounds as well.

#### Mesh #2
To be able to test for convergence, the mesh had to be modified and have its stress, displacement, and safety factor compared to the previous mesh. I changed the mesh and increased the number of elements to 4760. The new values were a max stress of 8.129e2 psi, displacement of .002302 inches, and safety factor of 4.907. convergence is found by finding the percent difference between the values of the first mesh to the second mesh. calculating the convergence gives a percent difference of 7.99% for stress, 21.27% for displacement, and 12.54% for the safety factor. another mesh must be made to converge to 7% or lower. the mass of the design will remain unchanged until the first redesign.

#### Mesh #3
The next mesh had a total elements of 14931. the corresponding values were a max stress felt of 914 psi, displacement of .002324 inches, and a safety factor of 4.364. The found convergence/percent differences for stress was calculated to be 11.7%, displacement convergence of 0.95%, and safety factor of 11.71%. Another mesh must be created to attempt to achieve convergence for all three.

#### Mesh #4
For the final mesh, I bumped the scale near to fine, and got a total number of elements of 41333. The new values were a stress of 1092 psi, displacement of .002338 inches, and a safety factor of 3.652. the final convergence for values were a stress convergence of 17.74%, displacement convergence of 1.03%, and safety factor 17.76%. The amount of convergences is limited to three. Because stress and the safety factor hasnt converge to seven percent. another mesh must be created to the max amount of elements possible

#### Mesh 5
The max amount of total elements is 63038, when shifted to the farthest right, going from coarse to fine. the new values are a stress of 1096 psi, displacement of .002344, and safety factor of 3.64. The calculated convergence were .36% for stress, .25% for displacement, and 0.32% for safety factor. The bracket can now be redesigned, and the calculations for all the convergences were done on paper and below.

### Design 2



## Decide


## Communicate

