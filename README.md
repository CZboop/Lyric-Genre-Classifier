# Lyric Genre Classifier
A Python classifier to predict the genre of a song based on lyric content. Uses Pandas, NumPy, Keras, TensorFlow and some Natural Language Toolkit. 

Currently has two separate classification methods.

First method was my take on TF-IDF, which was initially intended to be part of data preprocessing, but ended up working fairly well for classification by itself. The whole genre is treated as a text for the purposes of finding text frequency, and this is used alongside the number of songs from each genre that feature a given word, to find which words may be most indicative of each genre. Each song then has a score for each genre calculated based on which keywords it contains, taking into account the strength of the word's correlation to a genre from its TF-IDF value, in order to make predictions.
This was trained on around 5000 songs to differentiate between two genres (metal and R&B), with an accuracy of around 65%, or 30% better than chance.

Second method uses a LSTM recurrent neural network made with Keras/TensorFlow. This currently has an accuracy of around 62.5% when classifying between eight different genres (rock, metal, pop, indie, R&B, folk, electronic and jazz), or 400% better than chance. When trained to distinguish between two genres that are more objectively distinct (again, metal and R&B), this RNN was able to classify songs with an accuracy of around 88%.

Uses [this dataset](https://www.kaggle.com/mateibejan/multilingual-lyrics-for-genre-classification), slightly modified to remove commas and carriage returns within cells (actual end files used were too large for GitHub). 
Many thanks to the creator of the dataset
