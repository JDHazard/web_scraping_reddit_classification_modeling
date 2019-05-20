# Training a Classifier Using Text Data Scraped from Reddit's API

# Problem Statement

The goal of our project is to train a classifier using data scraped from two subreddit's using Reddit's API. Classifier models that priviledge NLP processes, such as Naive Bayes and simple Logistic Regression will be developed along with a Voting Classifier which will 'vote' based on Random Forest Classifier, AdaBoost Classifier, Gradient Boosting Classifer, and a Logistic Regression Classifier. Preprocessing and exploratory data analysis will utilize Count Vectorizer, Tfidf Vectorizer. Model success will be determined using built-in scores for each model by percentage. Our baseline is the percentage of each category before model fit. The scope of the project is limited by the amount of text data available in each subreddit. Our project has value to anyone looking to use text data to classify social media posts based solely on the text in the post. 

# Executive Summary

We were tasked to choose two different subreddits for this Natural Language Processing (NLP) challenge. Our models were trained to predict whether or not new text data would fit into one or the other subreddits. I choose two of my passions: The Classic Twilight Zone Series and Comic Books. My intuition and experince tell me that there will be some crossover terms between each subreddit particulary because a new interation of The Twilight Zone began on April 1st, 2019. Also, the comic book subreddit is a much broader topic and will include some crossover terminology. 

_Background on the The Twilight Zone and the r/TwilightZone subreddit_

[The Twilight Zone](https://www.imdb.com/title/tt0052520) show aired between 1959 and 1964 and is considered germinal, not only for Science Fiction television programming, but for Science Fiction as a literary genre. As creator and head writer, [Rod Serling](https://www.imdb.com/name/nm0785245/?ref_=ttfc_fc_wr1) contributed to all of the 156 episodes of the series. Along with other SFF luminaries such as [Richard Matheson](https://en.wikipedia.org/wiki/Richard_Matheson) and [Charles Beaumont](https://en.wikipedia.org/wiki/Charles_Beaumont), Rod Serling created some of the most memorable episodes in TV history. From screening [French Impressionist cinema](https://en.wikipedia.org/wiki/An_Occurrence_at_Owl_Creek_Bridge_(film)) to [wacky two-headed aliens](https://en.wikipedia.org/wiki/Mr._Dingle,_the_Strong) and casting everyone from Robert Redford to Buster Keaton; The Twilight Zone had something for every viewer and propelled televised science ficiton into the forefront of mainstream audiences. 

[**r/TwlightZone subreddit**](https://www.reddit.com/r/TwilightZone/)

    **About:** 'The subreddit dedicated to the Twilight Zone shows and movies.' 
    
    **Subscribers:** 8.6k Members
    
    **Top All-Time Post:** 'You can't skip that beautiful voice.' 

_Background on American comics books and the r/comicbooks subreddit_

Comic books have been part of the [American](https://en.wikipedia.org/wiki/History_of_American_comics) pop-cultural landscape from the beginning of the 20th century and incorporate nearly every genre, or subgenre, of literature. The subreddit encompasses not only American comics but the [English](https://en.wikipedia.org/wiki/British_comics), [Franco-Belgian](https://en.wikipedia.org/wiki/Franco-Belgian_comics),  and [Japanese](https://en.wikipedia.org/wiki/Manga) traditions, although there are separate subreddits for these distinct regions and cultures. The r/comicbooks subreddit has a wide cross-section of users asking questions and voicing opinions on of these topics and more. 

[**r/comicbooks subreddit**](https://www.reddit.com/r/comicbooks)

    **About:** 'A reddit for fans of comic books, graphic novels, and digital comics.'
    
    **Subscribers:** 849k True Believers 1k Skrull (850 members)
    
    **Top All-Time Post:** 'Representation is so important'



# Contents:

- [Data](http://localhost:8889/tree/data)
- [Notebooks](http://localhost:8889/tree/notebooks)
- [Presentation Slides](http://localhost:8889/tree/presentation)


## Conclusions and Recommendations:

#### Data was collected using a provided query push/shift function which is fully explained in the respective notebook. Non-text data was deemed extraneous and dropped from both datasets. Text was lemmatized, or parsed, using both RegexpTokenizer and WordNetLemmatizer and contractions dropped along with the word 'remove'. The Twilight Zone dataframe and Comic Book dataframe were then concatenated. Cleaned CSV's were saved as the appropriate files. 
#### Null values were examined imputed during the vectroizing and analysis phase using subject knowledge. CountVectorizer and TfidfVectorizer were used to lemmatize our text data and analyse our corpus parsed out as both 3 to 5 word phrases and 1 to 2 word phrases. Ultimately, focusing on one or two words in each dataset was ideal for classification modeling. 
#### Our Naive Bayes model, as explained in the notebook and scored at 98% & 97%, had a very low bias and low variance with only a 1% difference in training and testing models. Our Voting Classifier model, as explained in the notebook, had a slightly higher variance at 3% which indicates a slight overfitting. A Random Forest Classifier model, fitted immediately after the Voting Classifier, performed fairly poorly with a very high training score at 99.28% but a testing score of 94.50%, indicating an overfit model. 
#### The model best suited for NLP is Naive Bayes in this instance. Although clients may prefer a high perfoming model, such as our Random Forest Classifier, as a data scientist I would recommend caution when using it on unseen data. A robust model, like our Naive Bayes one, is a consistent classifier of text data. As with any NLP project, more data could be collected over time and/or the incorporation of reddit comments could be added to complicate our models. 