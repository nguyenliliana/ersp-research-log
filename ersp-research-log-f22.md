# LILIANA'S RESEARCH LOG
## [Reading Logs](https://docs.google.com/document/d/1PoUccoQWEsk7Ggka9py5NHr3Jg__zT7L_zBdZ5leOo0/edit?usp=sharing)

## Project Description
The goal of this research is to leverage automatic question-answer generation to develop an integrated system where teachers can collaborate with AI to create and customize interactive reading resources with question-answering functions for their students from kindergarten through second grade. Throughout this project, students will have a chance to 1) develop innovative AI models that expand the state-of-the-art NLP techniques (e.g., BERT, GPT) for automatically generating question-answer pairs for reading materials and customizing the training to meet the unique requirements of an educational context; and 2) building a dialog system with graphical user interfaces that is able to a) ask children a question, b) provide tailored feedback and explanation to children’s response, and/or c) rephrase the original question (usually open-ended) to a multiple-choice question as a way of scaffolding if the children do not answer the original question or answer it incorrectly.

# Week 10 (11/27-12/3)
## Meeting Summaries
**Research Group Meeting w/ Prof. Chang and Grad Mentors**
- No meeting this week for Finals.

**Meeting with Chinmay**
- Tuesday, Nov. 29
- We went over our proposal with Chinmay to receive further feedback on what we can improve on.  Main takeaways is to make our subproblems more clear within our problem statement, proposed solution, and evaluation. Overall, we fixed Prof. Mirza's concerns from her previous feedback. 

## Weekly Goals:
- [ ] Final Proposal Revisions
- [ ] Presentation Preparation

**Accomplished:**
**Sunday (4 hours) Proposal Revisions & Presentation)**
I spent a majority of my time revising the related works section. We had written this section early on in the quarter, so it was poor in quality and understanding. I reread the related research papers and rewrote a majority of the related works section to better explain the technology, their shortcomings, and relation to our research. I also removed papers that I found irrelevant to our specific research topic. In addition, I improved flow by fixing transitions and making connections between the subsections and technology mentioned. In addition, I revised the introduction of the Proposed Solution to be more clear in explaining that our system will utilize a QAG module and Dialogue system together and how they would work together (although this is later revised by another team member after our mentors clarify that we will have 3 submodules instead consisting of QAG, Answer Check, and Next Turn Policy).

**Tuesday (3 hours) Proposal Revisions**
Our group highlighted the 3 main subproblems that our research is trying to solve, so I took upon the task of rewriting the Problem Statement section to encompass the general problem we were seeking to solve and introduce and explain the subproblems. Furthemrore, I tried my best to explain the Answer Check Module and Next Turn Policy Module. For the Answer Check Module, we could either build an NLU module, or with time constraints we could set a threshold and use the BLEU score to verify correctness. For the proposal, I chose to explain the method using BLEU score (however we will try to figure out the specifics of the NLU method). The design behind the Next Turn Policy is also unclear. Our mentors told us we can hard code a rule set for this part. From what I resaerched, we would create a mapping function that would map the current state to the next action based on the output from the Answer Check module. 

# Week 9 (11/20-11/26)
## Meeting Summaries
**Research Group Meeting w/ Prof. Chang and Grad Mentors**
- No Meeting because Thanksgiving

**Research Group Meeting (Undergrads)**
- Meeting during Thanksgiving TBD

## Weekly Goals:
- [X] Proposal Revisions
- [X] Grad Student Interview

**Accomplished:**
**Sunday (3 hours) Proposal Revisions**
We had a group meeting to make large revisions to our proposal.  Our main concern was our motivation, research context, and problem statement section.  Since this was the first section we wrote weeks ago, it had many flaws and was not aligned to the main point of our research project.  So, we decided to start over from scratch.  We reevaluated as a group what we wanted the main takeaways to be and wrote it accordingly.  We had disagreements on what the purpose of the context section shoudld be and what content should be included for it. We decided to follow what the majority wanted and would see what feedback we would get for it on Wednesday from Prof. Mirza.  I wrote the first part of the context which went over the first sub-module of the QAG model. In addition, I wrote an introduction paragraph for the proposed solution which gave an overview of the final product before the subsections go into more technical detiail.  Lastly, I revised the BERT subsection of the related works section.  I wanted to explain the different models more clearly and point out how they build upon each other and how they differ.

