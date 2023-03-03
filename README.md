# 📚Awesome-ML-Lessons-Learnt📚
*A list of lesson learnt and things to watch out for in the Data Science and Machine Learning worlds*
***

## Table of contents
- [Data](https://github.com/kyaiooiayk/Awesome-ML-Lessons-Learnt/edit/main/README.md#data)
- [Project management](https://github.com/kyaiooiayk/Awesome-ML-Lessons-Learnt/edit/main/README.md#project-management)
- [Model training](https://github.com/kyaiooiayk/Awesome-ML-Lessons-Learnt/edit/main/README.md#model-training)
- [Classification](https://github.com/kyaiooiayk/Awesome-ML-Lessons-Learnt/edit/main/README.md#classification)
- [Training](https://github.com/kyaiooiayk/Awesome-ML-Lessons-Learnt/edit/main/README.md#model-training)
- [Recommender system](https://github.com/kyaiooiayk/Awesome-ML-Lessons-Learnt/edit/main/README.md#recommender-system)
- [Baises](https://github.com/kyaiooiayk/Awesome-ML-Lessons-Learnt/edit/main/README.md#biases)
- [Time series](https://github.com/kyaiooiayk/Awesome-ML-Lessons-Learnt/edit/main/README.md#time-series)
- [Deep Learning](https://github.com/kyaiooiayk/Awesome-ML-Lessons-Learnt/edit/main/README.md#deep-learning) 
***

## Data
- Don't assume the data is available.
- Don't assume the data is easy to get.
- Don't assume that the labels are perfect (human bias while labelling).
- Train-test leakage. Leaking information while splitting the data. Computing the mean and subtracting it from every image across the entire dataset and then splitting the data into train/val/test splits would be a mistake. Instead, the mean must be computed only over the training data and then subtracted equally from all splits (train/val/test). | [Ref](https://cs231n.github.io/neural-networks-2/) | [Notes](https://drive.google.com/drive/u/1/folders/1gqmJ9JAm_UR9Lzh6Zpj3R3pSLWUIdbQ7)
- **Not handling outliers in datasets properly** Outliers can either be a noise to ignore or important to take into account. ML algorithms differ in their sensitivity to outliers — AdaBoost is more sensitive to outliers compared to XgBoost which is more sensitive than a decision tree that would simply count an outlier as a false classification. | [Blog article](https://www.kdnuggets.com/2021/06/9-deadly-sins-ml-dataset-selection.html)
- **Using Normalisation instead of Standardisation** This is realted to issue of how to scale feature. To bring features to the same scale, use normalisation (MinMaxScaler) when the data is uniformly distributed and standardisation (StandardScaler) when the feature is approximately Gaussian. | [Blog article](https://www.kdnuggets.com/2021/06/9-deadly-sins-ml-dataset-selection.html)
- **Not verifying for duplicates in the training dataset** Double-checking often reveals that many of the examples in the test set are duplicates of examples in the training set. In such scenarios, the measurements of model generalization are non-deterministic (or meaningless). | [Blog article](https://www.kdnuggets.com/2021/06/9-deadly-sins-ml-dataset-selection.html)
- No unit tests for validating input data: In traditional software development projects, it is a best practice to write unit tests to validate code dependencies. In ML projects, a similar best practice needs to be applied to continuously test, verify, and monitor all the input datasets. This includes ensuring test sets yield statistically meaningful results and representative of the data set as a whole. | [Blog article](https://www.kdnuggets.com/2021/06/9-deadly-sins-ml-dataset-selection.html)
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
***

## Classification
- In fraud modeling, AUC is not the only metric that matters. You have to consider what is the fraud loss in $ and lifetime value $ lost should you ban the wrong user.
- **Inflating recall on imbalance dataset** If the data is resampled (oversampling) before splitting it into training and test  sets, the recall score will be inflated. The appropriate strategy is to split the data into a training and test set first and then to resample the data.
***

## Recommender system
- In a recommender system, CTR or NDCG is not the only metric that matters. You have to consider candidate diversity, feedback bias, and $ monetization generated from purchases or Ads
***

## Time series
- If the time time series is a random walk, using the R2 metric as a proxy to establish how good the predictive power of the model is, may suggest overly optimistic results when in reality the model has not predictive power at all. | [Blog article](https://www.linkedin.com/pulse/how-use-machine-learning-time-series-forecasting-vegard-flovik-phd/) | [Notes](https://drive.google.com/drive/u/1/folders/1gqmJ9JAm_UR9Lzh6Zpj3R3pSLWUIdbQ7)
- Target leakage: Think of it in terms of the timing or chronological order that data becomes available, not merely whether a feature helps make good predictions. | [Blog article](https://www.kaggle.com/code/alexisbcook/data-leakage/tutorial) 
- **Temporal leak** If you’re trying to predict the future given the past (for example, tomorrow’s weather, stock movements, and so on), you should not randomly shuffle your data before splitting it, because doing so will create a temporal leak: your model will effectively be trained on data from the future. In such situations, you should always make sure all data in your test set is posterior to the data in the training set. 
***

## Paradoxes
- Accuracy Paradox | [Tutorial](https://github.com/kyaiooiayk/Statistics-Probability-Notes/blob/main/tutorials/5%20Statistical%20Paradoxes.ipynb) | [Notes](https://drive.google.com/drive/u/1/folders/1YW0sN9uGx7bOUbXQOwmZ3RNGoeRDqbiz)
- False Positive Paradox | [Tutorial](https://github.com/kyaiooiayk/Statistics-Probability-Notes/blob/main/tutorials/5%20Statistical%20Paradoxes.ipynb) | [Notes](https://drive.google.com/drive/u/1/folders/1YW0sN9uGx7bOUbXQOwmZ3RNGoeRDqbiz)
- Gambler’s Fallacy | [Tutorial](https://github.com/kyaiooiayk/Statistics-Probability-Notes/blob/main/tutorials/5%20Statistical%20Paradoxes.ipynb) | [Notes](https://drive.google.com/drive/u/1/folders/1YW0sN9uGx7bOUbXQOwmZ3RNGoeRDqbiz)
- Simpsons Paradox | [Tutorial](https://github.com/kyaiooiayk/Statistics-Probability-Notes/blob/main/tutorials/5%20Statistical%20Paradoxes.ipynb) | [Notes](https://drive.google.com/drive/u/1/folders/1YW0sN9uGx7bOUbXQOwmZ3RNGoeRDqbiz)
- Berkson’s Paradox | [Tutorial](https://github.com/kyaiooiayk/Statistics-Probability-Notes/blob/main/tutorials/5%20Statistical%20Paradoxes.ipynb) | [Notes](https://drive.google.com/drive/u/1/folders/1YW0sN9uGx7bOUbXQOwmZ3RNGoeRDqbiz)
***

## Biases
- Self-selection bias
- Omitted variable bias
- Sponsorship or funding bias
- Sampling bias (also known as distribution shift)
- Prejudice or stereotype bias
- Systematic value distortion
- Experimenter bias
- Labeling bias
- Confirmation bias: people's tendency to process information by looking for, or interpreting, information that is consistent with their existing beliefs.
- Survivorship bias: the phenomenon where only those that ‘survived’ a long process are included or excluded in an analysis, thus creating a biased sample.
***

## Deep Learning
- Avoid using fully-connected layers or MLPs in general** For any structured data, like spatial functions, or field data in general, convolutions are preferable, and less likely to overfit. E.g., you’ll notice that CNNs typically don’t need dropout, as they’re nicely regularized by construction. For MLPs, you typically need quite a bit to avoid overfitting.
***
