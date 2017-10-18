---
layout: post
title: Capstone Project - NAPLAN Analysis for a Public High School
published: true
---

![_config.yml]({{ site.baseurl }}/images/students.png)

## NAPLAN Introduction

NAPLAN is National Assessment Program – Literacy and Numeracy

It is a national test for Australia Students in Year 3, 5, 7 and 9.

The NAPLAN tests would be used to determine if students were performing either above, at or below the National Minimum Standard.

The common assessment scale has ten bands. Band 1 is the lowest band and band 10 is the highest band.

From 2017, year 9 students need to get a mark of _**Band 8**_ or above in their NAPLAN tests to be to be eligible for attaining HSC.

Students who don't meet the minimum standard in their year 9 NAPLAN will have to sit extra test to reach HSC.

## The Public High School

My clinet for this project is a Public High School, which is one of the largest government schools in NSW.

The school would like to know which question they need to spend some additional time on to improve the Y9 Naplan score. They also want to identify thoes students at risk of not meeting the minimum standard, which is Band 8 in y9 naplan test. 

![_config.yml]({{ site.baseurl }}/images/q&band.png)

**NAPLAN includes both Literacy and Numeracy test, my project will focus on the numeracy test only.**

## Year 9 Numeracy
Firstly, let's see how is this school's performance in Y9 Numeracy test from 2012 to 2017.
In the below diagram, the blue part is the percentage of students who has reached band 8 and the orange part is the percentage of students who has scored Band 7 and below.

![_config.yml]({{ site.baseurl }}/images/y9num.png)


The average percentage of the students who has pass the numeracy test is 83%, which is pretty good because the average percentage for NSW students in 2016 is around 50%.

The orange part is the target of my project. I need to identify those students based on their previous performance. 

## Exam Questions Analysis

Before the prediction, I would like to find out is there any particular question type that teachers need to spend some additional time on.

![_config.yml]({{ site.baseurl }}/images/10questions.png)

The plot above shows the 10 Questions with lowest average score. All the question score is on a scale of 0-1. The tops 3 is Right-angled Triangles, volume and area, which has an average score less than 0.4. That means more than 60% students failed to answer those questions. Thus, those are the questions that teachers should pay more attention on.


## Verbs

There is another interesting feature in the questions that is the verbs.

By understanding the verbs, students recognize what the examination questions required and expected.

![_config.yml]({{ site.baseurl }}/images/verbs_all3.png)

The upper left picture shows all the verbs that has been used in Y9 Naplan Numeracy test from 2012 to 2017. It shows how often a verb appears in exam questions. Calculate, identify and solve are the three most frequently used verbs. 

The upper right chart displays the 5 verbs with lowest average score. The reason why those verbs get a lower score is probably because they do not appear frequently in the exam questions. student were not sure what the questions is asking. Their answer is not on the right direction.

So I suggest that teachers should spend addition time on explaining how to answer the questions with those verbs. 

## Prediction

![_config.yml]({{ site.baseurl }}/images/predictions.png)
 
The target is to predict the outcome of this student whether she can reach band 8 in Year 9 or not. The variables take into consideration is the performance in Y7 Numeracy Naplan test, that is the score for each question for this student.

After comparing with different models, such as decision tree, k nearest neighbours, I have chosen Logistic Regression as my prediction model. The reason why I choose this model is because this prediction is roughly linear, that means if a student is doing well in Y7 test then she is more likely to pass her Y9 test. Logistic Regression is a liner model which will work better in this situation.

After training this model, here are the most predictable questions in the model: 

1. Fractions, Decimals and Percentages 
2. Data 
3. Patterns and Algebra

Thus, this model tells me that if a student gain a higher score in those 3 question in Y7 NAPLAN, she is more likely to pass the y9 exam.

The evaluation tool I used is cross validation, train split test and roc auc score. The average score is 89%.


## Application for 2018 and 2019 Students

I use this model to predict the Numeracy Band for student who will take Y9 Naplan in 2018 and 2019.

In this table, high risk indicates those students has a very high probability of failing the y9 test. The minimal risk implies that those student are very likely to reach Band 8 or above.
There are around 15% students are in Medium and High risk that teachers should pay more attention on.



Another application for my model is to find out the performance for a particular student. Here are 3 random student I have selected from 2018 students. 

By giving the student ID, if this student information is in my dataset this model can shows the student's risk level and the top 3 questions that she need addition help with.


## Future Works

There are some other features that may affect the Y9 Naplan Band. To increase the accuracy, some factors may be taken into consideration. For example, does a student like math or hate math? Do they have extra lessons outside the school during the weekend?

NAPLAN include both Literacy and Numeracy test. I will complete the Literacy part analysis.

Furthermore, I would like to make a webpage. The website visitors only need to submit the Student id, if this student is in my dataset. The webpage will shows that for each subject, what is the risk level for Y9 NAPLAN and the top 3 questions she need to improve.


