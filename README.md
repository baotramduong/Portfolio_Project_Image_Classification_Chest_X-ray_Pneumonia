# Deep Learning Image Classification: Pneumonia 

Build a model that can classify whether a given patient has pneumonia, given a chest x-ray image.

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

163/163 [==============================] - 0s 2ms/step - loss: 0.0606 - acc: 0.9776

**Train loss & accuracy of the model: [0.060579925775527954, 0.977569043636322]**

20/20 [==============================] - 0s 1ms/step - loss: 1.1344 - acc: 0.7372

**Test loss & accuracy of the model is: [1.134368658065796, 0.7371794581413269]**

### Convolution Neural Network Model

<img src = '../main/Data & Figures/cnn_model_acc_loss.png' />
163/163 [==============================] - 94s 576ms/step - loss: 0.2301 - acc: 0.9080

**Train loss & accuracy of the model: [0.2301289588212967, 0.907975435256958]**

20/20 [==============================] - 8s 406ms/step - loss: 0.2944 - acc: 0.8702

**Test loss & accuracy of the model is: [0.29440099000930786, 0.870192289352417]**

### Transfer Learning with VGG16

<img src = '../main/Data & Figures/VGG16_cnn_model_acc_loss.png' />

163/163 [==============================] - 629s 4s/step - loss: 0.1416 - acc: 0.9503

**Train loss & accuracy of the model: [0.14156349003314972, 0.9503450989723206]**

20/20 [==============================] - 73s 4s/step - loss: 0.2886 - acc: 0.9006

**Test loss & accuracy of the model is: [0.28859254717826843, 0.9006410241127014]**

##  Summary of Key Findings

##  Summary of Actionable Insights

##  Future Works
