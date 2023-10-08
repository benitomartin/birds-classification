# BIRDS CLASIFFICATION 🦅

<p align="center">
    <img src="images/sample_image.jpg" width="500" height="400"/>
</p>

This repository hosts a notebook featuring an in-depth analysis of 2 **Pytorch EfficientNet** models, along with an app deployment using Gradio. The following models were meticulously evaluated:

- EffNetB0
- EffNetB2

The dataset used has been downloaded from [Kaggle](https://www.kaggle.com/datasets/gpiosenka/100-bird-species) and contains a set of 525 bird species. 84635 training images, 2625 test images(5 images per species) and 2625 validation images(5 images per species).

The app can be tested in **Hugging Face** following this [link](https://huggingface.co/spaces/bmartinc80/birds_pytorch).

## 🪶 Set Up

In the first stage, a set of helper functions was created in order to easily perform the modelling and prediction

- **Set seed**: Set random seeds for PyTorch operations, both on the CPU and the GPU
- **DataLoaders**: Create data loaders for training and testing datasets using PyTorch's DataLoader class
- **Writer**: SummaryWriter object for logging experiments and metrics in TensorBoard
- **Training and Testing**: Several functions for training and testing a PyTorch model 
- **Plots**: Several plots including loss curve, predictions and images

## 📳 Modelling

The first approach was to train 2 Pytorch EfficientNet models (EffNetB0, EffNetB2) with 5 and 10 epochs using the pretrained model weights of EffNetB0 for the DataLoaders in order to stablish a baseline. The EffNetB2 with 10 epochs showed the best performance above **93%** on the test set.

<p align="center">
    <img src="images/accuracy.png" />
</p>