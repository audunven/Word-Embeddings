# Word-Embeddings

This repository contains word embedding files created from running a Word2Vec pipeline on the following natural text sources:
* Wikipedia: Wikipedia hosts general-purpose knowledge. A prepared XML dump from October 2018 was downloaded from https://dumps.wikimedia.org/backup-index.html. 
* Skybrary, a wiki hosting aviation knowledge: https://www.skybrary.aero/index.php. Here, the entire Skybrary wiki was scraped (with permission from Eurocontrol) using dumpgenerator.py from WikiTeam (https://github.com/WikiTeam/wikiteam).

# Procedure used for creating the Word Embedding files
For both the mentioned sources the following configuration was applied:
* WikiExtractor.py (https://github.com/attardi/wikiextractor) was used to extract relevant text from the XML dumps.
* Gensim (gensim.utils.simple_preprocess()) was used for pre-processing.
* Gensim Word2Vec and the Skip Gram model was used for learning the embedding vectors.
* Window size: 5, minimum word count: 2, iterations: 5, embedding size: 300.
