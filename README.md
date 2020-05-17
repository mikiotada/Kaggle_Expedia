# ML_Expedia

The data was retrieved from Kaggle.com and can be found in the link down below.

Note: train.csv is too big to upload. The data in this repo is the reduced data that contains only 10 cluster ids.

https://www.kaggle.com/c/expedia-hotel-recommendations/data


# Project Summary

The goal of this project was to predict which hotel cluster a user will book based on their behaviors on the website and other various information. The business impact of this goal can help Expedia provide personalized hotel recommendations to their users to improve user experience with their vacation planning, which can ultimately increase revenue for Expedia.

We downsampled the original dataset from 0-99 (37 million samples) hotel cluster IDs to only 0-9 (4 million samples) hotel cluster IDs. In addition, for a more efficient workflow, we randomly sampled 1 million samples to minimize runtime. Models that we used for this project include Random Forest, Decision Tree, Multiclass Logistic Regression, and k-nearest neighbor. For this problem, precision is the north star metric because we want to develop a model that will predict hotel clusters as precise as possible.

After running the four different model with default hyperparameters, we found that Decision Tree and Random Forest are good baseline models to improve. After tuning for the best hyperparameters for these two models, we ran the models with 4 million rows dataset and achieved around 63% weighted average precision score for both Random Forest and Decision Tree.

In a business view, a weighted average precision around 63% in our context means that the model can correctly predict 63% each hotel cluster ID 0-9 in weighted average, is correctly predicted. Our model does a better job than randomly predicting a hotel cluster. However, productizing our model depends on how well the current Expedia's model performs. One advantage of our model is its speed in returning a result. Random Forest and Decision Tree are fast to show a predicted hotel cluster once the models are trained. For user experience perspective, a user doesn't have to wait a long time to see the outcome/predicted hotel cluster.
