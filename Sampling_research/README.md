<h1 align="center">Sampling research</h1>

## Description
Solving data science tasks we often face with lack of data or its imbalanced distribution. [Undersampling](https://imbalanced-learn.org/stable/under_sampling.html) and [oversampling](https://imbalanced-learn.org/stable/over_sampling.html) methods may help us to deal with these problems. Aim of these projects is to find out in which terms sampling methods could be most useful.
## Input data and expected result
There are 4 [datasets](https://github.com/SergeyMaslikhov/DS_projects/tree/main/Sampling_research/datasets) available. Each one is text sample labeled for classification. Three of them are english and one is russian. Expected result are plots that compare F1 measure on test set for classificators built with and without sampling methods.
## Results
Code consists of 2 parts (for preprocessing data and building models): <br>
[preprocessing_samples.ipynb](https://github.com/SergeyMaslikhov/DS_projects/blob/main/Sampling_research/preprocessing_samples.ipynb) is used for:
- Normalizing text in samples
- Deleting stop words
- Reorganizing dataset if needed (for example labeling objects with one class instead of set of classes)

[Sampling_research.ipynb.ipynb](https://github.com/SergeyMaslikhov/DS_projects/blob/main/Sampling_research/Sampling_research.ipynb) is capable of:
- Visualizing disbalance level - ratio between the smallest class in sample and the biggest one
- Optimizing hyperparemeters with Bayesian optimization
- Implementing ```class``` that takes sample and classifier as input and builds result matrix *N* x *M* of test scores, where *N* - number of disbalance levels, *M* - number of used sampling methods
- Plotting results of four samples for each classifier
- Saving results in excel file

## Requirements
To install necessary packages use:
```shell
pip install -r requirements.txt
```
