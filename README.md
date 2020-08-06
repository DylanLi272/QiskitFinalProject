# QiskitFinalProject

## Final Project of the Qiskit 2020 Summer School
**Objective:** Simulate the ground state of the molecule Lithium Hydride (LiH) with the lowest energy and error. 
The goal is to complete the molecular simulation in the *fewest number of steps*, and the *highest level of chemical accuracy*.

---

In this project we design, implement, and simulate a Variational Quantum Eigensolver algorithm for calculating the ground state energy of the LiH molecule. Each team member explores a different optimization path using the same base model. LiH is a 12 body molecule containing 4 protons, 4 electrons, and 4 neutrons. This creates a 12 body model, which becomes intractable when simulating it both with a classical and quantum computer. So, this model reduces the First Quantized Molecular Hamiltonian to a blank body interaction. Let's begin by describing the intermolecular forces of this molecule conceptually:

<p align="center">Molecular Hamiltonian = - Sum(Electron Kinetic Energy) - Sum(Nuclear Kinetic Energy) - Sum(Electron to Nuclear Coulombic Forces)</p>
 <p align="center">+ Sum(Electron to Electron Coulombic Forces) + Sum(Nuclear to Nuclear Coulombic Forces)</p>

#### Electron Kinetic Energy

The kinetic energy of a single electron can be described using classical mechanics:

Electron Kinetic Energy = <img src="https://render.githubusercontent.com/render/math?math=\frac{1}{2}\times m \times v^{2}">

Where m is the mass of an electron and v is the velocity of an electron in meters per second.

<img src="https://render.githubusercontent.com/render/math?math=">

<img src="https://render.githubusercontent.com/render/math?math=m=9.10938356 \times 10^{-31} kg v=\frac{m}{s}">

However, obtaining the precise velocity of an electron is impossible because of how small they are. There is nothing to measure an electron's movement against. Measurements always require some frame of reference. One advantage to using a quantum computer is that it allows us to estimate the velocity of an electron during simulation by using current and resistance (impedance) measurements on the microwave transceiver that ineracts with a Josephson Junction (Qubit). The estimate you can obtain for a electron's velocity using a quantum computer is more accurate because it is a representation of the quantum mechanical effect you are attempting to measure outside of a lab setting.

#### Nuclear Kinetic Energy

#### Electron to Nuclear Coulombic Force

#### Electron to Electron Coulombic Force

#### Nuclear to Nuclear Coulombic Force

The First Quantized Molecular Hamiltonian for LiH can be described with the following vector calculus formula: 

<p align="center"><img src="https://render.githubusercontent.com/render/math?math=H = -\sum_{i=1}^{N}\frac{1}{2}\triangledown_{i}^{2}-\sum_{A=1}^{M}\frac{1}{2M_{A}}\triangledown_{A}^{2}-\sum_{i=1}^{N}\sum_{A=1}^{M}\frac{Z_{a}}{r_{iA}}+\sum_{j>i}\frac{1}{r_{ij}}+\sum_{B>A}\frac{Z_{A}Z_{B}}{R_{AB}}"></p>


Choices of designing VQE algorithms and compare their performance under specified assumptions to each other and to the classically computed exact solution. In addition, we will look at how realistic device specific noises could impact the performance of VQE algorithms. 

When designing an algorithm to be run on an actual quantum computer, there are a lot of variables to consider and the choices you make for the algorithm could dynamically change given different hardware specifications. Therefore there is no right answer for how you should design your algorithm. The goal of this project is for you to understand the different components that comprise a VQE algorithm and showcase your understanding by comparing the performance of different algorithm instances.


### Meet the Team of Researchers

#### Justin Adams
  Preferred Pronoun:  He
  City/Location:  Burlington, United States
  University & Major: B.Sc. Electrical Engineering and B.Sc. Computer Science
  Company & Background/Industry: Q2-Computing Quantum Computation and Quantum Operating System based on NP Hard Reductions using Majorana Fermion Josephson Junctions
  Favorite Emoji:  Majorana Fermion
  Favorite Color: :blue_book:

#### Zarreen Reza
  Preferred Pronoun:  Her
  City/Location:  Montreal, Canada
  University & Major:  M.Sc. in Computer Science - University of Windsor
  Company & Background/Industry:  Data Scientist
  Favorite Emoji:  Qiskit Smart
  Favorite Color: :blue_heart: 
  
#### Name: Arpan Bhattacharjee
  Preferred Pronoun:   He
  City/Location:  Kolkata, India
  University & Major: B.Sc. in Physics - St. Xavier's College, Kolkata
  Company & Background/Industry:  Physics ( Theoretical )
  Favorite Emoji:  Quantum Idea
  Favorite Color: :green_apple:

#### Dylan Li
  Preferred Pronoun: He
  City/Location: Texas, United States
  University & Major: Texas Academy of Mathematics and Science - Computer Science
  Company & Background/Industry: Computer Science
  Favorite Emoji: Quasi Particle
  Favorite Color: :blue_heart:

