# AI Application

## Machine Learning

- Unsupervised
- Supervised 
- Semi-supervised

## An intuitive definition of learning:

An algorithm that learns is typically nothing else than a mathematical function that depends on a set of parameters that are tuned, hopefully in some smart way, to make the algorithm output as close as possible to some expected output.

**Where**:
- mathematical function → Algorithm Type
- tuned → Optimiser
- close as possible → Loss Function (a math formula to measure "closeness")

**Remember:** x are inputs, y are labels (or target variables). 
y = ax + b, and you need to find the most optimal parameters (a and b).

## Optimisation

Optimization is the process of adjusting a model's parameters to minimize the difference between the predicted output and the actual output (i.e., the error).
This is typically done through iterative methods like gradient descent. The goal is to improve the model's performance on a given task, such as classification or regression, by minimizing a loss function.
(In supervised learning).

**Where**:
- parameters → Represented as θ₁, θ₂, ..., θₙ
- difference → Loss function
- iterative methods → Optimization technique (e.g., Gradient Descent)


## Reproducibility and Replicability 

- “Reproducibility” refers to instances in which the original researcher’s data and computer codes are used to regenerate the results.
- “Replicability” refers to instances in which a researcher collects new data to arrive at the same scientific findings as a previous study.

### Reproducibility in Machine Learning – How to achieve it (I/III)

- Set Random Seeds:
Initialize random number generators with fixed seeds to ensure consistent results in processes like data shuffling, weight initialization, and data splitting.
- Version Control for Code:
Use version control systems like Git to track and manage changes in your code.
- Document the Environment:
Specify and share the versions of the programming language, machine learning libraries, and other dependencies used (e.g., Python, TensorFlow, scikit-learn). Tools like Docker or Conda can be used to create reproducible environments.
- Use a Seed for Data Splits:
If the data is split into training, validation, and test sets, ensure the splits are reproducible by using a seed.
- Logging and Experiment Tracking:
Use experiment tracking tools (like MLflow, TensorBoard, or Weights & Biases) to log experiments, including parameters, metrics, and results.
- Automate the Workflow:
Use workflow automation tools to script the entire pipeline, from data preprocessing to model training and evaluation.

## Neural Networks

A neural network is a math function that depends on a set of parameters that are tuned, hopefully in some smart way, to make the network output as close as possible to some expected output.

An epoch is one complete pass through the entire training dataset by the learning algorithm.

Main components:
- NN architecture (type of network, nr of layers etc)
- Loss function
- Optimiser (the algorithm to find the minimum of the loss function)

Layers:
- Input Layer: Accepts the raw data.
- Hidden Layers: Perform intermediate computations. Deep networks have many.
- Output Layer: Produces the final prediction (classification, regression, etc.).
    
A neuron has:
- the weights (arameters that scale the input features or neuron outputs. They determine the strength of the connections)
- the activation function (introduce non-linearity -- Swish, ArcTan, Softplus, Leaky ReLU, ELU)
- biases (parameters added to the weighted sum to shift the activation function. Helps the model better fit the data)

Without activation functions, a neural network—no matter how many layers—would behave like a simple linear model. This means it wouldn’t be able to learn complex patterns like images, speech, or natural language.

Training Process:
- Forward pass → compute predictions
- Loss computation → how wrong is the prediction?
- Backward pass → compute gradients
- Parameter update → use optimizer to adjust weights/biases

## Important Metrics 

- Accuracy: The proportion of correctly predicted observations out of all observations.
- Specificity: The proportion of actual negatives correctly identified (also called the true negative rate).
- Sensitivity (Recall): The proportion of actual positives correctly identified (also called the true positive rate).
- Balanced Accuracy: The average of sensitivity and specificity, useful for imbalanced datasets.
- F1 Score: The harmonic mean of precision and recall, balancing false positives and false negatives.
- AUC (Area Under the ROC Curve): Measures the model's ability to distinguish between classes across all thresholds.


**Confusion Matrix** is a diagnostic tool that contains multiple values (TP, TN, FP, FN) rather than a single score.
Sensitivity (also called Recall or True Positive Rate) -- is the proportion of actual positives that are correctly identified.
Specificity (also called True Negative Rate) -- the proportion of actual negatives that are correctly identified.


## One-hot-encoding

One-hot encoding is a technique used to convert categorical variables into a form that could be provided to machine learning algorithms to do a better job in prediction. It involves representing each categorical variable with a binary vector that has one binary value for each category of the variable.


## Model Validation

Overfitting -- happens when a machine learning model learns the training data too well—including its noise and outliers—resulting in poor generalization to unseen data.

Cross-validation -- a technique for evaluating how well your model will generalize to independent data by partitioning the dataset into multiple train/test splits.

**Methods:**
- Hold-out Approach. Split the dataset into a training set and a test set once to evaluate model performance.
- Monte-Carlo Cross Validation. Repeatedly random-split the data into training and test sets to get a more robust performance estimate.
- K-Fold Cross Validation. Divide the data into k equal parts, train on k-1 parts, and test on the remaining one—rotating until each fold has been used as a test set.
- Leave-one-out Cross Validation (LOOCV). A special case of k-fold where k = number of data points, training on all but one instance and testing on the remaining one.
- Y-Randomisation (or Y-Scrambling). Shuffle the output labels to test whether the model’s performance is due to real patterns or just chance.

## Tensorflow Keras

TensorFlow is an open-source machine learning framework developed by Google that provides a comprehensive ecosystem for building, training, and deploying machine learning (ML) and deep learning (DL) models. It lets you define computational graphs, where nodes represent operations (e.g., matrix multiplication) and edges represent data (tensors) flowing between operations. It's highly optimized for training neural networks and supports both CPU and GPU acceleration. TensorFlow models can be run on desktops, servers, mobile devices, and even in browsers (via TensorFlow.js).

Keras is an API for building models.

## Hyper parameter tuning

A parameter is a value that is learned from the training data during the model training process. Example: weights and biases in a neural network.
A hyperparameter is a setting used in the design or learning process of a machine learning model that is not learned from the training data. 

- Example: learning rate, number of epochs, batch size, number of hidden layers
- Set before training
- Often tuned manually or via search algorithms (grid/random/Bayesian)

**Types of Hyperparameters:**
- Continuous Hyperparameters. Can take any real value within a range. Example: learning rate, regularization strength.
- Discrete Hyperparameters with Infinite Possibilities. Can take whole number values, and theoretically unbounded. Example: number of epochs, hidden layers, neurons per layer.
- Discrete Hyperparameters with Finite Possibilities. Limited to a fixed set of values or categories. Example: choice of optimizer (Adam, SGD), activation function (ReLU, sigmoid), learning rate scheduler type.
