# RecipEasy: A Content-Based Recipe Recommender 

The goal of this project was to create a recipe recommender, where the user can input a list of ingredients, and the recommender would output a few recipes they can make at home. 

## Design and Data

I scraped ~16,000 recipes from Food.com, saving the following information to a csv file:  title, url, ingredients, total cooking time, number of steps (as another proxy for complexity), number of user reviews, and average user rating (out of 5 stars).  To build my model, I filtered this data to restrict the recipes to those having at least 4 reviews and an average rating of at least 4/5 stars.  This left me with a higher-quality subset of ~6,000 recipes that I could use in my recommender system.   For each recipe, I vectorized its ingredient list (as described in much more detail the "recipes-modeling" notebook and in the powerpoint presentation located on this page) and built a topic model using Non-negative Matrix Factorization (NMF).  Cosine similarity was used as the pairwise recipe ingredient comparison metric. 

## Tools and Algorithms

- Beautifulsoup for scraping
- Pandas and Numpy for data exploration, cleaning, transformation and analysis
- Spacy for part-of-speech tagging
- Nltk and Sklearn for tokenization, vectorization and modeling 

