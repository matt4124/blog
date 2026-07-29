---
layout: post
title: "Making an AI to detect Endometriosis"
header: false
---

*Python · Machine Learning · Neural Networks · Multilayer Perceptron · Bayesian Neural Networks · SHAP · Explainable AI*

## Overview

As part of the ENG40011 Engineering Technology Innovation Project in Semester 2, 2025, our group investigated how engineering and artificial intelligence could be applied to challenges in gynecology.

We focused on the difficulty of identifying and investigating endometriosis, a condition that can be challenging to recognise due to the wide variation in symptoms and the difficulties associated with timely diagnosis.

Our proposed solution was an AI-assisted online survey that analysed a patient's reported symptoms and estimated the likelihood that their symptoms may be associated with endometriosis. The system was designed as a potential screening and decision-support tool, rather than a replacement for professional medical diagnosis.

## The Problem

Endometriosis can be difficult to identify, particularly when symptoms are less severe or overlap with other conditions.

Our project explored whether information collected through a structured symptom survey could be used by a machine-learning model to identify patterns associated with endometriosis.

The goal was to create a more accessible tool that could potentially:

- Increase awareness of endometriosis
- Help individuals better understand their symptoms
- Provide information that could support discussions with healthcare professionals
- Assist in identifying cases that may warrant further medical investigation

## The Proposed Solution

We developed a concept for an AI-powered survey hosted through a website.

The proposed workflow was:

**Symptom Survey → Machine Learning Model → Risk Prediction → Explainable AI Results**

After completing the survey, a user would receive a prediction from the machine-learning model along with SHAP (SHapley Additive exPlanations) results.

The SHAP explanation would show how individual survey responses contributed to the model's prediction, providing greater transparency into the reasoning behind the result.

![Survey Question Example](/blog/images/uni_projects/endo_ai_question.JPG). 
![Survey Results Example](/blog/images/uni_projects/endo_ai_results.JPG). 
![Trained AI Models](/blog/images/uni_projects/endo_ai_models.JPG)  
![AI Models Compared Performance](/blog/images/uni_projects/endo_ai_model_comparisons.JPG) 


## My Role

I worked with another group member to develop and evaluate the machine-learning component of the system.

My work included:

- Finding and preparing a labelled dataset containing survey responses and associated endometriosis diagnoses
- Training multiple machine-learning models
- Comparing model performance using several evaluation metrics
- Investigating Bayesian neural networks as an alternative modelling approach
- Evaluating the trade-offs between model performance, computational requirements, and explainability
- Contributing to the selection of the final model used by the proposed system
- Model Development and Comparison

Rather than selecting a model based on a single performance metric, we trained and compared multiple machine-learning approaches using several measures of performance.

The models were evaluated and their results were combined into an overall comparative score to help identify the most suitable approach for the application.

This process demonstrated that selecting a model for a healthcare application involves more than simply choosing the model with the highest predictive performance. Factors such as computational requirements and the ability to explain predictions also need to be considered.

## Investigating Bayesian Neural Networks

One of the more interesting approaches investigated was a Bayesian Neural Network (BNN).

Unlike conventional neural networks, Bayesian neural networks represent model parameters using probability distributions. This allows the model to provide information about uncertainty alongside its predictions.

For example, rather than simply producing a prediction such as:

75% likelihood

a Bayesian model could potentially provide a prediction such as:

75% ± 12%

This additional uncertainty information could be valuable when applying machine learning to healthcare-related problems, where understanding the confidence of a prediction is important.

However, we ultimately decided not to use the Bayesian neural network in the final system. The model introduced challenges with integrating SHAP explanations and required significantly more computational resources for training and inference.

## Final Model

The final system used a Multilayer Perceptron (MLP), a type of feed-forward neural network.

The MLP provided a practical balance between predictive performance, computational requirements, and compatibility with the explainability methods required by the project.

SHAP was then used to provide insight into how individual survey responses influenced the model's output.

## Key Takeaways

This project provided experience in applying machine learning to a healthcare-related problem while considering the practical limitations of deploying AI in sensitive domains.

A key takeaway was that model selection is not solely about predictive accuracy. The final solution also needed to consider interpretability, computational requirements, and how users could understand the model's predictions.

The project also demonstrated the value of explainable AI techniques such as SHAP, particularly when developing systems where users and professionals need to understand why a model produced a particular result.
