# Coordinate Systems

## Points
A **Point** plotted in a **Coordinate System** will have values that indicate where it is. The values represent the amount of units the point is from a specified **Axis**. It is important to know where the **Up** is for each axis, which will help in debugging.

**Object Space** are coordinate systems for a specific object, with defined axises.

**Word Space** is the global/main coordinate system.

**Camera/View Space** is the coordinate system of the a camera object.

**Screen Space** is the coordinate system for the computer screen.

## Vectors
Vectors are lines, consisting of **Direction** and **Magnitude/Length**.

Different operations can be done on vectors:
* Addition
* Subtraction
* Multiplication
* Scale
* Magnitude
* Dot Product
* Cross Product

**Dot Product** denoted by $a.b$ where $a$ and $b$ are vectors, is useful for 

**Cross Product** denoted by $a \times b$ where $a$ and $b$ are vectors, is useful for finding the **Right Angle** of two vectors, called the **Normal**. Which is a vector that is of right angles between both individual vectors $a$ and $b$.

## Transformation
**Transformations** allow for changing points and vectors. The transformation that can be performed are:
* Scale (and Reflection)
* Rotate
* Shear/Skew
* Translate

**Matrices** are important in performing these transformations. Important transformations to note are, given $P_n=MP_o$ where $P_o$ is the **Original** matrix, $P_n$ is the **New** matrix, and $M$ is the **Transformation** matrix:
* Identity
$$I = \begin{bmatrix}1 & 0 \\ 0 & 1\end{bmatrix}$$
* Scale
$$S = \begin{bmatrix}s & 0 \\ 0 & s\end{bmatrix}$$
* Shear
$$I = \begin{bmatrix}1 & k \\ 0 & 1\end{bmatrix}$$
* Rotate
$$I = \begin{bmatrix}cos(\theta) & -sin(\theta) \\ sin(\theta) & cos(\theta)\end{bmatrix}$$
* Translate, there is no translation matrix when performing the operation above. Primarily because the operation uses multiplication. The proper operation would be:
$$P_n = m\begin{bmatrix}1 & 1 \\ 1 & 1\end{bmatrix} + P_o$$

**3D Homogenous** spaces have a different set of transformation matrices:
* Identity
$$I = \begin{bmatrix}1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1\end{bmatrix}$$
* Scale
$$I = \begin{bmatrix}s & 0 & 0 \\ 0 & s & 0 \\ 0 & 0 & 1\end{bmatrix}$$
* Rotate
$$I = \begin{bmatrix}cos(\theta) & -sin(\theta) & 0 \\ sin(\theta) & cos(\theta) & 0 \\ 0 & 0 & 1\end{bmatrix}$$
* Translate
$$I = \begin{bmatrix}1 & 0 & dx \\ 0 & 1 & dy \\ 0 & 0 & 1\end{bmatrix}$$

**Concatenation** can be applied to matrices, such that if $P_n = M_2M_1M_0P_o = M_nP_o$ where $M_n = M_2M_1M_0$. (I assume) ordering matters.

The approach to 3D transformation can be used for 4D transformations as well. That being the case, I don't know what the matrix operations for 4D looks like.

## Projection
...