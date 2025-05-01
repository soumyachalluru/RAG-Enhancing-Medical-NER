## 🛠️ Project Goals

- Handle ambiguous, abbreviated, or unclear entities using a RAG pipeline.
- Improve entity coverage, accuracy, and interpretability using LLM prompting.

---

## ✅ Completed Work

- ✅ Fine-tuned BERT for Medical NER using SFT (Supervised Fine-Tuning) and PEFT (Parameter-Efficient Fine-Tuning).
- ✅ Achieved:
  - **Weighted F1 Score**: 0.70  
  - **Accuracy**: 82%
- ✅ Integrated external knowledge using the **UMLS dataset** (470K annotated entries).
- ✅ Built a **RAG pipeline** using:
  - **Embeddings**: BioBERT
  - **Vector Store**: Pinecone
  - **Retrieval**: Cosine Similarity + Keyword Matching
  - **Prompting**:
    - 3-shot prompting
    - Retrieve-Task-Example prompting
    - Chain-of-Thought prompting
    - Instruction-based few-shot prompting

---

## 🔁 RAG Workflow

1. **Entity Extraction**: Run clinical notes through the fine-tuned BERT NER model.
2. **Entity Enhancement**:
   - Use BioBERT to embed extracted entity spans.
   - Query Pinecone to retrieve top-k relevant entries from UMLS.
   - Re-rank results using cosine similarity and keyword overlap.
3. **Prompt Engineering**:
   - Enhance output with carefully crafted LLM prompts based on retrieved knowledge.
4. **LLM Response Generation**: Generate refined entity labels, disambiguations, or expanded descriptions.

---

## 🔮 Future Work

- 🔧 **Refine Fine-Tuning**: Improve F1 score with better hyperparameters and training cycles.
- 🔗 **RAG Integration**: Seamlessly connect BERT and RAG stages into a unified pipeline.
- ✅ **Evaluation**: Compare NER performance with and without RAG on held-out clinical notes.
- ♻️ **Iterative Optimization**: Use feedback loops and error analysis to improve retrieval strategies and prompting logic.
