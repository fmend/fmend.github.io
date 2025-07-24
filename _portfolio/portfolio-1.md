---
title: "RAG Evaluation and Chat Assistant Optimization"
excerpt: "Working with the View Systems' development team to improve their retrieval pipeline and optimize thier chat assistant.<br/><br/><img src='/images/500x300.png'>"
collection: portfolio
---

The primary objective of my internship at [View Systems](https://www.view.io) was to develop and maintain a comprehensive Retrieval-Augmented Generation (RAG) evaluation pipeline for their LLM Assistant product. The company sought to determine optimal configuration parameters for individual users based on their specific data characteristics and use cases. This required architecting an external RAG pipeline independent of the user interface to enable large-scale performance testing and optimization. I collaborated directly with Founder and CEO Joel Christner and Co-founder and Senior Member of Technical Staff Blake Martz throughout this initiative.

## A Brief Introduction to View Systems

View Systems is an AI startup focused on delivering on-premises LLM Assistant solutions that enable organizations to leverage large language models while maintaining complete data sovereignty. Their core product allows users to deploy AI capabilities locally with their proprietary data, eliminating the need to transmit sensitive information to external services. The company also offers a secure SaaS alternative for organizations preferring cloud-based deployment while maintaining stringent security standards.

As a lean startup organization, View Systems operated with remarkable efficiency—I was among twelve employees participating in weekly company-wide meetings, which included the entire development team. The team's accomplishments were particularly impressive given their size, successfully launching their beta product in early December 2024, midway through my internship.

## Onboarding & Initial Implementation

My onboarding period involved establishing the development environment and familiarizing myself with View Systems' existing API architecture and development workflows. Under the guidance of my supervisor Blake Martz, I initially focused on constructing a foundational RAG pipeline with essential evaluation capabilities.

Through systematic research and implementation, I developed a baseline evaluation framework incorporating fundamental NLP metrics including recall, precision, and F1 scores. Given that View Systems had not previously employed an NLP specialist, I provided technical guidance to the development team on these core evaluation methodologies and their implications for system performance assessment. I subsequently expanded the evaluation to include advanced metrics such as semantic similarity, faithfulness measures, and mean reciprocal rank, creating a more comprehensive performance analysis framework.

## Implementation & Adaptation

The next few weeks had me working very closely with Blake as it was time to put theory and research into practice. This was very exciting as it was the first time that I was able to see, on a grander scale, what years of study looks like at implementation. Of course, this came with many hiccups that took tedious attention to detail to solve; as it turns out, building an all-new branch for an already established system is not as simple as it sounds. 

I initiated utilizing the Stanford Question Answering Dataset (SQuAD) for this project. SQuAD is comprised of Wikipedia articles and question-answer pairs from those articles, which was perfect for testing the retrieval of their RAG pipeline. SQuAD also has an additional dataset called SQuADShifts, which has alternate data sources, such as Reddit, Amazon reviews, and New York Times articles and comments. Each of these datasets has a very similar format to the original SQuAD, meaning I needed to do minimal formatting from dataset to dataset to allow for robust testing across diverse data. This allowed me to have a good idea of what parameters and models would work best generally.

Once I had everything ready to go, I began vigorously testing their system. The tests I performed were of various sizes but usually ranged at about 10,000 questions. After every test, I would tinker with a single variable at a time and try to optimize the system for solid retrieval and answers. At first, I made changes to specific settings, such as max concurrency (the amount of queries operating at the same time), max tokens (the amount of tokens retrieved in each chunk), rerank topK (the amount of chunks that undergo reranking), and the actual prompt for the generation model (the instruction given to the LLM about how to respond to each query).

When I found myself circling around the same metric highs, I began to manipulate the models doing the heavy lifting, such as the generation model for more precise answers, the embeddings model, and the reranker model to try and push my scores even higher. The generation model was something we had fiddled with before, so manipulations there were quicker tests to ensure that the answer quality was up to par; we didn't want our scores to be bogged down by poor answers when the retrieval metrics were so high. The reranker and embeddings models, however, were not models that we had changed before, and required some additional research into which models could be used to increase metrics without slowing down the total RAG processing time too much. 

All the models we drew from were from Hugging Face, and we ultimately landed on qwen2.5:7b for the generation model, BAAI/bge-small-en-v1.5 for the embedding model, and cross-encoder/ms-marco-MiniLM-L2-V2 for the reranker model. The much smaller reranker model was the most surprising of these. We started out using cross-encoder/ms-marco-MiniLM-L6-V2 (a 6-layer reranker model) and while it did perform faster than the L2 (2-layer), it did not perform as well, which is counterintuitive. We decided to sacrifice the time deduction for overall better scores. The embedding model change awarded us with the biggest bump in retrieval, which was not a surprise based on my research. We started out using sentence-transformers/all-MiniLM-L6-v2, and the change to the BGE model resulted in very little time sacrifices for much better scores. The generation model went through several iterations, but ultimately we came back to the one we started with; we determined that simplicity here was actually better for our purposes. 

## Evaluation criteria
Remember that each of the two projects in your portfolio will be evaluated on these points:

* **Length**: A summary of the project goals, technology used, and outcomes, as appropriate for a general technical audience, between 1000 and 3000 words (not counting code)
* **Content**: student’s experience demonstrates the learning outcomes for the MSHLT program [^note]
* **Code**: Code is contained in the site, or a link to the code (such as in a GitHub repository) exists on the site.
* **Professionalism**: Free of grammatical, mechanical, and stylistic issues
* **Above and beyond**: How well does this component communicate the most relevant features?

[^note]: The learning outcomes of the MSHLT program are:
    
    1. Students will demonstrate programming skills for the workplace.
    2. Students will be able to use fundamental algorithms and concepts in Natural Language Processing.
    3. Students will show knowledge of tools and packages used in Natural Language Processing.
