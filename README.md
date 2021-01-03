# nlp_negation
This is a python program to negate appropriate sentences in a text in order to improve sentiment analysis.

The goal here is to write a code that takes phrases from a text and, using the spaCy library, assesses the range of negation of those phrases, and if necessary, transform those phrases in such a way that it would easier for a sentiment analysis algorithm to pick up on them. This is done by adding the prefix "NOT_" to words in a sentence in order to reverse its polarity. 

For instance, the phrase:

"Didn't like this movie, but I"

would become:

"Didn't NOT_like NOT_this NOT_movie, but I"

Along with my code, there is a .json file containing both sample phrases and solutions.

I was able to obtain 92% accuracy while running my code on this sample data. And I believe that the ones that I missed were more the result of grammatical errors in the sentence given--for instance, a run-on sentence would throw off spaCy's Part Of Speech tagging, which would then make it difficult to negate the proper words.


The program contains only one file, negation_conversion.py, along with the data file, test1_t1.json

