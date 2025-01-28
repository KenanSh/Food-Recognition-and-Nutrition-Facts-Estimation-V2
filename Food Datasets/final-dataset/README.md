# Final Dataset
This section describes the final dataset created by combining and preprocessing the individual datasets used in this project.

## Prerequisites
Downloaded and preprocessed all the individual datasets (Food-101, Recipes5K, USDA-FNDSS, Nutrition5K) according to their respective README instructions.

## Data Organization

The final dataset resides in the final-dataset directory and has the following structure:
```
project_directory/Food Datasets/final-dataset/
├── images/
│   ├── apple/  # Subdirectory containing images of apples (at least 100k)
│   ├── .../  # More subdirectories for each of the 101 food categories
│   └── yogurt/  # Subdirectory containing images of yogurts (at least 100k)
├── metadata/
│   ├── food101_nutrients.csv  # Food-101 nutritional data
│   ├── recipes5k_ingredients.csv  # Recipes5K ingredient data
│   ├── ...  # Separate CSV files for metadata from each dataset
│   └── nutrition5k_info.csv  # Nutrition5K nutritional information
├── tfrecord/  
│   ├── food101.tfrecord
│   ├── recipes5k.tfrecord
│   └── nutrition5k.tfrecord
└── README.md
```

**Description**

- `images`: This directory contains a subdirectory for each of the 101 food categories. Each subdirectory holds a collection of at least 100,000 images belonging to that specific food category.
- `metadata`: This directory stores the preprocessed metadata from the individual datasets in separate CSV files. These files contain information about the ingredients and nutritional content of the food items.
- `food101_nutrients.csv`: Stores nutritional data associated with Food-101 images.
recipes5k_ingredients.csv: Stores ingredient data for recipes in the Recipes5K dataset.
- `nutrition5k_info.csv`: Stores nutritional information for food items in the Nutrition5K dataset.
- `tfrecord`: This directory contains TFRecord files generated from the preprocessed Food-101, Recipes5K, and Nutrition5K data. These TFRecord files are a serialized format specifically designed for efficient training in machine learning models.

**Processing Steps**

Navigate to the directories containing the individual datasets (USDA-FNDSS, Recipes5K, Food-101, Nutrition5K) respectively and execute their preprocessing scripts as mentioned in their READMEs. This ensures each dataset is prepared for further processing.
After preprocessing all individual datasets, navigate to the main directory and execute `data_pipeline.ipynb`. This script is responsible for combining and processing the preprocessed data from the individual datasets into the final dataset structure described above.