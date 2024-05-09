# Langchain RAG Project

This git repository is dedicated to studies on RAG models. In this project, we build a retrieval aumented generation app using the Langchain library and OpenAI. You can use this app to interact with your own documents/data sources. In this example, we use the 'Alice in Wonderland' book as the data source to be given to the model and the user is able to query on this document. 

Given your collection of documents/books/lectures, you want to be able to interact with that data using AI. For example, you might want to be able to ask questions about the data or perhaps build a customer support chatbot that follows a set of desired instructions. In this example, we use the 'Alice in Wonderland' book as the data source to be given to the model and the user is able to query on this document.

The agent will be able to use this documentation to provide response as well as quote the source where it got the information from originally. In this way it's always possible to check that the response comes from genuine sources rather than hallucinations.

The app passes through three main steps:

1 - Prepare the data
2 - Query for relevant data
3 - Craft the response 

To install dependencies:

```python
pip install -r requirements.txt
```
For the first step, we need to prepare the data and turn it into a vector database. To create the Chroma DB:

```python
python create_database.py
```
In the next step we also look at how to query the database for the relevant pieces of data. Finally, one can put the pieces together to for a coherent response. To query the Chroma DB:

```python
python query_data.py "How does Alice meet the Mad Hatter?"
```

You'll also need to set up an OpenAI account (and set the OpenAI key in your environment variable) for this to work. To set the OpenAI key:

```bash
export OPENAI_API_KEY='your-api-key-here'
```
