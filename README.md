# Numerical-Solution-to-Schrodinger-s-Equation

If the particle potential depends only on position x of the particle, the equation that governs the wave function of our quantum-mechanical system is One-dimensional Schrödinger equation. There are many problems for One-dimensional Schrödinger equation such as infinite square well, harmonic oscillator and etc. We also have one dimensional shape-invariant potentials such as Pöschl–Teller potential, Hydrogenic potential, Morse Potential and the Rosen-Morse potential.
In this project we will look at Hamiltonian with several different potentials given below.

<img width="561" alt="Screen Shot 1401-04-31 at 8 31 52 PM" src="https://user-images.githubusercontent.com/89476798/180478687-c60b2222-4b71-4791-a1d1-28aebb8b331f.png">



### Part 1 - Time-independent One-dimentional Schrodinger Equation
1. Take ψ0 = 0 and choose ψ1 any small number. We took 0.001 for ψ1 in our simulation. 
2. Choose a trial energy En.
3. Break ODE solver to 2 parts,right and left.Step ψl(x),which satisfies its boundary condition, in toward the right. Do this also for ψR. These to must reach the matching radius xmatch and satisfy this condition. In order to do so logarithmic derivative ψ′(x)/ψ(x) to be continuous.
4. Normalize.
5. Write a function that calculates the matching function ∆(E,x) as a function of energy and matching radius. This subroutine will be called by the bisection algorithm program to search for the energy at which ∆(E , x = 2) vanishes.
6. Choose value of tolerance and search until ∆(E,x) changes in only fourth decimal place.
7. Increase the value of the initial energy guess and search for excited states.

### Part 2 - Time-dependent One-dimentional Schrodinger Equation

1. Choose an intial wave. The common choice is a Gaussian multiplied by a plane wave.
2. Normalize.
3. Write Hamiltonian as a sparse matrix like Eq.33 given in report.
4. Make linear algebra system given in Eq.34 given in report.
5. Solve it using Tridiagonl matrix algorithm. We seperated the real and imagenery part and solve each part using numpy library \textit{np.linalg.solve}. 
6. Be considerate of boundary conditions.
7. You have calculated the wave function.
8. Do a production run with 100 time steps and animate it.
