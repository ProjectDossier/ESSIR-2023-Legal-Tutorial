# Official respository for Legal Tutorial in The 14th European Summer School on Information Retrieval

## Task definition:

The task of statute retrieval aims to identify the relevant statutes (i.e., candidate document) given a short description of a legal situation (i.e., query).

## Motivation
In countries following the Common Law system (e.g., India, UK, Canada, Australia, and many others), there are two primary sources of law

        1. Statutes which are the written laws
        2. Precedents or judgements of prior cases delivered by a court, which involve similar legal facts and issues are the current case, but are not directly indicated in the written law

While working on a new case a legal practitioner often relies on these statutes and precedents to understand how the Court has discussed, argued and behaved in similar scenarios. This task is aimed at creating retrieval systems capable of addressing this problem

## Dataset
We use the Artificial Intelligence for Legal Assistance (AILA) dataset, and focus on Task 1 - Precedent & Statute retrieval. AiILA is a series of shared tasks aimed at developing datasets and methods for solving variety of legal informatics problems.
  
To be more specific, we focus on TASK 1B, titled "Identifying relevant statutes" in a mutlti-stage setup. For first stage retrieval, we explore BM25 and Splade and for re-ranking on the top-k candidates retrieved by firs stage retriever, we use Large language models with few-shot in-context reasoninig where the number of training size is only two instance and we also fine-tune cross-encoders where the number of queries for training is 40 queries. We evaluate the re-ranker on ten qureies from the validation.

It is noteworthy to mention that our setup in cross-encoder re-ranking could be more fair if we had a sepearte test dataset. However, here, our objective is teaching students to implement and train mentioned methods.

## Tutorial plan

We started with an introduction to legal IR that presented by Sophia 

# Retrieval

## First stage Retrieval

### BM25 

#### Experiments

#### Results


### Splade

#### Hyper-parameters

#### Results

--- 

# Re-ranking

## Cross-encoder re-ranking

### Training script


### Evaluation Script

#### Effectiveness of MiniLM-MSMARCO-V2 on the test set

We finetune legal BERT on 40 queries and evaluate it on 10 queries as evaluation set

---
## Large language models as few-shot re-rankers for statute retrieval

---

## Evaluation table

| Methode                           | Backbone      | P@1 | P@5 | P@10 | recall@10 | recall@100 | Map@100 |
|-----------------------------------|---------------|-----|-----|------|-----------|------------|---------|
| BM25                              | Elasticsearch | ~   |     |      |           |            |         |
| Splade                            | BERT          |     |     |      |           |            |         |
| BM25 + Cross-encoder (fine-tuned) | BERT          |     |     |      |           |            |         |
| BM25 + LLM few-shot reranker      | Flan-T5       |     |     |      |           |            |         |


# Organizers

[Arian Askari](https://www.linkedin.com/in/arian-askari/), PhD candiate from Leiden University

[Tobias Fink](https://www.linkedin.com/in/tobias-fink-89b50a229/), PhD candidate from Tu Wien

[Sophia Althammar](https://www.linkedin.com/in/sophia-althammer-2a93b6b9/), PhD candidate from Tu Wien

[Alaa El-Ebshihy](https://www.linkedin.com/in/alaa-el-ebshihy/),  PhD candidate from Tu Wien
