# Movie Recommendation System: Project Overview
This project aims to build a movie recommendation system using content-based filtering and collaborative filtering techniques. The script uses the Sentence Transformers library for content-based filtering and the Surprise library for collaborative filtering.

## Installation
To run this script, install the dependencies using following command:
```bash
pip install -r requirements.txt
```
Install PyTorch using their [configurator](https://pytorch.org/get-started/locally/).
```bash
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
```
## Dataset
To proceed with the project, please download the dataset from the following link: [The Movie Dataset](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset).

## How it works
The script first cleans and preprocesses the movie metadata, keywords, and ratings data. It then builds a content-based filtering system by creating a "soup" of text that includes the genres, original language, overview, tagline, keywords, and production countries for each movie. The text is encoded using a pre-trained sentence transformer model, and cosine similarity is used to find similar movies based on the encoded text.

For collaborative filtering, the script uses the Surprise library to build a matrix factorization-based model. It trains the model using the ratings data and predicts ratings for a given user and movie.

The script also includes a hybrid recommender system that combines the content-based and collaborative filtering recommendations. It provides movie recommendations based on both the similarity of the selected movie and the predicted user ratings.

## Hugging Face Spaces

The trained movie recommendation model is hosted on Hugging Face Spaces. You can access the model and interact with it using the following link:
[Movie Recommendation Model on Hugging Face Spaces](https://huggingface.co/spaces/Gary0417/movie-recommendation-system)

![Movie Recommendation System](images/movie-recommendation-system.png)