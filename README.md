# essir-legal

## Task definition:

Given a query, identify relevant statutes. 

**Each query,** is a short description of a legal situation

**Each candidate document**, is a statute (Section of Act) from Indian law. 

Therefore, our corpus is a set of statuse that act as candidate document. There is in total 2,914 statutes as our 

There is a set of 197 statutes (Sections of Acts) from Indian law which build our document collection corpus.

, that are relevant to some of the queries. The title and description of these statutes are provided. For each query, the task is to identify the most relevant statutes (from among the 197 statutes).
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
---

## Large language models as few-shot re-rankers for statute retrieval
