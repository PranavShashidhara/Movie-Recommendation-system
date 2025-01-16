# Movie Recommendation System Using Netflix Dataset

This project implements a movie recommendation system using the **Netflix Prize Dataset**. The focus is on applying **Collaborative Filtering** methods to provide personalized movie recommendations. The system includes both **User-User Collaborative Filtering** and **Movie-Movie Collaborative Filtering**. 

## Key Steps:
### 1. Data Preprocessing:
- Processed a dataset of 100 million records, focusing on 100 movies and 2000 users for analysis.
- Performed **Exploratory Data Analysis (EDA)** on a 10 million record sample and the full dataset.
- Preprocessed data stored in **Parquet format** on **Amazon S3**.

### 2. Data Transformation:
- Converted the dataset into efficient dictionaries for reduced time complexity:
  - `user2movie`: Maps users to the movies they rated.
  - `movie2user`: Maps movies to the users who rated them.
  - `usermovie2rating`: Maps user-movie pairs to their ratings.
  - `usermovie2rating_test`: Used for testing purposes.

### 3. Collaborative Filtering:
- Implemented **User-User Collaborative Filtering** using **Matrix Factorization** on a subset of 10 million records (1,000 users, 200 movies).
- **Movie-Movie Collaborative Filtering** was also applied using the same subset.

### 4. Advanced Models:
- Implemented a **Restricted Boltzmann Machine (RBM)** for enhancing recommendation accuracy.

## Performance Metrics:
### User-User Collaborative Filtering:
- **Mean Squared Error (MSE):**
  - Train MSE: 0.5854
  - Test MSE: 0.8420
- **Root Mean Squared Error (RMSE):**
  - Train RMSE: ~0.765
  - Test RMSE: ~0.917

### Comparison with Netflix Prize Benchmark:
- The baseline RMSE for the competition was 1.025, with the winning RMSE target around 0.91.
- The model’s performance is close to the benchmark, demonstrating the robustness of the approach, especially on the test set.

## Tools and Technologies:
- **Big Data Processing:** PySpark, Databricks
- **Storage:** Amazon S3
- **Libraries Used:**
  - Python
  - `pyspark`, `numpy`, `pandas`
- **Modeling Techniques:**
  - User-User Collaborative Filtering
  - Movie-Movie Collaborative Filtering
  - Matrix Factorization
  - Restricted Boltzmann Machine (RBM)

## Conclusion:
This project successfully demonstrated the effectiveness of **User-User Collaborative Filtering** and **Movie-Movie Collaborative Filtering**. These methods produced promising results, with RMSE values closely aligned to the Netflix Prize benchmark. Although the other models (Bayesian Matrix Factorization and RBM) were developed for future refinement, the primary focus was on achieving strong performance in the collaborative filtering techniques. Further experimentation and optimization could help improve the models and expand the dataset for better scalability.


## Sources:
- [Netflix Prize Dataset](https://www.kaggle.com/datasets/netflix-inc/netflix-prize-data)
- [Netflix Prize Benchmark Scores](https://en.wikipedia.org/wiki/Netflix_Prize)
