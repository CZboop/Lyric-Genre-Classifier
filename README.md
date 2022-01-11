# Lyric Genre Classifier
A Python classifier to predict the genre of a song based on lyric content. Uses Pandas, NumPy and some Natural Language Toolkit. 

Classification is done with my take on TF-IDF. The whole genre is treated as a text for the purposes of finding text frequency, and this is used alongside the number of songs from each genre that feature a given word, to find which words may be most indicative of each genre. Each song then has a score for each genre calculated based on which keywords it contains, taking into account the strength of the word's correlation to a genre from it's TF-IDF value, in order to make predictions.

Trained on around 5000 songs to differentiate between metal and R&B.

Currently has an accuracy of around 65%

Uses [this dataset](https://www.kaggle.com/mateibejan/multilingual-lyrics-for-genre-classification), slightly modified to remove commas and carriage returns within cells (actual end files used were too large for GitHub). 

Many thanks to the creator of the dataset
