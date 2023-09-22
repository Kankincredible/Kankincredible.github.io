---
layout: post
title: "Project: Abstract Generation on arXiv Research Papers"
subtitle: "Empowering Research: Leveraging Advanced NLP for Abstract Generation"
author: "Yajie Wu"
header-style: text
background: '/img/posts/2023-08-22.jpg'
tags:
  - NLP
---

## Project Overview
This project focuses on generating abstracts for arXiv research papers. The goal is to summarize the essential information from the papers, providing quick insights without reading the entire content. The model is implemented using the Huggingface Longformer and pytorch-lightning, and trained intensively on eight V100 GPUs to ensure accuracy and efficiency.

## Implementation
Several methodologies have been employed to optimize the performance of the model and make the training process efficient and robust. Here is a quick overview of the implementation:
* **Model:** Huggingface Longformer
* **Framework:** pytorch-lighting
* **Training Hardware:** Eight V100 GPUs

## Memory Optimization Training Techniques
To optimize the memory consumption during the training phase and to enhance the model’s performance, several advanced memory optimization training techniques were applied, including:
* **Automatic Mixed Precision (fp16+fp32):** This method utilizes both float16 and float32 data types to speed up training and reduce memory usage without compromising the model's performance.
* **Gradient Accumulation:** It accumulates the gradients over several mini-batches before performing a model update, allowing the use of a larger effective batch size without increasing memory requirements.
* **Gradient Checkpointing:** This technique stores intermediate activations at checkpoints during the forward pass and recomputes them during the backward pass. It reduces memory usage at the expense of some additional computation.

## Performance
The model has been meticulously tuned to achieve optimal results. The hyperparameters were carefully adjusted, and a **43.2 Rouge Score** was achieved on the validation data. This score is commendable and is close to the State-of-the-Art (SOTA) score of **46.6**.

## Conclusion
This project demonstrates the effective implementation and training of a model capable of generating abstracts for arXiv research papers. By utilizing advanced memory optimization techniques and efficient training methods, this model achieves impressive results, close to the best-known performances in this domain. The combination of Huggingface Longformer and pytorch-lightning framework on powerful hardware has proven to be effective in dealing with such advanced natural language processing tasks.
