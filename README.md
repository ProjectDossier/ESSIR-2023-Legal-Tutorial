# essir-legal

## Task definition:

The task of statute retrieval aims to identify the relevant statutes (i.e., candidate document) given a short description of a legal situation (i.e., query).
Our corpus is a set of 2,914 statutes, and out of them, there are 197 satutes that are relevant to at least one or more queries. Each statute (candidate document) contain a title and description.

## Motivation
In countries following the Common Law system (e.g., India, UK, Canada, Australia, and many others), there are two primary sources of law

        1. Statutes which are the written laws
        2. Precedents or judgements of prior cases delivered by a court, which involve similar legal facts and issues are the current case, but are not directly indicated in the written law

While working on a new case a legal practitioner often relies on these statutes and precedents to understand how the Court has discussed, argued and behaved in similar scenarios. This task is aimed at creating retrieval systems capable of addressing this problem

## Dataset

## First stage Retrieval
### BM25 

#### Experiments

#### Results


### Splade

#### Hyper-parameters

#### Results

--- 

## Cross-encoder re-ranking

### Training script


### Evaluation Script

#### Effectiveness of MiniLM-MSMARCO-V2 on the test set

We evaluate the MiniLM trained on MS MARCO on our test set. Since the number of judged set of Aila is only 197 queries, we do no train 
---

## Large language models as few-shot re-rankers for statute retrieval
