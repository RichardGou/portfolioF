---
title: Air quality using ML
publishDate: 2024-01-17 00:00:00
img: /assets/airquality.png
img_alt: work data viz
description: |
  Estimating the air quality index (AQI) but with missing values (machines) so that it can be calculated easier and cheaper
tags:
  - Python
  - Data visualization
  - libraries
---

#### Air Quality Index (AQI) Analysis

##### Air Quality Index (AQI) Overview

The Air Quality Index (AQI) is a crucial tool for communicating air pollution levels to the public and forecasting future pollution. In this project, we explore a dataset of multiple pollutants to understand regional variations in AQI and investigate the possibility of reducing pollution impact by decentralizing urban areas. The primary focus is to evaluate whether AQI can be predicted using fewer components, thereby potentially lowering measurement costs.

Below, you will find a visualization showing the dispersion of our dataset, providing a quick overview of its composition:
<div style="text-align: center;">
    <img src="/assets/aqiHeatMap.png" />
</div>

##### Description and Formalization of the Problem

Measuring AQI is costly, involving multiple pollutants each requiring different protocols. Our goal is to identify if certain pollutants have a more significant impact on AQI and if some measurements can be omitted to reduce costs. We also aim to find pollutants measurable by similar means to optimize resource usage.

Global Impact and Measurement Accessibility
Lowering measurement costs can increase the geographic coverage of AQI monitoring. This is particularly relevant for countries with large unexploited areas, where breathable air is becoming a critical factor for development and habitation.

Prior to delving into machine learning analysis, we conducted a thorough data analysis to identify evident findings and correlations. Notably, the most significant correlation observed was between the AQI and PM2.5 particles, as illustrated below:

<div style="text-align: center;">
    <img src="/assets/aqireg.png" />
</div>

##### Methodology

**Classification study:** Utilizing Decision Trees and Logistic Regression for their efficiency and interpretability in order to find the AQI category.

**Regression Study:** Exploring various regression models, including Linear, Ridge, Lasso, and advanced techniques like Random Forest and Gradient Boosting, to predict AQI value accurately.

##### Observations and Results

<div style="text-align: center;">
    <img src="/assets/modelsScoreAQI.png" />
</div>

**Decision Tree** showed high accuracy but struggled with certain AQI categories, indicating **potential overfitting**.

**Logistic Regression** presented a more balanced performance across different AQI categories.

<div style="text-align: center;">
    <img src="/assets/aqiPca.png" />
</div>

**Principal Component Analysis (PCA) :** revealed that the first two components explained a significant portion of the dataset's variance, suggesting the potential for dimensionality reduction.

<div style="text-align: center;">
    <img src="/assets/modelsReg.png" />
</div>

**Regression Performance:** Random Forest Regressor emerged as the most effective model, corroborating the hypothesis about non-linear relationships in the dataset.


The **3D PCA** plot underscored the strong association of AQI with the first principal component, affirming the effectiveness of PCA in capturing essential data features.

##### General Conclusion
The project achieved a 90% accuracy rate in predicting AQI category with fewer components, supporting the hypothesis of cost-effective AQI measurement, for the regression study, our best model appeared to be the Random Forest regressor and achieved to predict very accurately (low RMSE) the exact value for the AQI. The analysis underscored the importance of data preprocessing, feature selection, and the careful choice of algorithms. Future improvements could include broader algorithm exploration and linking AQI data to global events. The findings also highlight areas with high air quality that could be potential sites for sustainable development.


#### html export of the jupyter project below:



<iframe src="/assets/aqi.html" style="width:100%; height:500px;"></iframe>


<!-- Le bouton avec une classe spécifique -->
<a href="/assets/aqi.html" target="_blank" class="mon-bouton">
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




