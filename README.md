# HANDWRITTEN CHARACTER RECOGNITION USING CONVOLUTIONAL NEURAL NETWORK

## A. PROJECT SUMMARY

**Project Title:** Handwritten Character Recognition

**Team Members:** 
- Cecilia Chong Ching Nee (B031910390)
- Siew Chung Seng (B031910342)
- Vishan Menan A/L Balakrishnan (B031910018)
- Muhammad Putra Alif Bin Ismail (B031910115)

![image](https://github.com/CeciliaChongChingNee/Artificial-Intelligence-Project/blob/main/team-member.JPG)
Figure 1 shows the team member of this project

**Objectives:**
- to develop a character recognition system
- to prepare dataset for model training of character recognition system
- to predict character accurately with handwritten character recognition system

## B. ABSTRACT

Early childhood education is the period of time from a child's birth to when they enter kindergarten.
It is an inportant time in children's live because it is when they first learn how to interact with other and 
also begin to develop interests that will stay with them through their whole lives. Learning and mental development 
begin immedietely after birth. Therefore, children greatly benefit by receiving education before kindergarten.

Since kindergarten begins around the ages of 5 to 6 for most children, after major brain development occurs, parents
should begin to educating children at younger ages. Many parents begin to educate their children during these important 
developmental years by teaching them the alphabets which is the fundamental of a language. Initiation of teaching children to 
acquire some fundamental knowledges could take a lot of times. Due to time constraints such as long schedules of work, many parents 
send their children to child's care centre to be taken care and also learn to recognise alphabet or even words as their early childhood
education. Unfortunately, the widespread of covid-19 disease has caused the lockdown of the country which leads to a situation where the child's care centre are not allowed to operate. Even though the parents have to work from home but they do not have time to teach their children.

In this project, we will be providing an interface where the user can learn to write and recognise alphabets. This project is suitable for 
the children under process of learning alphabets as it is easy to use. The user only have to click on an audio button then it will read out the alphabet to be written, after the user have wrote the alphabet click "Check Answer" to verify what they have written by using machine learning.

![image](https://github.com/CeciliaChongChingNee/Artificial-Intelligence-Project/blob/main/website.JPG)
Figure 2 shows the website of Handwritten Character Recognition

## C.  DATASET

This project will be split into 3 parts, which are:
- Preprocessing : Here we will focus on preprocessing the data to allow for better training results
- Training : Here we will focus on the training of the model and the validation of training results
- Deployment : In this stage we will deploy the model by loading it and allow user to interact with it through GUI such as website

Our dataset sample are shown as below:
![image](https://github.com/CeciliaChongChingNee/Artificial-Intelligence-Project/blob/main/dataset.png)

Figure 3 shows the sample of dataset that prepared by ourselves


Our dataset for training are shown as below:
![image](https://user-images.githubusercontent.com/80866120/115016783-224cec80-9ee8-11eb-8147-88782634bd45.png)
Figure 4 shows the sample of the data used for training the model


Our website for deploy the model are shown as below:
![image](https://github.com/CeciliaChongChingNee/Artificial-Intelligence-Project/blob/main/testing.JPG)
Figure 5 shows the sample of the testing for website


The dataset we'll be using contains 26 folders (A-Z) containing handwritten images in size 2828 pixels, each alphabet in the image is centre fitted to 2020 pixel box.

Each image is stored as Gray-level

Kernel CSVToImages contains script to convert .CSV file to actual images in .png format in structured folder.

The images are taken from NIST(https://www.nist.gov/srd/nist-special-database-19) and NMIST large dataset and few other sources which were then formatted as mentioned above.

Furthermore, we also developed a simple signature pad website that allow us collect actual data that would be use for model prediction during deployment. These images are written by using the same signature pad intended for deployment therefore simulating the actual performance. These data will be stored in another folder but in a similar manner and be only used for testing the model accuracy.

Our goal is to train a CNN model that is capable of predicting/recognizing the inputted image of a character.

## D.   PROJECT STRUCTURE

The following directory is our structure of our project

    E:.
    │   alphabet.yml
    │   AlphabetData.zip
    │   A_Z Handwritten Data.csv
    │   Final Project Notebook.ipynb
    │   image.jpg
    │   model_hand.h5
    │   README.md
    │   serverApp.py
    │
    ├───.ipynb_checkpoints
    │       Final Project Notebook-checkpoint.ipynb
    │
    ├───static
    │       app.js
    │       index.css
    │       index.js
    │       title.png
    │
    └───templates
            index.html
            website.html

## E   TRAINING THE HANDWRITTEN CHARACTER RECOGNITION MODEL

We are now ready to train our model using Keras, Tensorflow, and CNN.

Firstly, navigate to the project folder containing the files.
Then we shall open up jupyter notebook to preprocess, train and test the model.
We shall do that with the following command:

$jupyter notebook

Open the notebook named "Final Project Notebook.ipynb" and run all the source code in the notebook.
First we will load the dataset and preprocess it. Next, we will split the data into 8:2 ratio for training and testing data.
80% of the data will be the training data and the remaining 20% will be testing data. After that, we will train the model and validate
the result using the test data.

Lastly, we shall deploy the model with the following command

$python serverApp.py

This will deploy the flask web application to test and use our model and will be hosted at localhost:5000.
To port forward this localhost website to the public domain, we will be using ngrok to host it.

We will port forward it to the public domain using the following command:

$ngrok http 5000

The public address is then shown and can be used to access the website anywhere with an internet connection.

## F.  RESULT AND CONCLUSION

The following is the test result of our model against 74490 test images:

![demo](https://user-images.githubusercontent.com/33794652/120072832-3fb8cd00-c0c8-11eb-99cf-97faea98291f.png)

Figure 6 shows result of model training and validation

As shown in the figure above, we are able to get an accuracy of 95% on our model.

[![Figure7](https://img.youtube.com/vi/wEa8BHbnsCw/0.jpg)](https://www.youtube.com/watch?v=wEa8BHbnsCw "Figure 7")

Figure 7 shows demo by using handwritten character recognition web application

## G.   PROJECT PRESENTATION 

In this project, you will be able to create a Handwritten Character Recoginition system using Keras, TensorFlow and CNN. To create the model we collect image of handwritten character and preprocessed them into csv for training purpose. We fine-tuned the model and is able to obtained a classifier that is 95% accurate. We then load this model on a server that allows user to draw a character and use it to predict/recognize what did the user wrote.

[![demo](https://img.youtube.com/vi/vpcIf8Mx_AM/0.jpg)](https://youtu.be/vpcIf8Mx_AM "demo")
