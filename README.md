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

### CNN
The CNN model that is employed for the task has 3 cov layers with maxpooling layes and 2 dense layers. I have added batch normalization in the conv layers and dropouts in the linear layers to control over fitting. Also I have added weigh decay to apply regularization.

The model is traind unsing Callback methos-
* Learning Rate scheduling
* Model Checkpointing
* Early Stopping

I have tested the model on both nomal training data and augmented training data. While there was some overfitting while training with normal training data, while using augmented training data for training the overfitting was gone. The model is giving arounf 87% Accuracy.

### Transfer Learning
The pretrained model that is used is ResNet50. I have changed the final layer of the model with 2 dense layers. Same as the CNN model, I have added batch normalization in the conv layers and dropouts in the linear layers to control over fitting. Also I have added weigh decay to apply regularization.

The model is traind unsing Callback methos-
* Learning Rate scheduling
* Model Checkpointing
* Early Stopping

This time I only trained the model on the normal training data and with some overfitting the model achived aroud 95% accuracy.
