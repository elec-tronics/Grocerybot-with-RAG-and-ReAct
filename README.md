# Grocerybot-with-RAG-and-ReAct

## Overview
This project uses Retrieval Augmented Generation (RAG) and Reasoning + Acting (ReAct) to create a conversational bot, capable of assisting a customer in their grocery shopping journey.

## Scenario
Imagine you are a user of Cymbal Grocery, your favorite grocery store. You would like to cook something nice for dinner, like lasagne, but you don't know where to start, 
which ingredients to buy, or how to cook lasagne.

You enter the website and you find that Cymbal Grocery has just released a new conversational bot, GroceryBot!

GroceryBot will help you in your shopping journey by:
1. Suggesting you a recipe
2. Getting the list of ingredients and cooking instructions
3. Suggesting you products you will like to buy for that recipe
4. Helping you find new products you'd like to buy for your dinner!

## Objective & Requirements
The objective of this project is to develop **GroceryBot**!

One main requirement of this project is to make sure that this bot is **grounded**. Grounding refers to the process of connecting LLMs with external knowledge sources, such as databases.

In practice, this means that GroceryBot leverages:
1. The existing recipe catalog of Cymbal Grocery. GroceryBot should not suggest recipes that are not part of this catalog.
2. The existing product catalog of Cymbal Grocery. GroceryBot should not suggest products that are not part of this catalog.
3. A set of precomputed products suggested for a recipe.

To do this, Retrieval Augmented Generation (RAG) is used, which attempts to mitigate the problem of hallucination by inserting factual information (in this case, recipe and product information) into the prompt which is sent to the LLM.
