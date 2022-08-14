# Natural Langurage Processing Analysis on WeChat History Before and After Getting Married
This project is prepared by myself in the format of a paper as for my husband's Paper Aniversary gift. This repository contains the following files: 

* The Jupyter Notebook file: James_Surprise_NLP.ipynb, shows the source code of my statistical analysis. 
* The pdf file: James_Surprise_paper.pdf, is the finalized paper that I prepared and presented to my husband.
* The Data folder contains two data sets as input files for analyzing the most frequent words before and after marriage. 


The study period for this paper ranges from January 2021 to December 2021 and is segmented into 2 time phases, the pre-marriage period (before July 10, 2021) and the post-marriage period (after July 10, 2021). Due to the limitation of the WeChat App, the complete chat history could not be directly extracted. Therefore, the author randomly selects 100 messages during the pre-marriage time period and 100 messages during the post-marriage time period as two different sample sets, under the assumption that the data sets are unbiased. All WeChat messages are manually copied from the App and pasted into the .csv files for later analyses.

Once the data is collected, the author applies the NLP techniques to convert each text into analyzable words. The NLP
process consists of the following steps:
1. Word tokenization: word tokenization is the process of splitting a text into words. The author uses a built-in
Jieba (Neutrino, 2020) package in Python that segments each Chinese message into individual words.
2. Removal of stopwords: the stopwords in NLP are the most common words in data that we do not want to use
to describe the topic of the content. The author uses a stopword corpus (available online, with both Chinese and
English stop words) as the reference to remove stop words.
3. Removal of single-character words: the author removes the words with only a single Chinese character.

The statistical analysis consists of two parts. First, the author analyzes the most frequent words. At this stage, WordCloud images are created to visually represent the top words. Cloud creators are used to highlight popular words and phrases based on frequency and relevance. Second, the author performs sentiment analysis on the text content before and after getting married. At this stage, the author uses SnowNLP (Wang, 2020), a built-in Python module for the sentiment analysis of Simplified Chinese words. The built-in algorithm in this package uses a pre-trained sentiment prediction model such that given an input text, it outputs a sentiment score ranging from 0 to 1, with 0 representing the most negative sentiment and 1 representing the most positive sentiment. The author then analyzes the distributions of sentiment scores of WeChat messages for pre- and post-marriage time periods and applies a t-test to identify the
significance of the difference in sentiment value distributions.
