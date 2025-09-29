# Linear Regression
**Linear Regression** referred as **LR**

## Regression Model
Is a model/graph that shows the relationship between **Parameters**, and predict **Continuous Values**. It is shown as a **Line/Plane/Hyperplane** that best fits the data. 

## Linear Regression
LR is a **Regression** model, that uses a **Line**. So usually two inputs.

## Hypothesis Function
HP is a function that **Predicts** the **Output** from given **Inputs**

$$H_0(x)=\theta_0+\theta_1x_1+...$$

$\theta_0$ is the **Bias Parameter**, which shifts the trend to the correct location

$\theta_1$ is the **Bias Parameter** for the **Paramenter** $x_1$

$x_1$ is the value/input of **Paramenter 1**

### Summarised by:
$$H_0(x)=\theta^Tx$$

## Cost Function
CF calculates the mean **Cost** of predicting a certain amount of **Data Set** provided, with its respective inputs and outputs.

$$J(\theta)=1/2m\sum^m_{i=1}(h_\theta(x^i)-y^i)^2$$

$m$ is the **Amount** of data sets used

$h_\theta(x^i)$ is the **Predicted** output of **Data Set** $i$

$y^i$ is the **Actual** output of **Data Set** $i$

$(h_\theta(x^i)-y^i)^2$ is the **Degree** of **Difference** between the **Predicted** and **Actual** output

$1/2m$ is used to find the **Mean** of all the **Calculated Costs**

## Gradient Descent
GD is an **Iterative Optimization Algorithm** that is used to find the **Optimal Values** for the **Bias Parameters** $(\theta)$. Its iterative so it can be used repeatedly.

$$\theta_j=\theta_j-\alpha\frac{\delta}{\delta\theta_j}J(\theta)$$

$\alpha$ is the **Learning Rate**, which determines how fast the **Parameters** $(\theta)$ change

$\frac{\delta}{\delta\theta_j}J(\theta)$ is the **Derivative/Gradient** of the **Cost Function**

$-\frac{\delta}{\delta\theta_j}J(\theta)$ is the **Inverse** of the **Derivative**

GD adjusts the **Parameter** $(\theta)$ until it reaches a **Global Minimum**, where the **Cost** is at a **Minimum**, and the accuracy of the **Hypothesis Function** is at its highest.

## Process
1. **Initialise**
2. **Perform Hypothesis Function**
3. **Calculate Cost Function**
4. **Determine whether Parameters are Suitable**
    1. If **Cost** reaches a certain **Cost Threshold**, **Continue** to 5
    2. Otheriwse, **Do** 4.3, then **Repeat** 2-4
    3. **Perform Gradient Descent** and **Update Model**
5. **End**
