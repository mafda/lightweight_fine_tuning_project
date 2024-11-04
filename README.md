# Lightweight Fine-Tuning Project

Lightweight fine-tuning is one of the most important techniques for adapting
foundation models, because it allows you to modify foundation models for your
needs without needing substantial computational resources.

In this project, I will apply parameter-efficient fine-tuning using the
Hugging Face `peft` library.

## Methodology

In this project, I will bring together all of the essential components of a
PyTorch + Hugging Face training and inference process. Specifically, I will:

1. Load a pre-trained model and evaluate its performance Perform
2. parameter-efficient fine tuning using the pre-trained model Perform inference
3. using the fine-tuned model and compare its performance to the original model
