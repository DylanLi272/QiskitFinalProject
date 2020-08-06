# QiskitFinalProject

## Final Project of the Qiskit 2020 Summer School
**Objective:** Simulate the ground state of the molecule Lithium Hydride (LiH) with the lowest energy and error. 
The goal is to complete the molecular simulation in the *fewest number of steps*, and the *highest level of chemical accuracy*.

---

In this project we design, implement, and simulate a Variational Quantum Eigensolver algorithm for calculating the ground state energy of the LiH molecule. Each team member explores a different optimization path using the same base model. LiH is a 12 body molecule containing 4 protons, 4 electrons, and 4 neutrons. This creates a 12 body model, which becomes intractable when simulating it both with a classical and quantum computer. So, this model reduces the First Quantized Molecular Hamiltonian to a blank body interaction. Let's begin by describing the intermolecular forces of this molecule conceptually:

<p align="center">Molecular Hamiltonian = - Sum(Electron Kinetic Energy) - Sum(Nuclear Kinetic Energy) - Sum(Electron to Nuclear Coulombic Forces)</p>
 <p align="center">+ Sum(Electron to Electron Coulombic Forces) + Sum(Nuclear to Nuclear Coulombic Forces)</p>

#### Electron Kinetic Energy

<p align="center">The kinetic energy of a single electron can be described using classical mechanics:</p>

<p align="center">Electron Kinetic Energy = <img src="https://render.githubusercontent.com/render/math?math=\frac{1}{2}\times m \times v^{2}"></p>

<p align="center">Where m is the mass of an electron and v is the velocity of an electron in meters per second.</p>

<p align="center"><img src="https://render.githubusercontent.com/render/math?math=m=9.10938356 \times 10^{-31} kg"></p>
<p align="center"><img src="https://render.githubusercontent.com/render/math?math=v=\frac{m}{s}"></p>

Quantum mechanics attempts to simplify the mathematics of calculating the energy of particles that have a wave-particle duality (like electrons). This is accomplished by dividing the energy of the particle in to the following components: Translational energy, rotational energy, and vibrational energy. This simplification of the wave-particle duality is known as the Born-Oppenheimer approximation. The Born-Oppenheimer approximation is one of the basic concepts underlying the description of the quantum states of molecules and atoms. We apply this approximation to the quantum states of qubits to obtain an estimate of the electron's velocity in real life using the quantum computer's qubits as a representational model.

<p align="center">Key Note: Obtaining the precise velocity or position of an electron is impossible because of how small they are. Thus, we resort to estimating this electron kinetic energy using qubits as a representation of quantum mechanical interactions.</p>

#### Nuclear Kinetic Energy

<p align="center">The kinetic energy of protons in general can be described using classical mechanics:</p>

<p align="center">Proton Kinetic Energy = <img src="https://render.githubusercontent.com/render/math?math=\frac{1}{2}\times m \times v^{2}"></p>

<p align="center">Where m is the mass of a proton and v is the velocity of a proton in meters per second.</p>

<p align="center"><img src="https://render.githubusercontent.com/render/math?math=m=1.6726219 \times 10^{-27} kg"></p>
<p align="center"><img src="https://render.githubusercontent.com/render/math?math=v=\frac{m}{s}"></p>

<p align="center">Key Note: Given the size of the lithium nucleus. The nuclear kinetic energy of Lithium Hydride is negligible. It is important to recognize taht this property can not always be neglected in an atomic or molecular simulation. There are atoms that have extraordinary amounts of nuclear kinetic energy. The first atom on the periodic table that displays this unique nuclear kinetic energy combinatorics property is Technetium. Technetium is the first element in the periodic table that periodically emits a helium nucleus. Its half-life is 4.21 million years, and it decays in to Niobium. So, when simulating atoms or molecules it is important to be aware of when the nucleur kinetic energy is an important property in your atomic or molecular model.</p>

#### Electron to Nuclear Coulombic Force

#### Electron to Electron Coulombic Force

#### Nuclear to Nuclear Coulombic Force

The First Quantized Molecular Hamiltonian for LiH can be described with the following vector calculus formula: 

<p align="center"><img src="https://render.githubusercontent.com/render/math?math=\hat{H}=-\sum_{i=1}^{N}\frac{1}{2}\triangledown_{i}^{2}-\sum_{A=1}^{M}\frac{1}{2M_{A}}\triangledown_{A}^{2}-\sum_{i=1}^{N}\sum_{A=1}^{M}\frac{Z_{a}}{r_{iA}}+\sum_{j>i}\frac{1}{r_{ij}}+\sum_{B>A}\frac{Z_{A}Z_{B}}{R_{AB}}"></p>


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

