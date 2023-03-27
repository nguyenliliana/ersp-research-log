# LILIANA'S RESEARCH LOG - WINTER '23

This research log is meant for me to record my learning and research progress. 

# Spring Break

**Sun Mar 26:**
- group meeting: paper brainstorm, test prompts, experiment design
- generate prompts and images

Thoughts: 
- does a good job at filling in missing modifiers
- should I teach it the aesthetic modifiers: 8k, highly detailed, trending on artstation, 8k, octane render, Unreal Engine, high resolution
- doesn't suggest relevant artist most of the time

**Fri Mar 24: Reading**

Reading: [Zero-shot Generation of Coherent Storybook from Plain Text Story using Diffusion Models](https://arxiv.org/pdf/2302.03900.pdf)

Prompt Generation Process by Paper: 
1. Provide LLM with sentences from the story and instruct to describe each scene.
2. Provide LLm with output from previous step and instruct to summarize each noun phrase.
3. Enhance quality of generated images by using magic words popular to users, such as "highly detailed" and "insanely intricate". A simple instruction like "If the main subject of the prompt is a person, add facial descriptions such
as ‘symmetrical face’ or ‘beautiful eyes’" enhances realism of human main subjects.
4. Employ use of style modifiers to generate images in specific style. 

## Week 10

**Wed Mar 15: Revise Diverse Exemplars, Group Meeting with Mentors**

**Tues Mar 14: Additive Prompting**

## Week 9

**Wed Mar 8: Mentor Meeting, Diverse Exemplars/COT**

Diverse Exemplars/COT: 
From my literature review, I found that LLMs can fuse the reasoning processes of different exemplars together to solve a query that requires multiple types of reasoning, so a good set of exemplars should consist of relevant exemplars that cover the reasoning skills required for solving the query. This is pretty much Chain-of-Thought prompting. I chose [three diverse exemplars](https://docs.google.com/document/d/1z-ZKM7LHr1ohqsfan0QUPpUKZQlNNYFXLSYIeFEZbX4/edit?usp=sharing) that cover different reasoning skills I though ChatGPT would need for prompt engineering. I found that this was the best prompting strategy by far. I was surprised to see how well ChatGPT was generating SD prompts just from three examples. Next steps include defining what a set of diverse exemplars are. 

Paper Brainstorm Feedback from Mentor Meeting: 
1. Find the best prompting strategy and make that the main point of the paper. What are the best exemplars? Remove one component at a time to demonstrate how each component actually helps with good prompt engineering. For example, remove the explanation component. 
2. Define the scope. What query of user input does our method work for?
3. Think about what story we want to tell. We leveraged ChatGPT's knowledge to... We can impplement a LLM to supplement SD that doesn't have the same knowledge. We illicit knowledge from ChatGPT by...


**Tues Mar 7: Paper Brainstorm, Natural Language Exemplars**

I worked with my group to draft a rough [paper outline](https://docs.google.com/document/d/1UoYjrJ8-V13xL8-g8GOOzgyDWkjvkwegPC_nJC6GvNI/edit?usp=sharing) to present to the mentors. My goal is to sophisticate our experiment design and finalize the research direction. 

Natural Language Exemplars: 
From my literature review, I found that natural language is also important for good exemplars, so I converted my previous demonstrations to full sentences. I also changed "Suggested Prompt:" to "Using the given and suggested prompt modifiers, I suggest a well-formatted Stable Diffusion prompt with articles and unnecessary words removed:". Also, I added two new exemplars since my previous exemplars were too similar. I compared the generated prompts from the full sentence exemplars and generated prompts from the previous non-full setnence exemplars. I found that the generated prompts from the full sentence exemplars were better in format and conciseness, but the quality/accuracy of SD images were not always better. 



**Mon Mar 6: Reading about AMA Prompting**

[Ask Me Anything: A simple strategy for prompting language models](https://arxiv.org/abs/2210.02441)

Takeaways:
1. Prompts that encourage open-ended answers are more effective than prompts that limits the model to output certain answers/token (such as true/false question).
2. AMA's prompt format consists of a two-step promoting pipeline. First generate questions based on the inputkk and then prompt the LLM to answer the generated questions. They found that this applies quite generally and improves performance. I will experiment with this format of prompting.
3. The paper also explains how to create prompt collections at scale by recursively applying the LLM itself using a chain of functional prompts, referred to as prompt()-chain. While this was an interesting idea, it is not within the scope of my research. 


Brainstormed ideas to experiment with, mainly from the two readings.
[Experiment Brainstorm](https://docs.google.com/document/d/1CKsv9c_BGfEm8GYSLL-N0up17KrlQJKJaRqzm3DyoUs/edit?usp=sharing)

**Sun Mar 5: Reading about Exemplars**

[Complementary Explanations for Effective In-Context Learning](https://arxiv.org/abs/2211.13892)


Takeaways: 
1. "Natural language also plays an essential role in constructing effective explanations." I will experiment with full sentence explanations. 
2. "LLMs can fuse the reasoning processes of different exemplars together to solve a query that requires multiple types of reasoning." I will experiment with using different examples.  
3. "Good set \[of exemplars] should consist of relevant exemplars that cover the reasoning skills required for solving the query." I will experiment with making my exemplars more diverse. Do one with suggesting missing information with feature parameters given, one with suggesting missng information with feature parameters beyond the ones given, one tat demonstrates the need to be explicit to stable diffusion ('cutting bread **with a knife**')

## Week 8

**Wed Mar 1: Lexica Examples**

I experimented with using Lexica examples with no specific strategy. I concatenated it to my query. For example: 
[User:]
*I will give you a series of sentence examples and I want you to extract and use the prompt parameters.* 
*Examples:
*1. infinite golden gate bridge, sticker design vector art, 8k, trending on artstation*
*2. golden gate bridge at sunset by Thomas Kinkade, green dragon flying above, Greg Rutkowski. trending on artstation, Unreal Engine, cgsociety, Hudson River School, 8k render*
*3.   Golden gate bridge,it is raining, night time , peaceful atmosphere, moody lighting , digital art , highly detailed , high contrast, beautiful lighting, award winning , trending on art station, photorealistic, 8k* 
*4. infinite golden gate bridge by Beksinski and Luis Royo, 8k, trending on artstation*
*5. octopus attacking golden gate bridge, vector art, 8k, trending on artstation*

*Q: With temperature 0, generate me a prompt for A photo of the Golden Gate bridge.*

The nonstrategic approach obviously did not work since I did not demonstrate to ChatGPT what I wanted it to do with the five examples. Since the quality of prompts on Lexica varies, my goal with Lexica examples is for ChatGPT to extract the prompt modifiers and consider them as suggestions. I was thinking that this would be helpful with bizzare user prompts that ChatGPT would not understand. 


**Tues Feb 28: Try OpenAI Playground, Teach Prompt Parameter, Temperature 0**

I played with OpenAI playground to see if temperature influences the generated prompt. I found that the prompts generated from temp = 0.5 and prompts generated with temp = 0 did not differ much. 

I experimented with controlling temperature with ChatGPT since I read that you could tell ChatGPT directly what temperature to control its creativity. I found that trying to "control" ChatGPT was not possible and beyond the scope of what I'm trying to do with this research. It defeats the purpose of using ChatGPT.

I was able to teach ChatGPT the lists of prompt parameters if could use when suggesting missing prompt information to the user. After introducing the task, I say "Use these prompt parameters:". I found that using the word "use" instead of "learn" was better, and ChatGPT started pulling prompt parameters from the given lists. However, I would like to experiment with ChatGPT using prompt parameters beyond them since I would like to see ChatGPT's limits/capabilities. 

**Mon Feb 27: Utilize ChatGPT API**

I got the ChatGPT API to work on Google colab. It works with the access code and the chat shows up on the official website/interface when run in Google colab. This makes it easier, since I can put my queries into an array and run the program rather than copy and paste every time. I also write the output to a .txt file which also makes it easier for me to record my progress and label the chat logs more efficiently.

## Week 7
**Wed Feb 22: Experiment with Explanation, Teaching Prompt Parameters & Rules, Using Prompt Templates**

Progress:
1. Building upon last week's progress, I wanted to see if explaining the suggestions would help improve the suggestions, but I found my explanations were inconsistent and rather limited how well ChatGPT understood the demonstrations. It also did not help ChatGPT give better suggestions. 
2. I experimented with providing ChatGPT with a list of prompt parameters that could be used for different parts of the prompt, I hoped that it would give it a better idea of what helpful and relevant prompt parameters look like. While experimenting to see if this helped with ChatGPT's prompt generation across a diverse set of prompts, I found that the 3-4 demonstrations were too limited. I tried feeding tailored prompts to ChatGPT to see if it would utilize the prompt parameters I gave it, but the prompt parameters it used were repetitive and it did not utilize the list of prompt parameters to use the most relevant ones. 
3. Next, I wanted to see if ChatGPT could learn the ideal prompt format from these [prompt templates](https://openart.ai/presets). While ChatGPT did well for prompts similar to the templates given, it did terribly with prompts outside of the scope of the templates it learned from.
4. Playground vs ChatGPT: Playground only takes one input and gives one output. I experimented with its settings to see if I could get the same or better result as ChatGPT, but I found that the suggestions it gave were repetitive. 

Experiment with next: 
1. Since 3-4 demonstrations is not enough, I want to utilize the Lexica API to see if I can grab 10 relevant prompt examples using their search function and feed it into ChatGPT using a ChatGPT API. 

## Week 6
**Wed Feb 15: QA Indicating Missing Prompt Info & Provide Suggestions**

Building upon my progress, I demonstrated to ChatGPT how to label and suggest missing information using this format: 

*Q: Gordan Ramsey slicing bread.* 

*A: Photo of Gordan Ramsey slicing bread with a knife. 
Type: Photo
Subject: Gordan Ramsey
Setting:  **Missing**- Setting is missing/not defined. Suggestion-Professional kitchen
Lighting: **Missing**- Lighting is missing/not defined. Suggestion-Dramatic
Colors: **Missing**-Colors are missing/not defined. Suggestion-Realistic
Art Style: **Missing**-Art Style is missing/not defined. 
Extra Details: Slicing bread with a knife.* 

*Suggested prompt: A photo of Gordon Ramsay, slicing bread with a sharp knife, in a professional kitchen, with dramatic lighting.*

ChatGPT does a good job at providing relevant suggestions, and the suggested prompt has more detail that results in a better/more accurate image. It demonstrates the ability to iteratively edit a prompt with the user's inputs to get a concise and detailed prompt to get the user's ideal image. For example, I started with "A basketball ball on an empty court photo" and ended with "A photo of a basketball ball on the hardwood floor of an empty indoor basketball court, with a warm toned lighting and shadows. The ball is bathed in bright, vibrant colors that pop against the cooler background." 

**Tues Feb 14: Try Fixing Initial QA Attempt to Indicate Missing Prompt Feature**

With my first try, while ChatGPT did a good job at recognizing the prompt features, some improvements that I wanted to make was to teach ChatGPT to somehow prompt the user for the missing prompt features. It would be tricky to teach ChatGPT to directly ask the users for the missing prompt information, so rather I experimented with this format for demonstrations: 

*Q: A painting of a Goldendoodle in a suit in the sky with natural light and bright colors.* 

*A: A painting of a cute goldendoodle in the sky, wearing a suit, natural light, with bright colors. This prompt specifies the following: 
Type: painting
Subject: Goldendoodle
Setting: In the sky
Lighting: Natural
Colors: Bright
Art Style: **Missing** Art style is missing/not defined. 
Extra Details: Goldendoodle is wearing a suit*

*Q: Gordan Ramsey slicing bread.* 

*A: Photo of Gordan Ramsey slicing break with a knife. 
Type: Photo
Subject: Gordan Ramsey
Setting:  **Missing** Setting is missing/not defined. 
Lighting: **Missing** Lighting is missing/not defined. 
Colors: **MIssing** Colors are missing/not defined. 
Extra Details: Slicing bread with a knife.* 

ChatGPT was able to do this exactly as intended. It shows the user what information they're missing in their prompt. Tomorrow, I will train ChatGPT to both label and give suggestions for missing information, and write a suggested prompt. 

## Week 5
**Thurs Feb 9: Experiment with "Average" User Input to Demonstrate "Bad" vs Good Prompts**

I wanted to try and get the user input of an "average" user who has never read the prompt book or has ever tried using Stable Diffusion before, so I got a friend to be the "average" user. I gave them a set of images from the prompt book, and asked them to write the best prompts that they think would best help the Stable Diffusion model generate the image. In my demonstrations to ChatGPT using the QA approach, I compared the ideal prompts to the user prompts. The first time, I tried explaining the prompt features in full sentences, but the explanations were inconsistent and results showed that ChatGPT didn't learn as well. The second time, I stated the prompt features simply, for example, "Type:Painting". The generated prompts with this approach used a lot of adjectives and emotions (more than other methods). The images from human prompt and ChatGPT prompt were pretty different. Overall, I don't think these methods proved effective. 

[Chat Log](https://docs.google.com/spreadsheets/d/1_NPT-HjAvyftwLCw-PQQaEWw9XjZz9y43KYsArF2RO0/edit?usp=sharing)

Experiment With: 
1. Bad vs Good Prompt: What is a bad prompt? What is a good prompt? How do I teach ChatGPT this? 
2. Prompting for missing prompt feature. 

**Wed Feb 8: Mentor Meeting- Share Results & Feedback**

After sharing the results, we agreed that one example is not enough and that more demonstrations are needed to teach ChatGPT.

Experiment With: 
1. Giving a before and after or good and bad comparison that explains what changes were made to create a good prompt. 
2. Do more demonstrations with explanation of generating good prompt. 
3. What ChatGPT knows and Stable Diffusion knows are different. For example, with the phrase, "slice bread", ChatGPT can infer that slicing is done with a knife, but if that is not specified to the Stable Diffusion model, then it will not generate a knife in the image. How can we bridge this gap? How can we teach ChatGPT the abilties/limitations of Stable Diffusion. 
4. How can we TRANSLATE human prompts with ChatGPT to be a suitable prompt for Stable Diffusion to understand. 

Task: 
1. Run same experiment of 20 prompts using more demonstrations. 

**Tues Feb 7: Group Meeting- Evaluate Images & Analyze Data**


We each generated images with 4 human prompts and ChatGPT-generated prompts. The Stable Diffusion model generates 4 images for each prompt. The 4 images from the human prompt and the 4 images from the ChatGPT prompt were organized on a single slide in random order, then the evaluators ranked the 8 images from best to worst by prompt relevancy.

I coded a program on Colab using Python and Pandas Dataframe to process our data to see which images ranked the highest, human or ChatGPT prompts. However, there a few bugs I need to fix. We used my teammates program to generate the following results:

[Results](https://docs.google.com/spreadsheets/d/1sTEZddQdgxiaxVnKF13IPFYWU6l8gwv8PrVOZBry3yA/edit?usp=sharing)

From the results, we came to an understanding that one example is not enough. The ChatGPT-generated prompts do not follow the ideal prompt format outlined in the prompt book. In addition, the ChatGPT prompts vary immensely depending on the original prompt that the user inputs. 

**Mon Feb 6: Mentor Meeting**

We presented our[Research Outline](https://docs.google.com/document/d/1BLhkD2DzUr9ck6EBEAwrdXmzzBvtF9M6HpePg_gwQEg/edit?usp=sharing) to our mentors. 

Meeting Takeaways: 
1. Evaluating the images by ranking them is a good idea. We need to decide the criteria(s) to rank with: image quality, object indentifiability, and prompt relevancy are a few ideas. 
2. Task: Generate 20 prompts with ChatGPT and compare them to the human-made prompts. For this round of experimenting with ChatGPT, we only explained the task, the prompt format, and one example to ChatGPT before asking for a prompt. 
3. With the QA approach, ChatGPT does a good job at understanding the different features of a prompt, so it's able to take information from the user input and infer the features that would suit it, making the prompt more detailed which I thought was good. However, our mentor raises the question about whether the prompt generated from ChatGPT is simply better because it has more details, and if so, would it make a fair comparison to the original prompt? I think our goal is more so to translate a typical user's prompt to a prompt that is more suited and understandable for the Stable Diffusion model. 

**Sun Feb 5: Brainstorm Ways to Evaluate Image Generation**

I read [Adversarial Text-to-Image Synthesis: A Review](https://arxiv.org/pdf/2101.09983.pdf) which discusses current strategies to evaluate text-to-image synthesis models. They explained metrics like R-precision, VS Similarity, Captioning Metrics, and Semantic Object Accuracy. However, User Evaluation is the best since humans are abel to evaluate image quality, image diversity, object fidelity, text relevance, mentioned objects, and positional alignment. 

As a result of my reading, I will probably have my group stick with human evaluations. 

I also watched the video [Images as Data: Best practices for storing and organizing your research images](https://www.youtube.com/watch?v=vlVj3U01UeY&ab_channel=DigitalScholarshipHub-McGillUniversity). The workshop provides useful strategies on managing and organizing research images. They introduced the image management software Tropy, a free open-source software that allows users to organize and describe photographs of research material. I will try out this software and see if it would be useful for my research. 

[Brainstorm Notes](https://docs.google.com/document/d/1WkwLcFZPeCvPqvG-_D_xceiKCzw3hMaTZt9TrItFYZQ/edit?usp=sharing)

## Week 4
**Sat Feb 2: Experiment With QA and Traditional Explanation Approach on ChatGPT**

[Chain-of-Thought](https://docs.google.com/spreadsheets/d/1_NPT-HjAvyftwLCw-PQQaEWw9XjZz9y43KYsArF2RO0/edit?usp=sharing)
Chain-of-Thought teaches the language model in a Q & A+Explanation format.

[Traditional Explanation](https://docs.google.com/spreadsheets/d/1YwU35PStXOOcBS0bK4MbHqWsoK0Nl6hTa-f6TwS3wJg/edit?usp=sharing)

**Fri Feb 3: Research Outline**

I worked on a [research outline](https://docs.google.com/document/d/1WkwLcFZPeCvPqvG-_D_xceiKCzw3hMaTZt9TrItFYZQ/edit?usp=sharing) to present to our mentors. It outlines our understanding of the research question and task, the different experimental approaches we are considering, and questions we want to explore. 

**Thurs Feb 2: ChatGPT API**

1. I experimented with using a [ChatGPT API](https://github.com/acheong08/ChatGPT) to automate our inputs and the responses. For the browserless version, I am running into an error saying that the model doesn't exist. I will try using a different API key to see if this gets fixed. I also tried using the Browser version, where I am running into many issues with getting the chrome driver to work. The chromedriver unexpectedly exits with status code -6 or there is an UnboundLocalError: local variable 'driver' referenced before assignment.
2.  I also tried following this [blog](https://blog.nextideatech.com/how-to-use-chatgpt-with-python/). It was a simple approach and seemed to work, but on my first try, the error message said, "You exceeded your current quota, please check your plan and billing details. So it appears that this approach is not completely free like the first approach. 
3.  Lastly, I tried following this [youtube video](https://www.youtube.com/watch?v=S3okwVkxDgA&ab_channel=1littlecoder). I get the same issue of the chromedriver unexpectedly exiting with status code -6.

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