**Wednesday (1 hour) Grad Student Interview**
I interviewed Vaishali, a PhD studnet. Talking to Vaishali was extremely eyeopening in aspects of grad school involving research, academics, personal experiences, and career.  What surprised me was that grad students have felt discouraged or have had second thoughts about their research, and that this is a normal thing.  Over time, you learn to accept it and learn new ways to move through times where you feel stuck or discouraged.  In the end, you are working in a field/area that you are passionate in!  I learned that it’s important to try everything in undergrad, even the topics that you think you don’t like.  When you find a passion/interest, it will make your decision for grad school a lot easier, but it is normal to switch interests in grad school as well.  I feel like the grad student life is less mysterious now.  As a grad student, you have a flexible schedule of research, class, work (TA), and free time.  You build friendships with peers and professors.  Industry internships for grad students are different, and going into industry for a fulltime role as a grad student allows you to find specific roles of your interest that is beyond software engineering.  As a grad studnet, you are able to build a holistic view of computer science as a whole, further than you would in your undergrad.  Grad students have their ups and downs in their research, but ultimately they are working in a field that they are passionate with, and any progress is something to be proud of.  


# Week 8 (11/13-11/19)
## Meeting Summaries
**Research Group Meeting w/ Prof. Chang and Grad Mentors**
- Nov 18 @ 6pm
- Present individual text classification models. 
- Reflection: Our models worked, but they are not conventional uses of Bag of Words or TF-IDF.  The mentors explained to us the conventions and which parts of our code that we could improve. I found P(label) incorrectly since I divided the number of words in the label by the total number of words of all the labels, when instead, it should've been by number of docs instead of words.  

