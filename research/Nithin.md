# Component

Search Engine
# Proposed Technology

Neo4j +OpenSearch

# What does this component do?
Retrieves data from multiple sources based on the search query and displays them in the order of their relevancy. It is important to note that one retrieval strategy is not enough and that a combination of multiple retrieval strategies will be used as this allows us to get information that is not just a simple keyword retrieval but also historically important information and conceptually related information. 

# Why did you choose this technology?

- Reduced Architectural Complexity while supporting hybrid retreival requirements. OpenSearch handles semantic, keyword, and temporal retrieval, while Neo4j handles graph retrieval, allowing the system to perform comprehensive information retrieval. Compared to architectures that use separate vector databases, openSearch can perform both vector and keyword search within a single platform.
- The architecture is easily scalable and modular.
- Lots of enterprise deployments follow a similar architecture (with llamaindex).

# Advantages

- Comprehensive retrieval coverage (supports semantic, keyword, graph, and temporal retrieval)
- Better context for LLMs (the RAG pipeline would get context from the reranked results improving factual accuracy.)

# Limitations

- Semantic search performance may be lower than dedicated vector databases
- Running vector search, full-text search, graph traversal and reranking requires additional compute resources, storage, and latency compared to simpler retrieval architectures.

# Would you use it in Company Brain?

If implemented properly without mistakes it would be perfect for Company Brain so yes, I would.

# References

https://github.com/opensearch-project/OpenSearch
https://github.com/neo4j/neo4j
https://medium.com/aingineer/a-complete-guide-to-implementing-hybrid-rag-86c0febba474
