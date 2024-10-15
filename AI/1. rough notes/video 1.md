- types of ml:
	- ![[Pasted image 20241015204219.png]]


## env setup
- environment created: 
	- local folder i installed these to: `/Documents/temp/env`


## libraries installed



- `pip install scikit-learn`
	- for machine learning
- `pip install tensorflow`


### sentiment analyzer example
```python
from textblob import TextBlob
from newspaper import Article

import nltk
nltk.download('punkt_tab') 

url = 'https://en.wikipedia.org/wiki/Mathematics'
article = Article(url)

article.download()
article.parse()
article.nlp()

text = article.summary
print(text)

blob = TextBlob(text)
sentiment = blob.sentiment.polarity
print(sentiment)
```