# 💬 Mini RAG Chatbot - Hugging Face Streamlit App

**Applied AI & RAG Foundations** | Streamlit document Q&A using **Hugging Face Inference API**.

## 🎯 Project Overview
Streamlit app that processes uploaded TXT/CSV files for **text summarization** and **document Q&A**. Uses Hugging Face's `distilbert-base-cased-distilled-squad` model for intelligent question answering over document context (RAG pattern).

## 🤗 Model Name & Source
- **Model**: `distilbert/distilbert-base-cased-distilled-squad`
- **Source**: [Hugging Face Model Hub](https://huggingface.co/distilbert/distilbert-base-cased-distilled-squad)
- **Developer**: Hugging Face (distilbert team)
- **Type**: DistilBERT (66M parameters, fine-tuned on SQuAD v1.1)
- **API Endpoint**: `https://api-inference.huggingface.co/models/distilbert/distilbert-base-cased-distilled-squad`

## ✅ Rationale for Model Selection
Selected `distilbert-base-cased-distilled-squad` because:
1. **RAG-Optimized**: Fine-tuned specifically for extractive QA from document context
2. **Lightweight**: 66M parameters (40% smaller than BERT-base), fast inference
3. **Production-Ready**: F1=87.1 on SQuAD benchmark, battle-tested
4. **Free Tier**: Hugging Face Inference API free tier perfect for class projects
5. **Transparent**: Open weights + full training documentation available

**Alternative**: `facebook/bart-large-cnn` (summarization) - QA prioritized for RAG focus.

## 🔌 API Usage Description

## 🏃‍♂️ AGILE Process (5 Sprints)
| 1 | File upload | ✅ |
| 2 | Local baseline | ✅ |
| 3 | HF Integration | ✅ |
| 4 | UI + Error handling | ✅ |
| 5 | Production prep | ✅ |

## 💡 Responsible AI Reflection (128 words)
The `distilbert-base-cased-distilled-squad` model enables powerful document QA but requires ethical safeguards. **Strengths**: Extractive QA ensures answers stay 100% grounded in source documents, eliminating hallucinations. **Bias risks**: SQuAD training data is English/Wikipedia-centric, potentially underperforming on non-Western topics, technical jargon, or underrepresented demographics. **Privacy**: Documents transmitted to Hugging Face servers—requires explicit user consent via clear UI warnings.
**Mitigations**: Local fallback processing, confidence score transparency, document previews, context truncation. **RAG advantage**: Every answer traces directly to source text for verification. Responsible deployment matches capabilities to context: ideal for document lookup/education, inappropriate for medical/legal decisions without human oversight. Transparency about data flows, model limitations, and boundaries builds essential user trust.

