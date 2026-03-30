# Arabic-Handwritten-Characters-Generator
This project is about generating realistic images of Arabic hand-written characters using a Generative Adversarial Network (GAN). Specifically, a Deep Convolutional GAN (DCGAN) was implemented to learn from the dataset of handwritten character images and generate new synthetic images. This project aims to understand and apply deep learning concepts and to observe how adversarial training enables realistic image generation.

## How to Run (Jupyter Notebook)
1. Navigate to your desired directory, then clone this repository  
```
git clone https://github.com/AsmaaMesbah/Arabic-Handwritten-Characters-Generator.git
```
2. Navigate to the notebook directory  
```
cd ./Arabic-Handwritten-Characters-Generator/notebook
```
3. Open the notebook
```
jupyter notebook arabic-handwritten-characters-generator.ipynb
```
## How to Run (Google Colab)
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AsmaaMesbah/Arabic-Handwritten-Characters-Generator/blob/main/notebook/arabic-handwritten-characters-generator.ipynb)

## Dataset
### Description
This project uses the **Arabic Handwritten Characters Dataset** to train a generative model (DCGAN) for producing synthetic handwritten Arabic characters.

The dataset contains grayscale images of handwritten Arabic letters collected from multiple writers. Although the dataset includes labels for classification tasks, only the image data was used in this project for generative modeling.

### Dataset Overview
- Total images: **13,440**
- Image type: **Grayscale**
- Original resolution: **32 × 32 pixels**
- Number of classes: **28 Arabic characters**
- Format used: **MATLAB (.mat)**

### Source
The dataset was created by **Mohamed Loey** and is available on [Kaggle](https://www.kaggle.com/datasets/mloey1/ahcd1).

### Preprocessing
The following preprocessing steps were applied before training:

- Loaded `.mat` dataset into Python
- Extracted image data (labels were ignored)
- Resized images from **32×32 → 64×64**
- Normalized pixel values to **[-1, 1]** to match GAN training requirements
- Converted data into PyTorch tensors
- Organized into batches using a DataLoader

### Usage in This Project
The dataset is used to train a **Deep Convolutional GAN (DCGAN)**:
- Real images are used as input for the discriminator
- Random noise is used by the generator to produce synthetic handwritten characters
- The model learns to generate realistic Arabic character images through adversarial training

... TBC
