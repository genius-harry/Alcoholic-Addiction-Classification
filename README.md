
# Alcoholic Addiction Classification Using EEG Data

## Abstract
This project focuses on applying machine learning techniques to classify alcohol addiction using EEG data. The dataset, sourced from the UCI Machine Learning Repository, contains EEG signals from participants in control and alcoholic groups. The study explores various machine learning models, including a basic neural network, Convolutional Neural Network (CNN), ResNet, and an autoencoder. By transforming EEG signals from the time domain to the signal domain and generating RGB images for feature extraction, this project demonstrates the potential of EEG data and machine learning for accurately classifying alcohol addiction.

## Dataset
The dataset used in this project is from the UCI Machine Learning Repository and includes EEG signals recorded from participants in control and alcoholic groups. These participants were subjected to three experimental conditions: S1 (object), S2 (matching), and S2 (no-match). The EEG signals were collected during these experiments and form the basis for the machine learning models used in this study. *Note: The dataset is not uploaded to this repository. Please download and place the dataset files in the `data/` directory.*

## Data Preprocessing
1. **Data Cleaning:** The EEG data is cleaned to remove irrelevant columns and missing values.
2. **Signal Transformation:** The EEG signals are transformed from the time domain to the signal domain using Fourier transform and Power Spectral Density (PSD) computation.
3. **RGB Image Generation:** The EEG signals are split into three frequency bands (Alpha, Beta, Theta), which are then used to generate RGB images. Each color channel corresponds to one frequency band, allowing for visual representation of EEG data.

## Machine Learning Models
Four machine learning models were trained on the processed EEG data, each with distinct architectures and performance metrics:

1. **Base Model (Feedforward Neural Network)**
   - A simple feedforward neural network with fully connected layers.
   - **Accuracy:** 57%

2. **Convolutional Neural Network (CNN)**
   - A CNN designed to extract spatial features from the RGB images generated from EEG data.
   - **Accuracy:** 76%

3. **ResNet (Residual Network)**
   - A deep residual network (ResNet50) known for its ability to handle vanishing gradient problems.
   - **Accuracy:** 47%

4. **Autoencoder**
   - An encoder-decoder model that learns compressed representations of the EEG data for classification.
   - **Accuracy:** 100%

## Project Structure
- `code/`: Contains the code for data preprocessing and model training.
  - `models/`: Code for the various machine learning models (Base model, CNN, ResNet, Autoencoder).
  - `data_preparation/`: Scripts for cleaning, transforming, and splitting the EEG dataset.
- `data/`: Placeholder for the dataset files (Please place the EEG dataset here).
- `docs/`: Contains documentation and the project report in PDF format.
- `output/`: Placeholder for storing the results generated by the models.

## Setup and Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/genius-harry/Alcoholic-Addiction-Classification.git
    cd Alcoholic-Addiction-Classification
    ```

2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Download and place the EEG dataset in the `data/` directory.

4. Run the analysis:
    You can execute the individual model scripts located in the `code/models/` folder to train and evaluate the models.

## Results
The project achieved promising results, with the autoencoder model delivering perfect accuracy on the testing dataset. The confusion matrix and accuracy for each model provide insights into their performance, highlighting the strengths and weaknesses of different architectures in classifying EEG signals related to alcohol addiction.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Citation
If you use this project in your research, please cite:
```
@article{Yao2023AlcoholicAddictionEEG,
  title={Alcoholic Addiction Classification Using EEG},
  author={Yiran Yao},
  journal={December 2023}
}
```
