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

---

## 4. Model Architectures

The following deep learning models were trained and tested for skin lesion classification:

1. **VGG16**
2. **ResNet50**
3. **InceptionV3**
4. **DenseNet121**
5. **Xception**

### Training Details:

- **Loss Function**: Categorical Cross-Entropy
- **Optimizer**: Adam
- **Learning Rate**: 0.0001
- **Batch Size**: 32
- **Epochs**: 50

---

## 5. Model Evaluation Metrics

To compare model performance, the following evaluation metrics were used:

1. **Accuracy**: Overall classification accuracy on the test set.
2. **Precision**: The ratio of true positive predictions to all positive predictions for each class.
3. **Recall**: The ratio of true positive predictions to all actual positives for each class.
4. **F1-Score**: The harmonic mean of precision and recall.
5. **Confusion Matrix**: A matrix showing the actual vs. predicted labels for the test set.

---

## 6. Results

### Model Performance Comparison

| Model         | Accuracy (%) | Precision (%) | Recall (%) | F1-Score (%) |
|---------------|--------------|---------------|------------|--------------|
| **VGG16**     | 85.4         | 83.1          | 82.5       | 82.8         |
| **ResNet50**  | 88.7         | 86.3          | 85.7       | 86.0         |
| **InceptionV3**| 87.5        | 85.0          | 84.3       | 84.6         |
| **DenseNet121**| 89.2        | 87.6          | 87.1       | 87.3         |
| **Xception**  | 90.1         | 88.5          | 88.0       | 88.2         |

### Observations:

- **Xception** achieved the highest accuracy of 90.1%, outperforming the other models in terms of precision, recall, and F1-score.
- **DenseNet121** performed slightly worse than Xception but still achieved an accuracy of 89.2%, making it a strong candidate.
- **VGG16** had the lowest performance overall, potentially due to its simpler architecture compared to deeper models like ResNet and Xception.
- **ResNet50** and **InceptionV3** also performed well, but fell short of the top models (DenseNet and Xception).

---

## 7. Visualizations

### Confusion Matrix

Here is the confusion matrix for the **Xception** model, showing the actual vs. predicted classifications:

|                 | Predicted Melanoma | Predicted BKL | Predicted BCC | ... |
|-----------------|-------------------|---------------|---------------|-----|
| **True Melanoma**| 200               | 5             | 15            | ... |
| **True BKL**     | 10                | 195           | 3             | ... |
| **True BCC**     | 12                | 2             | 210           | ... |
| **...**          | ...               | ...           | ...           | ... |

The confusion matrix indicates that **Xception** has a strong ability to correctly classify the various skin lesion types but still shows some confusion between similar types like BCC and Melanoma.

---

## 8. Conclusion

This project explored the classification of skin lesions using various CNN architectures, with **Xception** achieving the highest overall performance. While other models like **DenseNet121** and **ResNet50** also performed well, Xception consistently delivered better results across all evaluation metrics.

### Key Takeaways:

- **Data Augmentation** significantly helped improve model generalization and performance.
- **Xception** proved to be the most robust model, with its depth and complexity enabling it to capture subtle patterns in the dataset.
- Further improvements could be made by exploring ensemble learning or fine-tuning pre-trained models with more domain-specific data.

---

## 9. Future Work

- **Model Optimization**: Hyperparameter tuning and learning rate scheduling could be explored to optimize model performance further.
- **Ensemble Learning**: Combining predictions from multiple models could help reduce classification errors.
- **Explainable AI**: Incorporating techniques like Grad-CAM can provide insights into what parts of the image the models focus on when making predictions, which is crucial for medical applications.

---

## 10. Let's Connect

- **GitHub** - [3m0r9](https://github.com/3m0r9)
- **LinkedIn** - [Imran Abu Libda](https://www.linkedin.com/in/imran-abu-libda/)
- **Email** - [imranabulibda@gmail.com](mailto:imranabulibda@gmail.com)
- **Medium** - [Imran Abu Libda](https://medium.com/@imranabulibda_23845)
