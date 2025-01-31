# Solving Difficult Math Problems
**Members: Tonyaradzwa Chivandire, Salih Erdal**
![](mathematics.jpeg)

## Project Description

This project will focus on training a neural network (NN) to solve math problems that are given in text form. 

## Introduction

Can a computer learn to solve math problems? This question motivates our study, and we seek to explore computers' problem-solving abilities in different areas of math by utilizing neural network architectures, e.g Recurrent NNs. 

The difficulty in teaching computers how to solve problems lies mainly in the fact that computers cannot "digest" a problem in the same way that humans do. When humans encounter problems, they extract the relevant information from what they are given; they decipher the pragmatic meaning of the terms to identify what the question is asking and apply a sequence of steps to arrive at a solution by using techniques that are not immediate in the questions. This is called mathematical reasoning, and whether computers can learn mathematical reasoning forms the basis of our inquiry. 

Before going into what exactly will constitute our research, we present a brief overview of the current literature. The area of using ML algorithms to teach computers how to solve math quesitons is relatively new, since it seems to be quite a challenging task that isn't very clearly defined. Since solving all kinds of math problems is not conceivable, current research usually focuses on solving problems in specific areas of math. Consequently, there are different methods tried for solving problems in different fields. One of the seemingly easier kinds of problems that people have focused on as proof of concept are arithmetic word problems. For example,[**Text2Math: End-to-end Parsing Text into Math Expressions**](https://arxiv.org/abs/1910.06571) by Yanyan Zou, Wei Lu. 2019 focuses on parsing arithmetic word problems and equations in a tree structure, which then can be solved. However, this method of creating expression trees is limited, since it is conceivably hard to turn most of the more interesting questions into a tree format. A more common approach to developing more generalizable mathematical reasoning abilities for computers is to use Recurrent Neural Networks. In these kinds of papers, the task of solving math questions is treated more like a machine translation/NLP task so that each problem is "translated" to a solution. For example, a study done by the Facebook AI team uses sequence-to-sequence models by feeding the NN a sequence of expressions representing math problems. Similar to the other study, this study mainly focuses on problems that can be converted into a tree structure, which are then converted to a sequence of expressions. Another study by David Saxton et al. similarly used LSTM and seq2seq models. However, they differed in their approach by inputting problems in free text format instead of preprocessing them into a structure. They generated their own dataset of problem-solution pairs in textual input/output form, and they compared the performances of the two models. 

In our research, we will try to implement the method that Saxton et al. applied in their paper and will use the synthetic dataset from their study in doing so. However, we will initially limit ourselves to trying to train a model to solve problems in only one field, which we might then apply to other fields. Through this research, we hope to get a better understanding of LSTM architectures by doing the implementation ourselves, and getting an intuition of why it might be better at solving some kinds of problems compared to other models. We think their method overcomes the difficulty of having to structurally represent problems in some format, and seems most open to experiment on. 

Some techincal challenges we anticipate facing include creating meaningful embeddings, deciding how to parse the input, and getting a sound understanding of how we can best utilize the LSTM architecture for our own problem. We also have to deal with limited computing resources, and we expect the size of our training dataset to potentially decrease the accuracy of our model. Minimally, we expect our model to perform with 70% accuracy for the arithmetic problems, which will be our first and primary focus.

After completing our research and training our model, we hope to be able to get a sense of what kinds of problems our model is best at solving. We might also compare the results of our study with those in Yanyan et al.'s paper that tried to create expression trees to solve arithmetic word problems. 

## Methods

where is data coming from?
  * https://github.com/deepmind/mathematics_dataset

what neural network architectures will we use?
  * we will try LSTM and sequence to sequence.

input type and shape:

output type and shape:
  
## Ethical Sweep

The model that we will be training may be used for good purposes, such as checking automatically if a student got the right answer in a question. If our model or future work can find solutions to problems that are not easily solvable by humans, it might lead to further discussions about the nature of some problems.  

## Referenced Works

[**Text2Math: End-to-end Parsing Text into Math Expressions**](https://arxiv.org/abs/1910.06571)
(Yanyan Zou, Wei Lu. 2019)

[**Using neural networks to solve advanced mathematics equations**](https://ai.facebook.com/blog/using-neural-networks-to-solve-advanced-mathematics-equations/)
(Facebook AI Blog)

[**ANALYSING MATHEMATICAL REASONING ABILITIES OF NEURAL MODELS**](https://openreview.net/pdf?id=H1gR5iR5FX) (David Saxton et al.. 2019)

[**Solving Math Equations with Neural Networks**](https://ai.plainenglish.io/solving-math-equations-with-neural-networks-f015351995e8)(Blog post)
