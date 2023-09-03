## Paper 1

[Eventful Transformers: Leveraging Temporal Redundancy in Vision Transformers](https://arxiv.org/abs/2308.13494)

[Code](https://github.com/WISION-Lab/eventful-transformer)

Abstract:

Vision Transformers achieve impressive accuracy across a range of visual recognition tasks. Unfortunately, their accuracy frequently comes with high computational costs. This is a particular issue in video recognition, where models are often applied repeatedly across frames or temporal chunks. In this work, we exploit temporal redundancy between subsequent inputs to reduce the cost of Transformers for video processing. We describe a method for identifying and re-processing only those tokens that have changed significantly over time. Our proposed family of models, Eventful Transformers, can be converted from existing Transformers (often without any re-training) and give adaptive control over the compute cost at runtime. We evaluate our method on large-scale datasets for video object detection (ImageNet VID) and action recognition (EPIC-Kitchens 100). Our approach leads to significant computational savings (on the order of 2-4x) with only minor reductions in accuracy.

## Paper 2

[Qwen-VL: A Frontier Large Vision-Language Model with Versatile Abilities](https://arxiv.org/abs/2308.12966)

[Code](https://github.com/QwenLM/Qwen-VL)

[Demo](https://modelscope.cn/studios/qwen/Qwen-VL-Chat-Demo/summary)

Abstract:

We introduce the Qwen-VL series, a set of large-scale vision-language models designed to perceive and understand both text and images. Comprising Qwen-VL and Qwen-VL-Chat, these models exhibit remarkable performance in tasks like image captioning, question answering, visual localization, and flexible interaction. The evaluation covers a wide range of tasks including zero-shot captioning, visual or document visual question answering, and grounding. We demonstrate the Qwen-VL outperforms existing Large Vision Language Models (LVLMs). We present their architecture, training, capabilities, and performance, highlighting their contributions to advancing multimodal artificial intelligence. Code, demo and models are available.

## Paper 3

[CoTracker: It is Better to Track Together](https://arxiv.org/abs/2307.07635)

[Code](https://github.com/facebookresearch/co-tracker)

[Demo](https://huggingface.co/spaces/facebook/cotracker?utm_source=twitter&utm_medium=organic_social&utm_campaign=research&utm_content=video)

Abstract:

Methods for video motion prediction either estimate jointly the instantaneous motion of all points in a given video frame using optical flow or independently track the motion of individual points throughout the video. The latter is true even for powerful deep-learning methods that can track points through occlusions. Tracking points individually ignores the strong correlation that can exist between the points, for instance, because they belong to the same physical object, potentially harming performance. In this paper, we thus propose CoTracker, an architecture that jointly tracks multiple points throughout an entire video. This architecture combines several ideas from the optical flow and tracking literature in a new, flexible and powerful design. It is based on a transformer network that models the correlation of different points in time via specialised attention layers. The transformer iteratively updates an estimate of several trajectories. It can be applied in a sliding-window manner to very long videos, for which we engineer an unrolled training loop. It can track from one to several points jointly and supports adding new points to track at any time. The result is a flexible and powerful tracking algorithm that outperforms state-of-the-art methods in almost all benchmarks.

## Paper 4

[RoboTAP: Tracking Arbitrary Points for Few-Shot Visual Imitation](https://arxiv.org/pdf/2308.15975.pdf)

[Project Page](https://robotap.github.io)

Abstract:

For robots to be useful outside labs and specialised factories we need to be able to teach them new useful behaviors quickly. Current approaches lack either the generality to onboard new tasks without task-specific engineering, or else lack the data-efficiency to do so in an amount of time that enables practical use. In this work we explore dense tracking as a representational vehicle to allow faster and more general learning from demonstration. Our approach utilizes Track-Any-Point (TAP) models to isolate the relevant motion in a demonstration, and parameterize a low-level controller to reproduce this motion across changes in the scene. We show this results in robust robot policies that can solve complex object-arrangement tasks such as shape-matching, stacking, and even full path-following tasks such as applying glue and sticking objects together, all from demonstrations that can be collected in minutes.

## Paper 5

[Can Programming Languages Boost Each Other via Instruction Tuning?](https://arxiv.org/abs/2308.16824)

[Code](https://github.com/NL2Code/CodeM)

Abstract:

When human programmers have mastered a programming language, it would be easier when they learn a new programming language. In this report, we focus on exploring whether programming languages can boost each other during the instruction fine-tuning phase of code large language models. We conduct extensive experiments of 8 popular programming languages (Python, JavaScript, TypeScript, C, C++, Java, Go, HTML) on StarCoder. Results demonstrate that programming languages can significantly improve each other. For example, CodeM-Python 15B trained on Python is able to increase Java by an absolute 17.95% pass@1 on HumanEval-X. More surprisingly, we found that CodeM-HTML 7B trained on the HTML corpus can improve Java by an absolute 15.24% pass@1.
