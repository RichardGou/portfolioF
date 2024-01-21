---
title: Machine learning for helping managing hospitals
publishDate: 2024-01-16 00:00:00
img: /assets/hospital.png
img_alt: work data viz
description: |
  Python for Data Analysis: Diabetes in 130-US Hospitals (1999-2008)
tags:
  - Python
  - Data visualization
  - Machine learning
---


### Project Focus :
We undertook a comprehensive study titled "Python for Data Analysis: Diabetes in 130-US Hospitals (1999-2008)." Our project aimed to analyze a decade's worth of clinical data from 130 US hospitals, focusing specifically on patients diagnosed with diabetes. The data encompassed various aspects such as laboratory tests, medications, and details of hospital stays up to 14 days.

#### Step 1 : Data Cleaning
- Missing Values: Identifying and addressing gaps in the dataset where information is absent.
- Multiple Encounters: Handling instances of repeated data entries for the same entities.
- Useless Columns: Removing columns that do not contribute valuable information for analysis.
- Missing Genders: Dealing with incomplete gender information in the dataset.
- Mapping the Data: Organizing and categorizing data to enhance clarity and usefulness.
- Data Types: Ensuring each data column is in its appropriate format (numerical, categorical, etc.).
- Re-Writing Data: Modifying data entries for consistency and correctness.
- Eliminating Zero Variance Data: Removing data that shows no variation and offers no insight.
- Custom Variables: Creating new variables tailored to specific analysis needs or goals.
- Feature Engineering - chi2: Applying Chi-square tests to identify and create relevant features.
- Data Balancing: Adjusting the dataset to handle imbalances in data representation.

#### Step 2 : Data Analysis
Here, our objective was to uncover relationships through data analysis between our target feature, which is the patient's readmission status, and other features. Below are some of our plots:
<iframe src="/assets/HospitalDataAnalysis.JPG" width="640" height="290" frameborder="0" allowfullscreen></iframe>

#### Step 3.1 : Study using machine learning, Classification
The goal is to predict whether a patient will be readmitted afterwards or not. Finding an answer is really important because it will help the hospital to immediately identify patients with more severe diseases or those who require an adapted treatment.
Here, we tested three different types of classifiers:

- Linear Regression: This model provided a baseline for understanding the relationship between the dependent and independent variables due to its simplicity and interpretability.

- Random Forest: Chosen for its ability to handle non-linear data, Random Forest combines multiple decision trees to enhance accuracy and offers insights into feature importance.

- Decision Tree: Utilized for its ease of interpretation and minimal preprocessing needs, this non-parametric model efficiently handles both numerical and categorical data.

Here are the results that we obtained :
<iframe src="/assets/ModelHospital1.JPG" width="640" height="360" frameborder="0" allowfullscreen></iframe>

#### Step 3.2 : Second study using machine learning, Regression
The objective is to forecast the duration of a patient's first hospital stay, thereby aiding the hospital in efficiently allocating rooms based on the anticipated length of stay.

We experimented with the following models:

<iframe src="/assets/ModelHospital2.JPG" width="640" height="460" frameborder="0" allowfullscreen></iframe>

Our best-performing model is Gradient Boosting, which achieved the lowest RMSE and has successfully predicted the number of days a patient will stay in the hospital with high accuracy.

#### Conclusion

In summary, our project not only provided crucial insights into the management of diabetes but also underscored the potential of machine learning in revolutionizing healthcare. We advocate for an informed, proactive approach in the management of chronic diseases, aiming for a healthcare system that prioritizes prevention and personalized care.



#### html export of the jupyter project below:



<iframe src="/assets/diabetes.html" style="width:100%; height:500px;"></iframe>


<!-- Le bouton avec une classe spécifique -->
<a href="/assets/diabetes.html" target="_blank" class="mon-bouton">
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




