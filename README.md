# Energy Minimization of Nanoparticle

## Overview

This project, conducted during the Winter Semester of 2022/2023, focuses on the energy minimization of nanoparticles using numerical methods and simulations. The primary goal was to study the Minima of Potential Energy using the Lennard-Jones Potential Function and perform stochastic simulations to determine the global potential energy of nanoparticle clusters.

## Keywords

- Numerical Approach
- Potential Energy Minimization
- Lennard-Jones Clusters
- Stochastic Simulations
- Nanoparticles
- Conjugate Gradient Descent

## Introduction

The objective of this project was to minimize the potential energy of nanoparticles to find their most stable structure. We began by placing atoms in a three-dimensional cube and then implemented numerical methods to minimize the potential energy using the Lennard-Jones equation.

Two key functions were developed:
- The **Energy Function**: Calculating the total potential energy.
- The **Force Function**: Calculating the derivative needed for minimization.

To enhance the efficiency of our minimization process, we used a **Line Search** function that locates the first minimum along a search direction, followed by the **Golden Section Method** to pinpoint the minimum. We then applied the **Conjugate Gradient Descent** method, which improves upon the steepest descent method by eliminating oscillatory behavior and reducing computational cost.

Multiple simulations were conducted with different initial configurations to identify various local minima. The configuration with the lowest energy was selected as the putative global minimum.

Three versions of code were developed to solve this problem, each improving upon the last. These versions are discussed in detail in the Solution section.

## Results and Discussion

### Energy Minimization and Convergence

![image](https://github.com/user-attachments/assets/7ce9f1a1-b4c9-4ebe-ba8e-fe09df3f83fe)

From the analysis of the graphs, it is evident that the minimum potential energy of the system decreases as the number of atoms (N) in the nanoparticle cluster increases. This trend is expected due to the nature of atomic interactions; as more atoms are introduced into the system, they form additional bonds that require more energy to be released for the system to achieve a stable, low-energy configuration. This behavior aligns with the theoretical understanding that a greater number of atoms in a cluster leads to a more complex structure, which in turn requires more significant energy adjustments to reach the most stable conformation.

### Conjugate Gradient Steps and Complexity

![image](https://github.com/user-attachments/assets/94e508e1-1efa-43b4-84d5-e1c3d095c272)

The graphs illustrates the relationship between the number of conjugate gradient steps and the minimization process. As the number of atoms increases, the structure of the nanoparticle becomes more intricate, necessitating more conjugate gradient steps to reach the minimum potential energy state. This is because the atoms must undergo more extensive rearrangements to find their optimal positions within the cluster. However, an exception is observed at N=2, where the minimum energy state is achieved almost immediately after the first conjugate gradient step, indicating that for very small clusters, the system is simpler and requires minimal adjustment to reach stability.

### Challenges in Scalability

![image](https://github.com/user-attachments/assets/85dba135-70e5-4801-976a-223995b242af)

Despite the successful application of the algorithms, the project encountered some challenges, particularly with scalability. As the number of atoms increased, the algorithm's performance showed some limitations. For example, at N=55, the resulting conformation was less uniform than expected, which suggests that the algorithm may need further refinement to maintain accuracy at higher atom counts. This discrepancy indicates that while the current approach is effective for smaller clusters, additional adjustments are necessary for handling larger systems with greater precision.

### Potential for Future Work

The project’s scope was primarily focused on minimizing potential energy for clusters of neutral atoms using the Lennard-Jones potential function. However, there are several potential avenues for future work. Incorporating atomic velocities, considering bonded (intramolecular) and non-bonded (intermolecular) interactions, and refining the numerical optimization techniques could lead to more accurate and scalable models. These enhancements would allow for more comprehensive simulations that could better replicate real-world nanoparticle behaviors, extending the applicability of the current findings.

## Conclusion

From the graphs and results presented, it is clear that the minimum potential energy is successfully reached, and the atoms conform to a nanoparticle in their stable configuration. The algorithms discussed were implemented effectively, though initial results required further numerical optimization to enhance efficiency.

The current code demonstrates good performance for small to medium-sized clusters, but scalability remains a challenge for larger systems. Further modifications and optimizations are necessary to achieve the highest accuracy with varying parameters.

The project has laid a solid foundation in potential energy minimization for microclusters of neutral atoms, with opportunities for expanding this work to more complex systems by incorporating additional physical interactions and improving the algorithm's scalability.

## Contact

For further information or queries, please reach out to me at [vuthanhptnkmai@gmail.com].
