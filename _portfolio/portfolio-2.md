---
title: "Brain Tumor Classification model"
excerpt: "Brain Tumor Classification CNN model<br/><img src='/images/tumor_predictions.png'>"
collection: portfolio
---

### Introduction:
In this project, I am presenting the performance analysis of a Convolutional Neural Network (CNN) model designed for the task of cancer detection from medical images. The CNN model was trained and evaluated using a dataset consisting of images labeled as either cancerous or healthy tissue.

### Model Architecture:
The CNN model architecture consists of three convolutional layers followed by max-pooling layers for downsampling. Each convolutional layer is followed by a rectified linear unit (ReLU) activation function to introduce non-linearity into the model. The final convolutional layer is connected to a densely connected layer with 512 neurons, also activated by ReLU. To prevent overfitting, a dropout layer with a rate of 0.5 is incorporated before the final output layer. The output layer consists of a single neuron activated by a sigmoid function, producing a binary classification output indicating the likelihood of cancer presence.

### Data Split:
The dataset was divided into training, validation, and test sets with a ratio of 60:20:20. The training set was used to train the model, while the validation set was utilized for monitoring model performance during training. The test set, separate from both training and validation data, was used to evaluate the final model's performance on unseen data.

### Training and Validation:
The model was trained using the Adam optimizer with a learning rate of 0.0001 and binary cross-entropy loss function. Training was conducted for 40 epochs. During training, the model achieved a training accuracy of approximately 97.14%. Validation accuracy was monitored to prevent overfitting and ensure generalization performance.

### Evaluation on Test Set:
The test dataset comprised 921 images, with a roughly equal distribution between cancerous and healthy tissue classes. The trained model was evaluated on this test set to assess its performance on unseen data. The evaluation revealed a test accuracy of approximately 96.31%, indicating strong generalization capabilities.

### Conclusion:
The CNN model demonstrated promising performance in accurately distinguishing between cancerous and healthy tissue from medical images. With a test accuracy of over 96%, the model shows potential for practical application in assisting medical professionals in cancer diagnosis. Further optimization of the model incorporating techniques such as k-fold cross-validation and hyperparameter tuning could potentially improve its performance even further.

Links to the code: 
 - [Github](https://github.com/KaragkounisL/Machine-Learning/blob/main/brain_tumor.ipynb)
