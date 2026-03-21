# ENG40011 - Engineering Technology Innovation Project
*Semester 2, 2025*

#### The Problem 
During this unit we had to find an issue in the field of gynecology to solve using engineering principles. The problem that our group were able landed on was in identifying/ diagnosing endometriosis. This is a pervasive issue within the medical community, partly due to the difficulty in detecting more minor or early stages of the condition. A part of this is likely due to [ambiguities around the condition](https://www.sciencedirect.com/science/article/pii/S240566182100023X). 
These issues all seem to drive stigmas around the condition, which can inhibit the ability of professionals to [diagnose the condition in a time effective manner, or at all](https://www.mdpi.com/1660-4601/18/15/8210). 

#### The Project Solution
Our group came up with a system that detects endometriosis via the use of an AI that uses the answers from a symptom survey to attempt to predict the likelihood that a respondant may have the condition. The purpose of this would be to both raise awareness of the condition, and help patients and medical professionals to figure out how they should approach investigating the symptoms. 
The AI driven survey would be hosted on a website for easier accessibility. 
![Survey Question Example](/blog/images/uni_projects/endo_ai_question.JPG). 
Upon completing the survey, the AI would also provide some SHAP results, which is basically a summary on how each survey answer contributed to the final prediction. 
![Survey Results Example](/blog/images/uni_projects/endo_ai_results.JPG). 

#### My Part
My role in the project was to find and train the AI algorithm on a dataset of survey data labelled with an associated endometriosis diagnosis (positive or negative result). I worked with another group member on this, where we both trained an assortment of AI algorithms:
![Trained AI Models](/blog/images/uni_projects/endo_ai_models.JPG)  
Each of the above models were compared in terms of a number of different performance measures (Each score was converted to a percentage and averaged to produce a cumulative score):
![AI Models Compared Performance](/blog/images/uni_projects/endo_ai_model_comparisons.JPG) 

An interesting AI model from this is the bayesian neural network (BNN), this model uses probability distributions for it's learned weights. This allows for the model to model uncertainty along with it's predicitions. Every other model we trained was able to output a probability between 0 and 1. While the bayesian neural network was able to output an uncertainty along with this prediction (eg 0.75 ± 0.12). We did not end up pursuing this model though due to issues with implementing SHAP, and the model requiring a lot of computation time to train and run. Thus the model we ended up using was the Multilayered Perceptron, in other words a feed forward neural network. 
