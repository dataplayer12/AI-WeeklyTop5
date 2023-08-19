# Listen to the Clubhouse room here

# Paper 1

[Sigmoid Loss for Language Image Pre-Training](https://arxiv.org/pdf/2303.15343.pdf)

[Twitter Thread](https://twitter.com/giffmana/status/1692641733459267713?s=20)

Abstract

We propose a simple pairwise sigmoid loss for image- text pre-training. Unlike standard contrastive learning with softmax normalization, the sigmoid loss operates solely on image-text pairs and does not require a global view of the pairwise similarities for normalization. The sigmoid loss si- multaneously allows further scaling up the batch size, while also performing better at smaller batch sizes. With only four TPUv4 chips, we can train a Base CLIP model at 4 k batch size and a Large LiT model at 20 k batch size, the latter achieves 84.5% ImageNet zero-shot accuracy in two days. This disentanglement of the batch size from the loss further allows us to study the impact of examples vs pairs and neg- ative to positive ratio. Finally, we push the batch size to the extreme, up to one million, and find that the benefits of growing batch size quickly diminish, with a more rea- sonable batch size of 32 k being sufficient. We hope our re- search motivates further explorations in improving the qual- ity and efficiency of language-image pre-training.

# Paper 2

[To Compress or Not to Compress- Self-Supervised Learning and Information Theory: A Review](https://arxiv.org/abs/2304.09355)

Abstract

Deep neural networks have demonstrated remarkable performance in supervised learning tasks but require large amounts of labeled data. Self-supervised learning offers an alternative paradigm, enabling the model to learn from data without explicit labels. Information theory has been instrumental in understanding and optimizing deep neural networks. Specifically, the information bottleneck principle has been applied to optimize the trade-off between compression and relevant information preservation in supervised settings. However, the optimal information objective in self-supervised learning remains unclear. In this paper, we review various approaches to self-supervised learning from an information-theoretic standpoint and present a unified framework that formalizes the self-supervised information-theoretic learning problem. We integrate existing research into a coherent framework, examine recent self-supervised methods, and identify research opportunities and challenges. Moreover, we discuss empirical measurement of information-theoretic quantities and their estimators. This paper offers a comprehensive review of the intersection between information theory, self-supervised learning, and deep neural networks.

# Paper 3

[FastViT: A Fast Hybrid Vision Transformer using Structural Reparameterization](https://arxiv.org/abs/2303.14189)

[Code](https://github.com/apple/ml-fastvit)

Abstract

The recent amalgamation of transformer and convolutional designs has led to steady improvements in accuracy and efficiency of the models. In this work, we introduce FastViT, a hybrid vision transformer architecture that obtains the state-of-the-art latency-accuracy trade-off. To this end, we introduce a novel token mixing operator, RepMixer, a building block of FastViT, that uses structural reparameterization to lower the memory access cost by removing skip-connections in the network. We further apply train-time overparametrization and large kernel convolutions to boost accuracy and empirically show that these choices have minimal effect on latency. We show that - our model is 3.5x faster than CMT, a recent state-of-the-art hybrid transformer architecture, 4.9x faster than EfficientNet, and 1.9x faster than ConvNeXt on a mobile device for the same accuracy on the ImageNet dataset. At similar latency, our model obtains 4.2% better Top-1 accuracy on ImageNet than MobileOne. Our model consistently outperforms competing architectures across several tasks -- image classification, detection, segmentation and 3D mesh regression with significant improvement in latency on both a mobile device and a desktop GPU. Furthermore, our model is highly robust to out-of-distribution samples and corruptions, improving over competing robust models.

# Paper 4

[Faith and Fate: Limits of Transformers on Compositionality](https://arxiv.org/abs/2305.18654)


Abstract

Transformer large language models (LLMs) have sparked admiration for their exceptional performance on tasks that demand intricate multi-step reasoning. Yet, these models simultaneously show failures on surprisingly trivial problems. This begs the question: Are these errors incidental, or do they signal more substantial limitations? In an attempt to demystify Transformers, we investigate the limits of these models across three representative compositional tasks -- multi-digit multiplication, logic grid puzzles, and a classic dynamic programming problem. These tasks require breaking problems down into sub-steps and synthesizing these steps into a precise answer. We formulate compositional tasks as computation graphs to systematically quantify the level of complexity, and break down reasoning steps into intermediate sub-procedures. Our empirical findings suggest that Transformers solve compositional tasks by reducing multi-step compositional reasoning into linearized subgraph matching, without necessarily developing systematic problem-solving skills. To round off our empirical study, we provide theoretical arguments on abstract multi-step reasoning problems that highlight how Transformers' performance will rapidly decay with increased task complexity.

# Paper 5

[Composable Function-preserving Expansions for Transformer Architectures](https://arxiv.org/abs/2308.06103)

[Code](https://github.com/google-research/google-research/blob/master/muNet/TransformerExpansions.ipynb)

Abstract

Training state-of-the-art neural networks requires a high cost in terms of compute and time. Model scale is recognized to be a critical factor to achieve and improve the state-of-the-art. Increasing the scale of a neural network normally requires restarting from scratch by randomly initializing all the parameters of the model, as this implies a change of architecture's parameters that does not allow for a straightforward transfer of knowledge from smaller size models. In this work, we propose six composable transformations to incrementally increase the size of transformer-based neural networks while preserving functionality, allowing to expand the capacity of the model as needed. We provide proof of exact function preservation under minimal initialization constraints for each transformation. The proposed methods may enable efficient training pipelines for larger and more powerful models by progressively expanding the architecture throughout training.
