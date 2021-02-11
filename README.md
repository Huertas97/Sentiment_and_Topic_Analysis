# Sentiment_Analysis

**Author**: Álvaro Huertas García 

# Index
 
 * [Repository purpose](#repository-purpose)
 * [SST2](#sst2)
 * [Type of Multilingual Data](#type-of-multilingual-data)
 * [Languages supported](#languagues-supported)
 * [How to use](#how-to-use)
 * [References](#references)

# Repository purpose

In this repository, we present the results obtained after developing Machine Learning and Deep Learning Transformer-based models for predicting a text’s polarity for English and Spanish language. 

# Machine Learning models

The Machine Learning Naïve Bayes, K-Nearest Neighbors, Logistic Regression and Random Forest algorithms are used as classifiers. Two strategies are followed to encode SST2 corpus data into vectors that will be used as inputs for the ML algorithms. In the first one, the word embeddings result from the training of Word2Vec over the SST2 corpus data combined with TF-IDF. In the second one, the word embeddings come from an already pre-trained Word2Vec model on part of the Google News dataset. This pre-trained Word2Vecmodel has the advantage of incorporating much more text data into the training.  In bothcases, to represent a sentence into a vector, we take the average of all the word vectors in asentence. Thus, the average vector represents the sentence embedding.

Regarding the Deep Learning Transformer-based models developed, the models used aretrained while minimizing Binary Cross-Entropy loss function value. Besides, during the traininghyperparameters are optimized, selecting those with the lowest loss value in the development set. Four Transformer-based models are used, two multilingual (XLM-RoBERTa and DistilBERTmultilingual) and two monolingual (DistilRoBERTa and DistilBERT fine-tuned for NLI andSTS Benchmark). 


The Google Collab notebooks in sst2_models folder show the code used for trainig both apporaches. Besides, during the training the results are logged in Weights and Biases: https://wandb.ai/huertas_97/SST2-train?workspace=user-huertas_97 and https://wandb.ai/huertas_97/SST-2-best_set/overview?workspace=user-huertas_97. 




# References

Richard Socher et al. “Recursive Deep Models for Semantic Compositionality Over a Sen-timent Treebank”. In:Proceedings of the 2013 Conference on Empirical Methods in NaturalLanguage Processing. Seattle, Washington, USA: Association for Computational Linguis-tics, 2013, pp. 1631–1642.url:https://www.aclweb.org/anthology/D13-1170
