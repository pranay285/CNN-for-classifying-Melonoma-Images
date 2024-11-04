# -Convolutional-Neural-Networks-for-Classifying-Melonoma-Images-
The research focused on the importance of accurately diagnosing cancer to avoid detrimental consequences such as delayed or ineffective treatment, patient suffering, and even death. To address this issue, I utilized deep learning methods to classify Melanoma Images, using data from the ISIC database for training and testing the models.

In this project, I have attempted to replicate the work of Abhinav Sagar and Dheeba Jacob in their
research on "Convolutional Neural Networks for Classifying Melanoma Images." The research
focused on the importance of accurately diagnosing cancer to avoid detrimental consequences such
as delayed or ineffective treatment, patient suffering, and even death. Misdiagnosis may result
from misinterpretation, inadequate testing, or limited access to diagnostic resources. Additionally,
incorrect cancer diagnoses may lead to unnecessary testing and treatment for patients who do not
have cancer. To address this issue, I utilized deep learning methods to classify Melanoma Images,
using data from the ISIC database for training and testing the models.
Introduction
The early detection and appropriate treatment of skin cancer can significantly increase a patient's
chances of survival. To identify skin cancer symptoms in patients at an early stage, deep learning
can be used to analyze images of skin lesions and classify them as either benign or malignant using
computer vision algorithms. By training a deep neural network on a large dataset of skin lesion
photos, the network can learn to recognize patterns and features that differentiate benign from
malignant lesions. With this knowledge, the network can then automatically classify new photos
of skin lesions into benign or malignant categories without the need for human expertise. This
automated approach can enable fast and accurate skin cancer identification, particularly in regions
where access to qualified dermatologists is limited. The accuracy rates of deep learning models
for skin cancer detection are high. In this project, we have reviewed the deep learning models
employed by the authors of the referenced paper and implemented new models to compare with
their previous findings.
Methods
Data Collection:
The author of this paper has taken the dataset from ISIC database for training and testing. The
dataset taken from ISIC was last updated in 2020 which has nearly 33000 images. The author has
used transfer learning and implemented the Resnet50 deep learning model to train the images from
the ISIC database. The author has used Jupyter Notebook as his environment and used various
libraries like Numpy, Pandas, Scikit-image, Matplotlib, Scikit-learn, and Keras in his code. The
author's code was taken from his github page and implemented first. The dataset was however
unavailable in the authors github page so was collected from the ISIC open dataset.

The images obtained from the ISIC dataset were used in a challenge in Kaggle which was
downloaded for the project. All the images were stored in a folder and a csv file which had
information on each image, including if the image depicted a malignant or benign tumor. The
images were sorted into two folders named benign and malignant using the csv file to make it easy
to access the different categories of images.
Data Pre-processing:
The images were sorted into 4 sets named as benign_train, benign_test, malign_train, and
malign_test. The number of images used by the author in the code were 3297 images, 2800 images
for training and 1497 images for testing. The images were then labeled as 0 for benign and 1 for
malignant fig1. The images were then used to train the Resnet50 model by the author. A total of
50 epochs were used while training the model.
Modeling:
In this project the number of images used for training are 7993 and for testing are 1601, so a larger
number of images were used to train the VGG16 model used in the project. A total of 50 epochs
were used while training the model.

Both ResNet50 and VGG16 have attained high accuracy rates in a variety of computer vision tasks
like object recognition and picture segmentation because they were trained on extensive image
classification datasets like ImageNet. However, because of its more complex architecture,
ResNet50 typically uses more computational power and trains more slowly than VGG16.

Fig1

This figure shows the different category of images used and have been labeled as 0 for benign and
1 for malignant

Results
In this section we present our findings.Firstly running the code provided by the author and then
implementing the updated code for the project, I have plotted the Accuracy vs Epochs graph Fig2,
Validation loss vs epochs graph Fig3, and ROC-AUC curve for the classifier Fig5.

Accuracy vs Epochs

Figure2

The above figure shows the plot for Accuracy vs epochs with the original code’s plot to the left
and the updated code’s plot to the right. It can be observed that although training the Vgg16 model
gave a lower accuracy in the beginning, the accuracy increased greatly to a higher value than that
of the ResNet50 at the end of the 50 epochs.

Validation Loss vs epochs

the Validation loss vs epochs curve which depicts how the loss of each
model changes over the training period. The left curve shows the plot for the Resnet50 model and
the right for the Vgg16 model.

ROC-AUC Curve


Prediction Results

the prediction result where benign tumors are identified correctly.

Discussion
To Summarize, this project was to understand and implement what the author of the paper
“Convolutional Neural Networks for Classifying Melanoma Images” had implemented. The
author in the paper explains the effectiveness of deep learning CNN models which can be used to
classify malignant and benign cancer using dermoscopy images. The authors have demonstrated
that a well trained deep Convolutional Neural Network algorithm can outperform dermatologists
in accuracy. Using transfer learning and fine tuning the CNN models it would be easier to identify
and classify cancer from the dermoscopy images provided. The author had implemented a
ResNet50 model and trained it with neatly 3300 images with 50 epochs and had obtained an
accuracy of 90%. Updating the authors code by training a Vgg16 model with nearly 8000 images
and with 50 epochs had given an accuracy of 94.2% which is greater than what the author was able
to get.
Applying an image preprocessing can give a better result, for example using a hair removal- image
processing technique can make the dermoscopy images more clearer for the model to understand
and can classify the images better.
