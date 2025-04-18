# BoardGameGPT: AI Rule Assistant

**Project Type**: AI Application | NLP | Q&A System | Kaggle Project
**Tools Used**: Python, Google Gemini API (Flash & Embedding models), google-genai SDK, Pandas, NumPy, Scikit-learn
**Data Source**: Provided Rulebook Text (Initially hardcoded/generated)

[Link to Kaggle Notebook](https://www.kaggle.com/code/christopherflynndev/board-game-rule-helper/notebook)

## **Objective**

Create a functional and reliable question-answering system capable of understanding natural language questions about specific board game rules and providing accurate answers sourced _only_ from the provided rulebook text, utilizing the power of Large Language Models (LLMs) combined with Retrieval-Augmented Generation (RAG).

## **Key Features**

- **Retrieval-Augmented Generation (RAG) Core**:

  - Ingests rulebook text and splits it into manageable semantic chunks.
  - Generates vector embeddings for each chunk using Google's `text-embedding-004` model to capture meaning.
  - Embeds user questions and performs semantic search (via cosine similarity) to find the most relevant rule snippets.
  - Feeds the question and retrieved context to `gemini-1.5-flash-latest` to generate a final answer grounded in the source text, minimizing hallucinations.

- **Python & GenAI Stack**:

  - Built entirely in Python within a Kaggle Notebook environment.
  - Leverages the `google-genai` SDK (v1.7.0 pattern) for seamless interaction with the Gemini API.
  - Utilizes Pandas and NumPy for data manipulation and numerical operations.

- **Natural Language Q&A**:

  - Allows users to ask questions about rules in plain English (e.g., "How do I win?", "What does the 'Explore' action cost?").
  - Provides answers synthesized by the AI but constrained by the retrieved, relevant rule sections.

- **Focused Notebook Implementation**:
  - Designed as a clear demonstration of the RAG pipeline within a self-contained Kaggle Notebook.
  - Focuses on the core AI capabilities rather than complex UI or deployment infrastructure.
  - Code includes error handling and API retry logic for robustness.

## **Environment & Implementation Highlights**

- Developed and runs entirely within a **Kaggle Notebook**.
- Utilizes **Kaggle Secrets** for secure management of the Google API Key.
- Demonstrates simulation of **Vector Search** using Scikit-learn's `cosine_similarity` on NumPy arrays.
- Code is documented with Markdown cells explaining each step of the RAG process.

🔗 **Nbviewer:** [Link](https://nbviewer.org/github/christopherFlynn/BoardGameGPT/blob/main/board-game-rule-helper.ipynb)  
🔗 **View Blog Post:** [Link](https://christopherflynn.dev/ai%20projects/natural%20language%20processing/python/boardgamegpt/)
