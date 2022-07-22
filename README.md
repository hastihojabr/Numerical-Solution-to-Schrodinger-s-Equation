# Numerical-Solution-to-Schrodinger-s-Equation
\usepackage{mathtools}
### Part 2 - Time-dependent One-dimentional Schrodinger Equation Solver

```math
\begin{equation}
    \Bar{H}\psi(x,t)=-\frac{\psi(x+\delta x)-2\psi(x,t)+\psi(x-\Delta x,t)}{\Delta x^2} +V(x)\psi(x,t)
\end{equation}
```
We write the Hamiltonian in sparse matrix form for one dimension.
\begin{equation}
\Bar{H}=\frac{-\hbar^2}{2m\Delta x^2}
    \begin{bmatrix}
    -2 & 1 & 0 & 0 &  0 \\
    1 & -2 & 1 & 0 &  0 \\
    0 & 1 & -2 & 1 & 0  \\
    0 & 0 & 1 & -2 & 1   \\
    0 & 0 & 0 & 1 & -2   
    \end{bmatrix}
+
    \begin{bmatrix}
    V(x_0) & 0 & 0 & 0 &  0 \\
    0 & V(x_1) & 0 & 0 &  0 \\
    0 & 0 & V(x_2) & 0 & 0  \\
    0 & 0 & 0 & V(x_3) & 0   \\
    0 & 0 & 0 & 0 & V(x_4)   
    \end{bmatrix}
\end{equation}

Equation 34 will be
\begin{equation}
    \left(I+\frac{i\Delta t}{2}\Bar{H}\right)\psi(x,t+\Delta t) = \left(I-\frac{i\Delta t} {2}\Bar{H}\right)\psi(x,t)
\end{equation}

\begin{equation}
    \psi(m,n)=\psi(m\Delta x,n \Delta t)
\end{equation}
