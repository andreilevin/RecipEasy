# RecipEasy: A Content-Based Recipe Recommender 

### 	 Project Presentation [Slides](https://github.com/andreilevin/RecipEasy/blob/main/AndreiPresentation.pdf) | [Video](https://youtu.be/dnke4mA-c6c):

[![Watch the video:](https://raw.githubusercontent.com/andreilevin/RecipEasy/main/youtube_screen.jpg)](https://youtu.be/dnke4mA-c6c)

## Summary

The goal of this project was to use natural language processing techniques to create a recipe recommendation engine where the user submits a list of ingredients and the recommender outputs a few recipes the user can then make at home.   After scraping ~16,000 recipes from Food.com, in the interest of recommending only excellent recipes I then filtered this dataset to keep only the ~6,000 recipes having at least 4 reviews and an average rating of at least 4 out of 5 stars.  For each recipe, I tokenized and vectorized its ingredient list in a novel "noun-adjacent" way (described in more detail  in the [presentation slides](https://github.com/andreilevin/RecipEasy/blob/main/AndreiPresentation.pdf) and in the [recipes-modeling](https://github.com/andreilevin/RecipEasy/blob/main/recipes-modeling.ipynb) notebook) and built a topic model using Non-negative Matrix Factorization (NMF).  I used cosine similarity as the pairwise recipe ingredient comparison metric. 

In the future, this recommender can be deployed to a web app such as Streamlit, and additional recipe content can also be incorporated— for example, the user can select the cuisine or type of dish (appetizer, main course, dessert, etc.), and filter recipes by ease of preparation (determined by number of steps and cooking time), and/or cooking techniques employed.

## Tools

- BeautifulSoup for web scraping
- Pandas and NumPy for data exploration, cleaning, transformation and analysis
- SpaCy for part-of-speech tagging of ingredients
- NLTK and Scikit-learn for tokenization, vectorization and modeling 
