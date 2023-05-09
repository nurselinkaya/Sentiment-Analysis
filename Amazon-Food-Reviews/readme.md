In this project, I will show two different approaches to sentiment analysis by using VADER Sentiment Analysis Tool and RobertA pretrained language model.

I start with importing the necessary packages. The dataset has almost 600k datapoints. To be able to save some time, I have chosen only the first 1000 datapoints. Otherwise, it can take up to 15 minutes to run the models in entire dataset. Then, I made a basic visualization of each score and their abundancy with a bar plot.

VADER Sentiment Analysis
VADER is Valence Aware Dictionary and sEntiment Reasoner in short. VADER is a rule-based sentiment analysis tool that uses a lexicon of words and phrases with associated sentiment scores to analyze the sentiment of a text. Additionally, it takes into account the intensity of sentiment and the presence of negation in a sentence to provide a more accurate sentiment analysis result.

I use the SentimentIntensityAnalyzer class from nltk.sentiment module, which is an NLTK implementation of VADER. As seen above, polarity_scores method gives four parameters: Negativity, neutrality, positivity and compound scores. The first three I believe quite clear, but to clarify the compound score: It basically positions the sentiment between -1 and 1. 1 is the most positive and -1 is the most negative in the spectrum. Now, I write a loop to calculate the each score for each sentiment and I will store the results in a dictionary.

Now, I have results of VADER Sentiment analysis and the scores given by the customers. I will check, what is the distribution of Compound Score according to Amazon Scores. For that, I use barplot from seaborn library.



RobertA Pretrained Language Model:
At the second part of the project, I will use RobertA for sentiment analysis.

RobertA is Robustly Optimized BERT Pretraining Approach in short. It is a state-of-the-art pretrained language model based on the Transformer architecture. RobertA is usually used for more complex NLP tasks such as language generation or question answering, however, can be used also for sentiment analysis. To be able to use this model, first I will import the necessary classes and the softmax function.

I use the pre-trained sentiment analysis model based on the Twitter RoBERTa architecture from the Hugging Face Transformers library.

The model can be accessed from the link below:

https://huggingface.co/cardiffnlp/twitter-roberta-base-sentiment
