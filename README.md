# ISIC Skin Lesion Classification Report

## 1. Introduction

Skin cancer is one of the most common types of cancer, and early detection plays a crucial role in increasing survival rates. This project focuses on classifying different types of skin lesions using deep learning models. Leveraging the **ISIC dataset**, which contains labeled images of skin lesions, the project applies various deep learning architectures to perform image classification.

### Project Objectives:

- Develop models to classify skin lesions into categories such as melanoma, benign keratosis-like lesions, and more.
- Compare different architectures to find the best-performing model.
- Provide a detailed analysis of each model’s performance.

---

## 2. Dataset

### ISIC Dataset Overview:

The dataset used in this project is the **ISIC Skin Lesion Dataset**, widely used in medical image analysis competitions. It contains thousands of labeled images of skin lesions, classified into various categories:

- **Melanoma**: The most dangerous form of skin cancer.
- **Benign Keratosis-like Lesions**: Non-cancerous lesions.
- **Basal Cell Carcinoma (BCC)**: A common form of skin cancer, but less dangerous than melanoma.
- **Actinic Keratoses (AKIEC)**: Pre-cancerous skin lesions.
- **Dermatofibroma (DF)**: Benign skin tumors.
- **Vascular Lesions (VASC)**: Blood vessel tumors or abnormalities.

### Dataset Statistics:

- **Number of Images**: 25,331
- **Image Size**: 224x224 pixels (resized for input into the models).
- **Classes**: 7 skin lesion classes.

---

## 3. Data Preprocessing

### Preprocessing Steps:

1. **Resizing Images**: All images were resized to 224x224 to suit the input size required by most deep learning models.
2. **Normalization**: Pixel values were normalized to the range [0, 1] to speed up convergence during training.
3. **Data Augmentation**: Image augmentation techniques, such as rotation, zoom, and horizontal flips, were applied to the training set to increase variability and avoid overfitting.
4. **Splitting**: The dataset was split into:
   - **Training Set**: 70% of the data
   - **Validation Set**: 15% of the data
   - **Test Set**: 15% of the data


## 6. Results and Analysis

### Model Performance Summary

| Model             | Accuracy | Precision | Recall  | F1-Score |
|-------------------|----------|-----------|---------|----------|
| EfficientNetB2 | 0.7886     | 0.7868      | 0.7886    | 0.7862     |
| EfficientNetV2B0 | 0.8396     | 0.84      | 0.84    | 0.7862     
| VGG16 (Fine-tuned)  | 0.6517   | -      | -    | -     |
| VGG19 (Fine-tuned)  | 0.6296   | -      | -    | -    |
| ResNet50 (Fine-tuned)| 0.5083  | -      | -    | -    |




## 10. Let's Connect

- **GitHub** - [3m0r9](https://github.com/3m0r9)
- **LinkedIn** - [Imran Abu Libda](https://www.linkedin.com/in/imran-abu-libda/)
- **Email** - [imranabulibda@gmail.com](mailto:imranabulibda@gmail.com)
- **Medium** - [Imran Abu Libda](https://medium.com/@imranabulibda_23845)
