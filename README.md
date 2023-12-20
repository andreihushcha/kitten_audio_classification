<div style="text-align: center;" style="border: 2px solid black;">
    <img src="images/main.png" alt="meow_kate_meow" width="600" height="400">
</div>


# Data Understanding
1. **Building the Dataset**

_1.1 Participants:_
- A lively and amicable 3.5-month-old male Scottish Fold kitten named Mio served as the primary subject.
- A group of human participants, including myself as a study author and my daughter Kate as a human meow vocalizer.

_1.2 Experimental Contexts:_  
Accompanied by the study author, the kitten was exposed to four distinct contexts aimed at eliciting varied meows:

- Waiting for Food (Condition `F`):
The author initiated routine morning recordings preceding mealtime, with food delivered after the recordings done.
- Seeking Attention in Isolation (Condition `A`):
The kitten was placed in an isolated room with ample provisions and signaled its need for attention by meowing at the closed door.
- Contentment (Condition `C`):
The kitten is purring while petted and caressed by author in a home environment for 3-5 minutes.
- Thrill (Condition `T`):
Meowing during a state of contentment.

Typically, vocalizations in a single exposure comprised multiple repeated meows.

2. **Data Acquisition Process**

The experiment spanned 12-15 days, conducted in the same room, with daily data collection using a Samsung Note20 phone equipped with the "Samsung Voice Recorder" app.  
Each recorded audio file, averaging 1.5-2.5 minutes, was converted to .wav format via www.cloudconvert.com  
Further processing included breaking down each .wav file into individual samples: meow (less than 3 seconds) and purrs (less than 5 seconds).

3. **Dataset Composition:**  

The dataset consists of:
- 96 samples obtained under Condition `F`
- 90 samples obtained under Condition `A`
- 66 samples obtained under Condition `C`
- 19 samples obtained under Condition `T`

Additionally, we included 99 meows from my daughter to aid the program in recognizing human meow.  
These samples are obtained under condition `KAT`  
This diverse set of vocalizations allows us predict artificial meows if users want to simulate meowing themselves.  

**Total: 370 audio files**

Individual sample description:  
202312071816_T_1.wav,  where
- 2023 = year recorded
- 12 = month recorded
- 07 = day recorded
- 18  = hour (24 hours) recorded
- 16 = minute  recorded
- T = condition recorded
- 1 = number of the sample
- wav = audio format of the sample
# Business Problem
Many people decide to get a kitten, but they don't always fully understand what these cute creatures need.  
Games, food or something else?  
And how to find out if they enjoy playing?

Our project consists of two key parts:
- **Model for predicting meowing categories:**  
We aim to create a model that accurately determines which category a meow belongs to with the best accuracy score.  
Data processing speed is also an important aspect, influencing the second part of our work.

- **Mobile app for owner training:**  
Based on the model's results, we are developing a mobile app.  
It provides new owners with the opportunity to learn how to understand their furry friends from the very first days in their new home.
# EDA
# Modeling
# Testing Best Model
# Deployment
# Conclusion
