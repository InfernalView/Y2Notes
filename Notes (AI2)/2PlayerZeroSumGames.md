# 2-Player Zero-Sum Games

## 2-Player Zero-Sum Games
These games can be defined as simply as **"One player's Gain, is the Other player's Loss"**. In this $B_{m \times n} = -A_{m \times n}$; where the sum of the players' gains and losses equal to zero.

...

The **Minimax Theorem** states that for any $x$ and $y$; where $max_xmin_yx^TAy \leq min_ymax_xx^TAy$, or put simply...; there exists $x$ and $y$ where $max_xmin_yx^TAy = min_ymax_xx^TAy$, in which such pairs $x$ and $y$ is a **Nash Equilibrium**. This theorem can be proven using **Linear Programming Duality**.

## Linear Programming
A general **Linear Program** has three components:
* A **Linear Object Function** to be maximized/minimized
* A **System of Linear Constraints**, given by inequalities
* And the **Decision Variables**

This is basically those math problems where your given constraints, a goal either as maximize or minimize, and try to find the value(s) that achieve this goal. The decision variable is another constraint, but it is just those 'given' constraints that is implied though not explicitly stated; ***E.g.*** $x \geq 0$.

## Modelling Linear Programs
Steps to solve a problem using linear programs:
* **Identify objective function**, ***I.e.*** the function that is to be minimized or maximized. ***E.g.*** *"Minimize the cost of buying different fruits"* as $Cost_{Minimum} = min(c_{apple}x_{apple}+c_{orange}x_{orange}+...)$.
* **Impose constraints**, ***I.e.*** constraints must be followed, and would narrow the **Feasibility Region** for the final answer. ***E.g.*** *"Must at least have a certain amount of calories in total"* as $Calories = (kcal_{apple}x_{apple}+kcal_{orange}x_{orange}+...)$.
* **Write down the problem**, ***I.e*** write down the known objective function and constraints, to clearly describe the problem as multiple equations and inequalities.
* **Then solve**, using any method to solve the linear program problem.

## Methods for Solving LPs
There are many methods for solving LPs. This includes:
* **Simplex** method, which is a worst-case for time complexity, as it is exponential and runs on $O(n^3)$.
* **Ellipsoid** method, which is a polynomial-time algorithm, which is slow in practise and worse than **Simplex**.
* **Karmarkar's** algorithm, which is also a polynomial-time algorithm, but usually runs as fast or even faster than **Simplex** with large amounts of inputs.

## Structure of LPs
The structure of LPs are described as the following:
* The constraints in a LP describe a **Convex Polytope** in $n$-dimentional space.
* The **Convex Polytope** corresponds to the **Feasible Region** that consists of all feasible solutions.
* The objective function will atain its maximum/minimum at a **Vertex** of the polutope.
* The set of constraints may be **Infeasible**, in which case the LP has no solutions. ***I.e.*** constraints so bad that there is literally no solution that satisfy all of them.
* A LP is **Unbounded** if it has some feasible solution but does not have a finite optimal objective value. ***I.e.*** The isn't enclosed, an so there will often be 'solutions' which are exceedingly far or high in value.

## Linear Programming Duality
Is used to solve two-player zero-sum games by using LPs to find the optimal solution for each player. The two problems are referred to as the **Primal** and **Dual** problem, where the primal problem takes either the perspective of the maximizing or minimizing player, and the dual problem takes the other.

The **Duality Theorem** is defined as this:
* Given that the **Primal** problem is $max(c^Tx)$ where $Ax \leq b$ and $x \geq 0$
* And the **Dual** problem is $min(b^Ty)$ where $A^Ty \geq c$ and $y \geq 0$
* Then a it states that the:
    * **Dual Gap** is given by $b^Ty - c^Tx$
    * And the duality is **Weak**, if for any feasible $x$ and $y$, then $c^Tx \leq b^Ty$. ***I.e.*** the utility of the maximizer is less or equal to the utility of the minimizer.
    * And the duality is **Strong**, if the optimal solution for the primal and dual problems, respectively as $x^*$ and $y^*$, are equal in utility as $c^Tx^* = b^Ty^*$.

## Nash's Theorem and Equilibrium Stuff (Not Examinable)
...
