This is a summary of my Food Vision project.

This is a Computer Vision project in TensorFlow that utilizes transfer learning and convolutional neural networks to perform food classification. 

## Table of Contents 
* [Motivation](#motivation)
* [Summary of approach](#summary-of-approach)
* [Results](#results)
* [Insights](#insights)
* [What I learned](#what-i-learned)
* [How to use this repository](#how-to-use-this-repository)

## Motivation
Upon researching computer vision and deep learning I stumbled on the Food101 research paper and found it intriguing and wanted to see if I could create a model to beat the results obtained.
![alt text](https://github.com/Vybavnag/Food_Vision_Project/blob/main/images/food101.jpg)


## Summary of approach
For this project, I decided to first create a baseline with as few parameters as possible. The loss curves for the base_line is shown here:
![alt text](https://github.com/Vybavnag/Food_Vision_Project/blob/main/images/base_loss.jpg)
It looked like the moddel was overfitting so I decided to add DataAugmentation.

The loss curves for the DataAugmentation is shown here:
![alt text](https://github.com/Vybavnag/Food_Vision_Project/blob/main/images/data_aug_loss.jpg)
looks like the accuracy took a hit and went down but seems like data is diverse providing variety in training. I then decided to unfreeze some layers and achieved an accuracy of 77%


## Results
Here are the results I achieved.
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

Here is what the loss curves look like:
![alt text](https://github.com/Vybavnag/Food_Vision_Project/blob/main/images/final_loss.jpg)

Here is when I compared before fine-tuning and after:
![alt text](https://github.com/Vybavnag/Food_Vision_Project/blob/main/images/final_comparing_loss.jpg)

## Insights
The results obtained by my final model might look worse than the baseline. However, while looking at the confusion matrices and using the pred_and_plot function at the end we can see that model_1 was overfitting on the training data as custom image predictions would not output the right results in comparison to the final model.

## What I learned
* Sometimes, simple is better. I tried EfficentnetB7 and got slightly worse results.
* Planning ahead is important. Start small and scale up so you don't overcomplicate it at the start.
* What are CNN's? How to create computer vision models and I understood the hyperparameters Tensorflow provides.
* How to use Transfer learning and the benefits/cons it provides.


## How to use this repository
Open the ipynb file in Google Colab or Jupyter Notebook and run. Make sure there is a GPU with high RAM.
