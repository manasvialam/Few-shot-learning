# Few-shot-learning


## Prototypical Networks on CIFAR-100
![FSL](https://github.com/user-attachments/assets/2edda847-5220-4c49-bcc7-89ed46c8852f)
This repository implements Prototypical Networks for few-shot learning using the CIFAR-100 dataset. The model leverages a pretrained ResNet-18 backbone for feature extraction.

### Key Components
Dataset: Utilizes CIFAR-100, consisting of 100 classes, with each class containing 600 images. The dataset is split into training and testing sets.

Prototypical Networks: The architecture computes class prototypes based on the support set and measures distances to classify query images.

### Training:

The model is trained using episodic training with N-way, N-shot, and N-query settings.

Optimizer: Adam

Loss function: CrossEntropyLoss

Evaluation: The model is evaluated on multiple tasks, computing accuracy, precision, recall, and F1 score.

### Code Overview
Imports: Libraries like PyTorch, torchvision, and easyfsl are used for model implementation and evaluation.

Data Preparation: The dataset is transformed, downloaded, and loaded using DataLoader with TaskSampler.

Model Definition: A custom Prototypical Networks class is defined, utilizing a pretrained ResNet-18 for feature extraction.

Training Loop: The model is trained over a specified number of episodes, updating the weights based on the computed loss.

Evaluation: The model is tested on the test set, and performance metrics are reported.


This repository includes two files featuring the same code but differing in the number of training episodes: one with 500 episodes and the other with 40,000 episodes. The substantial increase in training episodes has led to a marked improvement in the model's performance and accuracy, highlighting the significance of extensive training in achieving better results in few-shot learning tasks.
