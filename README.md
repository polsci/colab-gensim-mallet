# Colab + Gensim + Mallet

September 14, 2021  
Geoff Ford  
https://polsci.github.io/  
https://github.com/polsci/  

See also: [Binder + Gensim + Mallet](https://github.com/polsci/binder-gensim-mallet)

## Introduction

This repository is designed for students in DIGI405 at the University of Canterbury to do topic modeling through their browser using [Google Colab](https://colab.research.google.com/). It is relevant for others who want to do topic modeling through a browser with their own corpus.

Note: The notebook has been updated to enforce Gensim v3.8 (the last version to support running topic models via Mallet).

## A note to DIGI405 students

Make sure you are saving your notebook regularly as Google Colab times out (pretty sure this is after 90 minutes - if you can find the official Google documentation to confirm this please let me know!).

### Steps for DIGI405:

1. Launch the notebook in Google Colab (see below)
2. Run the first cells to upgrade Gensim and install Java and Mallet.
3. Run the cell to upload and extract the corpus zip file. Warning: uploads are quite slow.  
4. Use the notebook to create your topic model.  

## A note to everyone

Before running the notebook, please read the [Google Colab FAQ](https://research.google.com/colaboratory/faq.html).

## Launch the notebook in Google Colab

Click here to run the notebook:  
[Launch on Google Colab](https://colab.research.google.com/github/polsci/colab-gensim-mallet/blob/master/topic-modeling-with-colab-gensim-mallet.ipynb)

## Not in DIGI405?

If you are not from this course, you can of course upload your own corpus as a zip. Your corpus should consist of a single directory of txt files (one document per txt file). This isn't the fastest way to run topic models, but allows you to create a topic model through your browser without installing any software.

## A note about pyLDAvis

The environment should support [pyLDAvis](https://github.com/bmabey/pyLDAvis), however this is not implemented in the sample notebook. Add a cell like this to install it:  
```
!pip install pyLDAvis
```
Add a cell like this to run it (note: this is sloooowwww and not recommended!):  
```
import pyLDAvis.gensim as gensimvis
import pyLDAvis
vis_data30 = gensimvis.prepare(gensimmodel30, doc_term_matrix, dictionary)
pyLDAvis.display(vis_data30)
```
