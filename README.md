# Simple RAG Implementation
RAG Implementation method on a local system

# What is RAG?
* RAG is Retrieval Augmented Generation
It mainly comprises 3 main components as suggested in the name.
* Retrieval: The retrieval part is for getting information through a database, which can be a pdf, an SQL server, or some source. The source can be updated regularly and the information stored can be retrieved, without training.
* Augmented: Augmentation is the part where the information is attached to the generation system and the retrieval system, so now questions can be asked to the LLM in natural language and updated information and domain-specific information can then be output in a natural language format.
* Generation: This is the part where the above information from the retriever and the augmenter is used and then a new text in natural language is generated with the help of an LLM (let's say).

What this overall process does, is that it helps create an information bucket from where one can retrieve up-to-date data on a very specific data, while not having the burden of training it constantly. It is a powerful technique, and when combined with LORA/QLoRA, can help one run LLMs on less hardware and produce a natural language generation which can fetch up-to-date context-oriented data. 
