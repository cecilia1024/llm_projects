# llm_projects
# QLoRA Fine-Tuning LLaMA 2 for Text Summarization

## Overview
This project fine-tunes the [LLaMA 2](https://ai.facebook.com/llama/) model using [QLoRA](https://arxiv.org/abs/2305.14314) to generate high-quality text summaries efficiently. QLoRA enables low-rank adaptation, allowing fine-tuning on consumer hardware with reduced VRAM usage.

## Features
- **Low-Rank Adaptation**: Uses QLoRA to fine-tune LLaMA 2 efficiently.
- **Summarization Task**: Trained on text datasets for abstractive summarization.
- **Efficient Training**: Optimized for limited GPU resources.
- **Evaluation**: Uses rouge_score for performance assessment.

## Dataset
- The model is trained on [eil-code/dialogsum-test] containing diverse text summaries.

## Model & Training Setup
- **Base Model**: `meta-llama/Llama-2-7B` 
- **Fine-tuning Framework**: Hugging Face `transformers`, `peft`, `bitsandbytes`
- **LoRA Config**:
  - Rank: `32`
  - Alpha: `32`
  - Dropout: `0.05`
- **Optimizer**: ’paged_adamw_8bit‘
- **Training Steps**: `500` epochs

## Future Work
- Improve model generalization on different text domains.
- Experiment with different training hyperparameters.
- Deploy the fine-tuned model via an API.

## Acknowledgments
- [Hugging Face Transformers](https://huggingface.co/docs/transformers/)
- [QLoRA Paper](https://arxiv.org/abs/2305.14314)
- [dataset source](https://huggingface.co/datasets/neil-code/dialogsum-test)

## License
[MIT License](LICENSE)

