# Code Switching NLP | Code Saviours SI-26 | Halima Javed

This project focuses on **Roman Urdu-English code-switching detection and token-level language identification** using NLP and XLM-RoBERTa.

The project was completed as part of the **Code Saviours SI-26 Machine Learning Internship – Project 2**.

---
# Code Switching NLP

A language identification model that detects Roman Urdu and English tokens in code-switched sentences.

## Why This Matters

People in Pakistan often mix Roman Urdu and English in everyday messages, such as "Yaar kal presentation hai still not ready." This makes language identification more challenging for traditional NLP systems. This project helps identify which parts of a sentence are Roman Urdu and which are English, making it useful for code-switching detection and multilingual NLP applications.

##  Live Demo

Try the deployed Urdu-English Code-Switching Language Identifier:

👉 https://halimajaved592-urdu-english-code-switching-demo.hf.space/?__theme=system&deep_link=ytlgO7yuLF4
https://huggingface.co/spaces/halimajaved592/urdu-english-code-switching-demo

---

##  Hugging Face Model

The trained XLM-RoBERTa token classification model is available here:

👉  https://huggingface.co/halimajaved592/urdu-english-code-switching-xlm-roberta

---

## How It Works

The project uses an XLM-RoBERTa model trained on Roman Urdu-English code-switched text. Each token in a sentence is classified as URD, ENG, or MIX. The trained model is uploaded to Hugging Face and connected to a Gradio web interface. Users can enter a sentence and see the predicted language and confidence score for each token.

## Results

The model achieved the following results on the test set:

- Accuracy: **96.43%**
- Precision: **96.64%**
- Recall: **96.43%**
- Weighted F1-Score: **96.12%**

### Class-wise F1 Scores

- URD: **0.99**
- ENG: **0.95**
- MIX: **0.71**

## How to Run Locally

Clone the repository and install the required packages:

```bash
pip install transformers torch gradio spaces
Then run the application:

python app.py

The application will open as a Gradio interface where you can enter Roman Urdu-English sentences and view token-level predictions.

##  Project Overview

The goal of this project is to identify language at the token level in Roman Urdu-English code-switched text.

For example:

**Input:**

> Yaar kal presentation hai still not ready

The model identifies:

| Token | Language |
|---|---|
| Yaar | URD |
| kal | URD |
| presentation | ENG |
| hai | URD |
| still | ENG |
| not | ENG |
| ready | ENG |

---

##  Dataset

The dataset was created as part of the **Code Saviour SI-26 Project 2**.

It contains Roman Urdu-English sentences collected from publicly available sources where Roman Urdu and English are commonly mixed in everyday communication.

The data was cleaned, organized, tokenized, and manually labeled.

### Labels

- **URD** – Roman Urdu word
- **ENG** – English word
- **MIX** – Mixed-language token

### Dataset Information

- **Total Sentences:** 199
- **Total Token Rows:** 971
- **Languages:** Roman Urdu + English
- **Format:** CSV
- **Task:** Token-level language identification

### Dataset Columns

- `sentence` – Original mixed-language sentence
- `word` – Individual word/token
- `label` – Language label (`URD`, `ENG`, or `MIX`)

---

##  Model

The project uses **XLM-RoBERTa** for token-level language classification.

### Label Mapping

```text
URD → 0
ENG → 1
Built By

Halima Javed | Code Saviours SI-26 | 2026
SI26-ML-HJ-032

MIX → 2
