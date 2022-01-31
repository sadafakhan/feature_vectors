## Description

This program creates training and testing feature vectors for given text files. 
It takes parameters that specify a threshold frequency for rare words and a threshold frequency for features overall (excluding currentWord)

The input text files are labelled for part-of-speech. The output files consist of the feature vectors (for training and testing) after threshold filters are applied, in Mallet text format. 

It also outputs: 

* `train_voc`: Text file with the vocabulary that includes all the words appearing in train file. Has the format: '[word] [word frequency]', sorted by frequency in descending order. 

* `init_feats`: Text file that lists the features that occur in the training file. Has for format '[featureName] [frequency]', sorted by the frequency of the feature in the train file in descending order.

* `kept_feats`: Text file that is a subset of `init_feats`; only includes the features that are kept after applying the feature threshold. Has the same format and order as `init_feats`.s