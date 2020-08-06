# QiskitFinalProject

### Final Project of the Qiskit 2020 Summer School
**Objective:** Simulate the ground state of the molecule Lithium Hydride (LiH) with the lowest energy and error. 
The goal is to complete the molecular simulation in the *fewest number of steps*, and the *highest level of chemical accuracy*.

---

In this project we design, implement, and simulate a Variational Quantum Eigensolver algorithm for calculating the ground state energy of the LiH molecule. Each team member explores a different optimization path using the same base model. LiH is a 12 body molecule containing 4 protons, 4 electrons, and 4 neutrons. This creates a 12 body model, which becomes intractable when simulating it both with a classical and quantum computer. The First Quantized Molecular Hamiltonian for LiH can be described with the following vector calculus formula: 

<img src="https://render.githubusercontent.com/render/math?math= \center{H = -\sum_{i=1}^{N}\frac{1}{2}\triangledown_{i}^{2}-\sum_{A=1}^{M}\frac{1}{2M_{A}}\triangledown_{A}^{2}-\sum_{i=1}^{N}\sum_{A=1}^{M}\frac{Z_{a}}{r_{iA}}+\sum_{j>i}\frac{1}{r_{ij}}+\sum_{B>A}\frac{Z_{A}Z_{B}}{R_{AB}}}">

Choices of designing VQE algorithms and compare their performance under specified assumptions to each other and to the classically computed exact solution. In addition, we will look at how realistic device specific noises could impact the performance of VQE algorithms. 

When designing an algorithm to be run on an actual quantum computer, there are a lot of variables to consider and the choices you make for the algorithm could dynamically change given different hardware specifications. Therefore there is no right answer for how you should design your algorithm. The goal of this project is for you to understand the different components that comprise a VQE algorithm and showcase your understanding by comparing the performance of different algorithm instances.
