## Sentiment Analysis with VADER and RobertA

This project demonstrates two different approaches to sentiment analysis using VADER Sentiment Analysis Tool and a pretrained RobertA language model.

### Prerequisites
pandas
numpy
matplotlib
seaborn
nltk
transformers

### Dataset

The dataset used is the Amazon Fine Food Reviews dataset. The original dataset has almost 600k datapoints. To save time, the code in this repository only uses the first 1000 datapoints. If you want to run the models with the entire dataset, be aware that it can take up to 15 minutes to run.

### VADER Sentiment Analysis

VADER is a rule-based sentiment analysis tool that uses a lexicon of words and phrases with associated sentiment scores to analyze the sentiment of a text. Additionally, it takes into account the intensity of sentiment and the presence of negation in a sentence to provide a more accurate sentiment analysis result.

To use VADER, I use the SentimentIntensityAnalyzer class from the nltk.sentiment module. The polarity_scores() method is used to give four parameters: Negativity, neutrality, positivity, and compound scores.

The compound score ranges from -1 to 1, with 1 being the most positive and -1 being the most negative.

### RobertA Language Model

RobertA is a pretrained transformer-based language model developed by Hugging Face. It can be used for many natural language processing (NLP) tasks, including sentiment analysis.

In this project, RobertA is used to classify the sentiment of the Amazon reviews. 

### Results
The results of the sentiment analysis are plotted using seaborn. There are four plots:

Compound score vs. Amazon score
Positive score vs. Amazon score
Neutral score vs. Amazon score
Negative score vs. Amazon score

The compound score seems to be relevant to the Amazon scores in which 1 has negative values in the compound score, while 5 has the highest positive compound score. The barplots also show that score 1 has the lowest positive score as it should be and vice versa for the negative score.

### Conclusion
This project demonstrates two approaches to sentiment analysis and shows the distribution of sentiment scores in the Amazon Fine Food Reviews dataset. The VADER sentiment analysis approach uses a rule-based tool to analyze sentiment, while the RobertA approach uses a pretrained transformer-based language model. The results show that both approaches are able to classify the sentiment of the reviews.
