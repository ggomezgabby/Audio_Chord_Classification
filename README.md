# Audio_Chord_Classification (Major vs Minor)
Deep learning model to classify guitar chords as major or minor using STFT and CNNs

# Project Objective
This project aims to classify musical chords as Major or Minor using a Convolutional Neural Network (CNN).

Audio signals are first converted into spectrogram images, allowing the model to learn patterns from frequency and time information.

# Methodology

# 1. Audio Processing
- Input: WAV audio files
- Steps:
  - Short-Time Fourier Transform (STFT)
  - Convert amplitude to decibel scale
  - Normalize values between 0 and 1
  - Convert to grayscale image
  - Resize to 128 × 128
# 2. Dataset
- Two classes:
  - Major chords
  - Minor chords
- Data split:
  - 80% Training
  - 20% Validation
# 3. Model Architecture
The CNN model includes:
- Conv2D (32 filters)
- MaxPooling
- Conv2D (64 filters)
- MaxPooling
- Conv2D (128 filters)
- MaxPooling
- Flatten layer
- Dense layer (128 neurons)
- Dropout (0.5)
- Output layer (Sigmoid activation)

Loss Function: Binary Crossentropy  
Optimizer: Adam  

# Results
- The model achieved high training and validation accuracy
- Successfully distinguishes between Major and Minor chords
Note: Very high accuracy may indicate overfitting due to a limited dataset size.

# How to Run
1. Download dataset from (https://www.kaggle.com/datasets/deepcontractor/musical-instrument-chord-classification/code
2. Open the notebook: Chord_Classification.ipynb
3. Run all cells in order
4. Upload zipped dataset when prompted
5. Upload a .wav file when prompted
6. The model will predict whether the chord is Major or Minor

# Notes on Files

Due to GitHub file size limits:
- The trained model file (.h5) is not included
- The dataset is not included

To reproduce results:
1. Run the notebook
2. Upload dataset when prompted
3. Train the model
   
# Repository Structure
audio-chord-classification
- README.md
- Chord_Classification(1).ipynb
- .gitignore
- LICENSE

# Key Learnings
- Spectrograms allow audio signals to be processed as images
- CNNs are effective for audio classification tasks
- Proper preprocessing is critical for model performance

# Future Improvements
- Use Mel Spectrograms instead of STFT
- Increase dataset size
- Apply data augmentation
- Improve generalization to real-world audio

# Author
Gabriela Gomez  
Electrical Engineering Student  
University of British Columbia
