# 🌐 BharatBot

A **context-aware AI chatbot** fine-tuned on **Indian census data** using **LoRA (Low-Rank Adaptation)**.  
BharatBot supports intent detection, context retention, and culturally sensitive, unbiased responses. The repository contains preprocessing, intent dataset creation, LoRA adapters/checkpoints and an interactive Gradio demo.

---

## 🚩 Table of Contents
- [Overview](#overview)  
- [Key Features](#key-features)  
- [Project Structure](#project-structure)  
- [Quick Start](#quick-start)  
  - [Clone](#clone)  
  - [Install dependencies](#install-dependencies)  
  - [Run notebook (Colab/Jupyter)](#run-notebook-colabjupyter)  
  - [Launch Gradio app](#launch-gradio-app)  
- [Dataset](#dataset)  
- [Usage Examples](#usage-examples)  
- [Development / Reproducibility](#development--reproducibility)  
  - [Recommended `.gitignore`](#recommended-gitignore)  
  - [Git LFS for large model files](#git-lfs-for-large-model-files)  
  - [Requirements file sample](#requirements-file-sample)  
- [Ethical Considerations](#ethical-considerations)  
- [Contributing](#contributing)  
- [Contact](#contact)  
- [License](#license)  

---

## Overview

BharatBot is designed to demonstrate responsible application of conversational AI on public government datasets (Census of India 2011). The system converts tabular data into structured JSON/intents, fine-tunes a base language model using LoRA adapters to learn domain-specific responses, and deploys an interactive chatbot with context retention capabilities.

Goals:
- Provide accurate, source-grounded answers for demographic queries.
- Retain conversational context across multiple turns.
- Ensure cultural sensitivity, fairness and transparency.

---

## Key Features

- ✅ Data preprocessing & JSON/intent generation  
- ✅ Intent detection (pattern → intent mapping)  
- ✅ Context retention across multi-turn conversations  
- ✅ LoRA-based fine-tuning for lightweight domain adaptation  
- ✅ Gradio-powered interactive demo for quick testing  
- ✅ Ethical safeguards: no PII, bias mitigation, transparency on sources

---

## 📂 Project Structure

```bash
intent-detection-context-retention/
├── data/
│   ├── Intent.json             # Original intent dataset
│   └── lora_dataset.jsonl      # Processed dataset for LoRA fine-tuning
├── models/
│   └── lora_finetuned/         # Fine-tuned LoRA model checkpoints
├── src/
│   ├── intent_detection_context_retention.py   # Main training + chatbot pipeline
│   ├── data_loader.py          # (Optional) Data preprocessing logic
│   ├── train.py                # Training and fine-tuning scripts
│   ├── inference.py            # Chatbot inference + pipeline
│   └── gradio_app.py           # Gradio-based deployment
├── requirements.txt            # Python dependencies
├── README.md                   # Project documentation
└── LICENSE                     # License file


### 1. Chatbot Interface
![Chat UI](assets/screenshot_chat.png)
