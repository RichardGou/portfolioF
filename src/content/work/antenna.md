---
title: Optimization of Antenna Placement in a City
publishDate: 2024-01-15 00:00:00
img: /assets/antenna.png
img_alt: work data viz
description: |
   This project aim to solve an optimization problem without constraints, aiming to find the optimal position for a radio antenna in a city.
tags:
  - Python
  - Optimisation
  - Environment
---
#### Problem Definition
This project addresses an optimization problem to determine the optimal position of an antenna in a space populated with buildings and anti-buildings. The key elements include:

- Buildings: These are structures with known positions and populations. The goal is to optimize the antenna's signal coverage for these buildings.

- Anti-Buildings: Positioned similarly to buildings, they interfere with signal strength, necessitating the optimization function to reduce signal strength around them.

Both elements are generated randomly. Below is an example image illustrating the map.

<div style="text-align: center;">
    <img src="/assets/antennaBuildings.png" />
</div>
#### Objective Function
Below is a 3D plot depicting the values of the objective function across the city's map, which measures 50 by 100 units. This visualization clearly highlights the various positions of the anti-buildings and indicates what seems to be the optimal location for placing our antenna in darker blue.
 

<div style="text-align: center;">
    <img src="/assets/antennaCost.png" />
</div>

#### Problem Objective
The aim is to find the antenna **coordinates (a,b)** that minimize f(a,b), balancing signal coverage and attenuation near anti-buildings.

**Constraint :**
This optimization problem is unconstrained, allowing free positioning of the antenna within the defined space.

**Optimization Method :**
Numerical optimization methods, such as the Davidon-Fletcher-Powell (DFP) and Newton methods will be used.

#### Conclusion and Results Comparison

<div style="text-align: center;">
    <img src="/assets/antennaModels.png" />
</div>

**Note on Results :**
These results are specific to a given random initiation and may vary, but the observations generally hold.

##### Newton Optimization:
- Result: [36.31511861 55.2349728]
- Time Taken: 0.06209897994995117 seconds
- Iterations: 38

##### Davidon-Fletcher-Powell (DFP) Optimization:
- Result: [36.2714403 55.13881951]
- Time Taken: 0.13862085342407227 seconds
- Iterations: 100
- Both methods provided similar optimal coordinates, with Newton Optimization being slightly faster.

#### Strengths and Weaknesses
##### Newton Optimization:

- **Strengths:** Faster convergence and high accuracy.
- **Weaknesses:** Prone to local minima and sensitivity to initial conditions, especially near anti-buildings.

##### Davidon-Fletcher-Powell (DFP) Optimization:

- **Strengths:** Robust against different starting points, often faster in the given problem.
- **Weaknesses:** Slower due to more iterations, can be memory-intensive, less stable and accurate than Newton's method.

**In conclusion, Newton's method is faster but sensitive to initial conditions, while DFP is more robust but slower. The choice between them depends on the specific requirements of the problem.**

#### html export of the jupyter project below:



<iframe src="/assets/antenna.html" style="width:100%; height:500px;"></iframe>


<!-- Le bouton avec une classe spécifique -->
<a href="/assets/antenna.html" target="_blank" class="mon-bouton">
  Click here to open the project in a new tab
</a>

<style>
  /* Style spécifique pour le bouton avec la classe "mon-bouton" */
  .mon-bouton {
    position: relative;
    display: flex;
    place-content: center;
    text-align: center;
    padding: 0.56em 2em;
    gap: 0.8em;
    color: var(--accent-text-over);
    text-decoration: none;
    line-height: 1.1;
    border-radius: 999rem;
    overflow: hidden;
    background: var(--gradient-accent-orange);
    box-shadow: var(--shadow-md);
    white-space: nowrap;
  }

  @media (min-width: 20em) {
    .mon-bouton {
      font-size: var(--text-lg);
    }
  }

  /* Overlay pour les effets au survol */
  .mon-bouton::after {
    content: '';
    position: absolute;
    inset: 0;
    pointer-events: none;
    transition: background-color var(--theme-transition);
    mix-blend-mode: overlay;
  }

  .mon-bouton:focus::after,
  .mon-bouton:hover::after {
    background-color: hsla(var(--gray-999-basis), 0.3);
  }

  @media (min-width: 50em) {
    .mon-bouton {
      padding: 1.125rem 2.5rem;
      font-size: var(--text-xl);
    }
  }
</style>




