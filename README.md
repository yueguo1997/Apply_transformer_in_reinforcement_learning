# Bert vs Longformer - document classification

## Background
Project is aimed at compare the performance of bert and longformer model based on document classification task. 
Document classification is an important task in natural language processing that has many practical applications. It enables efficient organization and retrieval of information, personalization and recommendation, spam filtering, sentiment analysis, and compliance with regulatory requirements.

When classifying documents thorugh a transformer model, it can become a hard problem due to several reasons:
* Attention mechanism: The transformer model relies on the attention mechanism to attend to relevant parts of the input sequence. When the sequence is long, the number of attention calculations required increases Asignificantly, leading to computational overhead and memory constraints.

* Context window: The transformer model operates on fixed-size context windows, which limits the amount of context available to the model for making predictions. When dealing with long sequences, it becomes challenging to capture the relevant context effectively within these fixed-size windows.

* Data sparsity: Long sequences often contain a large number of tokens, but many of them may be irrelevant or redundant. This can lead to data sparsity, which makes it challenging for the model to learn from the data effectively.

## Model card

### Bert model
BERT (Bidirectional Encoder Representations from Transformers) is a pre-trained transformer-based language model introduced by Google in 2018. It is designed to produce context-aware word embeddings, which can be fine-tuned on downstream NLP tasks such as question answering, sentiment analysis, and natural language inference.

BERT is trained using a masked language modeling objective, where a random subset of words in the input sequence is masked, and the model is trained to predict the masked words. This allows the model to capture the bidirectional context of each word, enabling it to understand the meaning of a word in the context of the entire sentence.
![plot](https://miro.medium.com/v2/resize:fit:876/0*ViwaI3Vvbnd-CJSQ.png)

### Longformer
Longformer is a transformer-based language model designed to process long sequences of text efficiently. It was introduced by Beltagy et al. in 2020 as a solution to the problem of handling long sequences with transformer models.

The key innovation of Longformer is its attention mechanism, which is designed to consider a global context of the input sequence while still being computationally efficient. Unlike the standard transformer model, which attends to all tokens in the input sequence, Longformer selectively attends to a subset of tokens based on their relevance to the current token. This is achieved using a sliding window approach, where the attention mechanism considers a fixed-size window of tokens at a time, but can still take into account the entire input sequence.

<img src="https://github.com/yueguo1997/Document_classfication_by_Longformer/blob/11536dfe50b5463c84874600c056795160fa301a/Screen%20Shot%202023-04-17%20at%209.28.27%20PM.png" width="520" height="720"/>

### Difference between the models

Attention mechanism: Both BERT and Longformer use the self-attention mechanism to capture the relationships between different tokens in the input sequence. However, the attention mechanism in Longformer is modified to allow for long-range dependencies while keeping computational complexity under control. Specifically, Longformer uses a sliding window attention mechanism that only attends to a subset of the input tokens at a time, which reduces the computational cost while still allowing for long-range dependencies.


## Dataset description

### Resumes
This dataset is dealing with only has 130 samples in total, including good, bad ans medium performance resumes. 

### AG News Dataset
The AG News Dataset is a collection of news articles published between 1996 and 1998, which has been widely used for text classification tasks in natural language processing. The dataset consists of 120,000 news articles from four different categories: World, Sports, Business, and Science/Technology. Each article is labeled with one of the four categories, making it a multi-class classification problem.

| Dataset name| size |Average length | Classes|
| ------------- | ------------- | ------------- | ------------- |
| Resumes  | 130 |1k |3|
| News  | 120000  |30| 7|

## Experiement
### Resume classfication 
* Maximum length

| Model| 512 |1024 |2048 |4096 |8192 |
| ------------- | ------------- | ------------- | ------------- |------------- |------------- |
| Longformer | yes | yes |  yes| yes|no|
| Bert| yes | no | no |no|no|


### News file classification

* Training curve

<img src="https://github.com/yueguo1997/Document_classfication_by_Longformer/blob/dc3b1a88df840ce39e5e628bbd592ce7f62a9c97/Screen%20Shot%202023-04-15%20at%2010.38.15%20PM.png" width="360" height="220"><img src="https://github.com/yueguo1997/Document_classfication_by_Longformer/blob/cb0f4f6201126ab81af13d70f74c823dd6d49a7a/Screen%20Shot%202023-04-15%20at%2010.38.19%20PM.png" width="360" height="220"/>

* Training time

<img src="https://github.com/yueguo1997/Document_classfication_by_Longformer/blob/8261a85bc4c6aa12573d54a13dc6ac7e7fd85656/Screen%20Shot%202023-04-17%20at%207.51.42%20PM.png" width="360" height="220"><img src="https://github.com/yueguo1997/Document_classfication_by_Longformer/blob/8261a85bc4c6aa12573d54a13dc6ac7e7fd85656/Screen%20Shot%202023-04-15%20at%2010.38.26%20PM.png" width="360" height="220"/>


* Test accuracy


## Conclusion


## Next step



## Reference
[Bert model]()

[Longformer model]()

