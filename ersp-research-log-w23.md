# LILIANA'S RESEARCH LOG - WINTER '23

This research log is meant for me to record my learning and research progress.

## Week 4

**Fri Feb 3: Research Outline**


**Thurs Feb 2: ChatGPT API**


**Wed Feb 1: Group Meeting, New Resarch Topic!**

 Group Meeting w/ Prof. Chang and Mentors: 
 - After discussing about our goals to write a paper for EMNLP, our Prof. Chang and our mentors decided to choose a research topic that would be more feasible with our timeline. Thus, our new research question is the following: 
 - Stable Diffusion 2.1 is the latest text-to-image model from StabilityAI. It takes in a prompt and generates four images. However, writing a detailed and accurate prompt can prove to be difficult and time consuming. While humans can try our best to predict what prompt works best for our intended image, machines may be better at recognizing underlying patterns to the prompts that better communicate to the stable diffusion model what image to generate. ChatGPT is a conversational language model developed by OpenAI. It uses deep learning techniques to generate human-like text based on the input it receives. ChatGPT is trained on a large corpus of text data and can be used for various natural language processing tasks such as text generation. How can we make the process of making prompts easier by utilizing ChatGPT’s learning and adaptive abilities to train it to write prompts? 

**Tues Jan 31: Brainstorm, Group Meeting**

Group Meeting: 
1. Went over assignment from mentors where we experimented with a Stable Diffusion model. Our goal was to give it a detailed prompt that would give us a New Year greeting card with a bunny on it. 
2. Discussed our opinions on writing a short paper for a deadline coming up in a month. The paper would most likely be a proposal of an idea or implementation that we have in mind. We will need to ask our mentors and advisor about this. 

Obstacles: 
1. When running program (2), my program still runs out of RAM. I have figured out that it crashes while loading the fine-tuned BARG model since it isn't loading it into the GPU memory. 

Questions for (2): 
1. Why freeze the token and positional embeddings in the summarization model? 

Brainstorm: 
1. How do I train an NLU model to check for answer correctness? 
2. Is building the tri-module system we were thinking about something that can be considered research or make a decent research paper? 
3. Can we go about generalizing the QAG system to other more difficult text like history textbooks or biology textooks? 

**Mon Jan 30: Brainstorm**

Brainstorm: 
1. Can we generalize the QAG model to history or science books? What technical changes or improvements would we need? How would we go about getting/making a quality annotated data set? 
2. Is there a need to improve the question quality/diversity that Yao's model currently achieves? What improvements to answer extraction, question generation, and filtering would we need?
3.  How are the heuristics rule passed and followed by the system? 
4.  Would the system currenly be able to generate more complex questions like the causes and effects of a historical event if we were to fine-tune it on a certain data set? 

## Week 3
**Sat Jan 28: Finished Pre-Processing Data, Attempt to Fine-Tune BART QG**

Readings: 
1. [How to generate text: using different decoding methods for language generation with Transformers](https://huggingface.co/blog/how-to-generate)

Progress: 
1. (0) After adding the code to write the train split into the files, I finished preprocessing the data and saved it to my Google Drive. I will need to check with my teammates and mentors about whether the changes I made to the code are correct. Also, my processed data looks different than the preprocessed data that is provided in the [GitHub](https://github.com/WorkInTheDark/FairytaleQA_QAG_System), so I will have to check if I did it correctly. 
2. (1) I began to fine-tune the BART QG model, but the program only ran for about an hour until a process error is called: 'died with <Signals.SIGKILL:9>'

Stuck On: 
1. Fixing process error while fine-tuning BART QG model. 
2. Running out of RAM when trying to generate QA pairs with QAG system. 

**Fri Jan 27: Readings, Preprocessed Data and Began to Fine-Tune BART QG**

Readings: 
1. [End-to-End Synthetic Data Generation for Domain Adaptation of Question Answering Systems](https://arxiv.org/pdf/2010.06028.pdf)

Progress: 
1. (0) I read through and annotated the code to understand what preprocessing was being done. I preprocessed data for Finetuning BART QG. Files include test.source, test.target, val.source. val.target. I was confused as to why there wasn't code to write the processed training data to a file, but I realized that I could just write that missing part myself, so I will be doing that tomorrow. 
2. (1) I was able to start fine-tuning BART QG with the preprocessed data that the GitHub repo provided. I fixed imports and file paths. Due to time constraints, I will continue this tomorrow. 
3. (2) I fixed import errors and file paths. I was able to get everything to run until my runtime crashed due to running out of RAM. I may need to upgrade my Colab. 

**Wed Jan 25: Begin to Replicate Yao's QAG System**

Progress:
1. Started looking through the files in the GitHub. Read through most of the code and tried to understand it.
2. Met with mentor Yujian to discuss timeline for potential paper and any confusions with my readings. 


**Tue Jan 24: Readings**

Readings: 
1. [Sequence to Sequence Learning with Neural Networks](https://proceedings.neurips.cc/paper/2014/file/a14ac55a4f27472c5d894ec1c3c743d2-Paper.pdf) 
2. [BART: Denoising Sequence-to-Sequence Pre-training for Natural Language Generation, Translation, and Comprehension](https://arxiv.org/pdf/1910.13461.pdf)
3. [Language Models are Few-Shot Learners](https://arxiv.org/pdf/2005.14165.pdf)

## Week 2

**Mon Jan 16: Learn Linear Regression and Gradient Descent**

I watched Andrew Ng YouTube videos on linear regression and gradient descent as part of his Machine Learning series. 

> Takeaways:
  
  1. Have some function J(θ<sub>0</sub>, θ<sub>1</sub>) and want min<sub>θ<sub>0</sub>, θ<sub>1</sub></sub> J(θ<sub>0</sub>, θ<sub>1</sub>)
  2. Start with some θ<sub>0</sub>, θ<sub>1</sub>
  3. Keep changing θ<sub>0</sub>, θ<sub>1</sub> to reduce J(θ<sub>0</sub>, θ<sub>1</sub>) until we end at minimum.

**Tue Jan 17: Model Training**

I learned how to load datsets as PyTorch tensors using the torchtext Field and TabularDataset. Batches are created with BucketIterator. I employ the BERT architecture with a single additional layer for output prediction with the class BERTNLIModel. The constructor initializes with bert, hidden dimension, and output dimension. The forward pass of the model gets embedded representation of the input and applies a linar layer 'self.out' to map it to the output. 

**Fri Jan 20: Mentor Meeting**


## Week 1

**Wed Jan 11: Review BERT**

I watched videos first to get an overview of how BERT and Transformers work. Then, I read articles to get a technical understanding. 

> Takeaway: BERT is made up of stacked encoders from transformer architect as per the name, Bidirectional Encoder Representation from Transformer

**Thu Jan 12: Understand NLI Task**

My mentors challenged my group to finetune pre-trained BERT model to do sentence pair classification with the MultiNLI dataset. 

> Takeaways:
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

