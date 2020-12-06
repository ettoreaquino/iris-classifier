# IRIS FLOWER CLASSIFIER


> A very simple model to classify flowers based on the famous Iris flower dataset.

The dataset used here is one of the simplest Machine Learning study cases:
[**Iris**](https://en.wikipedia.org/wiki/Iris_flower_data_set).

I've separated it in two files: one for the features (flower measures) and one for the labels (flower species). The idea is handle tabular datasets structured in multiple files.
    
The original Fisher dataset contains a set of 150 records under five attributes - sepal length, sepal width, petal length, petal width and species:
      
| sepal length | sepal width | petal length | petal width |   species |
|      :-:     |     :-:     |      :-:     |     :-:     |     :-:   |
|      5.1     |     3.5     |      1.4     |     0.2     | I. setosa |
|      4.9     |     3.0     |      1.4     |     0.2     | I. setosa |
|      4.7     |     3.2     |      1.3     |     0.2     | I. setosa |
|      4.6     |     3.1     |      1.5     |     0.2     | I. setosa |
|      5.0     |     3.6     |      1.4     |     0.3     | I. setosa |
|      5.4     |     3.9     |      1.7     |     0.4     | I. setosa |
|      4.6     |     3.4     |      1.4     |     0.3     | I. setosa |
|      5.0     |     3.4     |      1.5     |     0.2     | I. setosa |
|      4.4     |     2.9     |      1.4     |     0.2     | I. setosa |
|      4.9     |     3.1     |      1.5     |     0.1     | I. setosa |
|      ...     |     ...     |      ...     |     ...     |    ...    |
    
Based on this dataset we can split it into two pieces. One for the flower measures, and the other for the corresponding species. Further ahead we are going to name this datasets as:
> **entries**: flower measurements dataset
    
>**classes**: the corresponding classification for the given measures entries

## CONFIGURATIONS:
I'll be using a Suport Vector Machine (SVM) algorithm to train our model. This algorithm is already implemented in a few Python frameworks but I chose to go with scikit-learn.

Regarding the Cross Validation method I'll be using the Stratified K Fold method:

[Stratified K Fold Cross Validation](https://www.geeksforgeeks.org/stratified-k-fold-cross-validation/)

## CLASSIFICATION
The classifier will be "pickled" using Python's `joblib` library, to be later used in a separate notebook dedicated to perform the prediction in a "service" fashion.