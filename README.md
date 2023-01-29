# Sign Recognition Project Jan 2023
A project to convert a sign to its equivalent text.
## Contents:
[Abstract](#abstract)
[Introduction](#introduction)
[Overall Description](#overall-description)
[LSTM](#lstm)
[Data-set Generation Process](#data-set-generation-process)
[Data-set Training Process](#data-set-training-process)
[Data-set Testing Process](#data-set-testing-process)
[Future Scope](#future-scope)

## Abstract:
Sign language is one of the oldest and most natural forms of language for communication.  Most people do not know sign language and interpreters are very difficult to come by, therefore we have come up with a real time method using neural networks for finger-spelling based Indian SignLanguage (ISL).

## Introduction:
### Purpose:
The purpose of the project is to build an AI assistant designed specifically for speech impaired individuals that converts sign language to text using a video call interface.
### Project Scope:
1. The app provides a cheap solution as compared to sign language interpreters which are just costly to buy.
2. It can simply be used with a web camera, making it efficient as compared to interpreters.
3. This project provides ease of access for speech impaired individuals, as no additional equipment is needed.

## Overall Description:
### Project Functions:
1. Accepting input from webcam
2. Detecting the signs
3. Displaying correct output(translated sign)
### Techstack:
1. Interfaces/Tools:
- Jupyter
- Webcam
2. Software dependencies:
- OpenCV
- Mediapipe
- Tensorflow
- Keras

## LSTM:
Our project uses the LSTM network. In concept, an LSTM recurrent unit tries to “remember” all the past knowledge that the network is seen so far and to “forget” irrelevant data. This is done by introducing different activation function layers called “gates” for different purposes.

## Data-set Generation Process:
We use the OpenCV library of python to capture images and snippets of the training data that gets stored into a folder ”MP Data” with each sign as a separate sub-folder. As of now the following are the signs that have been included:
- The Alphabet(A-Z)
- First 10 numbers(1-10)
- 12 Common phrases(hello, how are you, my name is, welcome, thank you, please, sorry, bye, good morning, good afternoon, good evening, good night)

## Data-set Training Process:
The model is trained using 3 layers of LSTM and 3 Dense layers with the Relu activation function and Softmax for the last layer. The optimizer used is Adam. The following data set has been trained for 300 epochs giving an accuracy of 84.60\% when it is tested against itself. Finally this model is saved and used for the training phase.
![image](https://user-images.githubusercontent.com/83157662/215320877-4e9ee3e5-b2e2-46bd-95a0-5d9ffce99051.png)
![image](https://user-images.githubusercontent.com/83157662/215320884-0ef23edb-b25d-45de-a19b-c6c8bf5d5c19.png)
![image](https://user-images.githubusercontent.com/83157662/215320905-26cf291c-cdb6-4144-a5d1-ab1626610d9b.png)

## Data-set Testing Process:
The testing of the model is done once we have the saved trained model. Here we have tested for some of the signs like 6, o, q, v, 8. 
![image](https://user-images.githubusercontent.com/83157662/215320923-fc0e3e1b-cfca-4942-80cf-2b2414534ea3.png)
![image](https://user-images.githubusercontent.com/83157662/215320933-120814ad-20d9-455f-90ec-0add29ddf1f2.png)

## Future Scope:
This project is still in its initial stages and definitely needs much improvement in terms of accuracy and additional signs to the data set, in order to predict a wider range of signs. Other scopes include:
- Front-end/UI for the application
- Conversion into a browser extension

Contributions to this repository are open via issues. Feel free to contact the authors in case of any problems :)
