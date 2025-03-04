# Training, Testing, Validation Dataset

This one is going to be very short and very simple. 

When trying to train a machine learning model, we split our data into training, testing and validation datasets. Each of these have a particular role in our training process and should not be used interchangable.

When training a model we want to train multiple versions of the model and pick the best one, we might have some decisions to make in terms of how complex we want the model to be (revisit bias vs variance tradeoff) or simply not know which architecture is the best for the job until we experiment. Thus, in order to enable this process, we split our overall dataset into training, validation, and testing data - usually a (70%, 15%, 15%) split. 

### Training: Given directly to each model version to learn its parameters

### Validation: Used to evaluate diffferent trained versions of the model to pick the best version (versions differ in hyper-peremetrs like # layers of the neural network)

### Testing: Only used at the very end to give consumers, client some representation of how well they can expect the model to do. No decisions should be made based on this testing dataset.

When you are trying to train a model yourself, there is rarely an reason not to do this split. The rare exceptions:
1) Your model does not require Training (KNN)
2) You are doing cross validation - in this case you are essentially doing the sample splits but in a different way. 