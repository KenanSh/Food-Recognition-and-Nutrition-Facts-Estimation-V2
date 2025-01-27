# Recipes5K Dataset Preprocessing
The Recipes5K dataset is a collection of recipes with corresponding images and ingredient lists, specifically designed for ingredients recognition tasks. 

## Dataset
- **Source:** [Recipes5k](http://www.ub.edu/cvub/recipes5k/)
- **Description:** The dataset contains 4,826 unique recipes, each consisting of an image and a list of ingredients. It covers a variety of dishes representing alternative ways to prepare the 101 food categories from the Food-101 dataset.
- **Images:** 4,826 images (one per recipe)
- **Ingredients:** 3,213 unique ingredients (on average 10 ingredients per recipe)
- **Food Categories:** 101 (aligned with Food-101)

## Data Organization
After downloading the Recipes5K dataset, extract the contents into the project directory. The expected directory structure should be:
```
project_directory/Food Datasets/Recipes5k
├── annotations/
├── images/
├── ingredients_simplification/  
├── preprocess_recipes5k.ipynb  # Script for preprocessing this dataset (refer to project README for order)
└── README.md
```

**Important Note**

Similar to the Food-101 preprocessing script, preprocess_recipes5k.ipynb might rely on other datasets being preprocessed first. Refer to the main project README.md file for the overall preprocessing order before running this script.