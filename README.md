---
layout: default
---

# Sign language based interaction

209_BO2
#### Nicolas Cheng
#### Yinghan Cui
#### Zeyu Wang


## Overview
A large number of spatially-distributed Internet of Things (IoT) has populated our living and work environments, motivating researchers to explore various interaction techniques. However, the majotity of techniques used today, such as *Amazon Alexa*, *Google Home* and *Siri*, are still limited t voice-based interaction. This brings about various difficulties in certain scenarios that voice command is not applicable. In addition, some people that are vocal impaired will never be able to enjoy these techniques. In order to resolve this, in this project we designed a **gesture-based** interaction technique with Alexa. The system takes live video of a person and transcribes the gesture into voice command for Alexa to process.

## Goals
```markdown
    Achieve IoT interaction for certain groups of disabled people
    Enable IoT interaaction in certain scenarios
```
This desired interaction techniques could be concluded in the following chart:

![Interaction Design](https://github.com/nickycheng4/209_BO2/blob/master/209_bakeoff_2/supportive_images/overview.png)

## System Flowchart

![Training Page](https://github.com/nickycheng4/209_BO2/blob/master/209_bakeoff_2/supportive_images/input.png)

To use this system, simply open the **index.html** file. In this first step, enter some commands that you would like to make to Alexa and then check the "end of sentence" box for each command. Then click the button *"click to train"*. 

![Training Process](https://github.com/nickycheng4/209_BO2/blob/master/209_bakeoff_2/supportive_images/trains.png)

In the second step, hold the *"add example"* button while do the gesture you would like to be transcribed into that command. Remember that at least 30 example counts is needed to teh system to have a satisfactory performance. When example number is around 100, the performence of the system is ideal. For the command "other", simply hold the add example button and do nothing, as this command is used to determine that the user is doing nothing. Once done with al the commands, click *"try the model"*.

![Final Interface](https://github.com/nickycheng4/209_BO2/blob/master/209_bakeoff_2/supportive_images/final.png)

Start using your gesture commands to interact with Alexa! Remember that **each time** before you input a specific command, you have to use the command **"Alexa"** to trigger the system! 

![Examples](https://github.com/nickycheng4/209_BO2/blob/master/209_bakeoff_2/supportive_images/2.jpg)

Above are some gesture suggesitons in case you need some examples.

![Hand recognition example](https://github.com/nickycheng4/209_BO2/blob/master/209_bakeoff_2/supportive_images/hand1.jpeg)

The system implements **KNN** for image classification. The advantage of KNN is that it does not require training time. After the user inputs training data, they are stored and when the user makes a gesture that has a matching confidence to certain stored gesture higher than the a preset threshold value, the related voice command with gesture will be played. The recognition flowchart is shown below. 

![Gesture Flowchart](https://github.com/nickycheng4/209_BO2/blob/master/209_bakeoff_2/supportive_images/gesture_flowchart.png)

You can find a detailed instruction in the demo video.

## Demo Video
![209HCI_bakeoff2_demo_2.mp4](https://github.com/nickycheng4/209_BO2/blob/master/209HCI_bakeoff2_demo_2.mp4)

## Reference Work

Knn Classifier:
https://github.com/tarunkolla/KNN-Classifier

UI:
General: https://github.com/collections/design-essentials
HTML & CSS: https://github.com/scotch-io
CSS Tips: https://www.hongkiat.com/blog/20-useful-css-tips-for-beginners/

Lip Language:
Lip language: https://github.com/astorfi/lip-reading-deeplearning
