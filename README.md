Energy Minimization of Nanoparticle - Winter Semester 2022/2023
Project Overview
This repository contains the code and documentation for the project Energy Minimization of Nanoparticles completed during the Winter Semester of 2022/2023 for the course on Thermodynamics, Modeling & Simulations. The primary objective of this project was to determine the minimum potential energy configuration of a nanoparticle using the Lennard-Jones Potential Function. We employed various numerical methods, including line search and conjugate gradient descent, to achieve this goal. This project also involved running stochastic simulations with different initial configurations to obtain the putative global minimum energy state of the nanoparticle.

Acknowledgements
We would like to express our gratitude to all the group members who contributed to this project. The collective effort and countless hours invested by the team were instrumental in achieving our results. We also extend our thanks to other groups who provided assistance when we encountered challenges. Special thanks to our supervisor, Abhishek Khetan, for his support, guidance, and inspiration throughout the project.

Abstract
This project investigates the minima of potential energy for a nanoparticle by using the Lennard-Jones Potential Function. Numerical methods such as line search and conjugate gradient descent were implemented to identify the global potential energy minimum. The stochastic simulations were run with different initial configurations, and the results were compared with the findings from the paper Global Optima of Lennard-Jones Cluster [1]. The project concluded with the successful visualization of the mechanically stable structure of a nanoparticle at its global optimum.

Keywords
Numerical Approach for Potential Energy Minimization
Lennard-Jones Clusters
Conjugate Gradient Descent
Line Search Method
Stochastic Simulations
Introduction
The main objective of this project is to find the minimum potential energy configuration for a nanoparticle, ensuring that it conforms to a stable structure. The process begins by placing atoms within a three-dimensional cubic lattice, where the size of the cube,
L, is proportional to the number of atoms, N.

To accomplish the energy minimization, we implemented two key functions:

Total Potential Energy Function: This function calculates the potential energy based on the Lennard-Jones equation.
Force Function: This is the derivative of the potential energy function and is used in the minimization process.
Numerical Methods
Line Search:
This function finds the first minimum along a search direction. Upon locating the minimum area, the Golden Section Method is used to refine the minimum location. This approach is efficient, reducing the number of function evaluations and thus lowering computational costs.
Conjugate Gradient Descent:
This method outperforms the basic steepest descent algorithm by considering previous steps, which helps eliminate oscillatory behavior. It computes new search directions, invokes the line search, and returns a nearby local minimum from a given initial value. This value represents the nearest stable configuration of the nanoparticle.
Simulation Process
Multiple simulations were conducted to identify several local minima with varying energy values, arising from different initial configurations. The configuration with the lowest energy was selected as the putative global minimum. The final outcome is a stable nanoparticle structure at this global minimum.

Code Versions
For the purpose of this project, we developed three different versions of the solution, each with slight modifications to improve efficiency and accuracy. These versions are documented in the solution section of this repository.

Solution
The project repository includes the following components:

Code:

version1.py: Initial implementation of the potential energy minimization.
version2.py: Improved version with optimized line search and conjugate gradient descent.
version3.py: Final version with additional refinements and optimizations.
Results:

Output files containing the energy values for different configurations.
Visualization of the final nanoparticle structure.
Documentation:

Detailed comments within the code explaining each function and method.
A report summarizing the findings and comparing them with the reference paper.
How to Run
Clone the repository:

bash
Code kopieren
git clone https://github.com/yourusername/nanoparticle-energy-minimization.git
cd nanoparticle-energy-minimization
Run the desired version of the code:

bash
Code kopieren
python version1.py
View the results in the output files or visualize the nanoparticle structure using your preferred visualization tool.

References
[1] D. J. Wales, "Global Optima of Lennard-Jones Clusters," Physical Review B, vol. 49, no. 34, pp. 12342-12349, 1994.
