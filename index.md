---
title: GenAI For Good
feature_image: "https://picsum.photos/1300/400?image=989"
feature_text: |
  # Mitigating/Grading Misinformation and Disinformation with Hybrid Model AI
  By [David Sun](https://www.linkedin.com/in/david-sun-315640233)<sup>*</sup> [Eric Sun](https://www.linkedin.com/in/zihao-sun-309b7a233/)<sup>*</sup> [Eric Gu](https://www.linkedin.com/in/eric-gu433/)<sup>*</sup> from University of California San Diego <br>
  Advisor: [Ali Arsanjani](https://www.linkedin.com/in/ali-arsanjani/) from Google Cloud

  <small><sup>*</sup>indicates equal contribution</small>
---

## About the project
The proliferation of fake news and misinformation, often amplified by large language models (LLMs), poses a significant threat to societal trust and stability. This paper introduces a hybrid veracity detection and scoring framework that leverages both generative AI and traditional machine learning to detect, rank, and mitigate misinformation and disinformation across diverse media formats. Our approach decomposes content into structured analytical components, using an ensemble of factuality factors such as frequency heuristics, malicious account indicators, and psychological manipulation cues to identify and assess deceptive patterns. By employing advanced techniques such as Retrieval-Augmented Generation (RAG), fractal chain-of-thought prompting, and function calling, our system dynamically refines predictions, enhancing transparency and reducing hallucinations. This hybridized LLM-based veracity machine not only facilitates precise misinformation detection but also provides a scalable and interpretable solution for managing the complexities of content veracity in an evolving digital landscape.

{% include button.html text="Codebase" icon="github" link="https://github.com/ericsun153/Veracity-Machine-and-Mitigation-Strategies" color="#0366d6" %} {% include button.html text="Report 📑" link="files/DSC180B_B01_2_Report.pdf" color="#f68140" %} {% include button.html text="Poster 📈" link="files/DSC180B_B01_2_Poster.pdf" color="#0d94e7" %} {% include button.html text="Demo ▶️" link="" %}

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

## Roadmap
<figure>
  <img src="assets/images/Roadmap.png" alt="">
  <figcaption>Figure 1. Roadmap of our project</figcaption>
</figure>

## Datasets
[**Liar PLUS**](https://github.com/Tariq60/LIAR-PLUS): Integration with Predictive AI

- Feature Extraction: The predictive AI can analyze the text data from LIAR-PLUS to extract features that are relevant to determining the truthfulness of statements. This could include linguistic features (like the complexity of language used), semantic features (like the presence of certain key phrases or concepts), and metadata (like the speaker's profile).

- Contextual Analysis: The detailed justifications provided in LIAR-PLUS allow the predictive AI to learn not just whether a statement is true or false, but why it was categorized as such. This deepens the model’s understanding, enabling it to better handle nuanced or borderline cases.

- Training Data: LIAR-PLUS serves as training data for the predictive AI (random forest model). The rich, annotated dataset helps in building robust models that are trained on both the statement and its contextual backing, improving the accuracy of predictions.

[**Politifact & Snopes**](https://www.politifact.com/): Integration with Generative AI

- Use of External Datasets: We enhance the performance and reliability of our veracity machine by leveraging external datasets extracted through web scraping techniques. We obtain data from platforms like PolitiFact and Snopes.com, which provide extensive information on the latest news stories and their truthfulness, as assessed by expert fact-checkers.

- Integration of Ground Truth Labels: These datasets offer crucial ground truth labels, including "True," "Half-True," and "False," along with detailed explanations that elucidate the rationale behind these assessments. By integrating these expert-verified annotations, we ensure that our model is trained and evaluated against high-quality, up-to-date information.

- Expansion of Data Extraction: We are currently expanding our approach to include not only the truthfulness labels but also the accompanying explanations for each verdict. These explanations provide essential context for understanding why content was classified in a particular way, delivering valuable insights into the underlying reasoning.

- Incorporation into System Prompts: Our plan is to incorporate these explanations into the system's prompts, allowing the AI to generate more informed and contextually relevant outputs. This enhancement will enable the veracity machine to provide users not only with accurate classifications but also the reasoning behind these classifications.

- Enhancing Transparency and Trust: By iteratively refining this approach, we aim to foster greater transparency and user trust. Our goal is to create a system capable of addressing the complexities of misinformation with both accuracy and depth.

## Methodology
**Predictive AI**

Combines traditional predictive AI models for statistical rigor and generative AI for nuanced content analysis. Anchors analysis with structured factuality scoring.

- Dataset: LiarPlus, fact-checking and fake news detection dataset

- Factuality features: Location, Education, Event coverage, Echo chamber, News coverage, Malicious account 

- Trained Model: Random forest classifier

- Output labels: True, mostly-true, half-true, barely-true, false, pants-fire


**Generative AI**

- Factuality Factors: Content veracity assessed through multi-dimensional factors, enableing precise and transparent decomposition of misinformation. Including:
  - Frequency Heuristics (repetition patterns, origin tracing).
  - Malicious Accounts (bot-like behavior, false content analysis).
  - Psychological Manipulation (emotional cues, echo chamber effects).

- Retrieval-Augmented Generation (RAG)
  - Fuses semantic retrieval and LLM generation.
  - Ensures grounding of outputs with verified facts and metadata.
  - Dynamically adjusts based on source credibility and temporal relevance.

- Fractal Chain of Thought (FCOT) Prompting: Advances traditional chain-of-thought prompting with iterative, layered analysis:

  - Evaluates factuality factors in multiple iterations.
  - Incorporates feedback loops for refined insights and improved veracity scoring.

Comparison to Traditional Prompting: <br>
Traditional: One-off evaluations, limited depth. <br>
FCOT: Recursive, multi-factor, transparent reasoning. <br>
Use factuality factors as objective functions. <br>
Update score at each iteration with the usage of function calling.

- SerpAPI Web Search 

By embedding these real-time search results into the prompt, the
GenAI gains access to a broader and more dynamic set of data, enabling it to cross-reference
claims made in the inputted news article with credible external sources.

- Function Calling

Function calls are strategically used to dynamically adjust analysis
parameters based on real-time feedback. This adaptability is essential for calculating the
effectiveness of various thought patterns generated by our algorithm, ensuring that the most
logical and factually consistent chains are prioritized.



## Results

### Prediction / Generative / Hybrid

Predictive Performance on Liar PLUS Dataset:
<table style="border-collapse: collapse; width: 100%; margin-bottom: 15px;" border="1" cellpadding="10" cellspacing="0">
    <thead>
        <tr style="background-color: #f2f2f2; text-align: left;">
            <th style="border: 1px solid black; padding: 10px;">Model Description</th>
            <th style="border: 1px solid black; padding: 10px;">Score (%)</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="border: 1px solid black; padding: 10px;">BERT Embedding Model</td>
            <td style="border: 1px solid black; padding: 10px;">43.7</td>
        </tr>
        <tr>
            <td style="border: 1px solid black; padding: 10px;">XGBoost/LightGBM (Boosting algorithm)</td>
            <td style="border: 1px solid black; padding: 10px;">33.1</td>
        </tr>
        <tr>
            <td style="border: 1px solid black; padding: 10px;">Random Forest Classifier (Bagging algorithm)</td>
            <td style="border: 1px solid black; padding: 10px;">67.8</td>
        </tr>
        <tr>
            <td style="border: 1px solid black; padding: 10px;">Sentiment Analysis (TF-IDF)</td>
            <td style="border: 1px solid black; padding: 10px;">45.9</td>
        </tr>
        <tr>
            <td style="border: 1px solid black; padding: 10px;">Word2Vec</td>
            <td style="border: 1px solid black; padding: 10px;">55.2</td>
        </tr>
    </tbody>
</table>

<p style="font-size: 18px; text-align: center; margin-top: 10px;">
    Table 1. Predictive Performance on Liar PLUS dataset
</p>



Overall Model Performance:
<table style="border-collapse: collapse; width: 100%;" border="1" cellpadding="8" cellspacing="0">
    <thead>
        <tr style="background-color: #f2f2f2;">
            <th style="border: 1px solid black;">Model Description</th>
            <th style="border: 1px solid black;">Score (%)</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="border: 1px solid black;">Baseline (Feeding straight into Gemini Flash 2.0)</td>
            <td style="border: 1px solid black;">19</td>
        </tr>
        <tr>
            <td style="border: 1px solid black;">Hybrid (Random Forest + Gemini)</td>
            <td style="border: 1px solid black;">34.3</td>
        </tr>
        <tr>
            <td style="border: 1px solid black;">Hybrid + RAG</td>
            <td style="border: 1px solid black;">40</td>
        </tr>
        <tr>
            <td style="border: 1px solid black;">Hybrid + RAG + Web Search</td>
            <td style="border: 1px solid black;">56.9</td>
        </tr>
        <tr>
            <td style="border: 1px solid black;">Hybrid + RAG + Web Search + FCOT Prompting</td>
            <td style="border: 1px solid black;">67.2</td>
        </tr>
        <tr>
            <td style="border: 1px solid black;">Hybrid (50/50) + RAG + Web Search + FCOT Prompting + Function Calling</td>
            <td style="border: 1px solid black;">65.3</td>
        </tr>
        <tr>
            <td style="border: 1px solid black;">Hybrid (70/30) + RAG + Web Search + FCOT Prompting + Function Calling</td>
            <td style="border: 1px solid black;">85.1</td>
        </tr>
    </tbody>
</table>
<p style="font-size: 18px; text-align: center; margin-top: 10px;">
    Table 2. Overall Model Performance 
</p>



Precision & Recall Result:
<figure>
  <img src="assets/images/pred-gen-hyb-results.png" alt="">
</figure>
<p style="font-size: 18px; text-align: center; margin-top: 10px;">
    Table 3. predictive vs generative vs hybrid accuracy
</p>

Prompting Comparison Result: [Prompting Comparison Link](https://docs.google.com/spreadsheets/d/1guFblrl9GR_bjLHH0QNgBTliiRjFmDHx/edit?gid=1613470116#gid=1613470116)

### Prompts Constructed
<!-- | Normal Prompting | Chain of Thought | Fractal Chain of Thought |
|-----|-----|------|
|||| -->
**Normal Prompting**

Use 3 iterations to check the veracity score of this news article. Factors to consider are Frequency Heuristic and Misleading Intentions. In each, determine what you missed in the previous iteration. Also put the result from RAG into consideration/rerank.
RAG: Here, out of six potential labels (true, mostly-true, half-true, barely-true, false, pants-fire), this is the truthfulness label predicted using a classifier model: {predict_score}.
These are the top 100 related statement in LiarPLUS dataset that related to this news article: {get_top_100_statements(input_text)}.
Provide a percentage score and explanation for each iteration and its microfactors.
Final Evaluation: Return an exact numeric veracity score for the text, and provide a matching label out of these six [true, mostly-true, half-true, barely-true, false, pants-fire]

**Chain of Thought**: [Chain of Thought Full Prompt Link](https://docs.google.com/document/d/1h3IiKepfN1FWOnzql5xU33B0uZhgsAfGbCo7d8PrKc8/edit?tab=t.06)

**Fractal Chain of Thought**: [Fractal Chain of Thought Full Prompt Link](https://docs.google.com/document/d/130o2t23nDi2KNnJH-wJexRciDvaC9lIGqHfl0ti-lGE/edit?tab=t.0)


### Further Discussion
- Chunking the input news into smaller paragraphs. The chunking methods can help the GenAI to detect each paragraph in detail to further produce much accurate interpretation on the results.

- Adding Langchain Agent and using more factuality factors to our model. Langchain Agent can help structuring our current model to learn and adapt better to the news and take time to fully analyze based on our factuality factors. It focuses on the data-centric aspects—like embeddings, chain logic, and integration with language models—to learn how to transform raw data into contextualized, conversational experiences. It also understands the end-to-end workflow—from defining user requirements to deploying robust AI solutions—and see how LangChain’s flexible architecture can fit seamlessly into diverse product strategies. 

- Adding more facuality factors can help the model analyze the news in multi-perspectives to produce more accurate score to counter misinformation.

- Expanding our dataset and refine our algorithms to better handle the dynamic and evolving nature of online information. Future work will
focus on automating the integration of real-time data feeds and enhancing the system’s adaptability to new and emerging types of misinformation.

### Ethical Consideration
- Bias and fairness in AI decision-making: AI models often inherit biases from their training data, which can lead to skewed misinformation classifications, particularly when dealing with politically or ideologically sensitive content. Addressed by ensuring the collected data are public and reliable. Using RAG process and metadata in the ChromaDB to further classify.

- Users awareness: Users should always be aware of how their data is being used and have the choice to opt out when possible. To protect privacy, these systems must follow strict security measures such as encryption and anonymization, ensuring that personal information is not misused. Addressed by user using personal Google Gemini API for API key. 

- AI transparency: must be transparent the process in how AI detects misinformation. Understanding why content is flagged as false or misleading and providng clear reasons for their conclusions, allowing users to see and verify the logic behind content classification. Addressed by sharing the full prompt engineering and use of FCOT. 
