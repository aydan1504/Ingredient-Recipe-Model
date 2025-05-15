# Recipe Model AI

A lightweight recipe recommendation system based on ingredient list matching.  
This project uses NLP and TF-IDF vectorization to recommend the most relevant recipe from a large dataset based on user-inputted ingredients. Images are included for visualization, but the recommendation is fully text-based.

## Project Overview

The goal of this project is to recommend recipes by analyzing a short ingredient description from the user.  
We apply a simple retrieval-based approach that:
- Extracts key nouns (ingredients) from the user's input using spaCy
- Converts all recipes' ingredients into TF-IDF vectors
- Computes cosine similarity between the user input and the dataset
- Returns the top 5 matching recipes

Images are displayed using the CLIP-preprocessed dataset, but are not used for prediction.

## Technologies Used

- Python
- Google Colab
- Pandas, NumPy, Matplotlib, Seaborn
- Scikit-learn (TF-IDF, cosine similarity)
- spaCy (NLP-based ingredient extraction)
- Transformers (CLIP for optional image display)

## Dataset

We used the [Food Ingredients and Recipe Dataset with Images](https://www.kaggle.com/datasets/pes12017000148/food-ingredients-and-recipe-dataset-with-images) from Kaggle.  
It contains:
- 13,582 food images
- Recipe titles, ingredients, and cooking instructions

Only the text data is used for recommendation. Image paths are used for optional visualization.

## How to Run

1. Open the `RecipeModel2.ipynb` notebook in Google Colab.
2. Install dependencies and mount your Google Drive if needed.
3. Run all cells step by step:
   - Download and load the dataset
   - Preprocess the ingredient texts
   - Build the TF-IDF matrix
   - Enter a natural ingredient phrase (e.g., *"chicken, garlic, onion"*) to get top 5 similar recipes

## Contributors

- Aydan Aghakarimova  
- Rufat Isgandarli  

## License

This project is licensed under the MIT License.
