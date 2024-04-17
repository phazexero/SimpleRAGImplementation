# Simple RAG Implementation
RAG Implementation method on a local system

# What is RAG?
* RAG is Retrieval Augmented Generation
It mainly comprises 3 main components as suggested in the name.
* Retrieval: The retrieval part is for getting information through a database, which can be a pdf, an SQL server, or some source. The source can be updated regularly and the information stored can be retrieved, without training.
* Augmented: Augmentation is the part where the information is attached to the generation system and the retrieval system, so now questions can be asked to the LLM in natural language and updated information and domain-specific information can then be output in a natural language format.
* Generation: This is the part where the above information from the retriever and the augmenter is used and then a new text in natural language is generated with the help of an LLM (let's say).

What this overall process does, is that it helps create an information bucket from where one can retrieve up-to-date data on a very specific data, while not having the burden of training it constantly. It is a powerful technique, and when combined with LORA/QLoRA, can help one run LLMs on less hardware and produce a natural language generation which can fetch up-to-date context-oriented data. 

Key Terms for Understanding Large Language Models (LLMs)
This document explains key terms related to Large Language Models (LLMs) and their functionalities.

1. Token:
* A sub-word unit of text.
* Example: "hello, world!" can be split into tokens like ["hello", ",", "world", "!"]
* Tokens can be entire words, parts of words, or punctuation marks.
* In English, roughly 1 token is equivalent to 4 characters and 100 tokens are approximately equal to 75 words.
* Text is broken down into tokens before being fed to an LLM.

2. Embedding:
* A numerical representation of data, often used for text.
* Example: A sentence can be represented as a vector with 768 values.
* Similar text pieces (in meaning) will ideally have similar embedding values.

3. Embedding Model:
* A model that transforms input data into a numerical representation.
* Example: A text embedding model might take 384 tokens and convert them into a 768-dimensional vector.
* Embedding models are distinct from LLM models, although they can be used in conjunction.

4. Similarity Search/Vector Search:
* This technique aims to find vectors close together in high-dimensional space.
* Similar text pieces, when passed through an embedding model, should have high similarity scores, while dissimilar texts will have lower scores.
* Common similarity measures include dot product and cosine similarity.

5. Large Language Model (LLM):
* A model trained to represent text patterns numerically.
* Generative LLMs can continue a sequence based on a provided input.
* Example: Given "hello, world!", a generative LLM might output "we're going to build a RAG pipeline today!".
* The generated text heavily depends on the training data and provided prompt.

6. LLM Context Window:
* The number of tokens an LLM can accept as input.
* Example (as of March 2024): GPT-4 has a default context window of 32k tokens (around 96 pages) but can handle up to 128k. Gemma (an open-source LLM from Google, March 2024) has a context window of 8,192 tokens (roughly 24 pages).
* A larger context window allows LLMs to consider more information for tasks like query answering or generation. This can be beneficial in applications like RAG pipelines, where a larger window enables the model to use more retrieved reference items.

7. Prompt:
* The input provided to a generative LLM.
* "Prompt engineering" is the art of crafting a specific text-based (or potentially image-based) input to achieve a desired output from the LLM.
* This technique leverages an LLM's in-context learning ability, allowing it to analyze the prompt and generate a suitable response based on its understanding of language. It's important to note that LLM outputs are probabilistic; hence, terms like "may output" are used.
