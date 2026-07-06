# Brain-tumor-detection-system
Deep Learning Project using VGG16 and CNN for Brain Tumor Detection
# Brain Tumor Detection System Using VGG16 Deep Learning Model

## 1. Overview

The Brain Tumor Detection System is a deep learning-based application developed to automatically identify different types of brain tumors from MRI scan images. Early detection of brain tumors is important for effective treatment and improved patient outcomes. Manual analysis of MRI scans by radiologists can be time-consuming and may be affected by human error. Therefore, this project uses a Convolutional Neural Network (CNN) with the VGG16 architecture to classify MRI images into different tumor categories.

The system performs image preprocessing, data augmentation, feature extraction, model training, and classification. The trained model can accurately predict the presence and type of brain tumor from MRI images.

---

## 2. System Architecture

The proposed system follows the following architecture:

1. **MRI Image Dataset Collection**

   * Brain MRI images are collected and organized into training and testing folders.

2. **Data Preprocessing**

   * Images are resized to 128 × 128 pixels.
   * Pixel values are normalized.
   * Image augmentation techniques are applied.

3. **Feature Extraction**

   * Pre-trained VGG16 model is used to extract important image features.

4. **Classification Layer**

   * Fully connected layers, batch normalization, and dropout layers are added.
   * Softmax activation is used for multi-class classification.

5. **Model Training**

   * The model is trained using the augmented dataset.
   * Early stopping is applied to prevent overfitting.

6. **Prediction and Evaluation**

   * The trained model predicts tumor classes.
   * Performance is evaluated using accuracy, confusion matrix, classification report, and ROC curves.

### Architecture Flow

MRI Images → Preprocessing → Data Augmentation → VGG16 Feature Extraction → Dense Layers → Softmax Classification → Tumor Prediction

---

## 3. Dataset Features

The dataset consists of brain MRI images categorized into multiple classes. Important features of the dataset include:

* Medical MRI brain scan images.
* Multi-class classification dataset.
* Images stored in separate folders according to tumor type.
* RGB image format.
* Resized to 128 × 128 pixels during preprocessing.
* Suitable for deep learning image classification tasks.

### Image Processing Features

* Rotation augmentation
* Width shifting
* Height shifting
* Zoom augmentation
* Shearing transformation
* Horizontal flipping
* Pixel normalization

These techniques increase dataset diversity and improve model generalization.

---

## 4. Dataset Used

The project uses a Brain MRI Image Dataset containing four classes:

| Class      | Description                         |
| ---------- | ----------------------------------- |
| Glioma     | Tumor originating from glial cells  |
| Meningioma | Tumor developing in the meninges    |
| Pituitary  | Tumor affecting the pituitary gland |
| No Tumor   | Healthy brain MRI images            |

### Dataset Structure

Training/

* Glioma
* Meningioma
* Pituitary
* No Tumor

Testing/

* Glioma
* Meningioma
* Pituitary
* No Tumor

The dataset is stored in Google Drive and loaded into the model using TensorFlow image generators.

---

## 5. Methodology Used

### Step 1: Data Loading

MRI images are loaded from training and testing directories. The images and labels are shuffled to ensure unbiased learning.

### Step 2: Data Visualization

Random MRI images are displayed to understand the dataset distribution and verify image quality.

### Step 3: Image Preprocessing

The images undergo preprocessing operations such as:

* Resizing to 128 × 128 pixels
* Normalization
* Conversion into suitable numerical format

### Step 4: Data Augmentation

To improve model robustness, augmentation techniques are applied:

* Rotation
* Zoom
* Shear transformation
* Horizontal flip
* Width and height shifts

# Step 5: Model Development

A transfer learning approach is used with the pre-trained VGG16 model.

Additional layers include:

* Flatten Layer
* Dense Layers
* Batch Normalization
* Dropout Layers
* Softmax Output Layer

 # Step 6: Model Training

The model is trained using:

* Adam Optimizer
* Sparse Categorical Cross-Entropy Loss
* Batch Size = 20
* Validation Split = 20%
* Early Stopping Technique

 # Step 7: Performance Evaluation

The trained model is evaluated using:

* Accuracy Graph
* Loss Graph
* Classification Report
* Confusion Matrix
* ROC Curve
* AUC Score

---

 # 6. Output

The system successfully classifies MRI images into one of the four categories:

* Glioma Tumor
* Meningioma Tumor
* Pituitary Tumor
* No Tumor

 Generated Outputs

1. Training Accuracy and Validation Accuracy Graphs.
2. Training Loss and Validation Loss Graphs.
3. Classification Report showing:

   * Precision
   * Recall
   * F1-Score
4. Confusion Matrix for prediction analysis.
5. ROC Curves and AUC values for each tumor class.
6. Final predicted tumor class for a given MRI image.

The results demonstrate that the VGG16-based deep learning model is effective for brain tumor detection and classification, providing reliable performance for medical image analysis applications.
