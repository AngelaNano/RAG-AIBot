# Mini RAG Chatbot - Streamlit Document Q&A

## Overview
Streamlit app for summarizing TXT/CSV files and answering questions about their content. Built with local processing (no external APIs required). Supports both summarization and keyword-based Q&A.

## Model/Source
- **Approach**: Pure Python heuristics (sentence scoring + keyword matching)
- **Libraries**: Streamlit, Pandas (CSV parsing), no pretrained models
- **Source**: 100% custom code, open source (MIT license)

## Model Selection Rationale
Chose **rule-based local processing** over Hugging Face/OpenAI APIs because:
- **Zero cost/quotas**: Perfect for classroom demos and unlimited usage
- **Transparency**: All logic visible/auditable (no black box models)
- **Privacy**: Documents stay local, no data sent to external services
- **Speed**: Instant responses vs API latency
- **AGILE-friendly**: Easy to iterate (5 sprints: file upload → CSV → summary → Q&A → UI polish)


## API Usage
No external APIs used. Processing pipeline:
1. **File → Text**: Pandas for CSV→string, raw decode for TXT
2. **Summary**: Score sentences by uniqueness + length → top 3
3. **Q&A**: Keyword overlap matching across all sentences
4. **RAG**: Full document context always injected into processing

## AGILE Process (5 Sprints)
