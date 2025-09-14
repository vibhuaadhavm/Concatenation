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
