# Survival Analysis on International Strokes Trial (IST-3)

**Authors:** Atlanta Liu, Maruthi Mutnuri

**Date:** Winter 2020

### What's in this repository?

This repository contains a final report for our advanced statistical modelling course, which looks at analyzing the survival rates for patients who were suffering from re-occurring ischemic stroke. The goal of this analysis was to find which medication (heparin or aspirin) improves overall survivability the most over the course of the 6-month period from the start of clinical randomization. The entire analysis was conducted through RStudio. Below is a general list of the procedures we followed for our analysis.

### Procedures

- Kaplan-Meier Survival Curve
- Log Rank Test
- Cox Proportional Hazards Modelling
- Testing Model Assumptions and Goodness of Fit:
  - Proportional Hazards Test
  - Linearity of Covariates
  - Influential Outliers
- Time Splitting Data
- Hazard Ratio Interpretations

### Kaplan-Meier Curve (Heparin vs Aspirin)

![Kaplan-Meier Curve](/Images/Kaplan_Meier.png)

### Study Limitations

We ran into quite a few limitations with this project. Initially, we wanted to run a Cox-Proportional Hazards model to test the differences in survival rates. However, we found that a few variables were not passing some of the model assumptions (proportional hazards). We decided to split the times using a SurvSplit model. While this helped us meet the assumption, it was not the most ideal way of dealing with this issue. A better way of dealing with this would be to use a stratified cox-proportional model, which allows us to  stratify the variables that failed to meet the assumptions. This stratification produces multiple baseline hazard ratios for each strata (so for each age group there would be a separate hazard ratio). Unfortunately, we ran into a few difficulties when we attempted this method and there was limited documentation online. In only half a week from choosing this dataset, we managed to pull together this report.


