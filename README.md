# Masked Autoencoder (MAE) Reimplementation

This repository contains the code and the pre-trained models for the reimplementation of the famous MAE paper as part of the final project for 18-786 Introduction to Deep Learning at CMU. The MAE is an innovative unsupervised learning method for visual representation.

## Authors

Sunghwan Baek(sunghwab)

Shutian Chen (shutianc)

## Project Structure

- `MAE_code.ipynb`: Jupyter notebook containing the main code for our reimplementation of the MAE model. The notebook includes the following sections:
  - `Preparation`: Setting up the training environment & Select the appropriate hyperparameters following the original paper.
  - `Building MAE Pre-Training Pipeline`: Implementing Patchify, Masking, Vit Encoder, and Vit Decoder.
  - `Visualization of Patchify & Masking`: Visualizing the patchify and masking process.
  - `Pre-Training the MAE Encoder`: Training the MAE model using the pre-training pipeline for 10, 50, and 100 epochs.
  - `Utilize the Pre-Trained MAE Encoder in Classification`: Using the pre-trained MAE encoder for the downstream classification task, and comparing the performance with the baseline model.
  
- `pretrained_models/`: Directory containing pre-trained models & training losses for different epochs:
  - `10 epoch/`
  - `50 epoch/`
  - `100 epoch/` - Contains models trained for 100 epochs.(This is the final model we used for the downstream classification task)
    - `loss_data_100.csv`: CSV file with loss data for the 100 epochs.
    - `mae_pretrained_100.pth`: PyTorch model file for the MAE model (MAE encoder) trained for 100 epochs.

- `requirements.txt`: List of Python dependencies for the project.

## Installation

To set up the project environment:

1. Clone this repository to your local machine.
2. Install the required dependencies by running `pip install -r requirements.txt` in your terminal.
3. Open `MAE_code.ipynb` in Jupyter Notebook or JupyterLab to view the implementation.

## Usage

To use the pretrained models:

1. Navigate to the `pretrained_models/` directory.
2. Choose the model according to the number of epochs you are interested in.
3. Use the model file (e.g., `mae_pretrained_100.pth`) to load the pretrained weights into your MAE implementation.

In the `MAE_code.ipynb`, because we did all the training on Google Colab, we place & load all the mdoel files 
from Google Drive. If you want to run the code on your local machine, you need to change the path to the model files.

For training new models or reproducing the training process, follow the instructions outlined in `MAE_code.ipynb`.