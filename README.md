# Movie Recommendation System

This project implements a movie recommendation system using collaborative filtering techniques. It leverages the MovieLens 100K dataset and employs Singular Value Decomposition (SVD) and cosine similarity to generate personalized movie recommendations for users. The project is implemented using a Jupyter notebook for ease of exploration and visualization.

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Overview

This movie recommendation system is designed to suggest movies to users based on their past ratings and the ratings of similar users. The project uses Python and several libraries including `pandas`, `scikit-learn`, and `requests`. The core algorithm is based on collaborative filtering using Truncated SVD for dimensionality reduction and cosine similarity for finding similar users. The implementation is done in a Jupyter notebook, making it easy to follow along and visualize the steps involved.

## Dataset

The project uses the [MovieLens 100K dataset](https://grouplens.org/datasets/movielens/100k/), which contains 100,000 ratings from 943 users on 1,682 movies. The dataset is well-suited for academic and learning purposes due to its manageable size and rich metadata.

## Project Structure

├── ml-100k/ # Extracted MovieLens dataset
├── Movie Recommendation System.ipynb # Jupyter notebook with the implementation
├── README.md # This README file
└── .ipynb_checkpoints/ # Jupyter notebook checkpoints (ignored)


## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/your-username/movie-recommendation-system.git
   cd movie-recommendation-system
   ```

2. **Install the required packages:**

	Ensure you have Python 3.7+ installed, then run:
	```bash
	pip install -r requirements.txt
	```
	
3. **Download the dataset:**

	The dataset is downloaded and extracted automatically when the Jupyter notebook is run.
	
## Usage
1. **Open the Jupyter Notebook:**
	Navigate to the project directory and launch Jupyter Notebook.
	
2. **Run the Notebook:**
	Execute the cells sequentially to load the dataset, preprocess the data, build the model, and generate recommendations.
	
## How It Works
The recommendation system operates as follows:

1. **Data Preprocessing:**

	The MovieLens dataset is loaded, and ratings and movies data are merged.
	A user-item matrix is created with users as rows, movie titles as columns, and ratings as values.

2. **Dimensionality Reduction:**
	Truncated SVD is applied to reduce the dimensionality of the user-item matrix, capturing the latent factors that explain the variation in user preferences.
	
3. **Similarity Calculation:**
	Cosine similarity is computed between users based on their latent factors, identifying users with similar preferences.
	
4. **Recommendation Generation:**
	For a given user, movies are recommended based on the ratings of the most similar users, excluding movies the user has already seen.
	
## Results
The system effectively recommends movies to users based on the preferences of similar users. Results can be customized by adjusting the number of SVD components or filtering based on certain criteria.
## License 
This project is licensed under the MIT License. See the LICENSE file for details.
