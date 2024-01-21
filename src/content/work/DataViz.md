---
title: Real estate analysis in France
publishDate: 2023-06-06 00:00:00
img: /assets/stock-1.jpg
img_alt: work data viz
description: |
  A project aimed at analyzing real estate information in France, trends, clustering...
tags:
  - Python
  - Data visualization
  - libraries
---

## Subject

> What is this all about ?

The data we are working with consists of real estate transactions that have taken place over the past five years in mainland France and the overseas departments and territories (DOM-TOM), excluding Alsace, Moselle, and Mayotte.

Prior to our analysis, we conducted data preprocessing due to the presence of a significant amount of missing values that could potentially alter the interpretation of certain analyses. Additionally, we encountered numerous duplicates, particularly instances where the same apartment was sold multiple times on the same day. These nuances were carefully addressed in our data preprocessing.

Once the data was cleaned, we utilized various libraries (such as numpy, seaborn, pandas, matplotlib.pyplot, folium, etc.) to create a variety of graphical representations for different interpretations, including 3D and 2D graphs, as well as heatmaps.



## My complete work (html export of the jupyter project) below:



<iframe src="/assets/ProjetPythonFinal.html" style="width:100%; height:500px;"></iframe>


<!-- Le bouton avec une classe spécifique -->
<a href="/assets/ProjetPythonFinal.html" target="_blank" class="mon-bouton">
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




