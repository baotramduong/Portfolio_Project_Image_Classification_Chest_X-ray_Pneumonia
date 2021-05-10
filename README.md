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

Original notebook on Kaggle: https://www.kaggle.com/baotramduong/deep-learning-mlp-cnn-transfer-learning-92-acc
           
2. An organized README.md file that describes the contents of the repository.

3. A short PowerPoint presentation (delivered as a PDF export) giving a high-level overview of the methodology used and recommendations for non-technical stakeholders. 

https://github.com/baotramduong/Portfolio_Project_Deep_Learning_Image_Classification/blob/main/Presentation.pdf

4. A Blog Post which can be found at: 

https://baotramduong.medium.com/x-ray-pneumonia-classification-with-deep-learning-6a81861150a1

5. A Video Walkthrough of my non-technical presentation, can be found at:

https://youtu.be/yGBB_ZeWuds

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

<img src = '../main/Data & Figures/mlp_model_plot.png' width='50%' height='50%'>

<img src = '../main/Data & Figures/mlp_model_acc_loss.png' />

**Train loss & accuracy: [0.08716818690299988, 0.9675996899604797]**

**Test loss & accuracy: [0.7084700465202332, 0.7948718070983887]**

<img src = '../main/Data & Figures/mlp_model_cm.png' width='50%' height='50%'>

<img src = '../main/Data & Figures/mlp_model_roc.png' width='75%' height='75%'>

### Convolutional Neural Network Model

<img src = '../main/Data & Figures/cnn_model_plot.png' width='50%' height='50%'>

<img src = '../main/Data & Figures/cnn_model_acc_loss.png' />

**Train loss & accuracy: [0.18603405356407166, 0.9273389577865601]**

**Test loss & accuracy: [0.3564613461494446, 0.8766025900840759]**

<img src = '../main/Data & Figures/cnn_model_cm.png' width='50%' height='50%'>

<img src = '../main/Data & Figures/cnn_model_roc.png'  width='75%' height='75%'>

### Transfer Learning with VGG16

<img src = '../main/Data & Figures/pretrainedCNN_model_plot.png' width='50%' height='50%'>

<img src = '../main/Data & Figures/VGG16_cnn_model_acc_loss.png' />

**Train loss & accuracy: [0.13685134053230286, 0.9465107321739197]**

**Test loss & accuracy: [00.23303863406181335, 0.9150640964508057]**

<img src = '../main/Data & Figures/VGG16_cnn_model_cm.png' width='50%' height='50%'>

<img src = '../main/Data & Figures/VGG16_cnn_model_roc.png'  width='75%' height='75%'>

##  Summary of Key Findings

|      |Model                             |Accuracy|Precision|Recall|F1 Score|AUC |
|------|----------------------------------|--------|---------|------|--------|----|
|0     |Multilayer Perceptron Model       |0.79    |0.84     |0.74  |0.75    |0.74|
|1     |Convolutional Neural Network Model|0.88    |0.89     |0.85  |0.86    |0.85|
|2     |Transfer Learning: VGG16 CNN Model|0.92    |0.91     |0.90  |0.91    |0.90|


##  Summary of Actionable Insights

Pneumonia are largely preventable in this age group and failure in long-term management or preventing it will result in increases of the risk of developing chronic pulmonary disorders in later adult life. Chang et al. (2013) suggests:

1. Focus on solving problems that are associated with increasing the risk of pneumonia such as overcrowding, access to clean water, malnutrition, anemia, young maternal age, low birth weight, and exposure to tobacco smoke and other environmental pollutants
2. Invest in resources to collect data systematically, especially in poor countries
3. Develop a universally agreed diagnostic gold standard for childhood pneumonia, especially one that can also differentiate between bacterial and non-bacterial pneumonia, which is currently a major limitation in clinical research in this area

##  Future Works

1. Build a multi-class classification deep learning model to distinguish between Normal, Viral Pneumonia, and Bacterial Pneumonia
2. Combine CNN models with other classifiers such as Support Vector Machine (SVM)
3. Tune parameters such as learning rate, batch size, try another optimizer, number of layers, different types of layer, number of neurons per layer, and the type of activation functions for each layer. GridSearchCV or RandomizedSearchSV can be used to achieve this.

## Reference

Chang, A. B., Ooi, M. H., Perera, D., & Grimwood, K. (2013). Improving the Diagnosis, Management, and Outcomes of Children with Pneumonia: Where are the Gaps?. Frontiers in pediatrics, 1, 29. https://doi.org/10.3389/fped.2013.00029

Geron, A. (2019). Hands-on machine learning with Scikit-Learn, Keras and TensorFlow: concepts, tools, and techniques to build intelligent systems (2nd ed.). O’Reilly.

Kermany, D. S., Goldbaum, M., Cai, W., Valentim, C., Liang, H., Baxter, S. L., McKeown, A., Yang, G., Wu, X., Yan, F., Dong, J., Prasadha, M. K., Pei, J., Ting, M., Zhu, J., Li, C., Hewett, S., Dong, J., Ziyar, I., Shi, A., … Zhang, K. (2018). Identifying Medical Diagnoses and Treatable Diseases by Image-Based Deep Learning. Cell, 172(5), 1122–1131.e9. https://doi.org/10.1016/j.cell.2018.02.010

Unicef. (2021, April 07). Pneumonia in children statistics. Retrieved April 13, 2021, from https://data.unicef.org/topic/child-health/pneumonia/#:~:text=A%20child%20dies%20of%20pneumonia,of%20these%20deaths%20are%20preventable.
