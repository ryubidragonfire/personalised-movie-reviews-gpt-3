# Personalised Movie Reviews using OpenAI GPT-3

This repository provides an example on how to get a personalised movie reviews. This is one of many examples that is using similar techniques in retrieving information given a set context with Azure OpenAI's GPT-3 language model. 

The purpose of this repo is to demonstrate the basic techniques to use the lanaguage model. It is by no means protraying the state of the art techniques. 

[02-personalised-reviews-summary.ipynb](./notebooks/02-personalised-reviews-summary.ipynb) shows example queries and responses, which also includes filed examples. It is up to you to judge the quality of responses, and do consider other techniques to improve upon the responses. 

# Dataset
The dataset used in this project is the [Rottentomatoes 400k Movie Reviews](https://www.kaggle.com/datasets/talha002/rottentomatoes-400k-review) which contains over 417,000 reviews of over 9300 movies written by over 5700 reviewers. This dataset is available from [kaggle](www.kaggle.com). However, given the compute time and resources, only top 20 movies with the most reviews, resulting in a total of over 9000 reviews, are used in this example. 

It contains columns: `Movie`, `Reviewer`, `Publish`, `Review`, `Date` and `Score`. However, in this repo, the column `Reviewer` has been removed. 

# Steps
The steps taken in this example are:

1. **Data Exploration** - Explore data used in this repo. 
2. **Get Embeddings** - Generate embeddings from documents using GPT-3.
3. **Personalised Movie Reviews** - Retrieve review relevant as per user's query, and generate a reponse to that query based on context. 

# Language Model
Language models used in this example are `text-davinci-003`, `text-search-davinci-doc-001`, and `text-search-davinci-query-001`. 

# Notebooks
This project consists of notebooks that perform the following tasks:

1. [00-explore-data.ipynb](./notebooks/00-explore-data.ipynb) - This notebook explores the data by looking at the distribution of classes, number of words per document, etc.
2. [01-get-embeddings.ipynb](./notebooks/01-get-embeddings.ipynb) - This notebook uses pre-trained word embeddings to create vector representations for each document.
3. [02-personalised-reviews-summary.ipynb](./notebooks/02-personalised-reviews-summary.ipynb) - This notebooks use a typical technique to provide a summary based of relevant reviews, as per user's query. 

# Future Work
- This example shows the capabilities of GPT-3 using a small subset of data. One key area to explore in the future is how to scale the solution to large data corpus.
- Cater for multi-lingual reviews.

# Related Repos
Related repos from the author:
- https://github.com/ryubidragonfire/document-analysis-using-gpt-3
- https://github.com/ryubidragonfire/code-explaination-openai

# References
- OpenAI repo: https://github.com/openai/openai-cookbook/ 
- Which embedding model to use? https://openai.com/blog/new-and-improved-embedding-model/ 
- OpenAI models: https://learn.microsoft.com/en-us/azure/cognitive-services/openai/concepts/models 

