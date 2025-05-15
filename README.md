# Recipe Model AI

A lightweight recipe recommendation system based on ingredient list matching.  
This project uses NLP and TF-IDF vectorization to recommend the most relevant recipe from a large dataset based on user-inputted ingredients.

## 🔗 Open in Colab

[Click here to open the notebook in Google Colab](https://drive.google.com/file/d/1AXmVKzj-bgBVhC_yJmQCTWsb8KXa_DxD/view?usp=sharing)

## Project Overview

The goal of this project is to recommend recipes by analyzing a short ingredient description from the user.  
We apply a simple retrieval-based approach that:
- Extracts key nouns (ingredients) from the user's input using spaCy
- Converts all recipes' ingredients into TF-IDF vectors
- Computes cosine similarity between the user input and the dataset
- Returns the top 5 matching recipes

This method is lightweight, fast, and does not require any training or deep learning.

## Technologies Used

- Python
- Google Colab
- Pandas, NumPy, Matplotlib, Seaborn
- Scikit-learn (TF-IDF, cosine similarity)
- spaCy (for ingredient extraction)

## Dataset

We used the [Food Ingredients and Recipe Dataset with Images](https://www.kaggle.com/datasets/pes12017000148/food-ingredients-and-recipe-dataset-with-images) from Kaggle.  
Although the dataset includes images, **only the text data** (ingredients, titles, instructions) was used in this project.

- 13,582 food entries
- CSV format with structured recipe information

## How to Run

1. Open the notebook in Google Colab using the link above.
2. Run all cells step by step:
   - Load and preprocess the ingredient texts
   - Vectorize recipes using TF-IDF
   - Enter an ingredient phrase (e.g., `"chicken, garlic, onion"`)
3. The system returns the top 5 most similar recipes from the dataset.

## Contributors

- Aydan Aghakarimova  
- Rufat Isgandarli  

## License

This project is licensed under the MIT License.
