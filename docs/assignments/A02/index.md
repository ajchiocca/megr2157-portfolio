# A2 – Truss Stress Analysis

## Objective
<br>
<br>
The objective of the assignment is to design a lightweight planar truss that meets requirements (Safety factor, weight optimization, etc) that would be important when designing a functional truss. This would be accomplished by first creating the truss design and modeling it in CAD software to find its mass properties and run the necessary simulations.
<br>
<br>

![Free Body Diagram](FBD.png)
## Analyze
### Truss
The first step is to, of course, create a truss design. I chose this truss design so that solving the forces in each truss was kept as simple as possible while still accounting for the design's overall strength, where the four truss members in the middle have zero newtons acting on them, making the outside members the only members in the truss affected by the load. When it comes to failure. The truss members in the middle can resist the nature of the load, which is to rotate counterclockwise on member CD (or CF and DF). An alternative truss design would be to create three equilateral triangles; however, I chose to keep my design because I have already uploaded and embedded the PNGs, and having to change the design would mean reuploading those images and recalculating it in its entirety.
<br>


![Truss](IMG_1378.png)
#### Member calculations
I used the method of joints and method of sections to find the force in each truss member. I first investigated joint C to start with a known force to solve for the other members acting on joint C. With the solved forces, the rest of the joints can be found. It's important to note that the four truss members in the middle will have zero newtons acting on them, so excluding them from the free body diagrams or the truss overall is acceptable. Support forces and known forces only act in the y-direction as well; therefore, the support force in the x-direction at A equates to zero. The solved truss gave members AD and BC as the largest at 33.334 kN, members BA and CD 26.667 kN, and the two support forces at 20 kN.
<br>
<br>
![JOINTS](JOINTS.png)
![MOS](MOS.png)

#### Normal stress
With the solved forces, the next step was to calculate the allowable normal stress the truss must comply with. The truss is made from A151 1040 cold-rolled, which has a yield strength of 82 kips per square inch. I converted the 82 ksi to 565.34 Megapascals or .0565 Gigapascals so that the stress and dividing units are the same as the truss dimensions. Dividing the yield strength by the factor of safety 3.5 gives the allowable stress on the truss. I then found the minimum cross-sectional area of the truss by dividing the maximum force felt in the truss, 33,334 kN, converted to newtons, divided by the allowable stress. The result was 206.4 millimeters squared.
<br>
<br>
![NOMSTRESS](NOMSTRESS.png)

#### Weight of the truss
The weight density of AISI 1040 Cold-rolled steel is 490 pounds per feet cubed. To find the weight, I used the formula of weight equal to density times the cross-sectional area and the truss members' respective lengths. I first converted the weight density to newtons per millimeters cubed to maintain metric units. The weight density over gravity is the density used, which was 7.83 * 10^-9 kilograms per millimeter cubed. The weight formula could be performed, and the result was the weight of the truss to be 58.66 newtons.
<br>
<br>
![WEIGHT_T](WEIGHT_T.png)

### Pins 
#### Shear stress
The force and allowable stress in the single shear pins must be evaluated as well. I created another free body diagram of pin A, and the only and largest force acting on it is 20 kN. The pins are made of hardened tool steel, with a yield shear strength of 170 ksi and a density of 0.278 pounds per square inch. I divided the maximum force by the yield strength to find the minimum cross-sectional area before applying the factor of safety. The minimum area with an applied factor of safety of 4 is 0.1057 square inches or 68.193 millimeters squared.
<br>
<br>
![PINSHEAR](PINSHEAR.png)
#### Weight of the pins
With a given density of the pins' material, the weight of the two pins can be calculated more easily. The mass of the pins is the density times the volume, and the pins are assumed to take the shape of a cylinder for simplicity. Setting the cross-sectional area to the area of a circle, the radius of the pin can be found. The radius of the pin is .1834 inches, and as the pins are cylindrical, the length of the pins must be the length of the truss. Assuming the cross-sectional area of the truss is a square, its length is 14.36 millimeters or 0.565 inches. Multiplying the volume times the density and the number of pins, two, gives the total mass, which came out to be .033 pounds or .147 newtons.
<br>
<br>
![WEIGHTPIN](WEIGHTPIN.png)

## Decide 
### CAD models
The mass calculated from SolidWorks for the truss and pins is 5896.43 grams and 7.88 grams. The measurements equate to 56.98 newtons and .153 newtons (combined pin mass), which are close to the estimated value from my calculations. Under the given external load of two 20 kN forces going in opposite directions, the truss design will be able to withstand the load. The links for the created Solid works parts are under the image that corresponds to them.

![CADCAD](CADCAD.png)
https://github.com/ajchiocca/megr2157-portfolio/raw/refs/heads/main/docs/assignments/A02/truss.SLDPRT

![PINPIN](PINPIN.png)

