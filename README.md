# Audio Processing and Genre Classification

This repository contains a series of Python scripts focused on audio signal processing, feature extraction, and genre classification using neural networks.

## Files Overview:

### audio_dataset_preparation.py

- Loads an audio file using the librosa library.
- Visualizes the waveform of the audio signal.
- Computes and plots the Fast Fourier Transform (FFT) of the audio signal to represent its frequency spectrum.
- Computes and visualizes the Short-Time Fourier Transform (STFT) to represent the signal's spectrogram.
- Extracts and visualizes the Mel-frequency cepstral coefficients (MFCCs) from the audio signal.

### audio_preprocess.py

- Extracts MFCCs from a dataset of audio files and saves the results in a JSON file.
- Provides functionality to process a dataset of audio files in various genres and store them along with the corresponding genre labels in a JSON file.
- This module can be run directly to process a default dataset and save the results to a default JSON file.

### audio_classifier.py

- Loads the dataset from a JSON file.
- Splits the dataset into training and testing sets.
- Builds a neural network model using TensorFlow and Keras to classify the audio signals into different genres.
- Compiles, trains, and validates the model.
- This module can be run directly to train a model on a default dataset.

## Usage:

## 1. Audio Visualization

To visualize the audio signal and its frequency representations, run the audio_classifier.py script. Make sure to set the correct path for the audio file you want to process.

```
file = "path_to_your_audio_file.wav"
```

## 2. Audio Feature Extraction

To extract MFCCs from a dataset of audio files and save the results in a JSON file, run the audio_preprocess.py script.

By default, it will process the dataset located at GTZAN_Data/genres_original and save the results in data.json.

To change the dataset path and output file:

```
DATASET_PATH = "path_to_your_dataset"
JSON_PATH = "path_to_your_output_file.json"
```

Then run the script:

```
$ python audio_preprocess.py

```

## 3. Audio Genre Classification

To train a neural network for genre classification, run the audio_classifier.py script.

By default, it will use the dataset located in data.json.

To change the dataset path:

```
DATASET_PATH = "path_to_your_dataset_file.json"
```

Then run the script:

```
$ python audio_classifier.py

```

Requirements:

- Python 3.x
- Libraries:
  - numpy
  - matplotlib
  - librosa
  - os
  - json
  - math
  - sklearn
  - tensorflow
