# **🛒 GroceryBot-with-RAG-and-ReAct**
GroceryBot – your intelligent grocery & recipe assistant powered by RAG + ReAct

## 📖 Overview
This project uses Retrieval Augmented Generation (RAG) and Reasoning + Acting (ReAct) to create a conversational bot, capable of assisting a customer in their grocery shopping journey.

## 🍝 Scenario
Imagine you are a user of Pepper Grocery, your favorite grocery store. You would like to cook something nice for dinner, like lasagne, but you don't know where to start, 
which ingredients to buy, or how to cook lasagne.

You enter the website and you find that Pepper Grocery has just released a new conversational bot, GroceryBot!

GroceryBot will help you in your shopping journey by:
1. 📖 Suggesting you a recipe
2. 🥕 Getting the list of ingredients and cooking instructions
3. 🛍️ Suggesting you products you will like to buy for that recipe
4. 🌟 Helping you find new products you'd like to buy for your dinner!

## 🎯 Objective & Requirements
The objective of this project is to develop **GroceryBot**!

One main requirement of this project is to make sure that this bot is **grounded**. Grounding refers to the process of connecting LLMs with external knowledge sources, such as databases.

In practice, this means that GroceryBot leverages:
1. The existing recipe catalog of Pepper Grocery. GroceryBot should not suggest recipes that are not part of this catalog.
2. The existing product catalog of Pepper Grocery. GroceryBot should not suggest products that are not part of this catalog.
3. A set of precomputed products suggested for a recipe.

To do this, Retrieval Augmented Generation (RAG) is used, which attempts to mitigate the problem of hallucination by inserting factual information (in this case, recipe and product information) into the prompt which is sent to the LLM.

## 🛠️ Tech Stack
**Programming Language**: Python

**Frameworks & Libraries**: LangChain (RAG & ReAct implementation), FAISS (vector database for local retrieval), ChromaDB (optional local vector store for experimentation), PyPDF (document parsing)

**LLM/AI**: Vertex AI Generative Models (Google Cloud)

**Core Concepts**: Retrieval-Augmented Generation (RAG), Reasoning + Acting (ReAct) Agent Architecture

**Databases / Storage**: Local FAISS index for Product & Recipe catalog, Precomputed recipe-to-product mappings

**Deployment / Tools**: Google Cloud AI Platform

## ⚙️ Implementation of the GroceryBot
This system is powered by Vertex AI Generative models and Langchain. 

To ground the model it is required to connect the LLM to the internal company databases. It is done by implementing a [ReAct like](https://ai.googleblog.com/2022/11/react-synergizing-reasoning-and-acting.html) Agent in Langchain, capable of taking decisions and decide when to query these databases.

In this project, only local databases are used. 
* The Product & Recipe catalog are defined locally using Faiss
* The details of a recipe and the suggested products to buy for that recipe are also stored locally
![image](https://storage.googleapis.com/github-repo/img/language/reference_architectures/spotbot/spotbot_architecture.png)

## 🤝 Contributing
Contributions are welcome! Please fork the repo and submit a pull request.
