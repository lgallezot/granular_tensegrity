# granular_tensegrity
This repository contains files used for the project "Geometric analysis of tensegrity-based granular
materials for support of semi-collapsed structures". Here you can find files used for simulations, data coming from real-life tests, and videos to illustrate what has been realized.

Instructions to use the files for simulation:
Warning: To run these .gh files, you need to have the Kangaroo2 and KangarooEngineering plug-ins installed
For Test 1 (Single unit deformation test), run the test1_test2_test4.gh file and follow the following steps:
  1. choose a geometry among Star3, T3 and Icosahedron
  2. branch the 1unit relay
  3. pretensions (strengths) used for radial and vertical cables were respectively 8 and 11.1 for T3, 19 and 11.1 for Star3, 11.1 and 11.1 for Icosahedron
  4. disable all the SollidPointCollide components
  5. use the Solver component in the first step (not the Bouncy solver)
  6. adjust the plate height for it to be just on top of the unit
  7. you can then choose the load applied on top of the plate by changing the dimensions of the bar

For Test 2 (Load-bearing performance in contained space), run the test1_test2_test4.gh file and follow the following steps:
  1. choose a geometry among Star3, T3 and Icosahedron
  2. adjust the population of units as desired
  3. branch the multiple_units relay
  4. pretensions (strengths) used are as in Test 1
  5. enable the SollidPointCollide component corresponding to the normal box (blue)
  6. use the Bouncy Solver in the first step
  7. To shrink the units, set the Solver's damping to 0.8 or below and enable the Spring component denoted as 'cable to shrink'
  8. To deploy the units, set the Solver's damping to 0.8 or below and disable the Spring component denoted as 'cable to shrink'
  9. To apply a load, follow the sam procedure as in Test 1

For Test 3 (Spread behavior of falling units), run the test3.gh file and follow the following steps:
  1. choose a geometry among Star3, T3, Icosahedron and Sphere
  2. adjust the population of units as desired

For Test 4 (Deployment in complex geometry), run the test1_test2_test4.gh file and follow the following steps:
  1. choose a geometry among Star3, T3 and Icosahedron
  2. adjust the population of units as desired
  3. branch the multiple_units relay
  4. pretensions (strengths) used are as in Test 1
  5. enable the SollidPointCollide component corresponding to the complex box (purple)
  6. use the Bouncy Solver in the first step (you can disable the solver in the second step as it is not used)
  7. To shrink the units, set the Solver's damping to 0.8 or below and enable the Spring component denoted as 'cable to shrink'
  8. To deploy the units, set the Solver's damping to 0.8 or below and disable the Spring component denoted as 'cable to shrink'
