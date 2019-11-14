
# Bidirectional Sequence Models - Lab

## Introduction

In this lab, we'll learn to make use of **_Bidirectional Models_** to better classify sequences of text!

## Objectives

You will be able to:

* Understand and explain the basic architecture of a Bidirectional RNN. 
* Identify the types of problems Bidirectional approaches are best suited for. 
* Build and train Bidirectional RNN Models. 

## Getting Started

We're going to use a **_Bidrectional LSTM Model_** to build a model that can identify toxic comments on social media. This dataset comes from the [Toxic Comment Classification Challenge on Kaggle](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge) in partnership with Google and Jigsaw.

## The Problem

From the "Data" section of the Kaggle competition linked above:

"You are provided with a large number of Wikipedia comments which have been labeled by human raters for toxic behavior. The types of toxicity are:

* toxic
* severe_toxic
* obscene
* threat
* insult
* identity_hate

You must create a model which predicts a probability of each type of toxicity for each comment."

This tells us a couple things about the problem, which will affect the overall architecture of our model. Although this may technically be a multiclass classification problem, in practice, our model will treat each comment as 6 concurrent instances of binary classification. This is because a toxic comment can fall into one or more of the categories listed above--for example, a  comment may be toxic, obscene, threatening, and insulting, all at the same time. 



