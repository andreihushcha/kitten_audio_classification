<div style="text-align: center;" style="border: 2px solid black;">
    <img src="images/main.png" alt="meow_kate_meow" width="600" height="400">
</div>

# FatKat: Deciphering Kitten's Meows with Neural Network-Based Audio Classification

Author: [Andrei Hushcha](https://www.linkedin.com/in/andrew-hushcha/)

## Overview
We aim to classify and understand kitten meows using advanced machine learning.  
This project focuses on revealing the complex acoustic patterns in kitten sounds using neural network model.  
Our goal is to translate these vocalizations into clear data, enhancing our understanding of feline-human communication through deep learning techniques.

## Data Understanding

1. **Building the Dataset**  
_1.1 Participants:_  
Mio, a 3.5-month-old Scottish Fold kitten.  
A group of humans including the study author and his daughter Kate.  
_1.2 Experimental Contexts:_  
- `F` aka food: Kitten recorded before mealtime.
- `A` aka attention: Kitten recorded meowing in an isolated room.
- `T` aka thrill: Kitten recorded while being petted.
- `KAT` aka human: Human participant randomly mimicking meows.

2. **Data Acquisition Process**  
The experiment spanned 15 days.  
Recordings were made using a Samsung Note20 equipped with the "Samsung Voice Recorder" app.  
Files were converted to .wav format and broken down into samples under 3 seconds.

3. **Dataset Composition:**  
The dataset consists of:
- 95 samples in `F`
- 95 samples in `A`
- 80 samples in `T`
- 98 samples in `KAT`  
Total: 368 audio files

Each sample is named in a format indicating the date, time, condition, and sample number.

3. **Prediction audio samples:**  

4 random samples from each condition, not included in dataset, and 1 extra by the author were chosen for prediction testing.

_`More details about building dataset can be found in the Notebook`_

## Business Problem
Many people decide to get a kitten, but they don't always fully understand what these cute creatures need.  
Games, food or something else?  
And how to find out if they enjoy playing?

This project consists of two key parts:
- **Model for predicting meowing categories:**  
We aim to create a model that accurately determines which category a meow belongs to with the best accuracy score.  
- **Mobile app for owner training:**  
Based on the model's results, we are developing a mobile app.  

## Methods
This project uses Dummy, XGBoost, Neural Network Sequential Models.  
Findings are informed by a strong understanding of Librosa, Tensorflow, Keras, Scikit Learn.

## Results
Neural Network Sequential tuned with Keras Tuner exhibited the highest accuracy on both the training and test datasets, with scores of 95.9% and 93.2%, respectively.  
In the final prediction phase, all files were predicted correctly, demonstrating the effectiveness of the model in classifying audio samples based on the features extracted.  

## Exploratory Data Analysis
Audio files share common properties:  
- .wav format
- mono channel
- sample rate of 44100 Hz
- 16-bit depth  
The audio data is stored in NumPy arrays.  

We explored files with diverse audio characteristics which offered various measures such as:  
- Waveform
- Spectral centroid
- Spectral bandwidth
- Spectral rolloff
- Zero-crossing value
- Mfcc
- Spectrogram
- Chromagram. 
<div style="text-align: center;" style="border: 2px solid black;">
    <img src="images/waveform_food.png" alt="waveform_food" width="500" height="300">
</div>

<div style="text-align: center;" style="border: 2px solid black;">
    <img src="images/centroid_thrill.png" alt="centroid_thrill" width="500" height="300">
</div>

<div style="text-align: center;" style="border: 2px solid black;">
    <img src="images/spectogram_attention.png" alt="spectogram_attention" width="500" height="400">
</div>

<div style="text-align: center;" style="border: 2px solid black;">
    <img src="images/chromagram_human.png" alt="chromagram_human" width="500" height="400">
</div>

Each condition can be described as below: 
- `food` showed fluctuating intensity and low-frequency dominance
- `attention` was marked by consistent high-frequency sounds
- `thrill` exhibited complex, variable sounds across a wide frequency range
- `human` demonstrated stable, monotone audio with a focus on lower frequencies

## Dataset Processing  
We processed audio files converting them into spectrograms.  
These features were extracted:
- Chroma Frequencies
- Spectral Centroid
- Spectral Bandwidth
- Spectral Rolloff
- Zero Crossing Rate
- Mel-frequency cepstral coefficients (MFCC), limited to 13 to prevent overfitting.  
## Modeling
We created and trained three models: Dummy, XGBoost, and Neural Network Sequential (NNS).  
The XGBoost and NNS were fine-tuned using GridSearchCV and Keras Tuner, respectively.     

The Confusion Matrix reveals a certain level of misclassification between the _food_ and _attention_.
<div style="text-align: center;" style="border: 2px solid black;">
    <img src="images/confusion_matrix.png" alt="confusion_matrix" width="500" height="400">
</div>

## Predictions
We used saved Neural Network Sequential model to predict the categories of random audio samples.
A sample of a prediction:  
File: 202312090945_F_predict.WAV  
Probabilities for each condition:  
attention: 3.65%  
food: 96.35%  
human: 0.00%  
thrill: 0.00%  
Predicted condition: ['food']

## Data Limitations
- Data is limited to a specific age, gender, and breed of the kitten
- Constraints extend to the specific environment and the kitten's behavioral range

# Conclusion
Overall, the project successfully utilized various audio analysis techniques and machine learning models to distinguish between different audio conditions.  
Tuned Neural Network Sequential model is considered the most effective for predictions.  
The high accuracy in model predictions highlights the potential of machine learning in sophisticated audio analysis tasks.

# Mobile App Development  
In progress.

