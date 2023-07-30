## Purpose
The purpose of this project is to use transfer learning for caption generation given an image input. This model will be useful for automated captioning for accessibility in the form of ALT text as well as automated captioning for SEO.

## Data
Data was downloaded from the [Flickr8k Images + Captions Kaggle Dataset](https://www.kaggle.com/datasets/aladdinpersson/flickr8kimagescaptions)

This dataset contains approximately 8k images with 5 captions each. Due to technical limitations, the dataset was downsampled to approximately 1200 images. The following sections describe the contents within the corresponding Jupyter Notebooks.

## EDA
The EDA notebook holds initial EDA on images and captions. Images were displayed alongside their captions. Random images and their first captions along with a single image and multiple captions were checked. Captions were then put into a dataframe alongside the relevant images for preprocessing.

## Pre-processing
The Pre-processing notebook includes deeper data analysis and pre-processing methods for both images and captions. Downsampling and ground truth caption selection are justified by analyzing word frequencies in the existing captions. Initially, only a single caption was taken for modeling, but this was later changed to including all 5 captions.

Pre-processing included tokenizing the natural language captions and extracting image features using EfficientNetV2S. NLP pre-processing will be done using Keras Tokenizer. All preprocessed dictionaries and dataframes were saved as pickle files for use in modeling.

## Modeling
The modeling notebook includes generator functions for model training, validation, and testing. Modeling proceeded in stages:
![image](https://github.com/ananyachattoraj/capstone/assets/15469141/a6dfb0f1-599f-49f2-a671-23da587d83bc)

Early modeling stages saw images that were simply converted into arrays for Conv2D and Pooling layers. Early modeling also only utilized a single caption as text input for Embedding and LSTM layers. Later models used extracted image features and all 5 captions tokenized. Generator functions and layer input requirements were updated accordingly.

The best performing model was Model 13. Details may be found in the modeling notebook.

## Final
The final notebook simply carries forward the model file and all required variables and functions in a clean notebook for test image and caption generation.
