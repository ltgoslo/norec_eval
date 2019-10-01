# NoReC_eval

## Overview 
NoReC_eval is a dataset of Norwegian full-text reviews where sentences are labeled to indicate whether they are _evaluative_ or sentiment-bearing, i.e. where they are intended by the author (or some other opinion holder) to serve as an evaluation or judgment. The data comprises roughly 8000 sentences across almost 300 reviews and 10 different thematic categories (literature, products, restaurants, etc.), and is a subset of the [Norwegian Review Corpus](https://github.com/ltgoslo/norec) (NoReC; [Velldal et al. 2018](http://www.lrec-conf.org/proceedings/lrec2018/pdf/851.pdf)). 

The annotations and first experimental results are described in the following paper from Nodalida 2019 by P. Mæhlum, J. Barnes, L. Øvrelid, and E. Velldal; [Annotating evaluative sentences for sentiment analysis: a dataset for Norwegian](https://www.aclweb.org/anthology/W19-6113/). The full [annotation guidelines](https://github.com/ltgoslo/norec_eval/blob/master/annotation_guidelines/guidelines.md) are also made available in this repo.

## Labeled categories
While sentences are annotated wrt being *evaluative*, they are not annotated with respect to positive/negative polarity. The reason for this is that polarity is often mixed at the sentence-level. Although most of the sentences labeled as evaluative will be subjective and personal, they can also include objective sentences. Moreover, our annotation scheme singles out a particular category of evaluative sentences called *fact-implied non-personal*. Evaluative sentences are also further sub-categorized as to whether they are considered *on-topic* with respect to the object being reviewed, and whether they express the *first-person* view of the author.

## Format
The data is distributed in a tab-separated format, with one tsv-file per review. The file names correspond to the document ids in NoReC, as to make it possible to cross-reference additional information there. There is one sentence-annotation per line, and the fields are as follows:

1, ID: the NoReC sentence id.  
2, E: indicates whether the sentence is evaluative (=1) or not (0).  
3, EFINP: indicates whether it is an evaluative fact-implied non-personal sentence (1) or not (0).  
4, NOT: 1 if the evaluation in not on topic, 0 otherwise.  
5, NFP: 1 if the evaluation is not first person, i.e. does not express the view of the author, 0 otherwise.  
6, IAD: flags inter-annotator disagreement; 1 if the annotators disagreed, 0 otherwise.  
7, text: the tokenized sentence.  

## Cite
If you use this dataset, please cite the following paper:

```
@InProceedings{MaeBarOvr19,
  author = {M{\ae}hlum, Petter and Barnes, Jeremy and {\O}vrelid, Lilja and Velldal, Erik},
  title = {Annotating evaluative sentences for sentiment analysis: a dataset for {N}orwegian},
  booktitle = {Proceedings of the 22nd Nordic Conference on Computational Linguistics},
  year = 2019,
  address = "Turku, Finland"
}
```
URL: https://www.aclweb.org/anthology/W19-6119/

## Terms of use

While the data is distributed under a Creative Commons Attribution-NonCommercial licence (CC BY-NC 4.0; access the full license text here: https://creativecommons.org/licenses/by-nc/4.0/), motivated by the need to block the possibility of third parties redistributing the orignal reviews for commercial purposes, please note that *machine learned models*, extracted *lexicons*, *embeddings*, and similar resources that are created on the basis of NoReC are not considered to contain the original data and so *can be freely used also for commercial purposes* despite the non-commercial condition.
