This is a summary of my Food Vision project.

This is a Computer Vison project in TensorFlow that utilizes transfer learning and convulutional neural networks to perform food classification. 

## Table of Contents 
* [Motivation](#motivation)
* [Summary of approach](#summary-of-approach)
* [Results](#results)
* [Insights](#insights)
* [What I learned](#what-i-learned)
* [How to use this repository](#how-to-use-this-repository)

## Motivation
Upon reaserching copmuter vision and deep learning I stumbled on to the Food101 reaserch paper and found it intreging and wanted to see if I could create a model to beat the results obtained.
![alt text](https://github.com/Vybavnag/Food_Vision_Project/blob/main/images/food101.jpg)


## Summary of approach
For this project, I decided to first create a baseline with as few parameters as possible. The loss curves for the base_line is shown here:
![alt text](https://github.com/Vybavnag/OpenAvenues_project/blob/main/images/19_Lambda-1.jpg)
It looked like the moddel was overfitting so I decided to add DataAugmentation.

The loss curves for the DataAugmentation is shown here:
![alt text](https://github.com/Vybavnag/OpenAvenues_project/blob/main/images/IMG_3388.jpg)\
looks like the accuracy took a hit and went down but seems like data is diverse providing variety in training. I then dcided to unfreeze some layers and accived an accuracy of 77%


## Results
Epoch 5/10
2368/2368 [==============================] - 115s 40ms/step - loss: 1.3341 - accuracy: 0.6511 - val_loss: 0.9124 - val_accuracy: 0.7461
Epoch 6/10
2368/2368 [==============================] - 90s 38ms/step - loss: 1.1738 - accuracy: 0.6893 - val_loss: 0.8474 - val_accuracy: 0.7608
Epoch 7/10
2368/2368 [==============================] - 88s 37ms/step - loss: 1.0501 - accuracy: 0.7180 - val_loss: 0.8073 - val_accuracy: 0.7697
Epoch 8/10
2368/2368 [==============================] - 87s 36ms/step - loss: 0.9531 - accuracy: 0.7417 - val_loss: 0.7768 - val_accuracy: 0.7757
Epoch 9/10
2368/2368 [==============================] - 85s 35ms/step - loss: 0.8658 - accuracy: 0.7624 - val_loss: 0.8006 - val_accuracy: 0.7823
Epoch 10/10
2368/2368 [==============================] - 83s 35ms/step - loss: 0.7923 - accuracy: 0.7787 - val_loss: 0.7941 - val_accuracy: 0.7776

## Insights
The data showcases a system that identifies trending products across different groupings, termed "buckets". Each product, denoted by an ID, has a trending percentage in these buckets; a positive value indicates rising popularity, while a negative hints at decreasing interest. For example, product "1307153" sees both growth and decline in different buckets.The speed layer offers real-time product recommendations for individual users, distinct from the general trend analysis. Lastly, the serving layer amalgamates these insights, pinpointing top trending products and interweaving real-time user-specific recommendations. Negative percentages, especially, highlight products witnessing waning demand or shifting consumer preferences in their respective categories.

## What I learned
* Sometimes, just analyzing data can teach us a lot, even without advanced predictions.
* Planning ahead is important. Decide what data you want to input and get out of your model before you start.
* What are Kafka systems.
* How to create an advanced data pipeline in python to analyze data and create reccomendations 
  


## How to use this repository
This repository has a main_code file which you should download as well as the dataset_link file which leads you to the datasets used. Download them in the same file and rub the main_code file preferably on JypterNotebook or GoogleColab. Main_code_outputs shows all the outputs I got, when you run the file you should get something similar. The rest of the files showcase what I learned week by week while working on this project with OpenAvenues.

