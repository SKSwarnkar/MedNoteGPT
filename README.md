# LLM-MedNote-Simplifier

This project uses OpenAI’s GPT-3.5-turbo to simplify synthetic clinical notes generated from [Synthea](https://synthea.mitre.org/downloads). It also performs urgency classification and visualizes prompt effectiveness using embeddings.

##  Features

-  Zero-shot prompting
-  Few-shot prompting (standard + conversational)
-  Chain-of-Thought (CoT)
-  Tree-of-Thought (ToT)
-  Urgency classification downstream task
-  Embedding visualization via t-SNE and Cosine Similarity
-  Evaluation using confusion matrix, accuracy, label distribution

##  Dataset

- Based on **100-patient synthetic records** from Synthea (CSV format)
- Notes are dynamically generated using patient tables (e.g., patients.csv, conditions.csv)

##  Models Used

- `gpt-3.5-turbo` (OpenAI)
- Chain-of-Thought and Tree-of-Thought templates for structured reasoning

##  Tools

- Python, Pandas, Matplotlib, Seaborn
- `t-SNE` for dimensionality reduction
- Graphviz for pipeline diagrams
- `sklearn` for classification metrics

##  Structure

```bash
LLM-MedNote-Simplifier/
├── data/                      # Synthea CSV files + synthetic notes
├── LLM_MedNotes_v1.2.ipynb    # Final cleaned notebook
├── cache/                     # Zero-shot, few-shot, and classification responses
├── images/                    # Flowcharts, t-SNE plots, confusion matrix
└── README.md
