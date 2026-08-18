# Proxy Tuning for Vision-Language Models

**Proxy Tuning for Vision-Language Models** is a parameter-free approach for improving large vision-language models (VLMs) for image captioning **without accessing or modifying their internal weights**.

The project extends proxy tuning to the vision-language domain by using a small fine-tuned **expert model** and its untuned **anti-expert counterpart** to steer a larger target VLM during inference through their output-logit differential.

## Key Contributions

* **Proxy tuning for VLMs:** Extends proxy tuning from language models to **vision-language models for image captioning**.
* **Weight-free adaptation:** Improves large pretrained VLMs without requiring access to their internal parameters.
* **Expert–anti-expert steering:** Uses the difference between a fine-tuned expert and an untuned model to guide the target model's decoding.
* **Decoding variants:** Explores DExperts-style weighting, contrastive decoding, **min-max normalization**, and **z-score normalization**.
* **Scalable VLM adaptation:** Demonstrates the approach across BLIP and BLIP-2 models and diverse medical, creative, and natural-image captioning datasets.

## Evaluation

The method was evaluated across datasets including **IU X-Ray, ROCO, Pokémon, MidJourney, Flickr8k, and COCO** using **BLEU-4, CIDEr, ROUGE-L, and cosine similarity**.

Experiments show that proxy tuning can improve large VLMs without direct weight access, with improvements of up to **15.5% BLEU** reported on the evaluated medical-domain setting.

### Status

**Research manuscript — not yet published.**

### Technologies

Python · PyTorch · BLIP · BLIP-2 · LoRA · Hugging Face · CUDA
