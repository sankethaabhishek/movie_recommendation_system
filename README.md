# Movie Recommendation System

## 🌟➡️👋🏽 Introduction
This project develops a basic movie recommendation system using the **MovieLens 25M dataset**. I used **Collaborative Filtering** techniques to recommend movies to users based on item-item similarity. Simply, this project build to suggest movies to users based on what they enjoy/like. The entire development process, from **Data Acquisition and Exploration** to **Model Implementation**, is tracked using Git and hosted on GitHub.

## 🎯📝 Goal of Project
The main goal of this project is to build a recommendation system that able to:
* Load and preprocess movie and rating data.
* Identify relationships between movies based on user ratings.
* Provide personalized movie recommendations to users.

## 📝💻 Dataset Used
I used **MovieLens 25M Dataset (ml-latest-small)** for this project, which contains:
* **movies.csv:** Movie IDs, titles, and genres.
* **ratings.csv:** User IDs, movie IDs, ratings, and timestamps.

This dataset is useful for demonstrating collaborative filtering techniques because it includes explict rating information.

## 🛠️⚙️ Technologies and Libraries Used
* **Python**
* **Pandas:** For data manipulation and analysis.
* **NumPy:** For numerical operations.
* **Matplotlib:** For basic data visualization.
* **Seaborn:** For enhanced statistical data visualization.
* **Jupyter Notebook:** For interactive develpment and analysis.
* **Git and GitHub:** For version control and collaborative development.

## ⭐️✨ Key Features
This project implements a basic **Item-Based Collaborative Filtering** approach, which includes:
* **Data Loading & Preprocessing:** Efficiently loading movie and rating data.
* **User-Item Matrix Creation:** Pivoting the data to represent user ratings for each movie.
* **Item Similarity Calculation:** Using Pearson correlation to find how similar movies are based on co-ratings.
* **Personalized Recommendations:** A function that suggests movies similar to one a user liked, while excluding movies they have already rated.

## 📊🔦💡 Data Exploration & Insights
Initial exploration revealed:
* **Dataset Size:** `movies.csv` contains 9742 movies, and `ratings.csv` contains 100836 ratings.
* **Missing Values:** No significant missing values were identified in key columns.
* **Rating Distribution:** Ratings are heavily skewed towards higher values (e.g., 3.0, 3.5, 4.0), indicating general user satisfaction.
* **Popular Genres:** Drama, Comedy, and Thriller are among the most prevalent genres.
* **User Activity:** Most users have rated a moderate number of movies, with a few highly active users.
* **Movie Popularity:** A small number of movies receive a vast majority of the ratings, while many movies are rarely rated.

## 🤖🔗 Recommendation System Logic
The system employs **Item-Based Collaborative Filtering**:
1.  **User-Item Matrix:** A matrix is constructed where rows represent users, columns represent movie titles, and values are the ratings. Unrated movies are `NaN`.
2.  **Item Similarity:** Pearson correlation is calculated between all pairs of movies. This measures how similarly users have rated any two given movies.
3.  **Personalized Recommendations:** To recommend for a user, the system identifies movies similar to one the user has highly rated. It then filters out movies the user has already seen to provide new suggestions.

## 🚀 How to Run Locally
Following guide is for set up and run this project on your local machine:

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/sankethaabhishek/movie_recommendation_system.git](https://github.com/sankethaabhishek/movie_recommendation_system.git)
    cd movie_recommendation_system
    ```

2.  **Download Dataset:**
    * Download the `ml-latest-small.zip` dataset from [MovieLens](https://grouplens.org/datasets/movielens/latest/).
    * Extract the contents of the `ml-latest-small` folder.
    * Copy `movies.csv` and `ratings.csv` (and any other `.csv` files like `links.csv`, `tags.csv` if they are present in your `data/raw` folder) into the `data/raw/` directory within your cloned repository.
        ```
        movie-recommendation-system/
        └── data/
            └── raw/
                ├── movies.csv
                └── ratings.csv
        ```

3.  **Set up Python Environment:**
    * Ensure you have [Anaconda](https://www.anaconda.com/products/distribution) or [Miniconda](https://docs.conda.io/en/latest/miniconda.html) installed.
    * Open your terminal and activate the base environment (or create a new one).
    * Install the required libraries:
        ```bash
        conda install jupyter pandas numpy matplotlib seaborn
        ```
        (If you prefer pip: `pip install jupyter pandas numpy matplotlib seaborn`)

4.  **Launch Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
    This will open the Jupyter interface in your web browser.

5.  **Explore the Notebooks:**
    * Navigate to the `notebooks/` folder in the Jupyter interface.
    * Open and run cells in `01_data_loading_and_initial_exploration.ipynb`, `02_data_exploration_and_cleaning.ipynb`, and `03_feature_engineering_and_basic_model.ipynb` sequentially to see the data loading, analysis, and recommendation logic in action.

## 🌱📈 Future Enhancements
Possible future improvements for this project include:
* Implementing more advanced collaborative filtering techniques (e.g., Matrix Factorization using SVD).
* Incorporating content-based features (e.g., movie genres, tags) to create a hybrid recommender.
* Addressing the "cold start" problem for new users/movies.
* Developing a user interface or API for the recommendation system.
* Conducting a more rigorous evaluation of recommendation performance using appropriate metrics.

## 🧑🏽‍🦱 Author
* **Sanketha Abhishek Waduge** - [GitHub Profile](https://github.com/sankethaabhishek)

Feel free to reach out if you have any questions or feedback!
