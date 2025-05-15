# Recipe Model AI

A lightweight, retrieval-based recipe recommendation system that combines visual and textual features.  
It uses a pre-trained CLIP model to extract image embeddings and TF-IDF to vectorize ingredient lists, retrieving the most relevant recipe using cosine similarity — all without training or fine-tuning.

## Project Overview

The goal of this project is to recommend recipes based on a food image or a list of ingredients.  
We apply a simple yet effective approach that:
- Uses CLIP (ViT-B/32) to extract visual features from food images
- Uses TF-IDF to represent textual ingredients
- Calculates cosine similarity to match user input with existing recipes
- Returns the top match from a large recipe dataset

This system is fast, scalable, and requires no training.

## Technologies Used

- Python
- Google Colab
- OpenAI CLIP (via `CLIP` module)
- Scikit-learn (for TF-IDF and cosine similarity)
- NumPy, Pandas, Matplotlib

## Dataset

We used the [Food Ingredients and Recipe Dataset with Images](https://www.kaggle.com/datasets/pes12017000148/food-ingredients-and-recipe-dataset-with-images) from Kaggle, which contains:
- 13,582 food images
- Recipe titles, ingredient lists, and instructions in structured JSON format

This dataset was directly used in our Google Colab notebook for testing and evaluation.

## How to Run

1. Open the `RecipeModel.ipynb` notebook in Google Colab.
2. Mount your Google Drive and upload the dataset files as needed.
3. Run the notebook step by step to:
   - Extract visual and textual features
   - Compute similarities
   - Retrieve the most relevant recipe based on the input

## Evaluation

Since the dataset lacks ground-truth labels for retrieval, evaluation was conducted manually.  
The system achieved an approximate success rate of:
- **80%** for visual (image-based) queries  
- **75%** for textual (ingredient-based) queries  

## Contributors

- Aydan Aghakarimova  
- Rufat Isgandarli  

## License

This project is licensed under the MIT License.
