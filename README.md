# Google Speech Commands Classification

## Table of Contents
- [Project Objective](#project-objective)
- [Dataset Information](#dataset-information)
- [Preprocessing](#preprocessing)
- [Data Augmentation Techniques](#data-augmentation-techniques)
- [Dependencies and installation instructions](#Dependencies and installation instructions)


## Project Objective
The objective of this project is to develop an ANN model that can recognize spoken digits (0 to 9) by analyzing audio data using MFCC (Mel Frequency Cepstral Coefficients) features. The model is trained on the Google Speech Commands dataset, utilizing data augmentation techniques to improve classification accuracy.

## Dataset Information
This project uses the **Google Speech Commands** dataset from Kaggle, which contains labeled audio recordings for each digit (0-9). Each clip contains a single spoken word, which serves as the training label.
### Dataset link: https://www.kaggle.com/datasets/neehakurelli/google-speech-commands/code

## Preprocessing
1. **Loading Audio Files**: Files are loaded and converted to a uniform sampling rate.
2. **MFCC Feature Extraction**: 40 MFCCs are extracted and averaged across time for each audio file to create fixed-length feature vectors.
3. **Label Encoding**: The labels (digits 0-9) are converted into numerical format.

## Data Augmentation Techniques
To improve model performance and generalization, the following augmentations are applied:
- **Time Stretching**: Alters the speed of the audio without changing the pitch.
- **Adding Noise**: Adds random background noise for robustness.
- **Dynamic Range Compression**: Modifies volume dynamics to simulate variations in loudness.

## Dependencies and installation instructions
To get started, install the necessary dependencies:

```bash
pip install numpy pandas librosa sklearn tensorflow matplotlib
