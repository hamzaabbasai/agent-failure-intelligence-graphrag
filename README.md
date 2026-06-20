# Agent Failure Intelligence GraphRAG

A GraphRAG project built using Neo4j, LangChain, LangGraph, and OpenAI
to analyze AI agent failures, identify root causes, and recommend fixes
using a structured observability dataset.

## Project Summary

This project builds a knowledge graph from AI agent incident logs and
uses graph-based retrieval with LLM reasoning to answer operational
questions.

It helps analyze:

-   Agent failures
-   Root causes
-   Fix patterns
-   Workflow issues
-   SLA breaches
-   Business impact

## Tech Stack

-   Python
-   Neo4j
-   LangChain
-   LangGraph
-   OpenAI API
-   Cypher Query Language
-   Pandas

## Dataset

This project uses a custom **AI Agent Observability Dataset**
containing:

-   10,000+ incident records
-   28 structured columns
-   Agent failures
-   Root causes
-   Fix actions
-   LLM usage
-   Workflow metadata
-   SLA breach tracking
-   Business impact metrics

Dataset Link:  
https://www.kaggle.com/datasets/hamzaabbasai/ai-agent-observability-dataset

## Project Structure

``` text
agent-failure-intelligence-graphrag/
│── data/
│   └── ai_agent_observability_dataset.csv
│── agent_failure_graphrag.ipynb
│── .env
│── .example.env
│── requirements.txt
│── README.md
```

## Setup

Install dependencies:

``` bash
pip install -r requirements.txt
```

Create a `.env` file:

``` env
OPENAI_API_KEY=your_openai_key
NEO4J_URI=your_neo4j_uri
NEO4J_USERNAME=your_neo4j_username
NEO4J_PASSWORD=your_neo4j_password
```

## Run

Open the notebook:

``` text
agent_failure_graphrag.ipynb
```

Load the dataset:

``` python
df = pd.read_csv("data/ai_agent_observability_dataset.csv")
```

Make sure the dataset file exists inside the `data/` folder.

## Example Questions

-   Why do Support Agents fail most often?
-   Which workflows generate the most incidents?
-   What root causes are linked to hallucination errors?
-   Which fixes resolve retrieval failures?
-   Which LLM models are linked to critical incidents?

