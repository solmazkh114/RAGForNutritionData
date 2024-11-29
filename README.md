# RAG with Nutrition Data

This project demonstrates how **Retrieval-Augmented Generation (RAG)** can be used to improve the responses of generative models in the context of **nutrition data**. 
By integrating LLMs (**BART**, **FLAN-T5**, and **BLOOM**) with **Qdrant**, a vector search engine, we enhance the ability to generate more 
accurate and informative answers to nutrition-related queries.


**Retrieval-Augmented Generation (RAG)** is a approach that combines **retrieval-based** and **generative-based** techniques to create more relevant and context-aware responses. The idea is simple: before generating an answer, the model first **retrieves** relevant pieces of information (from a knowledge base or external data) and then uses this information to **generate** a more insightful, factually grounded response.

In the context of large language models (LLMs), RAG can significantly improve performance in tasks that require domain-specific knowledge, which the models might not have learned during training. For example, while these models are good at generating fluent text, they may struggle with providing accurate or specific information, especially when the topic is niche or specialized, such as nutrition.

## Data Source

The **nutrition dataset** used for this project is from Kaggle and can be accessed at [Nutrition Dataset on Kaggle](https://www.kaggle.com/datasets/gokulprasantht/nutrition-dataset). This dataset contains information about various food items and their nutritional facts.

## Key Components

### 1. **Qdrant: Vector Search for Memory Augmentation**

In this project, we use **Qdrant** as the retrieval system, which allows us to store the nutrition data and retrieve the most relevant pieces of information based on user queries. Qdrant is an open-source vector search engine designed for efficient retrieval and storage of high-dimensional vector data. It is often used in machine learning and natural language processing (NLP) tasks, where the data is represented as vectors (numerical embeddings), such as word or sentence embeddings.  Qdrant is particularly suitable for memory-augmented generation tasks because it supports fast and efficient vector search, allowing us to retrieve relevant data based on the query. By converting the nutrition data into high-dimensional vectors using **Sentence Transformers**, Qdrant can quickly find the most relevant pieces of information for a given query.


### 2. **Sentence Transformers: Creating Meaningful Embeddings**

**Sentence Transformers** is a library used to convert textual data into **embeddings** (dense vector representations). These embeddings capture the semantic meaning of sentences, allowing models to compare and retrieve similar texts efficiently.

### 3. **Models Used: BART, FLAN-T5, and BLOOM**

We use three different models for generating the final response: **BART**, **FLAN-T5**, and **BLOOM**. These models are all powerful pre-trained language models but note that
they are not large enough to produce a good response. Due to lack of resource, we did not utilize larger models (like Meta Llama), but for sure, they will provide better reponses. 


