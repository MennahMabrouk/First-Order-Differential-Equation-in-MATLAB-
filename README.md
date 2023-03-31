# Frist-Order Differential Equation Solver using MATLAB
This repository contains a MATLAB program that can solve a first-order differential equation. The program follows the steps below:

+ Define the differential equation and any necessary initial conditions using symbolic variables.

+ Use the "dsolve" function to solve the differential equation.

+ Simplify the solution if possible.

+ Plot the graph using the "fplot" function.

### Example

Consider the differential equation:

```python
dy/dx = sin(2x) + cos(3x) - y
```
with initial conditions y(0) = 1 and y'(0) = 0.

Step 1: Define the differential equation and initial conditions

```python
syms y(x)
Dy = diff(y,x);
cond1 = y(0) == 1;
cond2 = Dy(0) == 0;
conds = [cond1 cond2];
eqn = diff(y,x) == sin(2*x)+cos(3*x)- y;
```
Step 2: Solve the differential equation using "dsolve"
```python
ySol(x) = dsolve(eqn,conds);
```
Step 3: Simplify the solution
```python
ySol = simplify(ySol(x));
```
Step 4: Plot the graph
```python
fplot(ySol , [0 20]);
xlim([0.0 20.0]);
ylim([-0.82 1.19]);
```
The resulting graph will show the solution to the differential equation over the interval [0, 20].

> Feel free to modify the code with your own differential equation and initial conditions to solve a different problem.



