# Official respository for Legal Tutorial in The 14th European Summer School on Information Retrieval

Welcome to the repoistory of legal tutorial in ESSIR'23!

In this tutorial, we will delve into the world of legal information retrieval, specifically focusing on the identification of relevant statutes given a brief description of a legal situation. This task is crucial for legal practitioners, as it enables them to access the written laws that may apply to their cases. We explore this subject in more detail in the following.

## Task definition:

The primary objective of statute retrieval is to identify the relevant statutes (from the candidate documents) based on a concise description of a legal scenario (query).

## Motivation
In countries that adhere to the Common Law system (e.g., India, UK, Canada, Australia, and many others), two main sources of law exist:
1. Statutes which are the written laws
2. Precedents or judgements of prior cases delivered by a court, which involve similar legal facts and issues are the current case, but are not directly indicated in the written law

Legal practitioners frequently rely on statutes and precedents when working on new cases. These resources help them understand how the court has discussed, argued and decided similar scenarios. Our tutorial aims to provide preliminary information on developing retrieval systems that can address this critical need.



## Dataset

For this tutorial, we leverage the Artificial Intelligence for Legal Assistance (AILA) dataset, specifically focusing on Task 1 - Precedent & Statute retrieval. AILA encompasses a series of shared tasks designed to create datasets and methods for solving various legal informatics challenges.

To be more precise, we concentrate on TASK 1B, titled "Identifying relevant statutes," in a multi-stage setup. In the initial stage of retrieval, we explore BM25 and Splade. For reranking the top-k candidates retrieved by the first-stage retriever, we employ large language models (LLMs) with few-shot in-context reasoning with only two training instances, and fine-tuned cross-encoders with 40 training queries. We evaluate the reranker using ten queries from the validation set.

It is important to note that while a separate test dataset would make our cross-encoder reranking setup more robust, our primary goal here is to teach students how to implement and train these methods effectively.

## Tutorial plan

Our tutorial is divided into several informative sessions:
1. **Introduction to Legal Information Retrieval**: Presented by [Sophia Althammar](https://www.linkedin.com/in/sophia-althammer-2a93b6b9/) and [Alaa El-Ebshihy](https://www.linkedin.com/in/alaa-el-ebshihy/) and [Alaa El-Ebshihy](https://www.linkedin.com/in/alaa-el-ebshihy/), this session provides an overview of legal information retrieval.        
2. **First Stage Retrievers with BM25 and Splade**: Taught by [Tobias Fink](https://www.linkedin.com/in/tobias-fink-89b50a229/), this session explores the implementation and usage of first stage retrievers, with code available in the "first_stage_retrievers" folder.        
3. **Reranking with BERT-based and Larage language models**: In the afternoon session, [Arian Askari](https://www.linkedin.com/in/arian-askari/) presents the process of fine-tuning and evaluating cross-encoder rerankers. This includes an investigation into how LLMs, particularly FLAN-T5, can effectively rerank statutes based on a legal question with minimal provided examples. The implementation of the reranking stage is available in the "[llms_transformers_rerankers](https://github.com/ProjectDossier/ESSIR-2023-Legal-Tutorial/tree/main/llms_transformers_rerankers)" folder.

       
Notes:

- You can check ut othe presentation slides in the "presentation" folder.

- All of our tutorial could be run with Google Colab without access to premium account.


<!--- 
# Retrieval

## First stage Retrieval

### BM25 
mple
#### Experiments

#### Results


### Splade

#### Hyper-parameters

#### Results

--- 

# reranking

## Cross-encoder reranking

### Training script


### Evaluation Script

#### Effectiveness of MiniLM-MSMARCO-V2 on the test set

We finetune legal BERT on 40 queries and evaluate it on 10 queries as evaluation set

---
## Large language models as few-shot rerankers for statute retrieval

---

--->

## Evaluation table

| Methode                           | Backbone      | P@1 | P@5 | P@10 | recall@10 | recall@100 | Map@100 |
|-----------------------------------|---------------|-----|-----|------|-----------|------------|---------|
| BM25                              | Elasticsearch | .1200   |  .0480   |  .0380   |     .0860      |     .4373       |     .0605    |
| Splade                            | BERT          |     |     |      |           |            |         |
| BM25 + Cross-encoder (fine-tuned) | BERT          |     |     |      |           |            |         |

BM25 + LLM few-shot reranker (Flan-T5): Try your prompt on [statute reranking notebook](https://github.com/ProjectDossier/ESSIR-2023-Legal-Tutorial/blob/main/llms_transformers_rerankers/solutions/3_statute_reranking_with_LLMs_solution.ipynb)  :)

 
# Organizers

[Arian Askari](https://www.linkedin.com/in/arian-askari/), PhD candiate from Leiden University

[Tobias Fink](https://www.linkedin.com/in/tobias-fink-89b50a229/), PhD candidate from Tu Wien

[Sophia Althammar](https://www.linkedin.com/in/sophia-althammer-2a93b6b9/), PhD candidate from Tu Wien

[Alaa El-Ebshihy](https://www.linkedin.com/in/alaa-el-ebshihy/),  PhD candidate from Tu Wien
