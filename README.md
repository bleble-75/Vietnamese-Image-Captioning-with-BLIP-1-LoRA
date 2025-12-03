# Vietnamese-Image-Captioning-with-BLIP-1-LoRA

This repository contains an implementation of a Vietnamese image captioning system based on the BLIP-1 vision–language model, fine-tuned with Low-Rank Adaptation (LoRA) on the UIT-ViIC dataset (ball sports subset).

## 1. Overview

- Task: Generate Vietnamese captions for images related to ball sports.
- Base model: BLIP-1 (Bootstrapped Language–Image Pre-training) with a ViT image encoder and Transformer text decoder.
- Fine-tuning method: LoRA for parameter-efficient adaptation.
- Dataset: UIT-ViIC (Vietnamese Image Captioning Dataset) – COCO-based ball sports subset with 5 human-written Vietnamese captions per image.

## 2. Main Features

- BLIP-1 fine-tuning with LoRA on Vietnamese captions.
- Config-based training pipeline (YAML).
- Support for training, evaluation and inference scripts.
- Evaluation with standard captioning metrics:
  - BLEU, METEOR, ROUGE-L, CIDEr, SPICE.
- Qualitative examples comparing zero-shot BLIP-1 and LoRA-fine-tuned captions.

## 3. Project Structure

```text
.
├─ src/
│  ├─ train.py          # LoRA fine-tuning pipeline
│  ├─ eval.py           # Evaluation with captioning metrics
│  ├─ inference.py      # Inference script for new images
│  ├─ data_loader.py    # UIT-ViIC dataset loader + collator
│  ├─ utils_common.py   # Path resolving, COCO-style JSON loading
│  ├─ utils_metrics.py  # COCO metrics (BLEU, METEOR, ROUGE-L, CIDEr, SPICE)
│  ├─ split_utils.py    # Train/val split helpers
│  ├─ check_dataset.py  # Dataset sanity checks
├─ configs/
│  └─ default.yaml      # Training configuration
├─ notebooks/
│  └─ exploration_and_logs.ipynb   # (optional) experiments and logs
├─ assets/
│  ├─ loss_curve.png
│  ├─ metrics_table.png
│  └─ qualitative_examples.png
├─ requirements.txt
└─ README.md
