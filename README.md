# Cricket Expert Chatbot Application - Generative AI


### Admin - Uploads PDF

    └── PDF Split
        └── Distributed in Chunks 
            └── Vectorized
                └── Titan Embedding Model leveraged to create vector representation
                    └── Save indices (S3 Bucket)

### User - Query passed in chatbot input


    └── Index files are downloaded from S3 and saved locally to build vector store
        └── Langchain RetrievalQA
            └── Saved Embedding Model leveraged to convert query into vector embedding
                └── Similarity Search executed
                    └── Gets back 5 matching documents and builds context
                        └── Leverage prompt template to provide query and context to LLM
                            └── Show LLM output

