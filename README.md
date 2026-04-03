# Text-Scraping-Document-Clustering-Topic-modeling
The objective of this project is to scrape a corpus of news articles from a set of web pages, pre-process the corpus, and then to apply unsupervised clustering algorithms to explore and summarise the contents of the corpus.   

Part 1. Text Data Scraping  This part of the project should be implemented as a Python script 

1. Identify the URLs for all news articles listed on the website: http://mlg.ucd.ie/modules/COMP41680/news/index.html 
2. Retrieve all web pages corresponding to these article URLs. 
3. From the web pages, extract the main body text containing the content of each news article. Save the body of each article as plain text.  

Part 2. Corpus Exploration  Tasks to be completed in your IPython notebook: 
1. Load the text corpus generated in Part 1. Apply any appropriate pre-processing steps and construct a document-term matrix representation of the corpus. 
2. Summarise the overall corpus by identifying the most characteristic terms and phrases in the corpus. 
3. Apply two alternative clustering algorithms of your choice to the document-term matrix to produce clusters of related documents. This might require applying each algorithm several times with different parameter values. 
4. For each clustering generated in Step 3, summarise the contents of the clusters. Based on your summary, suggest a topic/theme for each cluster.

Steps
1. I imported NLP, web scraping, and ML libraries. I used BeautifulSoup for extracting news articles, NLTK for preprocessing, and Scikit-learn for feature extraction and topic modeling.
2. I scraped all news article titles by filtering anchor tags whose links start with ‘article’, ensuring only relevant content is extracted
3. This function collects all article links from the webpage, which are later used to scrape full article content.
4. I extracted the main content of each article by targeting specific HTML tags containing the news body.
5. I extracted all hyperlinks from the webpage and converted them into complete URLs for further scraping.
6. I built a crawler that navigates through multiple pages and collects all article links and titles for analysis.
7. I created a custom tokenizer that removes noise and applies lemmatization to normalize words, improving model quality
8. I loaded all scraped articles into a list to prepare them for NLP processing.
9. I loaded all scraped articles into a list to prepare them for NLP processing.
10. I applied K-Means clustering on TF-IDF vectors to group similar news articles into topics.
11. I used the Elbow Method to determine the optimal number of clusters by minimizing within-cluster variance.

Improvement

As an improvement, I can replace K-Means with LDA for probabilistic topic modeling.
