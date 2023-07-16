## Purpose
The purpose of this project is to use transfer learning for caption generation given an image input. This model will be useful for automated captioning for accessibility in the form of ALT text as well as automated captioning for SEO.

## Data
Data was downloaded from the [Flickr8k Images + Captions Kaggle Dataset](https://www.kaggle.com/datasets/aladdinpersson/flickr8kimagescaptions)

This dataset contains approximately 8k images with 5 captions each. 

## EDA
Images and captions are EDA'd separately. This dataset is very clean: there are no null values and all images have the same number of captions. For deeper EDA, melding with the pre-processing workflow, I examine the most frequently used words to describe my training set. I also create an "average" image based on the values of the pixels in my training set.

## Pre-processing
Pre-processing includes tokenizing the natural language captions and preparing images as arrays. NLP pre-processing will be done using Keras Tokenizer and image prep will be done using Keras utilities such as img to array. Since images are not sorted into "categories" in the same sense as an image classifier system, Keras Image Data Generator is not used.

## Modeling
Modeling will be done using Keras EfficientNetV2S.

## To Do
- [x]get data (flicker 8k + captions)
- [x]EDA images
- [x]EDA captions
- [x]create training and test groups
- []exploring image layers in cnn
- []exploring layers of lstm
- []exploring supervised machine learning