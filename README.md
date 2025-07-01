# 🤖 RAG with Subquery Decomposition and Answer Synthesis

This project demonstrates an advanced **Retrieval-Augmented Generation (RAG)** pipeline using **LangChain**, **Google Gemini (via LangChain-Google-GenAI)**, and a vector store retriever such as **Chroma** or **FAISS**.

We use the **Query Decomposition** technique (RAG Fusion) to generate multiple subqueries for a single user question. Each subquery is executed independently through a retriever and an LLM, and finally, all their answers are merged to produce a comprehensive response.

---

## 🔍 Objective

To improve retrieval quality and generate more complete answers by:

- Generating **multiple diverse sub-questions** from the main question using an LLM.
- Retrieving documents independently for each subquery.
- Asking the LLM to generate answers to each subquery.
- **Synthesizing** all those answers into a final, rich answer for the original question.

---

## 🧠 Techniques Used

### ✅ 1. Multi-Query Generation
We use an LLM prompt to generate diverse reformulations of a single user query.

### ✅ 2. Subquery Answering with Contextual Memory

### ✅ 3. Final Answer Synthesis
All individual Q&A pairs are accumulated in a string (q_a_pairs). We then prompt the LLM to generate a synthesized final answer using
