# X-ray Pneumonia Image Classification with Deep Learning 

* Globally, a child dies of pneumonia every 39 seconds.
* Pneumonia kills more children than any other infectious disease, claiming the lives of over 800,000 children under five every year, or around 2,200 every day. This includes over 153,000 newborns.
* Pneumonia is a leading cause of morbidity and mortality in children younger than the age of 5 years.

Chest X-rays are primarily used for the diagnosis of this disease. However, even for a trained radiologist, it is a challenging task to examine chest X-rays. For this project, we will build a model that can classify whether a given patient has pneumonia, given a chest x-ray image.

## The Deliverables

There are 5 deliverables for this project:

1. A well documented Jupyter Notebook containing any code and comments explaining it.

            - Image Classification with Deep Learning
           
2. An organized README.md file that describes the contents of the repository.

             - README.md: describes the content and organization of content.
             - Data & Figures folder: contains all provided data and all figures for visualization.
             - Jupyter notebook
             
             * validation_date = test_generator:
             https://www.kaggle.com/baotramduong/x-ray-pneumonia-classification-test
             
             * validation_data = val_generator:
             https://www.kaggle.com/baotramduong/x-ray-pneumonia-image-classification-val
             
             - Presentation pdf

3. A short PowerPoint presentation (delivered as a PDF export) giving a high-level overview of the methodology used and recommendations for non-technical stakeholders. Can be found in the repository or at: 

4. A Blog Post which can be found at: 

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

**Train loss & accuracy of the model: [0.07288116216659546, 0.974693238735199]**

**Test loss & accuracy of the model is: [0.9555945992469788, 0.7532051205635071]**

<img src = '../main/Data & Figures/mlp_model_cm.png' width='50%' height='50%'>

<img src = '../main/Data & Figures/mlp_model_roc.png' width='75%' height='75%'>

### Convolutional Neural Network Model

<img src = '../main/Data & Figures/cnn_model_acc_loss.png' />

**Train loss & accuracy of the model: [0.25476858019828796, 0.8861196041107178]**

**Test loss & accuracy of the model is: [0.3085976541042328, 0.875]**

<img src = '../main/Data & Figures/cnn_model_cm.png' width='50%' height='50%'>

<img src = '../main/Data & Figures/cnn_model_roc.png'  width='75%' height='75%'>

### Transfer Learning with VGG16

<img src = '../main/Data & Figures/VGG16_cnn_model_acc_loss.png' />

**Train loss & accuracy of the model: [0.14143085479736328, 0.9453604221343994]**

**Test loss & accuracy of the model is: [0.23637154698371887, 0.9102563858032227]**

<img src = '../main/Data & Figures/VGG16_cnn_model_cm.png' width='50%' height='50%'>

<img src = '../main/Data & Figures/VGG16_cnn_model_roc.png'  width='75%' height='75%'>

##  Summary of Key Findings

|      |Model                             |Evaluate acc|Predict acc|Precision|Recall|F1 Score|AUC |
|------|----------------------------------|------------|-----------|---------|------|--------|----|
|0     |Multilayer Perceptron Model       |0.82        |0.82       |0.85     |0.78  |0.79    |0.77|
|1     |Convolutional Neural Network Model|0.88        |0.55       |0.52     |0.52  |0.52    |0.52|
|2     |Transfer Learning: VGG16 CNN Model|0.91        |0.52       |0.48     |0.48  |0.48    |0.48|


##  Summary of Actionable Insights

##  Future Works
