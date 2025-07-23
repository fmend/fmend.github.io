---
title: "RAG Evaluation and Chat Assistant Optimization"
excerpt: "Working with the View Systems' development team to improve their retrieval pipeline and optimize thier chat assistant.<br/><br/><img src='/images/500x300.png'>"
collection: portfolio
---

The primary goal of my internship at [View Systems](https://www.view.io) was to develop and maintain a Retrieval-Augmented Generation (RAG) evaluation pipeline for their LLM Assistant. They wanted to get an idea of the settings they would need for each individual user depending on the type of data they were using on their product. This required building an external RAG pipeline (from the UI) so that I could run largescale tests on data to evaluate performance. I had the opportunity to work with Founder and CEO, Joel Christner, and cofounder and Senior Member of Technical Staff and Software Engineer, Blake Martz, on this project.

## A Brief Introduction to View Systems

View is an AI startup company which aims to provide an LLM Assistant that can be used on-premises, allowing a user to supply their own data and harness the power of an LLM without having to outsource sensitive information. While this is the foundational product for their company, they also supply a similar service in the form of a SAAS product, giving the user the option of operating on a secure, completely online format rather than downloading the whole package.

As a startup, their team was incredibly small---I was one of twelve employees to attend weekly meetings for the company, which included all their developers. It was impressive to see the work they had done with such a small group in just over a year, having launched their beta product midway through my internship in early December 2024.

## Onboarding & Initial Tasks

As can be expected, I spent the first couple of weeks preparing my machine for the work ahead, as well as adapting to the API and workflow at View. After I got my bearings, my supervisor, Blake Martz, instructed me with the task of building a simple RAG pipeline. With some research, I was able to get together a simple enough pipeline with some simple metrics that could be used to evaluate RAG systems and gauge their performance. I started out with a demonstration of recall, precision, and F1 scores. Before I had arrived they did not have a Natural Language Processing (NLP) specialist, so much of my initial conversations with other developers was small instruction on the fundamentals of NLP and what these scores mean regarding their system. I also began researching other metrics which might be useful to their sytem and what we wanted to accomplish. I got myself acquainted with semantic similarity, faithfulness, and mean reciprocal rank, and added them to my pipeline.

## Implementation & Adaptation

The next few weeks had me working very closely with Blake as it was time to put theory and research into practice. This was very exciting as it was the first time that I was able to see, on a grander scale, what years of study looks like at implementation. Of course, this came with many hiccups that took tedious attention to detail to solve; as it turns out, building an all-new branch for an already established system is not as simple as it sounds. 

I initiated utilizing the Stanford Question Answering Dataset (SQuAD) for this project. SQuAD is comprised of Wikipedia articles and question-answer pairs from those articles, which was perfect for testing the retrieval of their RAG pipeline. SQuAD also has an additional dataset called SQuADShifts, which has alternate data sources, such as Reddit, Amazon reviews, and New York Times articles and comments. Each of these datasets has a very similar format to the original SQuAD, meaning I needed to do minimal formatting from dataset to dataset to allow for robust testing across diverse data. This allowed me to have a good idea of what parameters and models would work best generally.

Once I had everything ready to go, I began vigorously testing their system. The tests I performed were of various sizes, but usually ranged at about 10,000 questions. After every test, I would tinker with a single variable at a time and try to optimize the system for solid retrieval and answers. At first, I made changes to specific settings, such as max concurrency (the amount of queries operating at the same time), max tokens (the amount of tokens retrieved in each chunk), and the actual prompt for the generation model (the instruction given to the LLM about how to respond to each query).

Once I found myself circling around the same metric highs, I began to manipulate the models doing the heavy lifting, such as the generation model for more precise answers, the embeddings model, and the rerank model to try and push my scores even higher. 

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
