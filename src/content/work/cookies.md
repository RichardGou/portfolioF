---
title: Optimisation for a doll of biscuits
publishDate: 2024-01-15 00:00:00
img: /assets/biscuits.png
img_alt: work data viz
description: |
  Optimizing biscuit production from a single roll of dough
tags:
  - Genetic Algorithm
  - Constraint Satisfaction Problem
  - Dynamic Programming
---






### Project Focus :

Optimizing biscuit production from a single roll of dough, with an emphasis on maximizing the value of biscuits placed on the dough while considering defects and constraints like non-overlap and integer positions.

> Dynamic Programming :

- Served as a benchmark.
- Achieved an optimal solution score of 760.
- Exhibited efficient time and memory complexities.

>  Genetic Algorithms (GA)

- Multiple variants were developed, each improving profitability and defect handling.
- The best GA variant reached a total value of 600.

>  Greedy Search

- Implemented in three different heuristic-based methods.
- The most effective heuristic achieved a total value of 674.

>  Constraint Satisfaction Problem (CSP)

- Provided high value quality, achieving 760 in total value.
- Featured higher time and space complexities compared to heuristic methods.
- Using Or-tools libraries

### Conclusion
Our project underscores the importance of selecting appropriate algorithms for optimization problems. It showcases the trade-offs between different approaches in terms of complexity, speed, and effectiveness. We concluded that dynamic programming was the most effective method for this specific challenge, emphasizing the significance of choosing the right strategies for efficient and successful problem-solving.



#### html export of the notebook below:



<iframe src="/assets/cookies.html" style="width:100%; height:500px;"></iframe>


<!-- Le bouton avec une classe spécifique -->
<a href="/assets/cookies.html" target="_blank" class="mon-bouton">
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




