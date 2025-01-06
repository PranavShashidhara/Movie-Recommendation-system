
## Project Overview
This project aims to build a movie recommendation system using the Netflix dataset. The primary focus is on implementing User-User Collaborative Filtering for personalized recommendations.

### Key Steps:
1. **Data Preprocessing**:
- Processed the entire dataset of 100 million records.
- Extracted data for 100 movies and 200 users for analysis.
- Completed Exploratory Data Analysis (EDA) on a sampled subset of 10 million records.
- Stored preprocessed data in **Parquet format** using Amazon S3.

2. **Data Transformation**:
- Converted the data into dictionaries for efficient access and reduced time complexity:
  - `user2movie`: Maps users to the movies they rated.
  - `movie2user`: Maps movies to the users who rated them.
  - `usermovie2rating`: Maps user-movie pairs to their ratings.
  - `usermovie2rating_test`: Similar mapping for testing purposes.

3. **Collaborative Filtering**:
- Implemented **User-User Collaborative Filtering using Matrix Factorization** on a subset of ~200,000 records.
- Subset includes 1,000 users and 200 movies.

4. **Ongoing Development**:
- Currently developing User-User Collaborative Filtering models using:
  - Bayesian Matrix Factorization.
- Building a **Restricted Boltzmann Machine (RBM)** for recommendations.

## Performance Metrics
### Results from User-User Collaborative Filtering:
- **Mean Squared Error (MSE):**
- Train MSE: 0.5854
- Test MSE: 0.8420

- **Root Mean Squared Error (RMSE):**
- Train RMSE: ~0.765
- Test RMSE: ~0.917

### Comparison with Netflix Prize Benchmark:
- The competition's baseline RMSE was approximately 1.025, and the winning target was 0.91.
- The model's performance demonstrates close alignment with the desired benchmark, especially for the test set.

## Tools and Technologies
- **Big Data Processing:** PySpark
- **Storage:** Amazon S3
- **Libraries:**
- Python
- `pyspark`
- `numpy`, `pandas`
- **Modeling Techniques:**
- User-User Collaborative Filtering
- Standard and Bayesian Matrix Factorization
- Restricted Boltzmann Machine (RBM)

## Sources
- [Netflix Prize Dataset](https://www.kaggle.com/datasets/netflix-inc/netflix-prize-data)
- [Netflix Prize Benchmark Scores](https://en.wikipedia.org/wiki/Netflix_Prize)

## Conclusion
This project demonstrates an effective implementation of a User-User Collaborative Filtering-based recommendation system. The results closely align with the benchmark values from the Netflix Prize competition, validating the robustness of the approach. Further experimentation with larger datasets and advanced models like RBM and Bayesian Matrix Factorization can potentially improve performance.
