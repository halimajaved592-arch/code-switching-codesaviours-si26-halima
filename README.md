# Code Switching NLP | Code Saviours SI-26 | Halima Javed

This project focuses on **Roman Urdu-English code-switching detection and token-level language identification** using NLP and XLM-RoBERTa.

The project was completed as part of the **Code Saviours SI-26 Machine Learning Internship – Project 2**.

---

##  Live Demo

Try the deployed Urdu-English Code-Switching Language Identifier:

👉 https://halimajaved592-urdu-english-code-switching-demo.hf.space/?__theme=system&deep_link=ytlgO7yuLF4
https://huggingface.co/spaces/halimajaved592/urdu-english-code-switching-demo

---

##  Hugging Face Model

The trained XLM-RoBERTa token classification model is available here:

👉  https://huggingface.co/halimajaved592/urdu-english-code-switching-xlm-roberta

---

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
MIX → 2
