# 📚Awesome-ML-Lessons-Learnt📚
*A list of lesson learnt and things to watch out for in the Data Science and Machine Learning worlds*
***

## Table of contents
- [Data](https://github.com/kyaiooiayk/Awesome-ML-Lessons-Learnt/edit/main/README.md#data)
- [Project management](https://github.com/kyaiooiayk/Awesome-ML-Lessons-Learnt/edit/main/README.md#project-management)
- [Model training](https://github.com/kyaiooiayk/Awesome-ML-Lessons-Learnt/edit/main/README.md#model-training)
- [Classification](https://github.com/kyaiooiayk/Awesome-ML-Lessons-Learnt/edit/main/README.md#classification)
- [Recommender system](https://github.com/kyaiooiayk/Awesome-ML-Lessons-Learnt/edit/main/README.md#recommender-system)
***

## Data
- Don't assume the data is available.
- Don't assume the data is easy to get.
- Don't assume that the labels are perfect (human bias while labelling).
- Leaking information while splitting the data. Computing the mean and subtracting it from every image across the entire dataset and then splitting the data into train/val/test splits would be a mistake. Instead, the mean must be computed only over the training data and then subtracted equally from all splits (train/val/test). | [Ref](https://cs231n.github.io/neural-networks-2/) | [Notes](https://drive.google.com/drive/u/1/folders/1gqmJ9JAm_UR9Lzh6Zpj3R3pSLWUIdbQ7)

***

## Project management
- Don't fail to start over and reassess when you realise the project is going in weird directions.
- Don't fail to connect model's objective and the way the model might be used.
- Don't fail to appreciate the core of the problem could effectively be predicting something way bigger and more complex.
- Put usability and production needs before model accuracy and not viceversa.
- Don't start the ML project until you agreed on the scope with the client. Otherwise, the client may move the goalpost later.
- Don't touch the model until you understand what the real KPI for the business are.
- Don't start modelling unless you have performed a thoroughly EDA!
***

## Model training
- Don't train the model on the entire data. Split into train, valid, test. Fit your model on train, optimize on valid, and measure on test.
- Don't toss too many uncorrelated and unnecessary features. Reduce, reduce, reduce down to the essentials!
- Don't celebrate too early. Watch out for data leakage and overfitted model.

## Classification
- In fraud modeling, AUC is not the only metric that matters. You have to consider what is the fraud loss in $ and lifetime value $ lost should you ban the wrong user.
***

## Recommender system
- In a recommender system, CTR or NDCG is not the only metric that matters. You have to consider candidate diversity, feedback bias, and $ monetization generated from purchases or Ads
***

## Time series
- If the time time series is a random walk, using the R2 metric as a proxy to establish how good the predictive power of the model is, may suggest overly optimistic results when in reality the model has not predictive power at all. | [Blog article](https://www.linkedin.com/pulse/how-use-machine-learning-time-series-forecasting-vegard-flovik-phd/) | [Notes](https://drive.google.com/drive/u/1/folders/1gqmJ9JAm_UR9Lzh6Zpj3R3pSLWUIdbQ7)
***

## Paradoxes
- Accuracy Paradox | [Tutorial](https://github.com/kyaiooiayk/Statistics-Probability-Notes/blob/main/tutorials/5%20Statistical%20Paradoxes.ipynb) | [Notes](https://drive.google.com/drive/u/1/folders/1YW0sN9uGx7bOUbXQOwmZ3RNGoeRDqbiz)
- False Positive Paradox | [Tutorial](https://github.com/kyaiooiayk/Statistics-Probability-Notes/blob/main/tutorials/5%20Statistical%20Paradoxes.ipynb) | [Notes](https://drive.google.com/drive/u/1/folders/1YW0sN9uGx7bOUbXQOwmZ3RNGoeRDqbiz)
- Gambler’s Fallacy | [Tutorial](https://github.com/kyaiooiayk/Statistics-Probability-Notes/blob/main/tutorials/5%20Statistical%20Paradoxes.ipynb) | [Notes](https://drive.google.com/drive/u/1/folders/1YW0sN9uGx7bOUbXQOwmZ3RNGoeRDqbiz)
- Simpsons Paradox | [Tutorial](https://github.com/kyaiooiayk/Statistics-Probability-Notes/blob/main/tutorials/5%20Statistical%20Paradoxes.ipynb) | [Notes](https://drive.google.com/drive/u/1/folders/1YW0sN9uGx7bOUbXQOwmZ3RNGoeRDqbiz)
- Berkson’s Paradox | [Tutorial](https://github.com/kyaiooiayk/Statistics-Probability-Notes/blob/main/tutorials/5%20Statistical%20Paradoxes.ipynb) | [Notes](https://drive.google.com/drive/u/1/folders/1YW0sN9uGx7bOUbXQOwmZ3RNGoeRDqbiz)
***
