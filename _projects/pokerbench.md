---
layout: page
title: PokerBench
description: Small language model training and evaluation for poker decision-making under uncertainty.
period: 2025.08 - 2025.12
importance: 1
category: AI & ML Projects
github: https://github.com/doeunyy/pokerbench-slm-decision-making
---

## Overview

Poker is a challenging testbed for language models because it requires strategic reasoning under uncertainty, hidden-information reasoning, and precise numeric action prediction. This project explores whether small language models can learn poker decision-making behavior through task-specific fine-tuning.

## Method

We fine-tuned Qwen3, LLaMA-3.2, and Gemma variants on PokerBench, an instruction-action dataset of solver-labeled poker decisions. The project included zero-shot and few-shot baseline evaluation, QLoRA-based fine-tuning, and metric-based comparison using Action Accuracy and Exact Match.

{% include figure.liquid loading="eager" path="assets/projects/pokerbench/pokerbench_model_architecture.jpg" title="PokerBench fine-tuning and evaluation pipeline" caption="Figure 1. Fine-tuning and evaluation pipeline. PokerBench scenarios are formatted for QLoRA fine-tuning and evaluated with Action Accuracy and Exact Match." class="img-fluid rounded z-depth-1" %}

## Results

QLoRA fine-tuning substantially improved small language model performance compared with zero-shot baselines. Fine-tuned SLMs achieved strong Action Accuracy and Exact Match, showing that task-specific fine-tuning can help small models learn structured poker decision-making behavior under uncertainty.

{% include figure.liquid loading="eager" path="assets/projects/pokerbench/pokerbench_model_size_vs_performance_scatter.jpg" title="PokerBench model size versus performance" caption="Figure 2. Fine-tuned SLMs vs larger baselines. The comparison highlights the performance-resource trade-off across model scales." class="img-fluid rounded z-depth-1" %}

{% include figure.liquid loading="eager" path="assets/projects/pokerbench/pokerbench_slm_finetuning_overall_barplot.jpg" title="PokerBench SLM fine-tuning overall performance" caption="Figure 3. Zero-shot vs fine-tuned performance. Fine-tuning substantially improves small language model accuracy on structured poker decisions." class="img-fluid rounded z-depth-1" %}

<!-- ## My Contributions

- Conducted zero-shot evaluation of LLaMA-3-8B and LLaMA-2-13B using Hugging Face models.
- Performed few-shot API evaluation of Claude 4.0 Haiku.
- Contributed to the evaluation pipeline, result analysis, project report, and presentation materials.
-->

## Tech Stack

`Python` · `PyTorch` · `Hugging Face Transformers` · `QLoRA` · `LoRA` · `bitsandbytes`

## Links

- [\[Reference Paper\] PokerBench: Training Large Language Models to become Professional Poker Players](https://arxiv.org/abs/2501.08328)
