# Visualizing Gender Bias in Movie Reviews

The goal of this project is to highlight possible gender bias in film reviews in this data set. **The underlying assumption is that bias may appear in a variety of ways, from lower scores or more negative reviews by male critics for films starring or directed by women, to the appearance of ”gendered” adjectives or word associations that may be inconsistent depending on the gender of the critic.** There have been several movie reviews from the past year or more that have been called out for using sexist language and demeaning women, and there have been studies that have shown that male critics are usually harsher on movies starring women than female critics are. Read more about it [GitHub](https://womenintvfilm.sdsu.edu/wp-content/uploads/2018/07/2018_Thumbs_Down_Report.pdf): 
Around 3000 reviews were collected from the New York Times, annotated for the gender of the director/lead actor, and analyzed in several ways for possible gender bias.


The reviews were divided into 8 subsets: 
- Female critic reviews about female starring films (FcFa)
- Male critic reviews about female starring films (McFa)
- Female critic reviews about male starring films (FcMa)
- Male critic reviews about male starring films (McMa)
- ... and similarly for female and male-directed films.

## Metadata

Metadata refers to information about the data set in general. Some important facts about this data set:

- Around 3000 reviews total
- 924 reviews written by female critics
- 1903 reviews written by male critics

- 475 reviews about female-directed films
- 2352 reviews about male-directed films

- 653 reviews about male-starring films
- 1305 reviews about female-starring films

This translates to:

![Image of Yaktocat](https://roopa-ramanujam.github.io/iw2018/actor_director_breakdown.png)

## NLTK analysis

Python has a natural language processing tool called the Natural Language Toolkit, which has methods to count instances of certain words in text (as well as display their context). A list of words that are typically only used to describe females was counted in the subsets of data relating to actors, when they were used to describe women:

![Image of Yaktocat](https://roopa-ramanujam.github.io/iw2018/word_counts_female_true.png)

NLTK can also generate word clouds for sets of text, with words that are most frequent in the text appearing the largest. 

Female critics, female star
![Image of Yaktocat](https://roopa-ramanujam.github.io/iw2018/FcFa_wc.png)

Male critics, female star
![Image of Yaktocat](https://roopa-ramanujam.github.io/iw2018/McFa_wd.png)

Female critics, male star
![Image of Yaktocat](https://roopa-ramanujam.github.io/iw2018/FcMa_wd.png)

Male critics, male star
![Image of Yaktocat](https://roopa-ramanujam.github.io/iw2018/McMa_wd.png)

Female critics, female director
![Image of Yaktocat](https://roopa-ramanujam.github.io/iw2018/FcFd_wd.png)

Male critics, female director
![Image of Yaktocat](https://roopa-ramanujam.github.io/iw2018/McFd_wd.png)

Female critics, male director
![Image of Yaktocat](https://roopa-ramanujam.github.io/iw2018/FcMd_wd.png)

Male critics, male director
![Image of Yaktocat](https://roopa-ramanujam.github.io/iw2018/McMd_wd.png)

## Word2Vec analysis

Word2Vec is a tool that, given a body of text to train on, will build vectors for the words in the text. With Word2Vec you can input a word and get the words most similar to that word based off the input body of text alone. This analysis was conducted separately on each of the 8 subsets of data described above (FcFa, McFa, etc.) The most similar words to the input words are shown below:

Most similar words for actor subsets:

![Image of Yaktocat](https://roopa-ramanujam.github.io/iw2018/w2vactor.png)

Results for most similar words for director subsets:

![Image of Yaktocat](https://roopa-ramanujam.github.io/iw2018/w2vdirector.png)

## Sentiment analysis

The Stanford NLP lab created a tool that takes in a body of text and computes a sentiment and score for each sentence from 0-4. The values are "very negative"(0), "negative" (1), "neutral" (2), "positive" (3), "very positive" (4). 


The graphs below plot the percentage of a review that is assigned each of these labels, for all of the reviews:

![Image of Yaktocat](https://roopa-ramanujam.github.io/iw2018/actor_percent_sentiment_parallel.png)

(yellow = FcFa, teal = McFa, purple = FcMa, pink = McMa)

![Image of Yaktocat](https://roopa-ramanujam.github.io/iw2018/director_percent_sentiment_parallel.png)

(orange = FcFa, green = McFa, maroon = FcMa, lilac = McMa)

The tables below show the average percentages of these labels for a review from each data subset:

![Image of Yaktocat](https://roopa-ramanujam.github.io/iw2018/sent_actor_percent.png)
![Image of Yaktocat](https://roopa-ramanujam.github.io/iw2018/sent_director_percent.png)

