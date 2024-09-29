# Neural-Network-Challenge-2

## Introduction
This Jupyter notebook is designed to build and evaluate a neural network model for predicting two target variables: employee attrition (binary classification) and department (multiclass classification). I was provided assistance by Sean Morey, the instructor of the class. Brandon Wong, a BCS tutor, was a big help. Lastly, I could not have been able to finish this code without the help from the BCS Xpert Learning Assistant.

## Model Structure

The notebook builds a multi-output neural network model with two outputs:

    - Attrition Output: A binary classification using the sigmoid activation function.
    - Department Output: A multiclass classification using the softmax activation function.

The model is trained to simultaneously predict these two outputs using shared layers. Losses for both outputs are combined during training.


## Project Structure

1. Data Preprocessing:

    - Handled missing values, encodeded categorical variables, and normalized numerical data.
    - Performed train-test splits and reshaped data for input into the neural network.

2. Model Definition and Training:

    - Defined a neural network with multiple outputs using Keras' functional API.
    - The model was compiled with categorical crossentropy for the department output and binary crossentropy for the attrition output.
    - The model was trained for 100 epochs with validation accuracy as the primary performance metric.

3. Model Evaluation:

    - Evaluated the model's accuracy for both the attrition and department prediction tasks on test data.
    - Logged training and validation accuracy for both outputs across all epochs.

## Results

The notebook shows that while the model achieves reasonable accuracy on the test data, attrition prediction is challenging due to class imbalance.

## Potential Improvements

Class Imbalance Handling: Techniques like oversampling or undersampling could help improve attrition prediction.

Alternative Models: I would consider trying models like Random Forest, which may perform better with imbalanced datasets.