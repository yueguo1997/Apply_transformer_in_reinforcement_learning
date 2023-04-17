# Bert vs Longformer - document classification


## Background





## Model card

### Bert model
BERT (Bidirectional Encoder Representations from Transformers) is a pre-trained transformer-based language model introduced by Google in 2018. It is designed to produce context-aware word embeddings, which can be fine-tuned on downstream NLP tasks such as question answering, sentiment analysis, and natural language inference.

BERT is trained using a masked language modeling objective, where a random subset of words in the input sequence is masked, and the model is trained to predict the masked words. This allows the model to capture the bidirectional context of each word, enabling it to understand the meaning of a word in the context of the entire sentence.

BERT has achieved state-of-the-art results on a range of NLP tasks, surpassing the performance of previous models that used hand-crafted features. It has also been used in transfer learning settings, where it has been shown to outperform traditional approaches that rely on task-specific feature engineering.

### Longformer

Longformer is a transformer-based language model designed to process long sequences of text efficiently. It was introduced by Beltagy et al. in 2020 as a solution to the problem of handling long sequences with transformer models.

The key innovation of Longformer is its attention mechanism, which is designed to consider a global context of the input sequence while still being computationally efficient. Unlike the standard transformer model, which attends to all tokens in the input sequence, Longformer selectively attends to a subset of tokens based on their relevance to the current token. This is achieved using a sliding window approach, where the attention mechanism considers a fixed-size window of tokens at a time, but can still take into account the entire input sequence.

Longformer has been shown to achieve state-of-the-art results on a range of long-form text tasks, including document classification, question answering, and summarization. It has also been used to pretrain large-scale language models, demonstrating its effectiveness in capturing long-range dependencies in text.

### Difference 


## Dataset description

### recuter news

The documents in the Reuters-21578 collection appeared on the Reuters newswire in 1987. The documents were assembled and indexed with categories by personnel from Reuters Ltd. (Sam Dobbins, Mike Topliss, Steve Weinstein) and Carnegie Group, Inc. (Peggy Andersen, Monica Cellio, Phil Hayes, Laura Knecht, Irene Nirenburg) in 1987.

In 1990, the documents were made available by Reuters and CGI for research purposes to the Information Retrieval Laboratory (W. Bruce Croft, Director) of the Computer and Information Science Department at the University of Massachusetts at Amherst. Formatting of the documents and production of associated data files was done in 1990 by David D. Lewis and Stephen Harding at the Information Retrieval Laboratory.

Further formatting and data file production was done in 1991 and 1992 by David D. Lewis and Peter Shoemaker at the Center for Information and Language Studies, University of Chicago. This version of the data was made available for anonymous FTP as "Reuters-22173, Distribution 1.0" in January 1993. From 1993 through 1996, Distribution 1.0 was hosted at a succession of FTP sites maintained by the Center for Intelligent Information Retrieval (W. Bruce Croft, Director) of the Computer Science Department at the University of Massachusetts at Amherst.


#### Resumes


## Experiement

### News file classification


### Resume classfication 




## Conclusion


## Next step



## Reference
[Bert model]()

[Longformer model]()

