---
title: About the project
feature_image: "https://picsum.photos/1300/400?image=989"
feature_text: |
  # Mitigating/Grading Misinformation and Disinformation with Hybrid Model AI
  By [David Sun](https://www.linkedin.com/in/david-sun-315640233)<sup>*</sup> [Eric Sun]()<sup>*</sup> [Eric Gu]()<sup>*</sup> from University of California San Diego <br>
  Advisor: [Ali Arsanjani]() from Google Cloud

  <small><sup>*</sup>indicates equal contribution</small>
---

A brief introduction and abstract of our project

{% include button.html text="Codebase" icon="github" link="https://github.com/ericsun153/Veracity-Machine-and-Mitigation-Strategies" color="#0366d6" %} {% include button.html text="Report 📑" link="" color="#f68140" %} {% include button.html text="Poster 📈" link="" color="#0d94e7" %} {% include button.html text="Demo ▶️" link="" %}

## Introduction
In today's digital era, the rapid spread of misinformation and disinformation poses a significant societal challenge. Enabled by the rise of advanced technologies such as large language models and artificial intelligence tools, these phenomena undermine mutual trust and can have serious consequences on democratic processes and public safety. Individuals and entities can now easily create and disseminate unchecked information, reaching vast audiences at an alarming rate. This ease of spreading falsehoods not only threatens social harmony but also necessitates an urgent call for effective detection, evaluation, and mitigation strategies. This project aims to explore the growing impact of digital misinformation and disinformation, highlighting how emerging technologies facilitate their spread. It will also propose new solutions to enhance the resilience of information ecosystems against the onslaught of digital falsehoods.

### Why is our project unique?
Our veracity engine uses a suite of latest tools and techniques to power the analysis. This includes: 
- Factuality Factors: a detailed breakdown of of various directions of misinformation. This could include obvious political tendencies or covert agendas intending to misguide the readers toward a specific argument.  
- Fractal Chain of Thought (FCoT): an iterative Chain of Thought (CoT) prompting method that allows an LLM to score veracity based a rigorously defined objective function. Self reflect and updates its scoring based on workflow steps to reach a more conclusive result. 
- Mesop UI Package: new framework launched by Google in 2024 for easy chatbot/LLM application setup through Python. 
- Gemini 2.0 flash: the most advanced LLM model by the time of showcase on multiple benchmarks. 
- Hybrid between Predictive and Generative AI: the predictive classification using our trained metrics, based on the LiarPlus dataset, provides a concrete, empirical reference for the generative to build upon. Reduces hallucination.
- Retrieval-augmented Generation (RAG) + Google Search + Function Calling: suite of proven methods that enhance reasoning and fact-checking capability for specific domains. 

## Methodology


## Results

### Prediction / Generative / Hybrid
{% include figure.html image="assets/images/pred-gen-hyb-results.png" caption="Table 1. predictive vs generative vs hybrid accuracy" width="800"%}

### Prompts Constructed
| Normal Prompting | Chain of Thought | Fractal Chain of Thought |
|-----|-----|------|
||||


## Further Discussion

### Ethical Consideration

