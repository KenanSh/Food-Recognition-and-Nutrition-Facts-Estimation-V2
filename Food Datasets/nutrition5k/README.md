# Nutrition5K Dataset Preprocessing
The Nutrition5K dataset provides a rich collection of visual and nutritional data for real-world food samples.

## Dataset
- Source: [nutrition5k](https://github.com/google-research-datasets/Nutrition5k)
- Description: The dataset consists of data for 5,006 plates of food captured from Google cafeterias. 
Each plate includes:
    - Visual data:
        - 4 rotating side-angle videos
        - Overhead RGB-D images
    - Nutritional data:
        - Fine-grained list of ingredients
        - Per-ingredient mass
        - Total dish mass and calories
        - Fat, protein, and carbohydrate macronutrient masses

## Data Organization

After downloading the Nutrition5K dataset (if publicly available), extract the contents into the project directory. The expected directory structure should be:
```
project_directory/Food Datasets/Recipes5k
├── dish_ids/  
├── imagery/  
├── metadata/ 
├── preprocess_nutrition5k.ipynb
└── README.md
```

**Important Note**

The preprocessing script for this dataset (preprocess_nutrition5k.ipynb) might rely on other datasets being preprocessed first. Refer to the main project README.md file for the overall preprocessing order before running this script.
