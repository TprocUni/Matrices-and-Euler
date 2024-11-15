# Matrices-and-Euler
This code provides two key functionalities: a matrix transformation applied to geometric points and a demonstration of Euler's Method for solving differential equations. It also includes detailed derivations and visualisation of the results to validate both the transformations and the numerical method.


### Key Components

#### 1. Matrix Transformation

- **Purpose**:
  - Applies a matrix transformation to a set of points, visualizing the effect before and after the transformation.

- **Implementation**:
  - The function `matrixMultiply` calculates the transformed coordinates of a set of points using matrix operations.
  - The transformation involves horizontal and vertical shears and a scaling factor defined by constants `a` and `b`.

- **Visualization**:
  - Two subplots are created, showing the points before and after the transformation.
  - Each set of points (e.g., quadrilaterals and lines) is plotted in different colors for clarity.

- **Results**:
  - The transformation results in a combination of scaling, shearing, and slight rotation, altering the geometry of the plotted shapes.

---

#### 2. Euler’s Method

- **Purpose**:
  - Demonstrates **Euler's Method** for approximating the solution of the differential equation \( \frac{dy}{dx} = x + \frac{y}{5} \).

- **Implementation**:
  - The function `eulersMethod` iteratively computes approximate values of \( y \) using a specified step size.
  - The method is applied with decreasing step sizes (`1`, `0.2`, and `0.05`), showcasing the effect of step size on accuracy.

- **Validation**:
  - The exact solution is derived:
    \[
    y = -5x - 25 + 22e^{x/5}
    \]
    - This is plotted using the `graphIt` function to compare against the results of Euler's method.

- **Visualization**:
  - Separate graphs are generated for each step size, demonstrating increasing accuracy as the step size decreases.
  - The graph of the exact solution confirms the convergence of Euler's method for smaller intervals.

---

### Mathematical Derivation

- **Exact Solution**:
  - The differential equation is rearranged into standard form for solving:
    \[
    \frac{dy}{dx} - \frac{y}{5} = x
    \]
  - The integrating factor \( IF = e^{-x/5} \) is applied, transforming the equation:
    \[
    \frac{d}{dx}\left(y \cdot e^{-x/5}\right) = x \cdot e^{-x/5}
    \]
  - Using integration by parts, the solution is derived as:
    \[
    y = -5x - 25 + 22e^{x/5}
    \]

- **Comparison**:
  - Euler's method provides a numerical approximation, while the derived solution serves as a benchmark for accuracy.

---

### Observations

1. **Matrix Transformation**:
   - The transformation introduces distinct geometric changes like scaling and shearing.
   - The visual comparison effectively highlights the alterations between the original and transformed sets of points.

2. **Euler's Method**:
   - As the step size decreases, the numerical approximation aligns more closely with the exact solution.
   - This demonstrates the effectiveness of Euler's method, provided the step size is sufficiently small.

---

### Conclusion

The code effectively demonstrates both matrix transformations and Euler's method. The matrix transformation showcases the impact of linear operations on geometry, while Euler's method illustrates the accuracy and convergence properties of numerical solutions for differential equations.
