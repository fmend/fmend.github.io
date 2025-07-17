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

As can be expected, I spent the first couple of weeks preparing my machine for the work ahead, as well as adapting to the API and workflow at View. After I got my bearings, my supervisor, Blake Martz, instructed me with the task of building a simple RAG pipeline. With some research, I was able to get together a simple enough pipeline with some simple metrics that could be used to evaluate RAG systems and gauge their performance. I started out with a demonstration of recall, precision, and F1 scores. Before I had arrived they did not have a Natural Language Processing (NLP) specialist, so much of my initial conversations with other developers was small instruction on the fundamentals of NLP and what these scores mean regarding their system.

## Implementation & Adaptation

The next few weeks had me working very closely with Blake as it was time to put theory and research into practice. This was very exciting as it was the first time that I was able to see, on a grander scale, what years of study looks like at implementation. Of course, this came with many hiccups that took tedious attention to detail to solve; building an all-new branch for an already established system is not as simple as it sounds. 

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
