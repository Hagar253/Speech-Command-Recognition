# Speech-Command-Recognition

## Objective of the project
The objective of this project is to develop an ANN model that can recognize spoken digits (0 to 9) by analyzing audio data using MFCC (Mel Frequency Cepstral Coefficients) features. The model is trained on the Google Speech Commands dataset, utilizing data augmentation techniques to improve classification accuracy.

## Dataset information 
The dataset used is the Google Speech Commands dataset from Kaggle, which contains audio recordings of variety of words, but in our project, we'll be working on digits from "zero" to "nine." Each file is a short audio clip with a single word, which serves as the label for training the classifier.
### Dataset link: https://www.kaggle.com/datasets/neehakurelli/google-speech-commands/code

## Preprocessing Steps:
#### Data Loading: 
The dataset is downloaded from Kaggle and moved to a directory in the Colab environment for easier access.
#### MFCC Feature Extraction: 
MFCCs, a common feature in audio processing, are extracted to capture the essential characteristics of the speech data. Each audio file is represented by 40 MFCCs, averaged across time to create a fixed-length feature vector.
#### Data Augmentation:
Time Stretching: Speeds up the audio to simulate variations in speech rate.
Adding Noise: Random noise is added to make the model more robust to background noise.
Dynamic Range Compression: Reduces the dynamic range, simulating variations in loudness.
