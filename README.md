# Plant Leaf Classification with ResNet 🌱

## Project Overview 📋

This project aims to classify images of plant leaves, particularly potato leaves, using a deep learning model based on the ResNet architecture. The model is designed to be robust and efficient, utilizing residual convolutional blocks to capture complex features within the images.

## Table of Contents 📑

- [Project Overview](#project-overview-📋)
- [Installation](#installation-🛠️)
- [Data Preprocessing](#data-preprocessing-🖼️)
- [Model Architecture](#model-architecture-🏗️)
- [Training](#training-🏋️)
- [Results](#results-📊)
- [Contributors](#contributors-🤝)

## Installation 🛠️

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/username/plant-leaf-classification.git
   cd plant-leaf-classification
   ```

2. **Install Dependencies**:
   Ensure Python is installed (version 3.7 or later). Then, install the required packages:

   ```bash
   pip install -r requirements.txt
   ```

3. **Directory Structure**:
   Make sure your image directory structure is as follows:

   ```
   /Data
   ├── TrainData
   │   ├── Class1
   │   ├── Class2
   │   └── ...
   └── TestData
       ├── Class1
       ├── Class2
       └── ...
   ```

## Data Preprocessing 🖼️

- **Image Loading**:
  The script uses `os.walk` to traverse the dataset directory, loading images from each subfolder corresponding to a class. Images are resized to 64x64 pixels to ensure uniformity.
- **Normalization**:
  Images are normalized to have a mean of 0 and a standard deviation of 1, stabilizing the learning process.
- **Visualization**:
  Use the `plot_images` function to visualize sample images from the dataset.

## Model Architecture 🏗️

The model architecture is based on ResNet and includes the following components:

- **ResNet Blocks**: These blocks enable the model to train more efficiently by allowing information to pass between layers through residual connections.
- **Global Pooling**: Global pooling reduces each feature map to a single value, which helps prevent overfitting and reduces the number of parameters.

The model is compiled with the Adam optimizer and the `categorical_crossentropy` loss function, optimized for multi-class classification.

## Training 🏋️

The model is trained for 100 epochs with a batch size of 64:

- **Training Data**: Preprocessed and normalized images are used for training.
- **Model Saving**: After training, the model is saved as `ResNet_model_groupe_2.h5`.

To train the model, simply run the script:

```bash
python train_model.py
```

## Results 📊

The model is evaluated based on accuracy, with performance measured over several trials:

- The results show an average accuracy of **84.90%** across 10 tests.

## Contributors 🤝

This project was developed by:

- **ISSA IBRAHIM Moubarak**
