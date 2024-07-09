# Battle of the Semantics: GraphRag vs Embeddings Index

Retrieval Augmented Generation (RAG) is often performed by chunking long texts, creating a text embedding for each chunk, and retrieving chunks for including in the LLM generation context based on a similarity search against the query. This approach works well in many scenarios, and at compelling speed and cost trade-offs, but doesn't always cope well in scenarios where a detailed understanding of the text is required.

GraphRag ( [microsoft.github.io/graphrag](https://microsoft.github.io/graphrag/) ), a new indexing method released by Microsoft, promises to address this defficiency by using an LLM to analyse the indexed text and construct and knowledge graph of entities from it. This more detailed semantic understanding of the content of the text can result in searches that produces a more accurate and complete context for the LLM to work with in generation.

To compare both method, let's see what results we get when indexing and retrieving the text with both techniques.

See [battle-of-the-semantics.ipynb](battle-of-the-semantics.ipynb)