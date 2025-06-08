# Image_Classification_brain_cancer
This is an Image classification project using Pytorch.

## About the Dataset

### Brain Cancer - MRI Dataset
This dataset contains a comprehensive collection of MRI images for brain cancer research, specifically aimed at supporting medical diagnostics.

### Description
The Bangladesh Brain Cancer MRI Dataset is a comprehensive collection of MRI images categorized into three distinct classes:

-> Brain_Glioma: 2004 images
-> Brain_Menin: 2004 images
-> Brain Tumor: 2048 images

The dataset includes a total of 6056 images, uniformly resized to 512x512 pixels. These images were collected from various hospitals across Bangladesh with the direct involvement of experienced medical professionals to ensure accuracy and relevance. This dataset is valuable due to the difficulty in obtaining such medical imaging data and offers a reliable resource for developing and testing diagnostic tools.

This is the link of this dataset in Kaggle - https://www.kaggle.com/datasets/orvile/brain-cancer-mri-dataset

## About the Process
I have developed 2 model in this project. One is a simple ANN model with 3 dense layer. Another is a CNN model with 3 conv layer and 2 dense layer.

### ANN
It is just a simple model. I have added dropout layers to control Over fitting.

### CNN
It gave quite good result. I have added batch normalization in the conv layers and dropouts in the linear layers to control over fitting. Also I have added weigh decay to apply regularization.

The model is traind unsing Callback methos-
* Learning Rate scheduling
* Model Checkpointing
* Early Stopping
