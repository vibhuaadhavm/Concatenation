Task 1
from textblob import TextBlob
text = """
Python is a simple programming language.
It is a user friendly programming language.
It is a Interpreter.
"""
blob = TextBlob(
text,
tokenizer=None,
pos_tagger=None,
np_extractor=None,
analyzer=None,
classifier=None
)
review = TextBlob("Python is an Interesting Programming Language")
print("Sentence Sentiments:")
for s in review.sentences:
print(f"{s} -> {s.sentiment.polarity:+.2f}")
print("\nNoun Phrases:",review.noun_phrases)
print("\nCorrected text:",review.correct())
print("\nSpanish translation:",review.translate(to="es"))
8/15/25, 9:20 PM Lab1.ipynb - Colab
https://colab.research.google.com/drive/11hRnfMMMpKHSKhaDG0N-w6Lqn3at-1oh#printMode=true 1/2
Sentence Sentiments:
---------------------------------------------------------------------------
LookupError Traceback (most recent call last)
/usr/local/lib/python3.11/dist-packages/textblob/decorators.py in decorated(*args, **kwargs)
 34 try:
---> 35 return func(*args, **kwargs)
 36 except LookupError as error:
11 frames
LookupError:
**********************************************************************
 Resource punkt_tab not found.
 Please use the NLTK Downloader to obtain the resource:
 >>> import nltk
 >>> nltk.download('punkt_tab')

 For more information see: https://www.nltk.org/data.html
 Attempted to load tokenizers/punkt_tab/english/
 Searched in:
 - '/root/nltk_data'
 - '/usr/nltk_data'
 - '/usr/share/nltk_data'
 - '/usr/lib/nltk_data'
 - '/usr/share/nltk_data'
 - '/usr/local/share/nltk_data'
 - '/usr/lib/nltk_data'
 - '/usr/local/lib/nltk_data'
