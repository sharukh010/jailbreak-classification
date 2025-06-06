# Jailbreak Prompt Classification

This project demonstrates how to fine-tune a BERT-based model to classify text prompts as either **benign** or **jailbreak**. It uses the [jackhhao/jailbreak-classification](https://huggingface.co/datasets/jackhhao/jailbreak-classification) dataset and leverages Hugging Face's `transformers` and `datasets` libraries.

## 🔍 Project Overview

The goal is to develop a robust model that can differentiate between safe and potentially harmful (jailbreak) prompts, which is especially useful for content moderation and safety in LLM deployments.

## 📦 Dataset

- **Name**: `jackhhao/jailbreak-classification`
- **Features**:
  - `prompt`: The input text prompt.
  - `type`: Label indicating whether the prompt is `benign` or `jailbreak`.

## 🧰 Tools & Libraries

- [Hugging Face Transformers](https://huggingface.co/transformers/)
- [Hugging Face Datasets](https://huggingface.co/docs/datasets/)
- PyTorch

## 🧪 Preprocessing Steps

1. Loaded the dataset using `load_dataset`.
2. Filtered prompts based on length (< 5000 characters).
3. Tokenized prompts using `bert-base-uncased`.
4. Encoded labels: `benign` → 0, `jailbreak` → 1.
5. Removed unnecessary columns.
6. Prepared PyTorch DataLoaders with dynamic padding.

## 🧠 Model

- **Base model**: `bert-base-uncased`
- **Task**: Sequence Classification
- Fine-tuned using Hugging Face's training utilities (can be extended further).

## 🚀 Running the Project

### 1. Install Dependencies

```bash
pip install datasets transformers torch
```

### 2. Run the Notebook

Use Jupyter or any notebook environment to run `Jailbreak_classification.ipynb`.

### 3. (Optional) Train the Model

Integrate Hugging Face's `Trainer` API or a custom training loop to fine-tune the model further on your machine.

## 📈 Results
- Accuracy : 98.4%
- f1 score : 98.54%

## 📂 File Structure

```
├── Jailbreak_classification.ipynb   # Main notebook
├── README.md                        # Project documentation
```

## ✍️ Author

Pathan Sharukh Khan

## 📜 License

This project is open-source and available under the [MIT License](LICENSE).
