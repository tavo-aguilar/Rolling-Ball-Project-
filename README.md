# Rolling-Ball-Project
Simulation of a rolling ball given a 3D surface


## Overview
- This is a jupyter notebook modeling the movement of a rolling ball given a 3D surface. Simulations for the movement of bodies gives us useful information about an object's motion, given that there can be different variables affecting the path the object takes

## Physics / Math Background
- We make use of multidimensional differential equations to simulate the path of the object, in our case a rolling ball. The path of a rolling ball given a surface can be described by equations and calculating the gradient to see where the surface tends to be 'steeper' in some regions on th surface over others. 

## Methods
- For this project, we do utilize a 3D surface from matplotlib to visualize the surface the ball rolls on. The scipy package is also used since we need to make use of the integrate.solve_ivp command to solve for our differential equations using the RK45 method. numpy is imported to define times of evaluations using the .linspace command as well.
  
- The rest of the project utilizes common plot commands and loops to be able to evaluate and plot our simulations.  

## Results

- All results are in the notebook with their respective cells and the project is sectioned into different parts to better distinguish resuts from one another.

- The first section defines equations and plots the surface used for this simulation. We define the solution for the 1D harmonic oscillator since it will be a good starting point when deriving a solution for our multivariable case.
  
- We then transition to our ball in a bowl by noting that we are working with 2 harmonic oscilators rather than 1. Using the equations established in the first section, we define a solver and define initial conditions or the simulation. Once we utilize the .solve_ivp command for our solver, we are able to plot 2 solutions. The first plot describes the motion as a 'side to side' motion, while the other plot describes no change in that coordinate. This may seem confusing, but when looking at the second plot with the circle, it traces the path of the ball with no horizontal movement. From the first plot, we can see that the first solution eventually reaches equilirium, which is what we expect the ball to do in a physical system.

- In the second section, we use most of the same code while modifying the initial values to make it such that we place the ball 2 units to the right while giving it an initial velocity of 1 unit in the y-direction. The results are different from the previous section due to there now being displacement in both directions. The elliptical trajectory is plotted after and we can note over time the ball spirals into the minumum of the surface, as expected from a real physical system.

- With these simulation, we may want to consider the addition of an external force. We must go back to the solver and add a driving force. This is done by adding a phi dependence to both solutions and defining a time of oscillation (tOsc). With this new addition, we can see now that the results resemble a chaotic system, before eventually settling back to equilibrium. This external force is necessary to model since it will produce the most similar results in application.

## How to Run
1. Make sure to have the following packages imported: numpy, matplotlib and scipy
2. All the code is given in the notebook, run the cells in order to reproduce plots and results. Enjoy!

