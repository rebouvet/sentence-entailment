## Sentence entailment

### Introduction
Given two sentences of text, s1 and s2, the systems need to compute how similar s1 and s2 are.

### Dataset
The SICK data set consists of 10,000 English sentence pairs, each annotated for relatedness in meaning.  
File Structure: tab-separated text file

Fields:
 - sentence pair ID
 - sentence A
 - sentence B
 - semantic relatedness gold label (on a 1-5 continuous scale)
 - textual entailment gold label (NEUTRAL, ENTAILMENT, or CONTRADICTION)
 
##### Examples of sentence pairs with their gold entailment labels.

Entailment label | Example
------------     | -------------
| ENTAILMENT     | A: “Two teams are competing in a football match” <br/>B: “Two groups of people are playing football” |
| CONTRADICTION  | A: “The brown horse is near a red barrel at the rodeo” <br/>B: “The brown horse is far from a red barrel at the rodeo” |
| NEUTRAL        | A: “A man in a black jacket is doing tricks on a motorbike”<br/>B: “A person is riding the bicycle on one wheel”

_The SICK data set is released under a Creative Commons Attribution-NonCommercial-ShareAlike 3.0 
Unported License (http://creativecommons.org/licenses/by-nc-sa/3.0/deed.en_US)_

### Evaluation

Systems are evaluated on classification accuracy (the percent of labels that are
predicted correctly) for every sentence pairs. We are also interested in the precision/recall scores
for each class as well as a confusion matrix.

### Source code
To wrap your head around our pipeline take a look at the [baseline](https://github.com/Drakirus/sentence-entailment/blob/master/baseline.ipynb) notebook.  
Building upon the baseline we proposed enhancements (written in the `.py` files). 

### Papers
> [SemEval-2014](http://alt.qcri.org/semeval2014/cdrom/pdf/SemEval2014001.pdf)  
> [ Denotational and Distributional Approach to Semantics](http://www.aclweb.org/anthology/S14-2055)  
> [SentEval: An Evaluation Toolkit for Universal Sentence Representations](https://arxiv.org/abs/1803.05449)  
> [Supervised Learning of Universal Sentence Representations from Natural Language Inference Data](https://arxiv.org/abs/1705.02364)  
