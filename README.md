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

## Data Management

Can support both explicit rating data and implicit rating data
* Explicit rating data require users to indicate their interests proactively. However, explicit rating data are not always readily available as many users may be reluctant to rate products
* Implicit rating data are often readily available since they are mainly connected with users’ implicit behaviors. For example, purchase history, browsing history, mouse clicks etc.
* As such, many recommender models are centered on implicit rating data which indirectly reflects user’s opinion through observing user behavior

Can support various data splitting schemes
* Generate training set and test set for model evaluation (accuracy metrics)
* Generate leave-one-out (LOO) training set, test set and anti-test set for model evaluation (ranking metrics)
* Generate full training set and anti-test set for evaluation (diversity metrics) and training/prediction
* Generate user-specific anti-test set for prediction

## Model (Algorithm) Design

Can support both Collaborative Filtering (CF) model and Deep Neural Network (DNN) based model
* Collaborative Filtering model includes clustering models (KNN inspired models) and matrix factorization based models (SVD, NMF etc.)
The matrix factorization model is widely used in recommender systems for its better capability in dealing with sparsity and scalability. However, it can not capture complex nonlinear and intricate relationships that may be predictive of users’ preferences (replace dot production)
* Deep Neural Network model are designed and used to address those issues (AutoRec, BPR, NeuMF etc.)

Can support various recommendation tasks
* Explicit ratings prediction based on the explicit rating data
* Top-n recommendation ranks all items for each user personally based on the explicit/implicit rating data 
* DNN has been proven to be suitable to address the limitation of matrix factorization and enrich the expressiveness of matrix factorization. 
* Integration of DNN into ratings prediction based on the explicit rating data (AutoRec)
* Integration of DNN into item rankings based on the implicit rating data (BPR, NeuMF)

