# Clinical Decision Support System for Breast Cancer Diagnosis Using Ultrasound Imaging

## About the Project

Breast cancer is a major health concern, and early detection plays an important role in its diagnosis and treatment.

As part of this project, we developed a **Clinical Decision Support System (CDSS)** using deep learning to analyse breast ultrasound images and classify them into three categories: Normal, Benign, and Malignant.

The main aim of this project is not just to predict the class of an ultrasound image, but also to understand why the model makes a particular prediction and how confident it is about the result.

To achieve this, we combined ResNet-18, Grad-CAM, Test-Time Augmentation (TTA), and BI-RADS-based clinical interpretation into a single framework.

## Project Highlights

- Classifies breast ultrasound images into Normal, Benign, and Malignant categories.
- Uses ResNet-18 with transfer learning for image classification.
- Applies Grad-CAM to generate heatmaps and highlight image regions that influence predictions.
- Uses Test-Time Augmentation (TTA) to estimate prediction uncertainty.
- Maps classification results to BI-RADS categories.
- Provides clinical recommendations to support the interpretation of predictions.

## Dataset

We used the **BUSI (Breast Ultrasound Images) Dataset**, containing 780 ultrasound images across three classes:

- Normal
- Benign
- Malignant

The dataset is used for training and evaluating the deep learning model.

## Model Performance

The proposed ResNet-18 model achieved a **best validation accuracy of 93.16%**.

Model performance was studied using accuracy, precision, recall, F1-score, and a confusion matrix.

## Technologies Used

- Python
- Google Colab
- PyTorch
- OpenCV
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- KaggleHub

## How the System Works

1. An ultrasound image is given as input.
2. Image preprocessing and augmentation are performed.
3. The ResNet-18 model analyses the image and predicts its class.
4. Grad-CAM generates a heatmap to explain the prediction.
5. Test-Time Augmentation performs 20 prediction iterations to examine prediction consistency.
6. The predicted class is mapped to a BI-RADS category.
7. The system generates the final output with the prediction, confidence, visualization, uncertainty information, and clinical recommendation.

## How to Run

This project was developed using Google Colab.

1. Clone or download this repository.
2. Open the `.ipynb` notebook in Google Colab.
3. Run the notebook cells in sequence.
4. Install the required libraries when prompted.
5. Download the BUSI dataset through KaggleHub.
6. Execute the training and evaluation sections.
7. Explore the classification results and Grad-CAM visualizations.

## What I Learned

Working on this project helped me understand how deep learning can be applied to medical image analysis. It also gave me practical experience with transfer learning, image preprocessing, model evaluation, explainable AI, and uncertainty estimation.

One of the most interesting parts was implementing Grad-CAM because it helped us look beyond the final prediction and understand which regions of an ultrasound image influenced the model.

## Future Scope

There is still room to improve this system. Some possible improvements include:

- Training with larger and more diverse ultrasound datasets.
- Exploring more advanced deep learning architectures.
- Improving prediction speed for real-time use.
- Enhancing BI-RADS assessment and clinical recommendations.
- Developing a web or mobile interface for easier access.

## Disclaimer

This project is developed for academic and research purposes. It is intended as a decision-support research prototype and should not be used as a replacement for professional medical advice, radiologist interpretation, or clinical diagnosis.
