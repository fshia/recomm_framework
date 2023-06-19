# An integrated framework for recommender model development and deployment

## Introduction

Inspired by the Surprise library’s infrastructure, and the application of Deep Neural Network (DNN) to the recommender system, I come up with an idea to integrate the model development and deployment pipeline into a recommender framework. I name it Integrated Framework.

The integrated framework (IF) has 4 components:
* Data Management
* Model Design
* Model Evaluation
* Model Deployment

To summarize the highlights of IF:
* Support both explicit rating data and implicit rating data
* Support various data splitting schemes
* Support both Collaborative Filtering models and Deep Neural Network based models
* Support various recommendation tasks
* Support model evaluation metrics for various recommendation tasks
* Support analyzing and comparing the model(s) performance
* Support various optimization approaches
* Support model packaging that is useable across the enterprise
