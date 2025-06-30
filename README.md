# Joint modelling of CA19.9 and OS/RFS in Pancreatic Ductal Adenocarcinoma

## Introduction

This repository contains additional output and information to help interpret the results of a joint model invesitgating the association between longitudinal CA19.9 and OS/RFS in patients with Pancreatic Ductal Adenocarcinoma (PDAC).

Resutls are presented into two sections

* Lanadmark Analyses
* Dynamic Prediction

Following the analyses included in the manuscript, 4 models are fit:

1. Overall Survival Model with a current value association
2. Overall Survival Model with a current slope association
3. Recurrence Free Survival Model with a current value association
4. Recurrence Free Survival Model with a current slope association

## Landmark Analyses

Here we use the random effects from each model to estimate each patients percentage change in CA19.9 measured relative to baseline.  We use these percentages to categorise patients into one of 3 groups - 

* A reduction in CA19.9
* A moderate increase in CA19.9 (Increase <25%)
* A high increase in CA19.9 (Increase >25%)

We then use each of these groups to apply landmark analyses and produce Kaplan Meier plots to estimate survival probabilities.

## Dynamic Prediction 

Dynamic prediction estimated are obtained to estimate future longitudinal profiles of CA19.9 and survival probabilities conditional on the CA19.9 that has been observed up until some point in time.  We present conditioal probabilities for a patient with the following characteristics

  Treatment: GemCap
  Lymph Nodes: Positive
  WHO: 1
  Differentiation: 1 (Well)
  Diabetic: No
  Sqrt(Maximum Tumour Size): 5.5
  Trial: ESPAC4

For this hypothetical patient we generate predictions based on 5 scenarios of changing CA19.9 between baseline and 2 years follow-up

 * Decreasing from a baseline of 35 to 20 
 * Increasing from a baseline of 35 to 95 
 * Increaseing from a baseline of 35 to 1000 
 * Decreasing from a baseline of 100 to 1000 
 * Decreasing from a baseline of 100 to 35 


