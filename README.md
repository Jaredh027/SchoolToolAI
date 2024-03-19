# SchoolToolAI
This is a repo dedicated to creating RAG pipelines to help teachers and students with textbook-related work. Such as explaining textbook information in more or less detail and allowing teachers to create hw assignments and exams.

## Architecture Diagram

Here is how the system is designed:

```mermaid
graph LR
E(User Query) --> A(FRONTEND<br/>Chat UI<br/>Streamlit)
H(PDF of Textbooks) -- Text Split<br/>Chunks --> N(Vector DB)
N -- Related<br/>Textbook Info --> K(Augmented Prompt)
A --> K
A -- Retrieval --> N
K --> L((Mixtral 8X7B LLM))
L --> M(Streamlit<br/>Chat Output)
```
