# X-ray Pneumonia Image Classification with Deep Learning 

According to Unicef (2021):
* Globally, a child dies of pneumonia every 39 seconds.
* Pneumonia claims the lives of over 800,000 children under five every year, or around 2,200 every day. This includes over 153,000 newborns.
* Pneumonia is a leading cause of morbidity and mortality in children younger than the age of 5 years, killing more children than HIV/AIDS, malaria, and measles combined.

Chest X-rays are primarily used for the diagnosis of this disease. However, even for a trained radiologist, it is a challenging task to examine chest X-rays.
To solve this, deep learning (DL), a branch of machine learning (ML), inspired by the make-up of the human brain, are developed to detect hidden features in images which are not apparent or cannot be detected even by medical experts. With AI system aiding medical experts in expediting the diagnosis, earlier treatment can be prescribed, resulting in improved clinical outcomes.

## The Deliverables

There are 5 deliverables for this project:

1. A well documented Jupyter Notebook containing any code and comments explaining it.

Original notebook on Kaggle: https://www.kaggle.com/baotramduong/x-ray-pneumonia-classification-test
           
2. An organized README.md file that describes the contents of the repository.

             - Data & Figures folder: contains all provided data and all figures for visualization.
             - Jupyter notebook
             - Presentation pdf

3. A short PowerPoint presentation (delivered as a PDF export) giving a high-level overview of the methodology used and recommendations for non-technical stakeholders. Can be found in the repository or at: 

4. A Blog Post which can be found at: 

https://baotramduong.medium.com/x-ray-pneumonia-classification-with-deep-learning-6a81861150a1

5. A Video Walkthrough of my non-technical presentation, can be found at:

# **Notebook Table of Contents**

## PART I: EDA

<img src = '../main/Data & Figures/X-ray.png' />

<img src = '../main/Data & Figures/X-ray Condition.png' />

### Data Source

             - https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia
             - The dataset is organized into 3 folders (train, test, val) and contains subfolders for each image category (Pneumonia/Normal). 
             - There are 5,863 X-Ray images (JPEG) and 2 categories (Pneumonia/Normal).

Chest X-ray images (anterior-posterior) were selected from retrospective cohorts of pediatric patients of one to five years old from Guangzhou Women and Children’s Medical Center, Guangzhou. All chest X-ray imaging was performed as part of patients’ routine clinical care.

## PART II: Modeling

### Multilayer Perceptron Model
<img src = '../main/Data & Figures/mlp_model_acc_loss.png' />

**Train loss & accuracy: [0.07, 0.98]**

**Test loss & accuracy: [1.13, 0.74]**

<img src = '../main/Data & Figures/mlp_model_cm.png' width='50%' height='50%'>

<img src = '../main/Data & Figures/mlp_model_roc.png' width='75%' height='75%'>

### Convolutional Neural Network Model

<img src = '../main/Data & Figures/cnn_model_acc_loss.png' />

**Train loss & accuracy: [0.19, 0.92]**

**Test loss & accuracy: [0.32, 0.88]**

<img src = '../main/Data & Figures/cnn_model_cm.png' width='50%' height='50%'>

<img src = '../main/Data & Figures/cnn_model_roc.png'  width='75%' height='75%'>

### Transfer Learning with VGG16

<img src = '../main/Data & Figures/VGG16_cnn_model_acc_loss.png' />

**Train loss & accuracy: [0.12, 0.95]**

**Test loss & accuracy: [0.24, 0.92]**

<img src = '../main/Data & Figures/VGG16_cnn_model_cm.png' width='50%' height='50%'>

<img src = '../main/Data & Figures/VGG16_cnn_model_roc.png'  width='75%' height='75%'>

##  Summary of Key Findings

|      |Model                             |Accuracy|Precision|Recall|F1 Score|AUC |
|------|----------------------------------|--------|---------|------|--------|----|
|0     |Multilayer Perceptron Model       |0.74    |0.83     |0.66  |0.66    |0.66|
|1     |Convolutional Neural Network Model|0.88    |0.89     |0.86  |0.87    |0.86|
|2     |Transfer Learning: VGG16 CNN Model|0.92    |0.92     |0.90  |0.91    |0.90|


##  Summary of Actionable Insights

##  Future Works
1. Build a multi-class classification deep learning model to distinguish between Normal, Viral Pneumonia, and Bacterial Pneumonia
2. Combine CNN models with other classifiers such as Support Vector Machine (SVM)
3. Tune parameters such as learning rate, batch size, try another optimizer, number of layers, different types of layer, number of neurons per layer, and the type of activation functions for each layer. GridSearchCV or RandomizedSearchSV can be used to achieve this.
