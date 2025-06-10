---
permalink: /
title: "Freddy Mendoza"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a Master's of Science student at the University of Arizona in their [Human Language Technology program](https://linguistics.arizona.edu/ms-hlt). In 2023, I graduated cum laude from the University of Arizona with a BA in Linguistics and a minor in Computer Science.

My BA
======
In 2018, I tentatively dipped my toes back into school after having dropped out in 2010 due to feelings of aimlessness in my educational endeavors at the time. The much-needed years away allowed me to sharpen my interests, giving me space to confidently choose the direction I wanted to take. I have had a lifelong interest in language, nourished by a deep love for books and writing, though I had failed to recognize that as a viable area of study among the myriad interests of a 17-year-old brain.

As I prepared myself to return to the U of A by taking prerequisites at Pima Community College, I ran into a Ph.D. student who turned my attention to their HLT MS program. Already having had an interest in coding, it was an easy decision to declare C.S. as my minor, with the intention of finishing my BA and going on to the HLT Master's.

At the U of A, I was lucky to study semantics, syntax, phonetics, and other linguistic areas that I was surprised to find strongly support certain areas of computer science, especially as they relate to natural language processing. During my undergrad, I got to work with Dr. Sandiway Fong, the director of the in-person HLT program, on a Spanish syntactic parser he was working on. It was incredibly helpful to see some of the minutiae that go into building something as complex as a language parser, not to mention getting to work directly with someone so knowledgeable about computational linguistics.

My MS
======
In 2023, I began the HLT program at the U of A. I began to dig a little deeper on topics that I had began in my undergrad, such as human language technology, statistical natural language processing, and computational linguistics, while getting the opportunity to explore some new ones in speech technology and search engine optimization.

During this time, I was enlightened to the linguistic underbelly of machine learning. I was able to apply my knowledge of syntax and semantics to many projects in various classes, while learning a bit more about phonology and phonetics in speech tech.

For my internship, I got to work with Joel Christner at his startup, View Systems. There, I got to contribute to the development of their RAG evaluation pipeline and core prompt engineering. I tested their LLM Assistant to try and improve context retrieval strategies depending on the type of data being supplied to the RAG pipeline. Here, I got to explore the vast world of embedding and rerank models, implementing many of them as a means of improving retrieval to their Assistant.



Getting started
======
1. See [README.md](https://github.com/uazhlt/professionalGHpages.github.io/blob/main/README.md) for getting set your repository set up and configured properly to render as a website.
1. Change this file to have the content you need for the *Professional introduction*--or, if you'd prefer to put that information onto a page that is *not* the landing page for your site, simply make it clear from this page where a reader could find that professional introduction. Think of it as a combination of a general-purpose cover letter in a job application and a personal statement for your application to the graduate program. It might briefly introduce your educational and work history, describe what you're currently working on, but also include the issues that motivate you and that you hope to work on in the future. Make sure your introduction meets the requirements outlined in the evaluation rubric.
1. Add information about your internship and at least one other coding project into files (either in Markdown or in HTML format) in the `_portfolio/` folder. You should find two stubs there, one in each format, but you can choose to have each of your portfolio files in whichever format you prefer. Make sure your write-ups meet the requirements outlined in the evaluation rubric.
1. Add the information that you'd like to have on your CV into `_pages/cv.md`. Make sure your CV meets the requirements outlined in the evaluation rubric.

Be sure to complete this information and submit your URL to the faculty evaluator by the deadline each term. The evaluator will prepare a feedback sheet for you to indicate how your site scored relative to the rubric. If there are significant points that need to be improved, you want to ensure you have time to receive that feedback and implement any revisions before the end of the term.

Site-wide configuration
------
The main configuration file for the site is in the base directory in [_config.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_config.yml), which defines the content in the sidebars and other site-wide features. You will need to replace the default values there with ones about yourself and your site's github repository; read this file carefully to make sure you've updated them all. The configuration file for the top menu is in [_data/navigation.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_data/navigation.yml). For example, if you want to add a section for *Talks* back into the site, you can add a navbar item for that (in navigation.yml) to add them back into the header. Make sure there's still a `talks.html` file in the _pages directory, and then add files for individual talks in the _talks directory. You'll follow a similar process to restore other navbar items or create your own.

Create content & metadata
------
For site content, there is one markdown file for each type of content, which are stored in directories like _publications, _talks, _posts, _teaching, or _pages. For this template, only the _posts and _portfolio directories have been kept, but you can see the [original AcademicPages repository](https://github.com/academicpages/academicpages.github.io) for an example, if you'd like to add any of those categories back in.

If you choose to add some of these categories back to your site, you may find a lot of useful utilities to make updates to the site information work more smoothly. For example, each talk is a markdown file in the [_talks directory](https://github.com/academicpages/academicpages.github.io/tree/master/_talks). At the top of each markdown file is structured data in YAML about the talk, which the theme will parse to do lots of cool stuff. The same structured data about a talk is used to generate the list of talks on the [Talks page](https://academicpages.github.io/talks), each [individual page](https://academicpages.github.io/talks/2012-03-01-talk-1) for specific talks, the talks section for the [CV page](https://academicpages.github.io/cv), and the [map of places you've given a talk](https://academicpages.github.io/talkmap.html) (if you run this [python file](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.py) or [Jupyter notebook](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb), which creates the HTML for the map based on the contents of the _talks directory).

**Markdown generator**

The creator of the AcademicPages template has also created [a set of Jupyter notebooks](https://github.com/academicpages/academicpages.github.io/tree/master/markdown_generator
) that converts a CSV containing structured data about talks or presentations into individual markdown files that will be properly formatted for the AcademicPages template. The sample CSVs in that directory are the ones used to create the site at stuartgeiger.com. His usual workflow is to keep a spreadsheet of publications and talks, then run the code in these notebooks to generate the markdown files, then commit and push them to the GitHub repository.

For more info
------
More info about configuring AcademicPages can be found in [the guide](https://academicpages.github.io/markdown/). The [guides for the Minimal Mistakes theme](https://mmistakes.github.io/minimal-mistakes/docs/configuration/) (which this theme was forked from) might also be helpful.
