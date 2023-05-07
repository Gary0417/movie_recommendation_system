# Movie Recommendation System: Project Overview
This project aims to build a movie recommendation system using content-based filtering and collaborative filtering techniques. The script uses the Sentence Transformers library for content-based filtering and the Surprise library for collaborative filtering.

## Dependencies
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

The script also includes a hybrid recommender system that combines the content-based and collaborative filtering recommendations. It provides movie recommendations based on both the similarity of the selected movie and the ratings of other users.

## Limitations
- The script assumes that the movie metadata, keywords, and ratings data are available in the specified format. You may need to modify the code if your data is structured differently.
- The script uses a pre-trained sentence transformer model for content-based filtering. If you want to use a different model or train your own, you will need to make the necessary modifications.
- The collaborative filtering model used in the script is a basic matrix factorization model. You may want to explore more advanced algorithms for better performance.
- The recommendations provided by the script are based solely on the movie data and user ratings. Other factors, such as user preferences, movie popularity, and release date, are not taken into account.