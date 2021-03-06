
# Image- Classification (Pneumonia-X-rays)
Phase 04 project Image Classification with Deep Learning 
# Detecting Pneumonia in Chest X-Rays
![xray](https://github.com/reynoso811/Image-Classification-Pneumonia-X-rays-/blob/main/Screen%20Shot%202021-12-02%20at%2010.51.08%20AM.png)

**Author**: Robert Reynoso


December 03, 2021

## Business Problem

Using Neural Networks, to what degree of accuracy can we detect Pneumonia in chest X-rays?
Using these models and learnings to later be implemented in future image classification problems.

## Data

* Guangzhou Women and Children’s Medical Center
    - There are 5,863 X-Ray images (JPEG) and 2 categories (Pneumonia/Normal)
    - Selected from retrospective cohorts of pediatric patients of one to five years old 
    - All chest X-ray imaging was performed as part of patients’ routine clinical care.
* Provided by Kaggle
    - https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia 


## EDA (Exploratory Data Analysis)
![EDA](https://github.com/reynoso811/Image-Classification-Pneumonia-X-rays-/blob/main/Screen%20Shot%202021-12-02%20at%2010.47.49%20AM.png)
* Data Exploration using Pandas Profling

* Distribution of Images
    - Train Images
        - A total of 5216 Images
    - Test Images
        - A total of 624 Images
    
* Both Data Sets are Imbalanced
    - Favoring Pneumonia in both cases 
    
* Normal X-Rays are labeled 0

* Pneumonia X-Rays are labeled 1
    - Regardless of the type of pneumonia


## Models
![Test](https://github.com/reynoso811/Image-Classification-Pneumonia-X-rays-/blob/main/Screenshot%20from%202021-12-06%2020-53-58.png)

* 5 part iterative modeling process with results: 


* Baseline MLP (Multi Layer Perceptron) Model:
    - The best accuracy the MLP model could achieve was about 75%.
    
        - The instability in the model can be seen in the loss and accuracy curves. We can see the instability in the variance 
          of the curves on both graphs ranging from 5.00 to 25.00 %, at certain points without subsiding. This can be seen 
          with the divergence of both curves beyond 20 Epochs. The training data almost reachs perfection, while the testing 
          data fails to improve.
          
        - The model is overfitting, quite a bit. We can see around Epoch 20 on the Binary Accuracy graph that the model 
          doesn't not improve.
          
        - This model could be improved/tuned by using differnet activation functions, trying different optimizers, 
          including early stopping and different degrees of dropouts.
        
        
* Baseline CNN Model Model:
    - The best accuracy the MLP model could achieve was about 74%

        - Simple sequential model was used, starting with 5 double convolutional networks of kernel size (3, 3) and max pooling with pool size (2, 2).            Additionally has batch normalization and dropout
        
           
* Pre-trained Model (VGG16):
    - The best accuracy from the Transfer Learning CNN Model was about 94%:

        - This model was saved and used to make predictions on our validation data
        - This was done due to the high accuracy of this model


* Talos Tuned CNN Model:
    - The model is still running....
        - I will update this part upon completion...
        

##  Conclusion and Recommendation

* Pre-trained Model was the best model
    - Transfer learning generally refers to a process where a model trained on one problem is used in some way on a second 
      related problem.
        - VGG-16 is a dataset of over 14 million images belonging to 1000 classes
    - One or more layers from the trained model are then used in a new model trained on the pneumonia images.
 


## Next Steps: 

* Try different activation functions 


* Re-run tuned CNN


* Try to use Grad-CAM class activation visualization



***

## For More Information

Please review my full technical analysis in [Notebook](https://github.com/reynoso811/Image-Classification-Pneumonia-X-rays-/blob/main/Phase_04_MLP_CNN_talos.ipynb) or my nontechnical analysis in [presentation](https://github.com/reynoso811/Image-Classification-Pneumonia-X-rays-/blob/main/Phase_04%20-%20Image%20Classification.pdf).

For any additional questions, please contact **Robert reynoso at robert@birdstop.io**