**Research Group Meeting (Undergrads)**
- Monday Nov 14: Text Classification Model Progress Check- exchanged ideas and helped each other fix bugs (Virtual)
- [Wednesay Nov 16: Text Classification Model Finalization & Revise Proposal (In-Person)](https://docs.google.com/document/d/1RYQG6mx5mbA8hwumKXg3fXIxW1G_2asDkg1xo9kUVBo/edit?usp=sharing)

## Weekly Goals:
- [X] Draft Evaluation and Implementation Plan
- [X] Peer Review Proposal
- [X] Text Classification Model

**Accomplished:**

**Sunday (2 hours) Evaluation and Implementation Plan**
I attended a group meeting with my fellow undergrads where we discussed the proposed solution section.  The previous week, we had asked our grad mentors what the exact technical impementations the project would be executing.  He was extemely helpful in sending us a detailed response with an overview of the solution and reference papers.  The solution consisted of two modules, so we divided ourselves into two group to focus on each module.  I decided to take on the question-answer pair generation module.  I read about the technical contributions and detailed setup and translated my understanding over to the draft.  

**Tuesday (1 hour) Peer Review Proposal**
I was assigned Professor Bultan's group's project proposal.  Their project is about implementing a working prototype onto angr which will utilize differential symboic execution on order to recognize functional equivalence within code blocks.  Their project is also aiming to have a faster runtime performance.  I read through it three times in order to give a proper review of their introduction, related works, proposed solution, implementation plan, and evaluation. I prepared notes to provide feedback in class.  My two main suggestions is to make a clear distinction as to what their new technical contribution is and to define their metrics more clearly in their evaluation plan. 

**Wednesday (3 hours) Text Classification Model**
I finally had a breakthrough in my understanding of how to build a Text Classification Model. After watching a Naive Bayes video, I realized that it wasn't as complex as I orignally thought it had to be.  I completely started over, and wrote my code from scratch.  I tokenized the words and built a vocabulary using the training data.  Then, I found the term frequency of every word in the vocab for each label.  Next, I coded the Naive Bayes function which used the equation P(label|sentence) = P(label)* P(word1|label) * P(word2|label) * ... to return the label with the highest probabilty.  After testing my model on the testing data, it had an 89% accuracy.  

# Week 7 (11/6-11/12)
## Meeting Summaries
**Research Group Meeting w/ Prof. Chang and Grad Mentors**
- Meeting canceled for holiday. 

**Research Group Meeting (Undergrads)**
- [Monday, Nov. 9 (Virtual)](https://docs.google.com/document/d/1aZAPX7DiJDm612g00SXtV9bSFanentMxM5fggmdxGR4/edit?usp=sharing): Text Classification Model & Proposed Solution Section
- Friday, Nov. 11 (In-Person): Text Classification Model Progress Check and Proposal Revisions 
- Absentees: None

## Weekly Goals:
- [X] Draft Proposed solution section.
- [X] Read papers assigned by mentors. 
- [X] Reflection 3

**Accomplished:**

**Monday (2 hours) Proposed Solution**
I attended a group meeting with my fellow undergrads where we discussed the proposed solution section.  The previous week, we had asked our grad mentors what the exact technical impementations the project would be executing.  He was extemely helpful in sending us a detailed response with an overview of the solution and reference papers.  The solution consisted of two modules, so we divided ourselves into two group to focus on each module.  I decided to take on the question-answer pair generation module.  I read about the technical contributions and detailed setup and translated my understanding over to the draft. 

# Week 6 (10/30-11/5)
## Meeting Summaries
**Research Group Meeting w/ Prof. Chang and Grad Mentors**
- Friday, Nov. 4 @ Phelps 3530
- Present our understanding of introductory PyTorch
- Reflection: We need to have a lower level of understanding of the technicalities of the text classification model. 

**Research Group Meeting (Undergrads)**
- [Monday, Nov. 9 (Virtual)](https://docs.google.com/document/d/1aZAPX7DiJDm612g00SXtV9bSFanentMxM5fggmdxGR4/edit?usp=sharing): Text Classification Model & Proposed Solution Section
- Absentees: None

## Weekly Goals:
- [X] Draft Proposed problem and Related Work
- [ ] Read papers given by mentors. 
- [X] Finish Introduction to Pytorch. 
- [X] Understand Text Classification Model.
 

**Accomplished:**
**Sunday (2 hours) Proposal Part 1: Proposed Problem and Related Work**
During our group meeting, we brainstormed for the "Research context and problem statement" section.  After discussing thoroughly, we put our ideas into full and concise sentences.  We spent time revising and finalizing it in order to make a clear introduction and transition to our problem statement.  We made a list of clarifying questions to ask Prof. Chang and our mentors. In addition, we also chose three references to discuss.  I chose one and analyzed how others have addressed similar problems and why are their solutions were not sufficient.  

> SDNet: Contextualized Attention-Based Deep Network For Conversational Question Answering

Conversational Question Answering (CoQA) requires a model to be capable of reading a passage and answer questions in dialogue.  To incorporate conversation into reading comprehension, models are required to fully understand the given passage and context of previous questions and answers to provide accurate responses.  So, traditional neural MRC (Machien Reading Comprehension) models are not suitable to be directly applied to this scenario. The paper proposes SDNet which is a contextual attention-based deep neural network for the task of CoQA with state of the art results where its effectiveness outperformed the previous best model by 1.6% F1.  This was achieved by implementing the use of interattention and self-attention along with Recurrent BIdirectional LSTM layers.
> Generate: A NLG system for Educational Content Creation

Generate is a proposed AI-human hybrid system that addresses the generation of assessment content in an efficient and scalable way.  The system implements NLG approaches and Transformer architecture to leverage substantive pretraining on several generic text as corpora to produce sophisicated context-dependent text as the basis for item creation.  Their solution is insufficient because it does not provide the option for free response style questions.  Another issue, is that Generate requires for specifications such as providing a content map or item type and topics to be generated, but the general user may not understand how to provide the best inputs for the AI model to perform well, which would be unintuitive for teachers.  
> Asking Questions the Human Way: Scalable Question-Answer Generation from Text Corpus

ACS-QG is proposed by Liu et a. to improve on the ineffectiveness of current models to generate quality and diverse question-answer pairs for unstructured text  It's BERT-based and extracts multiple types of information from text to improve question generation.  While the model can create the original question-answer pair, it is insufficent in creating follow up questions based on the user's answer. 


# Week 5 (10/23-10/29)
## Meeting Summaries
**Research Group Meeting w/ Prof. Chang and Grad Mentors**
- Friday, Oct. 28 @ Phelps 3530

**Research Group Meeting (Undergrads)**
- Friday Oct. 28 @ Library
- Absentees: None
- Tasks: Finish Research Context and Problem Statement and Related Work
- Goals: Finish Intro PyTorch & Text Classification Model


## Weekly Goals:
- [X] Complete literature search part 2
- [X] Reflection 2
- [X] Complete literature search part 3
- [X] Research meeting
 

**Accomplished:**
- Attended NLP Reading Group
- Completed Introduction to PyTorch

**Sunday (1.5 hour) Extended Literature Search**
I extended my literature search to include papers after the BERT paper and chose specific ones that aligned more closely with our research topic. I utilized Google Scholars to find papers that cited the BERt paper.  In addition, I searched the ACL proceedings to find recent papers in the past two years that involved models that implemented QA and conversation.  I organized my findings on the group Mural and added the papers to the Related Works and References section of our project proposal draft.  


# Week 4 (10/16-10/22)
## Meeting Summaries
**Research Group Meeting w/ Prof. Chang and Grad Mentors**
- Weekly meetings start Week 5

**Research Group Meeting (Undergrads)**
- Friday, Oct. 21 @ Zoom 
- Absentees: None
- Tasks: Finish Extended Literature Search & Complete Mural and Update Overleaf doc
- Goals: Finish Intro PyTorch & text classification model


## Weekly Goals:
- [X] Finish preparing for teaching topic. 
- [x] Literature Search and Proposal Preliminary Work
- [x] Research group meeting
 

**Accomplished:**
- Attended the NLP Reading Group for the first time!

**Sunday (4 hours) Teaching Topic** 
- I chose to teach about transformers, since it is an essential part of NLP models and specifically BERT. First, I did general research on the Transformer architecture, and then, narrowed my research to better explain the different components/steps.  After finishing my research notes on Google Docs, I made a Google slides presentation where I used mostly visuals to illustrate my teachings.  I prepared speaker notes to assist my presentation. 

*Teaching Topic Questions*
> What do you want your "student" to be able to know and do at the end of the session?

I want my student to be able to explain the steps within a Transformer architecture.  From the presentation, they should understand how a transformer is able to an attention mechanism that learns contextual relations between words in a text.    

> How are you using visual aids for your explanations? 

My slides are mostly visuals that depict multiple steps and concepts within the Transformer architecute, such as self and cross attention.

> What exercise or review question will you have your "student" perform or answer at the end of your session?

For my exercise at the end, I will provide a picture of the Transformer architecture with no labels, and ask them to explain the image as much as they can remember and understand.  At the end, I will fill in missing areas.   

**Tuesday (0.5 hour) Literature Search**
- I completed the first part of our literature search which was to find existing works that most closely relate to our BERT paper.  I chose works that were referenced multiple times throughout the paper and contributed important insight. I organized my findings on the group Mural with the work's title, venue, and authors. I used arrows and labels to show the correlations. 




# Week 3 (10/9-10/15)
## Meeting Summaries
**Research Group Meeting w/ Prof. Chang and Grad Mentors**
- Date/Time: Friday Oct. 14 6-7pm  
- Weekly meetings Friday 6-7pm (in-person @Phelps 3530).
- NLP Research Meeting: Tues 3-4pm (@HFH 1132).
- Slack communication will be set up.
- Plan is to have weekly assignments and present our understandings (mainly PyTorch).

**Meeting with Chinmay**
- (starts in 2nd half of the Fall quarter)
- New Insights, Challenges Resolved, Questions:   

## Weekly Goals:
- [X] Finish deeper reading of research paper
- [X] Prepare for 3-min presentation on BERT paper
- [X] Choose a teaching topic
- [X] Prepare to teach group on technical topic
- [X] Have second group meeting


**Accomplished:**
- Attended Tuesday CS 165B lecture
- Had first meeting with Prof. Chang and grad mentors

**Sunday (1 hour) Deeper Reading**
-  I completed a deeper reading on the BERT research.  Since I was reading through it again after clearing up confusions with terms and concepts, I had an easier time progressing through the paper.  I also gained a better understanding by reading through it again.  I like summarizing my findings and understandings with the guided questions since I'm able to organize my thoughts and the main parts of the paper for myself.  I referenced my part 2 readings notes for the class presentation.  

**Tuesday (1.5 hours) Teaching Topic** 
- I chose to teach about transformers because new ML models, such as BERT, are based on transformers. BERT paper talked a lot about transformers, and my group didn't truly  understand what they really are. I think learning and teaching about transformers will widen my understanding of machine learning and NLP models. 
- I took notes from YouTube videos by Google Cloud Tech.  In addition, I searched and took notes on terms and concepts from the videos that were unclear, and I found visuals that illustrated the concepts.   

# Week 2 (10/2-10/8)
## Meeting Summaries 

**Team Meeting**
- Friday, Oct. 7 @ Library
- Absentees: Edwin
- Tasks: Prepare for presentation on BERT paper
- [Link to Notes](https://docs.google.com/document/d/1WacnE0pgiFf6AJWSzdX2_lNgiEeIEsQM5zRqOD7xafo/edit?usp=sharing)

**Meeting with Chinmay**
- (starts in 2nd half of the Fall quarter)
- New Insights, Challenges Resolved, Questions:   

## Weekly Goals:
- [X] Initial group meeting
- [X] Research paper prep
- [X] Read and respond to a research paper
- [X] Set up group page and message Chinmay
- [X] Contact grad mentor about preferred form of communication
- [X] Ask advisor/mentor about 30-min meeting separate from research group meeting


**Accomplished:**
- Attended CS 165B Tuesday Lecture

**Sunday (0.5 hours) Research Paper Prep**
 - I read and took notes on _[How to Read an Engineering Research Paper](https://cseweb.ucsd.edu//~wgg/CSE210/howtoread.html)_ using a [Google Doc](https://docs.google.com/document/d/1unK0qxUArQEp5eAXJGOXkT8TbEykZZeIV8mQt6xxS7s/edit?usp=sharing). I organized the key parts of the article that I would want to reference later on when I read a research paper such as the essential questions and tips.  I found that the article was helpful in preparing me to read a research paper efficiently. 

**Monday (0.25 hours) Contacted Advisor/Mentor**
- I drafted an email with Shamita to contact our advisor and mentors about their preferred form of communication and choosing a weekly meeting time that would work best for all of us.  I set up a when2meet for my group to fill out and send to our advisor and mentors to give them a general idea of our availability.  We sent the email draft to our group to get any thoughts or suggestions.  We made any final edits with the help or our teammates, and Shamita sent the email with us CC'ed.  

**Tuesday (1.5 hours) Read Research Paper**
- I read, annotated, and took notes on the research paper, “BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding”.  My [notes](https://docs.google.com/document/d/1PoUccoQWEsk7Ggka9py5NHr3Jg__zT7L_zBdZ5leOo0/edit?usp=sharing) followed the guiding questions that Prof. Mirza provided us.  I found the guiding questions extremely helpful, especially with approaching a long and unfamiliar research paper.  I was able to read more purposefully and it helped me get a better understanding of the research paper.  It took me 1.5 hours which was longer than I expected.  I think next time, I will be able to read more efficiently.  

**Friday (1 hour) Group Meeting**
- We had a group meeting on Friday 5-6pm. I took meeting notes, so that we could keep a record of what we discussed and also have a place to brainstorm.  Edwin was absent, so the meeting notes would be very useful for him to catch up on what he missed.  To summarize what we accomplished during our meeting, we finalized and sent our group page to Cinmay, prepared for the 3-min presentation on BERT, brainstormed teaching topics for Week 4, sent a follow up email to Prof. Chang and our mentors, and set learning goals for the group.  For more details, the meetings notes are linked [here](https://docs.google.com/document/d/1WacnE0pgiFf6AJWSzdX2_lNgiEeIEsQM5zRqOD7xafo/edit?usp=sharing). 

# Week 1 (9/25-10/1)
## Meeting Summaries
**Grad Mentor/Research Group Meeting**
- Date/Time/Location, Attended, Presenter(s), Learned, Interactions with Prof, Tasks, Questions 

**Team Meeting**
- Date/Time/Location, Attended, Understandings, Tasks for the Week, Questions


**Meeting with Chinmay**
- (starts in 2nd half of the Fall quarter)
- New Insights, Challenges Resolved, Questions:  

## Weekly Goals:
- [ ] Attend research group meeting and record attendance
- [X] Set up research log
- [X] Complete Reflection 1: Identity and ERSP preliminary thoughts
- [X] Reflect on research logs

**Accomplished:**
* Signed ERSP contract
* Attended Chang's Tuesday Lecture for CS 165B
* Attended Chang's Thursday Lecture for CS 165B and got added to Gauchospace. 
* Asked Chang about his research meetings and will receive information in an email in the future. 
* Finalized group meeting date/time: Friday 5pm
* Set up discord server for group

**Monday (1.5 hours) Log Set Up & Reflection 1**
- To set up my research log, I chose to do it in a github repo since it can be best organized with my other CS projects.  I also think it would be a good chance for me to become familiar with using Markdown.  

**Tuesday (0.25 hours) CS110/ERSP Contract & Study Consent Form**
- I read and signed the ERSP contract and Study Consent form with the PDF editor Kami and submitted it to Gauchospace. 

*Initial Thoughts on ERSP*
> What I am most excited about in ERSP. 

I am excited to apply my skills in a professional research setting.  I haven't had enough professional experience where I was able to utilize my programming skills to its potential, so I'm excited to learn a lot from working in labs with a team and with faculty members.  I look forward to working with AI, ML, and NLP concepts for the first time and cultivating new skills in this area.  

> What I am most nervous about in ERSP. 

I'm nervous about not being able to contribute to the research project as well as my teammates.  I definitely will not lack in effort and determination, but my wish is to be a reliable and active team member that is able to contribute to the project in many different ways.  I will be sure to stay motivated this quarter and prepare myself by learning the related skills and attend CS 165B as recommended.

*Log Reflection*

I was impressed by how organized and detailed the logs were.  Tony and Jacqueline both used Github for their research logs, so their format looked very similar.  Tony used more checkmarks where as Jacqueline used more bullet points.  Miranda used google sites so she is able to make her headers, subheaders, and parts look more distinct and thus easier to read.  I think the logs are useful for researchers to keep track of their progress especially when you set weekly goals and keep track of your accomplishments.  The detailed logs are helpful for the researcher to look back on but also educational for others who read the journal to see and understand what happened throughout the 10 weeks.  It's impressive to see how they accomplish their goals each week, and set higher goals for the next week each time. 
