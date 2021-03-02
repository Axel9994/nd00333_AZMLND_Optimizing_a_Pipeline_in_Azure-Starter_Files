# Optimizing an ML Pipeline in Azure

## Overview
This project is part of the Udacity Azure ML Nanodegree.
In this project, we build and optimize an Azure ML pipeline using the Python SDK and a provided Scikit-learn model.
This model is then compared to an Azure AutoML run.

## Summary
This project is a Azure Machine Learning Pipeline using Bank Marketing Data for predict if a client 
subscribed a deposit in a term using Binary Classification Algorithm, Running a Hyperdrive Pipeline
for Hyperparameter Optimization or Azure Automatic Machine Learning

The Final Solution was the LightGBM Algorithm with MaxAbsScaler for normalization that score 0.9136
that is sligthy better than the best HyperDrive Run of Logistic Regression with Regulation strength 
of 0.3 and 50 max iterations

## Scikit-learn Pipeline
I am using Azure Machine Learning Hyperdrive for build Scikit-learn pipeline with bank marketing data, 
Tune C and max_iteration hyperparameters in Logistic Regression. The Hyperdrive pipeline help to tune
these parameters using Random Parameter Sampling and Bandit Policy.

I choose Random Parameter Sampling because I can choose dynamically random hyperparameter in parallels 
using the compute cluster

I choose Bandit Policy for implement early stopping policy based in the distance from 
the best run of experiment using the slack_factor

## AutoML
The model generated by the AutoML Pipeline was a Voting Ensemble with newton-cg solver and 0.9176 accuracy
## Pipeline comparison
Both Pipelines has a similar performance with a slighty best performance the Voting Ensemble Pipeline

## Future work
Future Work is Apply AutoML excluding XGBoost and with more experiment time for get the best posible model from Azure AutoML


