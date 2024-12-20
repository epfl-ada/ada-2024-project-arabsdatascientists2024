# Beyond Talent: Unveiling the Hidden Factors Behind an Actor's Success

## Abstract

It is safe to say that movies are part of our lives. Who hasn’t dreamed of being the star on the big screen? What if we told you we’ve cracked the code to becoming a successful actor? Sure, talent is essential, but could other factors—like physical attributes, social background, or the roles you play—hold the key to stardom? The film industry is a labyrinth of challenges, where countless dreamers compete, but only a select few rise to fame. In this exploration, we unveil the hidden factors that shape an actor's journey to success. After reading this, ask yourself: Do you have what it takes to shine? Would you dare to take your shot?

## Research Questions

- To what extent does the character played influence the public’s affection?
- Do an actor’s physical attributes, such as height or ethnicity, contribute to their success?
- How does an actor’s social background impact their career success?
- How can an actor’s success be assessed based on box office revenue and public ratings?
- Are actors more famous during their life or after their death?

## Proposed Additional Datasets (if any)

**CelebA :**  This dataset regroups more than 200K images of 10177 unique celebrities each described by 40 binary attributes. CelebA is very valuable for identifying which physical traits (heights, smile, hair color...) contributes to an actor's "success". We contacted the author of the dataset to have access to celebrities' name as they were missing in the public version.

**IMDB :** IMDb is probably the largest database collection related to movies. In the context of our project, it is extremelly useful to analyze the correlation between an actor popularity and box office revenues, movie ratings and reviews. It contains lots of crucial factors - audience feedback, sentiment analysis - which are worth exploring to answer our research question.

**RottenTomatoes :** This website is well known for providing informative reviews on movies, we can use both the audience score and certified critics to decide if a movie is worth being watched. By analyzing the scores from this dataset we gain further insights on how well an actor performs in a given movie.

**Oscars and Awards :** Oscars win and nomination are key indicators of an actor recognition and career achievment. It is the Motion Picture Academy members who get to vote and determine the winner, these professional opinions can change an actor's life and boost its career.

**BoxOfficeMojo :** BoxOfficeMojo is another dataset allowing to assess a movie performance. By looking at the life time gross and the rankings of movies between 1888 and 2016 (what we have in our original dataset) we gain additional success metrics.

**Metacritic :** This dataset aggregates "metascores" and "userscores" to rate a movie, based on the collection of millions of reviews. It allows us to assess how well movies are received by critics but also by the public which helps identify successful movies. It also contains some additionnal information about the movies, which helped us complete our plots for example.

**Webscrapping:**

* Completing missing values in already existign features : As a couple of important columns for our analysis are filled with NaN values. We decided to enrich and complete these columns with webscrapping. The webscrapping was done using a programmable search engine and the creation of our own API. With the help of these elements, we search for whatever the query is (e.g actor's height) and extract the information that corresponds to this query. As the code contains our API key, we will not publish it for security. However, the functions used are in a .py document savedd locally. **CE QUIL Y AVAIT AVANT, A MODIFIER !**
* Incorporating new features : First, we queried Wikidata for attributes like education and occupation, though we ultimately retained only these two from that source. Next, we scraped short biographies from Wikipedia and used sentence embeddings to infer nuanced categories such as socioeconomic background, education level, and early life opportunities. These categories were identified by comparing biography embeddings to representative phrase embeddings and selecting the closest semantic match. We dropped the original education attribute from Wikidata and the occupation attribute due to better, more specific data elsewhere. Finally, we kept all NLP-derived categories from the Wikipedia stage, as they provided more contextual richness.

## Methods

We will employ the methods we discovered in the course to analyze the datasets:

**Data visualization:** Using scatter plots, bar charts, and heatmaps to clearly represent tendencies.

**Correlation analysis:** to identify relationships between actor success and variables like physical attributes, movie genres, or roles.

**Regression Models:** Linear and logistic regression models to assess the impact of quantifiable traits (e.g., box office earnings, age).

**Classification Models:** Learning models to predict actor success based on input variables like physical attributes, roles, and social background. We could use classification or clustering if needed.

**NLP Models :**

* "all-MiniLM-L6-v2" model : (after webscrapping actors biographies we stated earlier) We used this transformer-based sentence embedding model known for its efficiency and strong performance to convert both our curated reference phrases and each actor’s biography into high-dimensional embedding vectors. We chose some categories and wrote their corresponding phrase embeddings and then computed cosine similarities between the biography embedding and each category’s representative phrase embeddings to quantify their semantic alignment.

**Clustering Models:** K-means and GMM (Gaussian Mixture Models)

* K-means :
* GMM : The goal is to identify meaningful clusters of actors based on various attributes. First, we adapted the dataset to our model needs. After trying several cluster counts, a moderate number of clusters (four) was chosen, considering both statistical criteria (like AIC/BIC) and the desire to avoid over-complicating the model. However, when examining these clusters, it became clear that they did not form distinctly interpretable groups. Neither a single attribute, such as Score_PCA_2_scaled, nor a combination of simple numeric or categorical features, created a clear pattern of separation. Visualizations showed substantial overlap among clusters. This suggests that the chosen features and approach did not yield easily distinguishable clusters (the data’s underlying structure may be too complex, or the selected features insufficient)..

**Deep Learnig Models:** MLP (Multi-Layer Perceptron), used with and without CelebA dataset.

* Without CelebA : We use a supervised learning approach to predict the transformed target (Score_PCA_2_scaled) by treating it as a classification task. Initially, the MLP’s performance metrics (accuracy, precision, recall, and F1-score) were modest. The class distribution was skewed, and the model struggled to achieve strong predictive results. After applying a logarithmic transformation to the target, which helped redistribute classes more evenly, the model’s performance improved well (from 35% to 71% test accuracy). MLP demonstrated the potential to extract more meaningful patterns when the target was reshaped.
* With CelebA : In an attempt to refine the model further, CelebA attributes (such as specific facial features) were integrated into the analysis. The hypothesis was that these additional characteristics might provide new, informative signals for predicting the transformed target. However, the incorporation of CelebA attributes did not lead to improved results, we have slightly worse results than the version without CelebA data (drop form 71% to 60% test accuracy). The model may have become more complex without gaining beneficial information, or these attributes may not correlate strongly with the target.

## Proposed Timeline

**Week 1:**

- Finalize web scraping: Based on TA feedback, complete web scraping to fill missing data (actor height, box office revenue, social background).

**Week 2:**

- Analyze individual parameters looking for independant factors contributing to an actor's success (visualize trends, run statistical tests, document findings), apply machine learning models(using clustering to group actors based on similar traits and success metrics, classification models to predict success based on analyzed parameters.)

**Week 3:**

- Identify combinations and interactions between parameters, run tests on combinations.
- Draft the data story's structure.

**Week 4:**

- Finalize results and data story, combine all results into a data story, finalize deliverables.

## Organization within the Team

- **Ali** : Webscrapping to incorporate new features, GMM clustering techniques, MLP deep learning techniques.
- **Lylia** :
- **Zaynab** :
- **Yassin** :
- **Christian** :

## Limits