## Communicate
### Truss members failure mode
#### Yielding 
Members CF, DF, CH, CB, AJ, and DJ are the most likely to fail due to the yield strength. The fact that these members are in tension makes them more susceptible because stretching steel, in this case cold-rolled AISI 1040 steel, is a ductile material in this case and takes less strength than it does to compress it. Limiting members in tension is not realistic, but a design modification to stop the possibility of those members failing is to add more members in tension; that way, the load is distributed over more members and keeps it in the elastic range.
#### Fracture
Fracture occurs when an external load or internal stress exceeds the material's strength. Members CF, DF, BH, BE, EA, and AJ have the possibility to fail from fracture, considering external forces are concentrated at the joints and experience the most internal force. Adding more members connected to joints A, B, C, and D would reduce the likelihood of fracture failure, for the internal forces derived from the external load would be distributed to more members, lowering the overall stress that could exceed the steel's strength.
#### Buckling
Buckling is most common in members connected to a pin or experiencing compressive force in both directions. Member, DJ, AJ, BE, and AE are the only members in compression that could fail due to buckling. Reducing buckling failure is possible by again, adding more members so that any members are not overloaded. increasing the thickness or shortening the length will require stronger forces to induce buckling as well, for buckling is most effective at higher slenderness ratios
### Pins failure modes
The expected failure mode of the pins would be direct shear for the pin located on Joint B, and bending on the pin at Joint A. I used Claude AI to generate possible failure modes of pin, and with my prompt being "generally speaking what are expected failure modes in pins. are there credible sources i can cite than confirm how my pin will fail? I have my truss in a trapezoidal shape, with the pins on the corners of the long side, with their respective support forces in opposite directions." Claude AI gave me seven different ways a pin could fail, with the response verifying my original hypothesis. Pin B (at joint B) has its support force in the negative y direction and member BH in the positive y direction. Direct shear occurs when parallel forces slide apart a material. Member BH is not completely in the y direction, but the portion of the force acting upwards may inflict direct shear regardless. Pin A would most likely fail due to bending considering the forces acting on joint A are in opposite direction. Member AJ raises the most concern for its going in the opposite direction as the support force and is at an angle. Between those forces, the pins behavior would be to turn clockwise while attempting to stay in its position until the interval forces eventually overwhelm the support force and breaks the pin. Here is the full response Claude AI gave me:

Pin connections in a truss (or any pin-jointed link) typically fail in one of a handful of well-characterized ways. For a pin at the corner of a truss member, loaded by the reaction/support force, the credible list is basically:

1. Direct shear of the pin
The pin shears across its cross-section(s). If it's a single-shear joint (pin through two plates lapped together), shear area = one cross-section; if double-shear (pin through a clevis with the member sandwiched inside, or a gusset between two flanges), shear area = two cross-sections, so double shear is much stronger for the same pin diameter. This is usually the governing/primary failure mode people check first.

2. Bearing failure (pin or plate)
Local crushing/yielding where the pin presses against the hole wall — either the pin itself yields/deforms, or the plate material around the hole yields and the hole elongates (ovalizes). Bearing stress = load / (diameter × plate thickness).

3. Tear-out (edge shearing) of the plate
If the edge distance from the hole to the free edge of the plate is too small, the material between the hole and the edge shears out in the direction of load — two shear planes tearing free. This is a plate/lug failure mode, not a pin failure mode per se, but it's the most common practical cause of "pin joint" failures in the field because designers under-detail edge distance.

4. Net-section tension failure
The plate fails in tension across its net width (gross width minus hole diameter) at the pin location — governs when the plate is narrow relative to the hole.

5. Bending of the pin
If there's any gap between the loaded members (e.g., a lug that isn't tightly sandwiched, or if the two opposite-direction forces you describe aren't perfectly collinear/coplanar), the pin sees a bending moment in addition to shear. This is a common failure mode when people assume "pin = pure shear" but the geometry actually introduces an offset or moment arm.

6. Fatigue / fretting
For cyclic loads, cracks can initiate at the pin surface or at the hole edge (stress concentration), often accelerated by fretting wear if there's any relative micro-slip between pin and hole. This is the dominant failure mode in bridges, machinery, and anything with repeated loading rather than one-time static load.

7. Bearing-induced hoop/tensile failure around the hole
Related to bearing, but framed as the hole "trying to split open" — relevant for thin plates or lugs, sometimes called "hoop tension" failure in lug analysis.

On your specific geometry
Two pins at the corners of the long side of a trapezoidal truss, with support reactions in opposite directions, sounds like it's setting up either (a) a couple/moment reaction pair, or (b) a two-point support where the truss could see combined shear + bending at each pin if the reaction lines aren't collinear with the member's neutral axis. Worth explicitly checking: whether the pin sees single or double shear in your actual bracket/gusset detail, and whether the opposing forces introduce any eccentricity (bending) rather than pure shear at each pin.

Credible, citable sources
Shigley's Mechanical Engineering Design (Budynas & Nisbett) — standard mechanical engineering textbook; has direct shear/bearing pin design equations and is widely cited in coursework and industry.
AISC Steel Construction Manual — has a specific section on pin-connected members (eyebars/pin plates), including required edge distance and net-section rules to prevent tear-out — this is the actual code-referenced source if this is a civil/structural steel truss.
Roark's Formulas for Stress and Strain (Young & Budynas) — has stress concentration factors around loaded holes, useful for the bearing/hoop stress case.
Bruhn, "Analysis and Design of Flight Vehicle Structures" and Niu, "Airframe Stress Analysis and Sizing" — if this is aerospace-context, these are the classic references for lug/pin joint failure modes (bearing, shear-out, net-tension) with the exact interaction diagrams engineers use.
ASME B18.8.1 / B18.8.2 — dimensional/mechanical standards for clevis and cotter pins if you need pin material/size specs.
If you tell me whether this is a civil (AISC-governed) truss or a machine-design/aerospace context, I can point you to the specific section/equation in the right one of these rather than the general list.



