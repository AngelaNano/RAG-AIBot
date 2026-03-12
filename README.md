# 💬 Mini RAG Chatbot - Hugging Face Streamlit App

**Applied AI & RAG Foundations** | Streamlit app using **Hugging Face Inference API** for document Q&A and summarization.

## 🎯 Project Overview
Streamlit chatbot that answers questions about uploaded TXT/CSV files using Hugging Face NLP models. Supports both **summarization** and **domain-specific Q&A** with full RAG context injection.

## 🤗 Model Name & Source
- **Model**: `distilbert-base-cased-distilled-squad` (Question-Answering)
- **Source**: Hugging Face Model Hub
- **API**: Hugging Face Inference API (`https://api-inference.huggingface.co/models/`)

## ✅ Rationale for Model Selection
**distilbert-base-cased-distilled-squad** was selected because:
1. **RAG-Optimized**: Specifically fine-tuned for extractive QA from document context
2. **Lightweight**: 66M parameters, fast inference (<1s), CPU-friendly  
3. **Proven**: SOTA on SQuAD benchmark, battle-tested in production
4. **Free Tier**: Hugging Face Inference API free tier perfect for class project
5. **Transparent**: Open weights, full training details available

**Alternative considered**: `facebook/bart-large-cnn` (summarization) - DistilBERT chosen for primary Q&A focus.

## 🔌 API Usage Description
