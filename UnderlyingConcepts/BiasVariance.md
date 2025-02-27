# Bias Variance Tradeoff in Machine Learning

The Bias Variance tradeoff is a core underlying concept that any ML practioner should be aware of. It depicts the the tradeoff between simple and complex models in machine learning. 

First we will define the two concepts seperately, and then look at their interaction together. 

Direct definitions of the concepts:
### Bias : A measure of the inability of a machine learning method to capture a "true" relationship in data i.e how constrained a model is by design.

### Variance: A measure of how much a model's predictions change when trained on different subsets of data i.e how flexible a model is to its training data.

These two terms are also often related to overfitting and underfitting, so we should cover those relations too. 
1. High Bias often leads to underfitting: A model with high bias, means a model is so rigid that its unable to capture the underlying relationship altogether, it  does not even begin to fit to the training data, thus: underfitting.

2. High Variance often leads to overfitting: A model whose predictions change significantly based on different subsets of training data would struggle to generalize to data that it has not seen, whislt doing very well on data that is it trained on, thus: overfitting.

Based on these definitions, its obvious to see that our aim is a model with low bias (i.e one that has complete ability to capture any relationship in data completely) and low varaince (a moel that does not drastically switch its prediction). That being said, we can rarely do both at the same time. If I make my model constrained by design, it has a harder time bending to training data. On the other hand if I allow my model to be flexiblle to the training data, then there is little constraint to it in the first place.  

This relationship is called the Bias-Variance tradeoff.

In practicle terms, we often try to find a middle-ground between bias and variance, on that minizes both at the same time - this ofcourse is not a science by any means as data in the real world can follow all kinds of crazy patterns. Being aware of the reason for this tradeoff, you should be better equiped to find a model that is able to find that sweet spot. 

## Script:
That was a lot of information, below is a short paragraph to sumarize this tradeoff in 30 seconds.

The bias variance tradeoff refers to the inherent tradeoff between making a model simple or complex. Bias is measure of its simplicity, if a model has high bias, it has a harder time fitting to data that may be outside the models scope of complexitiy, like fitting a a linear model to quadratic data - this phenoma is often called underfitting. Variance is a measure of complexity, a model with high varaiance will have a very easy time fitting to data, so much so that it will fit its parameters to the noise of the data too to achieve even better training accuracy, like fitting a 3rd degree polynomial to quadratic data (with some random noise) - this pheonoma is often called overfitting. We aim to find the sweet spot between these 2 models, coping with having our model be not to simple and not too complex simoultenously is refered to ass the bias variance tradefoff.


**Note: A qualifier to this tradeoff is that the data you are dealing with has random variance in it, i.e, variance that is not predictable. Otherwise a infintely complex model could learn this random variance and would be able to have a perfect fit on both training and testing data alike. 