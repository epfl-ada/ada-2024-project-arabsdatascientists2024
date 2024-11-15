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

- **CelebA :**  This dataset regroups more than 200K images of 10177 unique celebrities each described by 40 binary attributes. CelebA is very valuable for identifying which physical traits (heights, smile, hair color...) contributes to an actor's "success". We contacted the author of the dataset to have access to celebrities' name as they were missing in the public version.
- **IMDB :** IMDb is probably the largest database collection related to movies. In the context of our project, it is extremelly useful to analyze the correlation between an actor popularity and box office revenues, movie ratings and reviews. It contains lots of crucial factors - audience feedback, sentiment analysis - which are worth exploring to answer our research question.
- **RottenTomatoes :** This website is well known for providing informative reviews on movies, we can use both the audience score and certified critics to decide if a movie is worth being watched. By analyzing the scores from this dataset we gain further insights on how well an actor performs in a given movie.
- **Oscars and Awards :** Oscars win and nomination are key indicators of an actor recognition and career achievment. It is the Motion Picture Academy members who get to vote and determine the winner, these professional opinions can change an actor's life and boost its career.
- **BoxOfficeMojo :** BoxOfficeMojo is another dataset allowing to assess a movie performance. By looking at the life time gross and the rankings of movies between 1888 and 2016 (what we have in our original dataset) we gain additional success metrics.
- **Metacritic :** This dataset aggregates "metascores" and "userscores" to rate a movie, based on the collection of millions of reviews. It allows us to assess how well movies are received by critics but also by the public which helps identify successful movies. It also contains some additionnal information about the movies, which helped us complete our plots for example.
- **Webscrapping:** As a couple of important columns for our analysis are filled with NaN values. We decided to enrich and complete these columns with webscrapping. An example for heights is available in the notebook showing the efficiency of this technique. The webscrapping was done using a programmable search engine and the creation of our own API. With the help of these elements, we search for whatever the query is (e.g actor's height) and extract the information that corresponds to this query. As the code contains our API key, we will not publish it for security. However, the functions used are in a .py document savedd locally.

## Methods

We will employ the methods we discovered in the course to analyze the datasets:

**Data visualization:** Using scatter plots, bar charts, and heatmaps to clearly represent tendencies.

**Correlation analysis:** to identify relationships between actor success and variables like physical attributes, movie genres, or roles.

**Regression Models:** Linear and logistic regression models to assess the impact of quantifiable traits (e.g., box office earnings, age).

**Classification Models:** Learning models to predict actor success based on input variables like physical attributes, roles, and social background. We could use classification or clustering if needed.

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

- **Exploration of ideas**: We hesitated between two ideas so we divided the group in two, in order to explore quickly to make a well-tought choice
- **Searching for additional datasets**: Each member looked for additional datasets we could use to complete our data
- **Cleaning and handling the data**: We chose the main datasets we will be using and cleaned them. Our goal was to create common dataframes for later use, so we all have a commom basis we can work on. To this end, we grouped the data into the datframes movie_metadata and character_metadata.
- **Filling missing information**: We are lacking information about box-office revenue (incomplete), height(incomplete), social background (inexistant) so we decided to Web scrap. We already did for height (in a subset of character_metadata), in order to see if it is feasible but we have some questions about that for the Teaching Team (cf. Questions for TAs) before extanding to the other parameters. We also added several datasets which either contained additionnal informations or aimed to complete some missing values.
- **Subset analysis**: We wanted to make sure that our project is feasible so we decided to take a subset and do a quick analysis to see if we come up with the desiered conclusions. We chose to test the potential relation between the box office revenue of movies and the actors that participated.

## Questions for TAs (optional)

- Question 1: We would like to discuss our webscrapping method with a TA. Indeed, we are using API from google cloud console and they give you 300$ of credit when signing up to use APIs and other features but we were wondering if maybe the school has an agreement with google or any other organization and that we could haave accesss to school accounts for this matter. Moreover, as it is our first time using APIs, we published our code in one of the branches the key was published therefore. We changed the key but we dont know what are the consequences of that and how we should handle such issues.

## Limits

- Maybe an economic limit as for the usage of webscappring using APis. We are awaiting for your response
