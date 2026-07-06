# Brain Tumor Detection Using Deep Learning

## Overview

Brain tumors are one of the most serious health conditions that can affect the human brain. Detecting them at an early stage is very important because it helps doctors provide the right treatment and improves the chances of recovery. Traditionally, radiologists examine MRI scans manually to identify tumors, but this process can take time and may sometimes lead to errors.

In this project, a deep learning-based system is developed to automatically detect and classify brain tumors from MRI images. The model uses the VGG16 architecture, a well-known Convolutional Neural Network (CNN), to learn important patterns from MRI scans and classify them into different tumor categories. By automating the detection process, the system can support medical professionals in making faster and more accurate diagnoses.



## System Architecture

The proposed system follows a sequence of steps to perform brain tumor classification.

First, MRI images are collected and organized into training and testing datasets. These images are then preprocessed by resizing them to a standard size and normalizing the pixel values. To improve the model's learning capability, various image augmentation techniques are applied.

After preprocessing, the images are passed through the VGG16 model, which extracts important features from the MRI scans. These extracted features are then processed by additional dense layers that perform the final classification. The output layer predicts the type of tumor present in the MRI image.

The overall workflow of the system can be summarized as:

MRI Images → Image Preprocessing → Data Augmentation → VGG16 Feature Extraction → Classification Layers → Tumor Prediction



## Dataset Features

The dataset used in this project consists of brain MRI images belonging to different tumor categories. Each image contains valuable visual information that helps the model learn the characteristics of various brain conditions.

Some important features of the dataset include:

* MRI images of human brains.
* Images categorized into multiple classes.
* High-quality medical imaging data.
* RGB image format.
* Images resized to 128 × 128 pixels before training.
* Suitable for deep learning-based image classification.

To improve model performance and reduce overfitting, several augmentation techniques are applied, such as image rotation, zooming, shearing, shifting, and horizontal flipping. These techniques help create more variations in the dataset and allow the model to generalize better.



## Dataset Used

The project uses a Brain MRI dataset that contains four classes:

1. Glioma Tumor
2. Meningioma Tumor
3. Pituitary Tumor
4. No Tumor

The dataset is divided into training and testing folders. Each folder contains separate subfolders for the four classes. This organized structure makes it easier to train and evaluate the deep learning model.

The dataset provides a balanced collection of MRI images that enables the model to learn the visual differences between healthy brains and different tumor types.



## Methodology Used

The implementation of the project consists of several stages.

### Data Collection and Loading

The MRI images are collected and loaded into the system from the dataset folders. The images are shuffled to ensure that the model learns effectively without any bias.

### Data Visualization

Before training, sample images are displayed to understand the dataset and verify that the images are correctly labeled.

### Image Preprocessing

The MRI images are resized to a fixed dimension of 128 × 128 pixels. Pixel values are normalized so that the model can process the images efficiently.

### Data Augmentation

To improve the diversity of the training data, augmentation techniques such as rotation, zooming, shearing, width shifting, height shifting, and horizontal flipping are applied.

### Model Development

The VGG16 pre-trained model is used as the base network for feature extraction. Additional layers such as Dense layers, Batch Normalization layers, and Dropout layers are added to improve classification performance and reduce overfitting.

### Model Training

The model is trained using the Adam optimizer and Sparse Categorical Cross-Entropy loss function. Early stopping is implemented to prevent unnecessary training once the model stops improving.

### Performance Evaluation

After training, the model's performance is evaluated using different metrics, including accuracy, loss, precision, recall, F1-score, confusion matrix, and ROC curves.



## Output

The developed system successfully predicts the category of a given brain MRI image. The model can classify images into one of the following classes:

* Glioma Tumor
* Meningioma Tumor
* Pituitary Tumor
* No Tumor

The output of the project includes training and validation accuracy graphs, loss curves, classification reports, confusion matrices, and ROC-AUC analysis. These results help measure the effectiveness of the model and demonstrate its ability to accurately classify brain tumors from MRI scans.

Overall, the project shows how deep learning techniques can be used in the healthcare field to assist in the early detection and classification of brain tumors, making the diagnosis process faster and more reliable.
