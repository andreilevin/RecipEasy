# RecipEasy: A Content-Based Recipe Recommender 

### 	 Project Presentation [Slides](https://github.com/andreilevin/RecipEasy/blob/main/AndreiPresentation.pdf) | [Video](https://youtu.be/dnke4mA-c6c):

[![Watch the video:](https://raw.githubusercontent.com/andreilevin/RecipEasy/main/youtube_screen.jpg)](https://youtu.be/dnke4mA-c6c)

## Summary

The goal of this project was to use natural language processing techniques to create a recipe recommendation engine based on a user-submitted list of ingredients.   To build the recommender, I first scraped ~17,000 recipe webpages from [Food.com](https://www.food.com/);  in the interest of recommending only excellent recipes, I then filtered this dataset to keep only the ~6,000 recipes having at least 4 reviews and a minimum average rating of 4 out of 5 stars.  For each recipe, I tokenized and vectorized its ingredient list in a novel "noun-adjacent" way (described in the [presentation slides](https://github.com/andreilevin/RecipEasy/blob/main/AndreiPresentation.pdf) and in the [recipes-modeling](https://github.com/andreilevin/RecipEasy/blob/main/recipes-modeling.ipynb) notebook) and built a topic model using Non-negative Matrix Factorization (NMF).  I used cosine similarity as the pairwise recipe comparison metric. 

In the future, this recommender can be deployed to a web app via Streamlit or Heroku, and additional recipe content besides the ingredients list can also be incorporated— for example, the user could select the cuisine or type of dish (appetizer, main course, dessert, etc.), and filter recipes by ease of preparation (determined by number of steps and cooking time), and/or cooking techniques employed.

## Tools

- BeautifulSoup for web scraping
- Pandas and NumPy for data exploration, cleaning, transformation and analysis
- SpaCy for part-of-speech tagging of ingredients
- NLTK and scikit-learn for tokenization, vectorization and modeling 
