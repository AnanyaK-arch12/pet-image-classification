# Pet Breed Classification Using ResNet50

A deep learning project that uses **Transfer Learning with ResNet50** to classify images of cats and dogs into 16 different categories.

The project uses a pretrained convolutional neural network to extract image features and classify pet breeds. It demonstrates image preprocessing, data augmentation, model training, and performance evaluation using TensorFlow and Keras.

## Project Overview

Identifying different pet breeds from images can be challenging because many breeds have similar visual characteristics.

This project explores how transfer learning can be used to classify pet images by adapting a pretrained ResNet50 model to a 16-class classification task.

## Features

* Classification of 16 cat and dog categories.
* Transfer learning using pretrained ResNet50.
* Image resizing and preprocessing.
* Data augmentation using random flipping and rotation.
* Training and validation performance visualization.
* Evaluation using a separate test split.
* Prediction on pet images.

## Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Matplotlib
* Jupyter Notebook

## Model Architecture

The project uses ResNet50, a deep convolutional neural network pretrained on ImageNet.

The implementation:

* Loads ResNet50 with pretrained ImageNet weights.
* Freezes the pretrained base layers.
* Uses the extracted image features for classification.
* Trains the classification layers for the 16 pet categories.

## Dataset

The project uses a local image dataset containing 16 categories of cat and dog breeds.

**Important:** The dataset is not included in this GitHub repository because of its large size.

To run the notebook, you must obtain the same dataset used by the project and place it in the expected local directory.

The notebook expects the image folder at:

```text
./images
```

Make sure the dataset's folder structure and class names match the notebook's data-loading code.

## Data Preprocessing and Augmentation

The notebook applies the following steps:

* Resizes images to 224 × 224 pixels.
* Prepares images for the ResNet50 model.
* Applies random flipping and rotation for data augmentation.
* Splits the dataset into training, validation, and testing subsets.

### Dataset Split

| Subset     | Percentage |
| ---------- | ---------: |
| Training   |        60% |
| Validation |        20% |
| Testing    |        20% |

## Training Configuration

| Parameter          | Value     |
| ------------------ | --------- |
| Model              | ResNet50  |
| Pretrained weights | ImageNet  |
| Input image size   | 224 × 224 |
| Number of classes  | 16        |
| Optimizer          | Adam      |
| Epochs             | 10        |

## Project Structure

```text
pet-image-classification/
│
├── pet classifier.ipynb
├── .gitignore
├── README.md
│
└── images/                 # Not included in this repository
    ├── class_1/
    ├── class_2/
    └── ...
```

The folder names above illustrate the expected organization. Use the actual class folder names and structure required by the notebook.

## How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/AnanyaK-arch12/pet-image-classification.git
cd pet-image-classification
```

### 2. Create a virtual environment (optional but recommended)

```bash
python -m venv venv
```

Activate it on Windows:

```powershell
venv\Scripts\activate
```

### 3. Install the dependencies

```bash
pip install tensorflow numpy matplotlib pillow jupyter
```

If the notebook uses additional libraries, install them as required.

### 4. Add the dataset

Obtain the dataset used by the project separately.

Create the `images` folder in the repository directory and organize the images into the class folders expected by the notebook.

The dataset is not automatically downloaded by this project.

### 5. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 6. Run the notebook

Open `pet classifier.ipynb`.

Run the notebook cells in order, ensuring that the dataset is correctly placed before executing the data-loading and training cells.

## Model Evaluation

The notebook evaluates the trained model using a separate test split and includes visualizations of training and validation performance.

Actual accuracy and loss values can be added here after confirming the results from a completed run.

## Learning Outcomes

This project provided practical experience with:

* Transfer learning.
* Pretrained CNN architectures.
* Image classification.
* Image preprocessing and augmentation.
* Training and validation workflows.
* Model evaluation and visualization.

## Future Improvements

* Experiment with fine-tuning selected ResNet50 layers.
* Compare performance with other pretrained architectures.
* Improve classification performance through hyperparameter tuning.
* Add a simple interface for uploading and classifying pet images.
* Evaluate model performance across individual breed categories.

---

**Author:** Ananya K.
**Project:** Pet Breed Classification Using ResNet50
