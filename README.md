# 💬 Mini RAG Chatbot - Hugging Face Streamlit App

**Applied AI & RAG Foundations** | Streamlit document Q&A using **Hugging Face Inference API**.

## 🎯 Project Overview
Streamlit app that processes uploaded TXT/CSV files for **text summarization** and **document Q&A**. Uses Hugging Face's `distilbert-base-cased-distilled-squad` model for intelligent question answering over document context (RAG pattern).

## 🤗 Model Name & Source **[REQUIRED]**
- **Model**: `distilbert/distilbert-base-cased-distilled-squad`
- **Source**: [Hugging Face Model Hub](https://huggingface.co/distilbert/distilbert-base-cased-distilled-squad)
- **Developer**: Hugging Face (distilbert team)
- **Type**: DistilBERT (66M parameters, fine-tuned on SQuAD v1.1)
- **API Endpoint**: `https://api-inference.huggingface.co/models/distilbert/distilbert-base-cased-distilled-squad`

## ✅ Rationale for Model Selection **[REQUIRED]**
Selected `distilbert-base-cased-distilled-squad` because:
1. **RAG-Optimized**: Fine-tuned specifically for extractive QA from document context
2. **Lightweight**: 66M parameters (40% smaller than BERT-base), fast inference
3. **Production-Ready**: F1=87.1 on SQuAD benchmark, battle-tested
4. **Free Tier**: Hugging Face Inference API free tier perfect for class projects
5. **Transparent**: Open weights + full training documentation available

**Alternative**: `facebook/bart-large-cnn` (summarization) - QA prioritized for RAG focus.

## 🔌 API Usage Description **[REQUIRED]**
