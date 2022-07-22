# Numerical-Solution-to-Schrodinger-s-Equation

### Part 2 - Time-dependent One-dimentional Schrodinger Equation Solver

1. Choose an intial wave. The common choice is a Gaussian multiplied by a plane wave.
2. Normalize.
3. Write Hamiltonian as a sparse matrix like Eq.33.
4. Make linear algebra system given in Eq.34.
5. Solve it using Tridiagonl matrix algorithm. We seperated the real and imagenery part and solve each part using numpy library \textit{np.linalg.solve}. 
6. Be considerate of boundary conditions.
7. You have calculated the wave function.
8. Do a production run with 100 time steps and animate it.
