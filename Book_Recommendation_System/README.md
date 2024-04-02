## Book Recommendation System

This project implements a book recommendation system using various techniques including content-based filtering, collaborative filtering, and a hybrid approach. It leverages machine learning models to provide personalized book recommendations based on user preferences and book features.

### Features:

1. **Data Preprocessing:**
   - Reads data from CSV files containing information about books and user ratings.
   - Preprocesses the data, including handling missing values, formatting author names, and normalizing text.

2. **Content-Based Filtering:**
   - Utilizes TF-IDF vectorization to analyze textual features such as book descriptions, titles, authors, and genres.
   - Computes cosine similarity to recommend books based on similarity in content.

3. **Collaborative Filtering:**
   - Constructs a user-item matrix from user ratings.
   - Trains a k-NN model to find similar books based on user-item interactions.

4. **Hybrid Model:**
   - Combines both content-based and collaborative filtering approaches to provide more diverse and accurate recommendations.

5. **Improvement with Popularity and Rating:**
   - Enhances content-based recommendations by considering popularity and rating factors.

### Usage:

The project offers functionalities to retrieve book recommendations either as JSON or directly as DataFrames.

Example usage:

```python
# Retrieve recommendations for a specific book
json_output = get_recommendations_as_json(book_id=13, model_type='improved', top_n=10)
recommended_books = json.loads(json_output)
```

### Dependencies:

- numpy
- pandas
- scikit-learn
- scipy

### Note:

Make sure to have the required datasets (`books_enriched.csv` and `ratings.csv`) available in the same directory or provide the appropriate paths for data loading.

For more details on implementation and usage, please refer to the code documentation and comments.
