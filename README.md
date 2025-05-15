# Recipe Model AI

A lightweight recipe recommendation system based on ingredient list matching.  
This project uses TF-IDF vectorization and cosine similarity to suggest the most relevant recipe from a large dataset, based only on text input — no training or image input required.

## Project Overview

The goal of this project is to recommend recipes by analyzing a user-provided list of ingredients.  
We apply a simple retrieval-based approach that:
- Vectorizes ingredient lists using TF-IDF
- Compares them against a recipe dataset
- Returns the most similar recipe based on cosine similarity

No training or fine-tuning is needed, making this method fast and efficient.

## Technologies Used

- Python
- Google Colab
- Scikit-learn (TF-IDF, cosine similarity)
- Pandas, NumPy

## Dataset

We used the [Food Ingredients and Recipe Dataset with Images](https://www.kaggle.com/datasets/pes12017000148/food-ingredients-and-recipe-dataset-with-images) from Kaggle.  
Although the dataset contains images, this project only uses the **textual recipe information**, including:
- 13,582 ingredient lists
- Recipe titles and cooking instructions

## How to Run

1. Open the `RecipeModel2.ipynb` notebook in Google Colab.
2. Upload the Kaggle dataset files to your Drive (JSON format).
3. Run the notebook step by step:
   - Load and preprocess ingredients
   - Vectorize inputs using TF-IDF
   - Compute cosine similarity
   - Return the closest-matching recipe

## Evaluation

We evaluated the system manually by checking if the returned recipes matched the given ingredients.  
It performed well in most cases, especially for common or specific ingredient combinations.

## Contributors

- Aydan Aghakarimova  
- Rufat Isgandarli  

## License

This project is licensed under the MIT License.
