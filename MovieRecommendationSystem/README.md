# Content-Based-Movie-Recommender-System-with-sentiment-analysis-using-AJAX

![Python](https://img.shields.io/badge/Python-3.8-blueviolet)
![Framework](https://img.shields.io/badge/Framework-Flask-red)
![Frontend](https://img.shields.io/badge/Frontend-HTML/CSS/JS-green)
![API](https://img.shields.io/badge/API-TMDB-fcba03)

The Content-Based Recommender System suggests movies that are similar to the ones a user likes, while also analyzing the sentiments of reviews provided by the user for those movies.

Movie details such as title, genre, runtime, rating, and poster are retrieved through the TMDB API (https://www.themoviedb.org/documentation/api). Using the IMDb ID of the movie, I performed web scraping on the IMDb site with beautifulsoup4 to gather user reviews and then conducted sentiment analysis on those reviews.

## How to get the API key?

Create an account in https://www.themoviedb.org/, click on the `API` link from the left hand sidebar in your account settings and fill all the details to apply for API key. If you are asked for the website URL, just give "NA" if you don't have one. You will see the API key in your `API` sidebar once your request is approved.

## How to run the project?

1. Clone or download this repository to your local machine.
2. Install all the libraries mentioned in the [requirements.txt] file with the command `pip install -r requirements.txt`
3. Get your API key from https://www.themoviedb.org/. (Refer the above section on how to get the API key)
3. Replace YOUR_API_KEY in **both** the places (line no. 15 and 29) of `static/recommend.js` file and hit save.
4. Open your terminal/command prompt from your project directory and run the file `main.py` by executing the command `python main.py`.
5. Go to your browser and type `http://127.0.0.1:5000/` in the address bar.
6. Hurray! That's it.

## Similarity Score : 

   The system determines the most similar items to the ones a user likes using similarity scores, which are numerical values ranging from 0 to 1. These scores indicate how closely two items resemble each other, with 0 representing no similarity and 1 indicating identical items.

To calculate this similarity, the system compares the textual descriptions of the items, such as their title, genre, plot summary, and other relevant details. By evaluating the textual content of both items, it generates a similarity score based on how alike the descriptions are. This comparison is often done using a method known as cosine similarity.

Cosine similarity measures the angle between two vectors in a multidimensional space, where each vector represents the text of an item (e.g., using TF-IDF or word embeddings). If the angle between the vectors is small (i.e., the vectors point in the same direction), the cosine similarity score will be close to 1, meaning the items are very similar. Conversely, a larger angle results in a lower similarity score, indicating the items are less alike.

In summary, the similarity score is a numerical value that reflects the degree of similarity between the text descriptions of two items, with cosine similarity being a common method for calculating it. This helps the system recommend movies that are most like the ones a user enjoys.
   
## How Cosine Similarity works?
 Cosine similarity is a metric used to assess the similarity between two documents, regardless of their size. It calculates the cosine of the angle between two vectors in a multi-dimensional space. This method is beneficial because, even if two similar documents are far apart in terms of Euclidean distance (due to differences in document length), they may still be oriented closer together. In other words, documents with a smaller angle between their vectors will have a higher cosine similarity, indicating they are more similar.

### Sources of the datasets 

1. [IMDB 5000 Movie Dataset](https://www.kaggle.com/carolzhangdc/imdb-5000-movie-dataset)
2. [The Movies Dataset](https://www.kaggle.com/rounakbanik/the-movies-dataset)
3. [List of movies in 2018](https://en.wikipedia.org/wiki/List_of_American_films_of_2018)
4. [List of movies in 2019](https://en.wikipedia.org/wiki/List_of_American_films_of_2019)
5. [List of movies in 2020](https://en.wikipedia.org/wiki/List_of_American_films_of_2020)


