# Sentence Level Claim Substantiation and Feedback

A NLP package for my third year project at The University of Manchster.

## Description

Aims to provide writing feedback on text based on human interpretable feedback and claim extraction.

## Structure

```
slcs/
|-- main.py
|-- data/
|-- models/
    |-- relevance/
    |-- verification/

```

## Installing

## Development

## Testing

## Usage

## Approach

The goal is to provide a model which can extract unsubstantiated claims on a sentence level, and hence tell the trustworthiness, and coherence of a given piece of text.

- coherence (as measures by number of high-level concepts per sentence, number of jumps between topics)
- trustworthiness (as measured by number of unsubstantiated claims)

Detecting claims and assertions in unstructured text.

How are we going to determine what is an unsubstantiated claim or not?

What do unsubstantiated claims look like compared to evidence based claims?
- The difference between fact and opinion, and
- the difference between stated fact and substantiated fact

How can we extract such information from a text :
The approach is to detect claims and then determine based on context whether they were substantiated.

- POS tagging
- NER
- Topic modeling
- Key topic extraction

Considerations for approaches:

Not restricting us to specific pieces of writing, there exist high variation in text structure and writing style. This makes a fully supervised learning approach unsuitable, given the lack of properly labelled training data.

Much of the work done on this is in the area of news and politics, leading to a relative lack of resources in the academic space.
However, academic writing is a compelling resource, given the evidence based nature of the writing.
Due to their structure, neural nets when applied to NLP can capture basic structure and understanding of language and can thus be fine-tuned on down-stream tasks with limited data.

Sota are BERT and DistilBert models, the latter being a smaller version, which still has on par performance with its big brother.

FEVER dataset https://github.com/QiangAIResearcher/Fact-Extraction-and-Verification

ASAP dataset

Biomedical abstract claim detection https://github.com/titipata/detecting-scientific-claim

Fact checking extraction https://github.com/claimskg/claimskg-extractor

Claim extraction by AIDA https://github.com/TomJansen25/Extracting-Core-Claims

given text detect claim summary https://github.com/tonghuikang/given-text-detect-claim-summary

EXPLORE Generating Scientific Claims for Zero-Shot Scientific Fact Checking

scientific claim generation https://github.com/allenai/scientific-claim-generation

FEVER git https://github.com/awslabs/fever