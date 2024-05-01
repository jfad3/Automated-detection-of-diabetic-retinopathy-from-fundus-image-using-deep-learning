BalencedResNet.py

This file contains the code for training a ResNet50 model for image classification using Keras. Here's a step-by-step explanation:

Import necessary libraries and set random seeds for reproducibility.
Define model parameters such as batch size, epochs, learning rates, image dimensions, number of classes, etc.
Define a custom metric function kappa for calculating Cohen's Kappa score.
Specify the directories for training, validation, and test data.
Create data generators using ImageDataGenerator for data augmentation and preprocessing.
Define a function create_model to build the ResNet50 model architecture with custom output layers.
Create an instance of the model using create_model.
Freeze the base model layers initially for warm-up training.
Compile the model with an Adam optimizer and categorical cross-entropy loss.
Train the model for a few epochs with the base layers frozen (warm-up training).
Unfreeze all layers and compile the model again with a lower learning rate.
Define callbacks for early stopping and learning rate reduction.
Train the model for more epochs with all layers trainable (fine-tuning).
Save the trained model.
Plot the training history (loss, accuracy, and kappa score) using Matplotlib.

Baseline_Model.py

This file contains the code for training a baseline CNN model using PyTorch. Here's a step-by-step explanation:

Import necessary libraries and set device (GPU or CPU) for training.
Load the dataset using ImageFolder and apply data transforms.
Split the dataset into training, validation, and test sets.
Create data loaders for each set using DataLoader.
Define functions check_accuracy_part34 and train_part34 for evaluating and training the model.
Define a custom Flatten module to flatten the input tensor.
Define the CNN model architecture using sequential layers (Conv2d, BatchNorm2d, ReLU, MaxPool2d, Dropout, Linear).
Create an instance of the model and define the optimizer.
Train the model using train_part34 function.
Evaluate the trained model on the test set using check_accuracy_part34.

Baseline_Model_save.py

This file is similar to Baseline_Model.py but includes additional code for saving the trained model and plotting the training history. The steps are the same as Baseline_Model.py with the following additions:


Save the trained model using torch.save.
Plot the training loss and validation accuracy using Matplotlib and save the plots.

Util.py

This file contains utility functions and modules used in the other files. It includes the same imports as Baseline_Model.py.
