# Adaptive-LoRA-Router
Fine tuning LLM for more than one downstream task with the help of LoRA adapters

Overview

Large Language Models are typically fine-tuned for a single downstream task, resulting in multiple specialized models that consume significant storage and computational resources. While Low-Rank Adaptation (LoRA) enables parameter-efficient fine-tuning by learning lightweight adapters instead of updating the entire model, most implementations still focus on a single domain.
This project explores a modular alternative.
Instead of maintaining multiple independently fine-tuned language models, a single Qwen 3B base model is shared across several domain-specific LoRA adapters. At inference time, an intelligent routing component determines the user's intent and dynamically loads the most appropriate adapter.

The initial implementation focuses on three domains:

Code Generation
Mathematical Reasoning
Content Writing
