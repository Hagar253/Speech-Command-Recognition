# Google Speech Commands Classification

## Table of Contents
- [Project Objective](#project-objective)
- [Dataset Information](#dataset-information)
- [Preprocessing](#preprocessing)
- [Data Augmentation Techniques](#data-augmentation-techniques)
- [Instructions for Running the Code](#Instructions-for-Running-the-Code)
- [Dependencies and installation instructions](#Dependencies-and-installation-instructions)


## Project Objective
The objective of this project is to develop an ANN model that can recognize spoken digits (0 to 9) by analyzing audio data using MFCC (Mel Frequency Cepstral Coefficients) features. The model is trained on the Google Speech Commands dataset, utilizing data augmentation techniques to improve classification accuracy.

## Dataset Information
This project uses the **Google Speech Commands** dataset from Kaggle, which contains audio recordings of variety of words, but in our project, we'll be working on digits from "zero" to "nine." Each file is a short audio clip with a single word, which serves as the label for training the classifier.
### Dataset link: https://www.kaggle.com/datasets/neehakurelli/google-speech-commands/code

## Preprocessing
1. **Data Loading**: The dataset is downloaded from Kaggle and moved to a directory in the Colab environment for easier access.
3. **MFCC Feature Extraction**: MFCCs, a common feature in audio processing, are extracted to capture the essential characteristics of the speech data. Each audio file is represented by 40 MFCCs, averaged across time to create a fixed-length feature vector.
4.**Data Augmentation**:
     - Time Stretching: Speeds up the audio to simulate variations in speech rate.
     - Adding Noise: Random noise is added to make the model more robust to background noise.
     - Dynamic Range Compression: Reduces the dynamic range, simulating variations in loudness.
5. **Label Encoding**: The labels (digits 0-9) are converted into numerical format.
6. **Data Scaling**: To improve model performance, features are scaled to zero mean and unit variance.

## Instructions for Running the Code
1. **Download the Dataset**: Ensure the dataset from Kaggle (google-speech-commands) is available.
2. **Load Dependencies**: Use the dependencies specified below. The code relies heavily on librosa for audio processing, tensorflow for model training, and sklearn for encoding and splitting data.
3. **Run the Code Cells Sequentially**: Follow the cell sequence to:
     - Import the dataset
     - Extract and augment audio features,
     - Define, compile, and train the model,
     - Visualize training and validation results.
     - 
## Dependencies and installation instructions
To get started, install the necessary dependencies:

```bash
pip install numpy pandas librosa sklearn tensorflow matplotlib
