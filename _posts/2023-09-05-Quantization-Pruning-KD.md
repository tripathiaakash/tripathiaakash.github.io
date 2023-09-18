---
layout: post
title: "Quantization vs Pruning vs Knowledge Distillation"
date: 2023-09-05 10:55:40 +0000
category: LLMops
---

In the LLM world, when it comes to inference, there are mostly two major requirements from a well run and a well built LLM system:
1. High Accuracy vis-a-vis hence more usage
2. Low latency vis-a-vis hence low costs

And these two requirements are the part of a tradeoff that plagues almost all ML models/systems. Most accurate LLMs are highly complex multi-layer transformer models trained on trillions of tokens. Due to this, during inference time, billions of computations are required to generate a single token. Hence, it eats up the computational resources.
In order to solve this problem, there are three common techniques:
1. Quantization:
2. Pruning:
3. Distillation: