# Neural Networks for Multiclass Classification

Suppose you want to build a simple neural network to recognize handwritten digits from 0 to 9. The goal is to classify grayscale images of these digits based on their pixel data.

You have a dataset containing 5000 images of digits 0 through 9, each resized to 20×20 pixels and flattened into 400 features. Using this data, you can train a neural network model to predict which digit (from 0 to 9) an input image corresponds to.

<img width="455" height="411" alt="Screenshot 2025-07-16 at 11 30 46" src="https://github.com/user-attachments/assets/98e69ecc-5745-4921-b1b8-8ff96801f301" />

### Model representation

The neural network we will use is shown below.

This has two dense layers with ReLU activations followed by an output layer with a linear activation.
 - Recall that our inputs are pixel values of digit images.
 - Since the images are of size  20×20, this gives us  400 inputs

<img width="663" height="212" alt="Screenshot 2025-07-16 at 13 09 21" src="https://github.com/user-attachments/assets/b0cf5ae9-560f-4c30-a17f-86057128246f" />


## Results

After training the model, you can evaluate its performance on test data and visualize how well it classifies each digit.

The model achieves high accuracy distinguishing between the ten digits based on pixel intensity patterns. Most predictions are correct, with very few errors observed across thousands of examples.

Example Predictions
The model takes an input array of 400 pixel values (each between 0 and 1). It returns a vector of probabilities for each digit class, and the digit with the highest probability is selected as the prediction. For example:

Input: Flattened pixel array of a digit 2 image
Output: Prediction = 2 (digit two)

Input: Flattened pixel array of a digit 7 image
Output: Prediction = 7 (digit seven)

Input: Flattened pixel array of a digit 9 image
Output: Prediction = 9 (digit nine)
