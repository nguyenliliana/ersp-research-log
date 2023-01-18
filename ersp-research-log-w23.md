# LILIANA'S RESEARCH LOG - WINTER '23

This research log is meant for me to record my learning and research progress.

## Project Description
The goal of this research is to leverage automatic question-answer generation to develop an integrated system where teachers can collaborate with AI to create and customize interactive reading resources with question-answering functions for their students from kindergarten through second grade. Throughout this project, students will have a chance to 1) develop innovative AI models that expand the state-of-the-art NLP techniques (e.g., BERT, GPT) for automatically generating question-answer pairs for reading materials and customizing the training to meet the unique requirements of an educational context; and 2) building a dialog system with graphical user interfaces that is able to a) ask children a question, b) provide tailored feedback and explanation to children’s response, and/or c) rephrase the original question (usually open-ended) to a multiple-choice question as a way of scaffolding if the children do not answer the original question or answer it incorrectly.

## Week 2

**Mon Jan 16: Learn Linear Regression and Gradient Descent**
I watched Andrew Ng YouTube videos on linear regression and gradient descent as part of his Machine Learning series. 

*Takeaways:*
  1.Have some function J(θ<sub>0</sub>, θ<sub>1</sub>) and want min<sub>θ<sub>0</sub>, θ<sub>1</sub></sub> J(θ<sub>0</sub>, θ<sub>1</sub>)
  2. Start with some θ<sub>0</sub>, θ<sub>1</sub>
  3.Keep changing θ<sub>0</sub>, θ<sub>1</sub> to reduce J(θ<sub>0</sub>, θ<sub>1</sub>) until we end at minimum.

**Tue Jan 17: Model Training**
I learned how to load datsets as PyTorch tensors using the torchtext Field and TabularDataset. Batches are created with BucketIterator. I employ the BERT architecture with a single additional layer for output prediction with the class BERTNLIModel. The constructor initializes with bert, hidden dimension, and output dimension. The forward pass of the model gets embedded representation of the input and applies a linar layer 'self.out' to map it to the output. 

## Week 1

**Wed Jan 11: Review BERT**

I watched videos first to get an overview of how BERT and Transformers work. Then, I read articles to get a technical understanding. 

*Takeaway:*

BERT is made up of stacked encoders from transformer architect as per the name, Bidirectional Encoder Representation from Transformer

**Thu Jan 12: Understand NLI Task**

My mentors challenged my group to finetune pre-trained BERT model to do sentence pair classification with the MultiNLI dataset. 

*Takeaways:*
1. Load BERT model and attach an additional layer for classification
2. Process and transform sentence-pair data for task
3. Fine-tune BERT model for sentence pair classification

**Fri Jan 13: Preprocess MNLI Dataset**

I set up the colab, importing necessary modules like torchtext and pandas. I imported the MNLI dataset and organized it into a dataframe using pandas. I extracted the necessary columns to prepare for preprocessing. 

Columns after preprocessing: 
1. gold_label
2. sequence: \[cls] sentence 1 \[sep] sentence 2 \[sep]
3. attention mask: \[1] * len(sentence) --> string
4. token type:  \[0] * len(sentence) +  \[1] * len(sentence) --> string

![df_train.head()](/assets/preprocessing.PNG)

