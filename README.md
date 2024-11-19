# LexSumm and LexT5: Benchmarking and Modeling Legal Summarization Tasks in English

This repository contains the code and models for the paper *LexT5: Benchmarking and Modeling Generative Legal Tasks in English*, which introduces the LexT5 model and the LexGen benchmark for legal summarisation tasks.

## Introduction

In the field of legal NLP, there has been a focus primarily on predictive tasks, with generative tasks receiving less attention. To address this, we introduce LexGen, a benchmark specifically designed for training and evaluating legal generative tasks in English. LexSumm includes eight English legal summarisation datasets from various jurisdictions, such as the US, UK, EU, and India. 

We also introduce **LexT5**, a legal-oriented sequence-to-sequence model that addresses the limitations of existing encoder-only models in the legal domain. The model is pre-trained on a large corpus of legal texts and can be fine-tuned on the LexGen benchmark.

## Models

We provide the pre-trained **LexT5** models, which can be fine-tuned for legal summarisation tasks. The models are available in three sizes, catering to different computational needs:

- **LexT5-Small:** 60M parameters  
  [Download LexT5-Small](https://huggingface.co/santoshtyss/lt5-small)
  
- **LexT5-Base:** 220M parameters  
  [Download LexT5-Base](https://huggingface.co/santoshtyss/lt5-base)
  
- **LexT5-Large:** 770M parameters  
  [Download LexT5-Large](https://huggingface.co/santoshtyss/lt5-large)

## Datasets

### LexSumm

The full **LexSumm** dataset, containing eight legal summarisation datasets from multiple jurisdictions, can be downloaded here:

- **[Full LexSumm Dataset](https://huggingface.co/datasets/CJWeiss/LexSumm)**: Collection of all datasets below.

Each dataset adheres to the same format with columns: `input`, `output`, and `id`. Below are brief descriptions of the individual datasets included in **LexSumm**:

- **[BillSum](https://huggingface.co/datasets/CJWeiss/billsum_id_rename)**: US Congressional bills with summaries by the Congressional Research Service.
- **[InAbs](https://huggingface.co/datasets/CJWeiss/inabs_id_rename)**: Indian Supreme Court cases with headnotes as summaries.
- **[UKAbs](https://huggingface.co/datasets/CJWeiss/ukabs_id_rename)**: UK Supreme Court judgments with official press summaries.
- **[EurLexSum](https://huggingface.co/datasets/CJWeiss/eurlexsum_id_rename)**: Summaries of enforced EU legislation from the EUR-Lex platform.
- **[GovReport](https://huggingface.co/datasets/CJWeiss/govreport_id_rename)**: U.S. Government Accountability Office reports with expert-written summaries.
- **[MultiLexSum-Long](https://huggingface.co/datasets/CJWeiss/multilong_id_rename)**: Multi-paragraph summaries of U.S. civil rights lawsuits.
- **[MultiLexSum-Short](https://huggingface.co/datasets/CJWeiss/multishort_id_rename)**: Single-paragraph summaries of civil rights lawsuits.
- **[MultiLexSum-Tiny](https://huggingface.co/datasets/CJWeiss/multitiny_id_rename)**: One-sentence summaries of civil rights lawsuits in Twitter-like format.

### ZeroLexSumm

The full zero-shot dataset: **ZeroLexSumm** can be downloaded here:

- **[Full ZeroLexSumm Dataset](https://huggingface.co/datasets/CJWeiss/ZeroLexSumm)**: Collection of all zero-shot datasets below.

All ZeroLexSumm datasets are derived from the respective LexSumm datasets and adhere to consistent format with columns: `input`, `output`, `id`, `cluster`, `old_id` and `length`. 

- `cluster`: which inout bracket 0-8k, 8k-16k, 16k+ and longest
- `old_id`: ID in the LexSumm dataset
- `length`: length of the input

Here you can find the seperate datasets included **ZeroLexSumm**:

- **[BillSum](https://huggingface.co/datasets/CJWeiss/LGZ_billsum)**
- **[InAbs](https://huggingface.co/datasets/CJWeiss/LGZ_inabs)**
- **[UKAbs](https://huggingface.co/datasets/CJWeiss/LGZ_ukabs)**
- **[EurLexSum](https://huggingface.co/datasets/CJWeiss/LGZ_eurlexsum)**
- **[GovReport](https://huggingface.co/datasets/CJWeiss/LGZ_govreport)**
- **[MultiLexSum-Long](https://huggingface.co/datasets/CJWeiss/LGZ_multilong)**
- **[MultiLexSum-Short](https://huggingface.co/datasets/CJWeiss/LGZ_multishort)**
- **[MultiLexSum-Tiny](https://huggingface.co/datasets/CJWeiss/LGZ_multitiny)**

## Citation

If you use LexT5 or LexSumm in your research or application, please cite our paper:

```bibtex
@inproceedings{t-y-s-s-etal-2024-lexsumm,
  title = "{L}ex{S}umm and {L}ex{T}5: Benchmarking and Modeling Legal Summarization Tasks in {E}nglish",
  author = "T.y.s.s, Santosh and Weiss, Cornelius and Grabmair, Matthias",
  booktitle = "Proceedings of the Natural Legal Language Processing Workshop 2024",
  month = nov,
  year = "2024",
  address = "Miami, FL, USA",
  publisher = "Association for Computational Linguistics",
  url = "https://aclanthology.org/2024.nllp-1.35",
  pages = "381--403",
}
