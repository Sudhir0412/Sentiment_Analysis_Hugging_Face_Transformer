## Sentiment analysis with Hugging Face Transformer(pretrained model)

##### Importing the Required Libraries:
import transformers 
from transformers import pipeline
import torch <br>
####### transformers: This library provides state-of-the-art pre-trained models for natural language processing tasks. 
####### pipeline: A utility function in the transformers library that simplifies the use of pre-trained models. 
####### torch: The PyTorch library, which is used as the backend for the transformer models. 

##### Creating a Sentiment Analysis Pipeline:
classifier = pipeline('sentiment-analysis')
pipeline('sentiment-analysis'): This line initializes a sentiment analysis pipeline using a pre-trained model. The pipeline makes it easy to perform sentiment analysis without manually loading a model or handling tokenization.
classifier: The resulting object from the pipeline function, which you can use to analyze the sentiment of text.

##### Checking the Type of the Classifier:
type(classifier)
This line returns the type of the classifier object. Typically, this would be something like transformers.pipelines.base.Pipeline.

##### Using the Classifier to Analyze Sentiment:
classifier("This is not a nice thought to go there and come without enjoying anything")

The text "This is not a nice thought to go there and come without enjoying anything" is analyzed for its sentiment.

##### Output Explanation:

output: [{'label': 'NEGATIVE', 'score': 0.9996657371520996}]
output: The classifier returns a list of dictionaries.

label: Indicates the sentiment of the input text. In this case, it's NEGATIVE, meaning the text has a negative sentiment.
score: Represents the confidence score of the sentiment prediction. Here, 0.9996657371520996 indicates a very high confidence that the sentiment is negative.
