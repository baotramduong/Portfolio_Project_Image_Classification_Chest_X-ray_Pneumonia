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
             - Part I: Jupyter notebook
             - Part II: Jupyter notebook
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

**Train loss & accuracy of the model: [0.060579925775527954, 0.977569043636322]**

**Test loss & accuracy of the model is: [1.134368658065796, 0.7371794581413269]**

### Convolution Neural Network Model

<img src = '../main/Data & Figures/cnn_model_acc_loss.png' />

**Train loss & accuracy of the model: [0.2301289588212967, 0.907975435256958]**

**Test loss & accuracy of the model is: [0.29440099000930786, 0.870192289352417]**

### Transfer Learning with VGG16

<img src = '../main/Data & Figures/VGG16_cnn_model_acc_loss.png' />

**Train loss & accuracy of the model: [0.14156349003314972, 0.9503450989723206]**

**Test loss & accuracy of the model is: [0.28859254717826843, 0.9006410241127014]**

##  Summary of Key Findings

|      |Model                             |Evaluate acc|Predict acc|Precision|Recall|F1 Score|AUC |
|------|----------------------------------|------------|-----------|---------|------|--------|----|
|0     |Multilayer Perceptron Model       |0.75        |0.75       |0.84     |0.67  |0.68    |0.67|
|1     |Convolutional Neural Network Model|0.88        |0.55       |0.52     |0.52  |0.52    |0.52|
|2     |Transfer Learning: VGG16 CNN Model|0.88        |0.52       |0.48     |0.48  |0.48    |0.48|


##  Summary of Actionable Insights

##  Future Works

1. Correct class imbalance with oversampling technique
2. 
