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

## Data

Dataset: UIT-ViIC
Source: UIT-ViIC (Vietnamese Image Captioning Dataset).
Subset: ball sports images derived from COCO.
Each image: 5 human-written Vietnamese captions.
Example caption:
"Một cầu thủ đang sút bóng trong một trận đấu bóng đá."

Note: The dataset is not included in this repository. Please obtain UIT-ViIC from the official source and place it under your data directory.
