# Food-101 Dataset Preprocessing
The Food-101 dataset is a popular benchmark for food image recognition tasks. It contains a total of 101,000 images categorized into 101 different food classes. Each class consists of 750 training images and 250 test images. Here's a breakdown of the key aspects of this 

## dataset:
- **Source:** Food-101 dataset
- **Description:** The dataset consists of images of various food items belonging to 101 categories.
- **Images:** 101,000 total images (750 training images and 250 test images per category)
- **Classes:** 101 (e.g., pizza, apple, hamburger)
**Note:** The labels for the test set images are manually cleaned, while the training set may contain some noise.

## Data Organization
After downloading the Food-101 dataset, you should extract the contents into the project directory. The expected directory structure should look like this:

```
project_directory/Food Datasets/food-101
├── images/
├── meta/
├── preprocess_food101.ipynb  # Script for preprocessing this dataset (refer to project README for order)
└── README.md
```

**Important Note**

The preprocessing script for this dataset **(preprocess_food101.ipynb)** relies on other datasets being preprocessed first in a specific order. Please refer to the main project explanation file for the overall preprocessing order before running this script.

By following these guidelines, you'll have the Food-101 dataset prepared for use within your food recognition and nutrition facts estimation project.