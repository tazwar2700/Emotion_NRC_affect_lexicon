# emotion
This module is a emotion classifier that classifies emotion of a list of words and gives aggregated scores for each emotion. The classifier is based on NRC Affect Intensity Lexicon. The lexicon has close to 10,000 entries for eight
emotions that Robert Plutchik argued to be basic or universal. Some words
has multiple emotions to varying degree. Here is how the classifier works:

•The classifier first matches the words with the lexicon and fetches the
emotions and intensity score for each matching from the lexicon.

• Then it sums the scores along the emotions and gives a mood score of
the song. The emotion intensity are given from 0 to 1 in floats so the
aggregated score is a float as well.

• It multiplies the number of appearances of these mood words in the song
with the intensity score to give a corrected weighting of each emotion.

## Installation
Run the following to install:

'''python
pip install emotion_nrc_affect_lex
'''
## Usage
'''python
from emotion import*
text = ["love", "hate", "like"]
em = Emo(text)
em.weighted_emotion_scores
em.affect_dict
em.raw_emotion_scores
em.word_frequencies
'''
