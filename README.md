# essir-legal

## Task definition:

The task of statute retrieval aims to identify the relevant statutes (i.e., candidate document) given a short description of a legal situation (i.e., query).

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

We finetune legal BERT on 40 queries and evaluate it on 10 queries as evaluation set

---
## Large language models as few-shot re-rankers for statute retrieval
