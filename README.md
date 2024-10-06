# Recipe-Visualization-Application

## Overview
This project analyzes the **EpiRecipes** dataset, which contains thousands of recipes along with their ratings, ingredients, and nutritional information. The analysis focuses on understanding trends, relationships, and outliers in the dataset, providing key insights into recipe types, dietary preferences, and more. The project includes data cleaning, feature engineering, and several exploratory data analysis (EDA) tasks.

## Dataset
The dataset used in this project is sourced from Kaggle: [EpiRecipes Dataset](https://www.kaggle.com/datasets/hugodarwood/epirecipes). It contains various columns such as recipe title, ratings, calories, protein, fat, sodium, ingredients, and tags like meal types, cooking methods, and regions.

### Downloading the Dataset
To replicate this project, the dataset can be downloaded directly from Kaggle using the Kaggle API.

#### Steps to Download:
1. Go to your [Kaggle Account](https://www.kaggle.com/account).
2. Scroll down to the **API** section and click **Create New API Token**. A `kaggle.json` file will be downloaded.
3. Upload the `kaggle.json` file to your project directory and run the following commands:

```bash
pip install kaggle
mkdir -p ~/.kaggle
cp kaggle.json ~/.kaggle/
chmod 600 ~/.kaggle/kaggle.json
kaggle datasets download -d hugodarwood/epirecipes
unzip epirecipes.zip
```
## Project Structure

### 1. Data Cleaning and Preprocessing
- Handled missing values in important columns like calories, protein, fat, and sodium.
- Removed duplicate rows to ensure unique recipes.
- Standardized text columns by converting them to lowercase.
- Applied Winsorization to handle outliers in nutritional columns.

### 2. Feature Engineering and Categorization
The dataset's 680 columns were categorized into:
- **Recipe Information**: Titles, ratings, and nutritional data.
- **Ingredients**: A comprehensive list of all ingredients.
- **Meal Types**: Categories such as breakfast, lunch, dinner, and snacks.
- **Cooking Methods/Tools**: Includes methods like bake, grill, fry, and tools like blender.
- **Tags/Occasions**: Dietary tags and event-specific tags (e.g., Christmas, low-carb).
- **Regions**: Locations associated with recipes (e.g., California, Japan).

### 3. Exploratory Data Analysis (EDA)
Tasks performed:
- **Highly Rated Recipes**: Top-rated recipes for specific occasions like Christmas.
- **Low Nutrition, High Rating**: Recipes low in calories or fat but highly rated.
- **Quick High-Protein Recipes**: Quick meals that are both highly rated and protein-rich.

## Project Highlights
- Data cleaning with outlier handling and imputation.
- Extensive exploratory data analysis (EDA) with visualizations.
- Recipe recommendations based on analysis of nutritional and rating data.

## Conclusion
This project provides a thorough analysis of the EpiRecipes dataset, delivering insights into recipe ratings, ingredient patterns, and nutritional content. These insights can be leveraged to enhance recipe platforms by offering better recommendations and improving user experience.

