# Code for deriving aggregation kernel in a flux driven system.

## Code description

The script solves stationary advection-diffusion equation with cylindrical symmetry in polar coordinates for a range of Peclet numbers. Using the found soluion we integrate the flux along the surface of a center particle and find the dependence of aggregation kernel on Peclet number. To speed up computations we use **joblib**. The equation is solved using an implicit scheme, to solve the sparse linear system we use **scipy.sparse**. The program doesn't require any command line arguments.

## Results

Based on [this publication](https://link.springer.com/article/10.1134/S096554252304005X).

* The equation in the proposed problem set can be solved analytically. However due to that fact that the solution is formed by an infinite series, derivation of a simple formula for aggregation kernel is problematic. That is why we use Pade approximation technique. Example of a numerical solution for distinct Peclet numbers:

![cartezian.jpg](/cartezian.jpg)

