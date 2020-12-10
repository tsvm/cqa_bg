# Community Question Answering in Bulgarian

This repository contains data for the paper "Finding Good Answers in Online Forums: Community Question Answering for Bulgarian" by Tsvetomila Mihaylova, ivan Koychev, Ivelina Nikolova and Preslav Nakov.

It was published at [CLIB 2016](https://dcl.bas.bg/clib2016/proceedings/).

## Data

The data for the current study is collected from the largest online forum in Bulgaria - [BGMamma](https://www.bg-mamma.com/). 
The forum has topics in various categories, each topic is a thread with comments from different users. In
order to prepare the data in a format suitable for our task, we first selected topics with titles containing
‘въпрос’ (the Bulgarian word for ‘question’). The first comment in the topic is considered as a question.
The next five comments in the topic are considered as answers to this question. We annotated manually
80 questions with the first 5 answers from the thread for each of them, i.e., 400 question-comment pairs.
Each answer is annotated as either Good (it gives a direct answer to the given question) or Bad (it does
not give a direct answer to the question).

We split the annotated questions into training and test set. The training set has 50 questions with 5
answers each, i.e., 250 question-answer pairs. 

The test set has 30 questions with 5 answers each, i.e., 150 question-answer pairs. 

After the data was annotated, the topic categories, question texts, question subjects and comment
texts were translated from Bulgarian to English with the [Microsoft Translation API](http://www.microsoft.com/en-us/translator/translatorapi.aspx).

As an additional training data we use the Train-1 set from [SemEval-2016 Task 3](https://alt.qcri.org/semeval2016/task3/). From them, we took only the comments
on positions from 1 to 5 in the forum thread. The difference of the SemEval labeling of the comments is
that they also include Potentially Useful labels. We consider those labels Bad.

