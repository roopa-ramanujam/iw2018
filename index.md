# Visualizing Gender Bias in Movie Reviews

The goal of this project is to highlight possible gender bias in film reviews in this data set. There have been several movie reviews from the past year or more that have been called out for using sexist language and demeaning women, and there have been studies that have shown that male critics are usually harsher on movies starring women than female critics are. Read more about it here: ![link](https://womenintvfilm.sdsu.edu/wp-content/uploads/2018/07/2018_Thumbs_Down_Report.pdf)

Around 3000 reviews were collected from the New York Times and analyzed in several ways for possible gender bias.

## Metadata

Metadata refers to information about the data set in general. Some important facts about this data set:

- Around 3000 reviews total
- 924 reviews written by female critics
- 1903 reviews written by male critics

- 475 reviews about female-directed films
- 2352 reviews about male-directed films

- 653 reviews about male-starring films
- 1305 reviews about femlae-starring films

The reviews were divided into 8 subsets: 
- Female critic reviews about female starring films (FcFa)
- Male critic reviews about female starring films (McFa)
- Female critic reviews about male starring films (FcMa)
- Male critic reviews about male starring films (McMa)
- ... and similarly for female and male-directed films.

## NLTK analysis

Python has a natural language processing tool called the Natural Language Toolkit, which has methods to count instances of certain words in text (as well as display their context). A list of words that are typically only used to describe females was counted in the subsets of data relating to actors:

![Image of Yaktocat](https://roopa-ramanujam.github.io/iw2018/word_counts_female_true.png)


### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/roopa-ramanujam/iw2018/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
