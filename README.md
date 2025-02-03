# Food Ingredients Recognition and Calorie Estimation using Multi-Task Deep Learning

This project tackles the challenges of food image recognition and calorie estimation using a multi-task deep learning approach. The model aims to:

- Recognize food ingredients from a given image.
- Estimate the calorie content of the food item in the image.
- By combining these tasks, the model leverages the relationship between ingredients and calories to improve its overall accuracy.

## Installation

### Prerequisites
- Git installed on your system.
- [Anaconda](https://www.anaconda.com/products/distribution)

### Steps
1. Clone the repository:
```bash
git clone https://github.com/KenanSh/Food-Recognition-and-Nutrition-Facts-Estimation-V2.git
```

2. Create and activate the conda environment:
```bash
cd Food-Recognition-and-Nutrition-Facts-Estimation-V2
conda env create -f environment.yml
```

3. Activate the environment:
```bash
conda activate food_calories
```

**(Optional) Set up GPU Support:**
If you have a GPU and want to leverage it for faster training, you'll need to install the following:

- **CUDA Toolkit 11.2:** Follow the official NVIDIA CUDA Toolkit installation guide (https://developer.nvidia.com/cuda-downloads).
- **cuDNN SDK 8.1.0:** Download and install cuDNN from NVIDIA's website (https://developer.nvidia.com/cudnn).
- **Alternatively,** you can refer to the TensorFlow documentation for GPU setup (https://www.tensorflow.org/install/gpu).

## Usage
This section provides a high-level overview of the project's directory structure and key functionalities.

### Directory Structure
`Food Datasets:` This directory stores various datasets used in the project. Each dataset folder includes a README file with download instructions, preprocessing steps, and a script for preprocessing the data. The final-dataset folder contains the preprocessed data used for model training.
`Ingredient Embeddings:` This directory (if applicable) houses code for generating text embeddings to compare ingredient similarity. This can be used to impute missing nutritional information for ingredients.
`main:` This directory contains the core scripts for building and training the model:
`build_model.ipynb:` The main Jupyter Notebook for defining, building, and training the deep learning models.
`data_pipeline.ipynb:` A prerequisite script that serializes all datasets into TFRecord files for efficient data feeding into the model during training (executed before build_model.ipynb).


### Results 
The table below provides a template for recording key metrics:

| #  | Experiment Name           | Description                                         | Epochs | Food category precision | Food ingredients precision | Calorie MAE | Carbs MAE | Protein MAE | Fat MAE |
|----|---------------------------|-----------------------------------------------------|--------|-------------------------|----------------------------|-------------|-----------|-------------|---------|
| 1  | flat_efficientnetB1       | Final Ingredients                                  | 5      | 1.0                     | 0.84                       | 0.28        | 0.03      | 0.02        | 0.03    |
|    |                           | Final Category with transfer learning from ingredients | 5      | 0.83                    | 0.78                       | 0.5         | 0.06      | 0.02        | 0.05    |
|    |                           | Final Category without transfer learning from ingredients | 50     | 0.91                    | 0.87                       | 0.42        | 0.05      | 0.01        | 0.04    |
|    |                           | Fine Tune Final Category without transfer learning | 100    | 0.82                    | 0.87                       | 0.41        | 0.04      | 0.01        | 0.04    |
| 2  | MobileNetv3               | -                                                 | 2      | 1.0                     | 0.83                       | 0.31        | 0.04      | 0.03        | 0.03    |
| 3  | NASNet Mobile             | -                                                 | 10     | 0.78                    | 0.77                       | 0.52        | 0.06      | 0.02        | 0.05    |
| 4  | Wide Slice EfficientNetB1 | Final Category without Transfer learning          | 25     | 0.88                    | 0.86                       | 0.44        | 0.05      | 0.01        | 0.04    |
|    |                           | Fine Tune Final Category without Transfer learning | 20     | 0.92                    | 0.89                       | 0.41        | 0.05      | 0.01        | 0.04    |

**Note:** Results seem quite reasonable, especially considering potential resource limitations
