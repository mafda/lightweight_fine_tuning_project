# Lightweight Fine-Tuning Project

Lightweight fine-tuning is one of the most important techniques for adapting
foundation models, because it allows you to modify foundation models for your
needs without needing substantial computational resources.

In this project, I will apply parameter-efficient fine-tuning using the
Hugging Face `peft` library.

> [See notebook](src/lightweight_finetuning.ipynb)

## Methodology

In this project, I will bring together all of the essential components of a
PyTorch + Hugging Face training and inference process. Specifically, I will:

1. Load a pre-trained model and evaluate its performance Perform
2. parameter-efficient fine tuning using the pre-trained model Perform inference
3. using the fine-tuned model and compare its performance to the original model

## Description

* PEFT technique: I used **LoRA** as my PEFT technique. LoRA is the only PEFT
  technique that is compatible with all models at this time.
* Model: I used **distilbert-base-uncased** as my model. This is a relatively
  small model that is compatible with sequence classification and **LoRA**.
* Evaluation approach: The evaluation approach covered in this project was the
  `evaluate` method with a **Hugging Face** `Trainer`.
* Fine-tuning dataset: I use a dataset from Hugging Face's datasets library
  [stanfordnlp/imdb](https://huggingface.co/datasets/stanfordnlp/imdb).

## Project Setup

### Clone this repository

```shell
(base)$: git@github.com:mafda/lightweight_fine_tuning_project.git
(base)$: cd lightweight_fine_tuning_project
```

### Configure environment

- Create the conda environment

    ```shell
    (base)$: conda env create -f environment.yml
    ```

- Activate the environment

    ```shell
    (base)$: conda activate peft
    ```

- Download the [base
  model](https://drive.google.com/drive/folders/10oHiSKabEgOMj1p88Dw0hSIN1gSHoyvG?usp=share_link).
  Unzip the folder and place it in the repo, at location
  `path/to/lightweight_fine_tuning_project/model/`.

- Download the [peft
  model](https://drive.google.com/drive/folders/10oHiSKabEgOMj1p88Dw0hSIN1gSHoyvG?usp=share_link).
  Unzip the folder and place it in the repo, at location
  `path/to/lightweight_fine_tuning_project/model/`.

- Donwload the [lora
  model](https://drive.google.com/drive/folders/10oHiSKabEgOMj1p88Dw0hSIN1gSHoyvG?usp=share_link)
  for the dog dataset.  Place it in the repo, at location
  `path/to/lightweight_fine_tuning_project/model/`.

## Project Structure

```shell
.
├── README.md
├── environment.yml
├── model
│   ├── base
│   ├── lora
│   └── peft
└── src
    └── lightweight_finetuning.ipynb
```

## References

- [Generative AI Nanodegree
  Program](https://www.udacity.com/course/generative-ai--nd608)

---

made with 💙 by [mafda](https://mafda.github.io/)
