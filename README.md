# Defect Classification using VGG

This project demonstrates how to create a grayscale image classification model to classify a image dataset mixed with both normal and several kinds of defect image using VGG architecture in PyTorch. The model is trained on a dataset of images with corresponding labels read from a CSV file.

## Table of Contents

- Features
- Requirements
- Dataset Preparation
- Model Architecture
- Training
- Testing
- Results
- How to Use

## Features

- Uses PyTorch for building and training a convolutional neural network (CNN).
- Processes grayscale images.
- Supports batch training with a DataLoader.
- Saves model state and predictions to CSV.

## Requirements

To run this project, you need the following libraries:

- Python 3.6 or higher
- PyTorch
- Pandas
- PIL (Pillow)
- tqdm
- torchvision

You can install the required libraries using pip:

```bash
pip install torch torchvision pandas pillow tqdm

Dataset Preparation
1. Ensure you have your dataset organized as follows:
	/path/to/dataset/
    		train.csv               # CSV file with image paths and labels
    		test.csv                # CSV file with image paths
    		train_images/           # Directory containing training images
    		test_images/            # Directory containing test images
2. The train.csv should have two columns: the first column with image filenames and the second with corresponding labels.

Model Architecture
The model defined in this project is a modified VGG architecture, optimized for grayscale images. It consists of:
* Several convolutional layers with ReLU activation.
* Max pooling layers for downsampling.
* Fully connected layers for classification.
Training
1. Set your training parameters, including the number of epochs and batch size.
2. The training process includes the following steps:
o Load images using a custom GrayscaleDataset.
o Forward pass through the model.
o Compute loss and backpropagate.
o Update model weights using an Adam optimizer.
Testing
To evaluate the model on a test dataset:
1. Define the test dataset and create a DataLoader.
2. Use the trained model to predict labels for the test images.
3. Save the predictions along with image IDs to a CSV file.
Results
The results, including the model predictions, are saved in a CSV file named test_predictions.csv.
How to Use
1. Modify the paths in the code to point to your dataset.
2. Run the training script to train the model.
3. Use the provided testing script to evaluate the model on new images.



