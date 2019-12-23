# Image-classification-using-CNN
Classification of images to identify a distracted driver


KERAS MODEL PARAMETER DETAILS
For intermediate layers we have used relu activation function 
1.	For final layer to classify images into 10 different classes, we have used softmax function.
2.	We have experimented with steps_per_epoch values in set (100,200,300,1000,2000), steps_per_epoch =2000 gave the best results.
3.	We limited training epochs to 10 to avoid model overfitting,as there was no significant improvement in model accuracy after epoch 6.
4.	We used drop out rate of 25%  for our convolutional layers and 50% of our fully connected layers to train small sets of neurons at a time, rather than the whole set. 
This helped neurons to specialize in specific tasks, rather than all neurons generalizing together.

PERFORMANCE EVALUATION USING KERAS NEURAL NETWORK
➢	Input image size: 32X32  Model training time: 1X  Model Accuracy : 0.975

  
As we can see above there is very slight increase in model accuracy increase after 6th epoch.Hence to avoid the overfitting of model, training is stopped after 10 epochs.
➢	Input image size: 64X64 Model  Training time :2X    Model Accuracy:0.986

  
As we can see above there is very slight increase in model accuracy increase after 3rd epoch.Hence to avoid the overfitting of model, training is stopped after 10 epochs.
After comparing both models, we can conclude that to slight better performance can be achieved using 64X64 input images but it would increase the model training time twice. So there is trade off between training time and accuracy. 

SVM Model
PARAMETER DETAILS: 
In our model using the SVM, we have performed image preprocessing and Feature Extraction by dimensionality reduction of the original image to 64X64 image. In order to make sure that the image does not lose its importance, we have implemented anti-aliasing technique and then the images are flattened to take into consideration the memory issues for processing large image files.
Evaluation
Classification Report-
The classes predicted for drivers using the SVM gives us almost perfect values for Precision, Recall and F1-score in the training data. The best score of the model is 99.5%

Confusion Matrix -
It gives the performance of a classification model on a set of test data for which the true values are known. It gives a table for comparison of True Positives with False Positives.


