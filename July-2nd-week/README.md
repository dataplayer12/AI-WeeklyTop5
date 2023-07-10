# Paper 1

[Segment Anything Meets Point Tracking](https://arxiv.org/abs/2307.01197)

[Code](https://github.com/SysCV/sam-pt)

Abstract:

The Segment Anything Model (SAM) has established itself as a powerful zero-shot image segmentation model, employing interactive prompts such as points to generate masks. This paper presents SAM-PT, a method extending SAM's capability to tracking and segmenting anything in dynamic videos. SAM-PT leverages robust and sparse point selection and propagation techniques for mask generation, demonstrating that a SAM-based segmentation tracker can yield strong zero-shot performance across popular video object segmentation benchmarks, including DAVIS, YouTube-VOS, and MOSE. Compared to traditional object-centric mask propagation strategies, we uniquely use point propagation to exploit local structure information that is agnostic to object semantics. We highlight the merits of point-based tracking through direct evaluation on the zero-shot open-world Unidentified Video Objects (UVO) benchmark. To further enhance our approach, we utilize K-Medoids clustering for point initialization and track both positive and negative points to clearly distinguish the target object. We also employ multiple mask decoding passes for mask refinement and devise a point re-initialization strategy to improve tracking accuracy. Our code integrates different point trackers and video segmentation benchmarks and will be released

# Paper 2
[What Should Data Science Education Do with Large Language Models?](https://arxiv.org/abs/2307.02792)

Abstract:

The rapid advances of large language models (LLMs), such as ChatGPT, are revolutionizing data science and statistics. These state-of-the-art tools can streamline complex processes. As a result, it reshapes the role of data scientists. We argue that LLMs are transforming the responsibilities of data scientists, shifting their focus from hands-on coding, data-wrangling and conducting standard analyses to assessing and managing analyses performed by these automated AIs. This evolution of roles is reminiscent of the transition from a software engineer to a product manager. We illustrate this transition with concrete data science case studies using LLMs in this paper. These developments necessitate a meaningful evolution in data science education. Pedagogy must now place greater emphasis on cultivating diverse skillsets among students, such as LLM-informed creativity, critical thinking, AI-guided programming. LLMs can also play a significant role in the classroom as interactive teaching and learning tools, contributing to personalized education. This paper discusses the opportunities, resources and open challenges for each of these directions. As with any transformative technology, integrating LLMs into education calls for careful consideration. While LLMs can perform repetitive tasks efficiently, it's crucial to remember that their role is to supplement human intelligence and creativity, not to replace it. Therefore, the new era of data science education should balance the benefits of LLMs while fostering complementary human expertise and innovations. In conclusion, the rise of LLMs heralds a transformative period for data science and its education. This paper seeks to shed light on the emerging trends, potential opportunities, and challenges accompanying this paradigm shift, hoping to spark further discourse and investigation into this exciting, uncharted territory.

# Paper 3

[Initial Task Allocation for Multi-Human Multi-Robot Teams with Attention-based Deep Reinforcement Learning](https://arxiv.org/abs/2303.02486)

Abstract:

Multi-human multi-robot teams have great potential for complex and large-scale tasks through the collaboration of humans and robots with diverse capabilities and expertise. To efficiently operate such highly heterogeneous teams and maximize team performance timely, sophisticated initial task allocation strategies that consider individual differences across team members and tasks are required. While existing works have shown promising results in reallocating tasks based on agent state and performance, the neglect of the inherent heterogeneity of the team hinders their effectiveness in realistic scenarios. In this paper, we present a novel formulation of the initial task allocation problem in multi-human multi-robot teams as contextual multi-attribute decision-make process and propose an attention-based deep reinforcement learning approach. We introduce a cross-attribute attention module to encode the latent and complex dependencies of multiple attributes in the state representation. We conduct a case study in a massive threat surveillance scenario and demonstrate the strengths of our model.

# Paper 4

[QIGen: Generating Efficient Kernels for Quantized Inference on Large Language Models](https://arxiv.org/abs/2307.03738)

[Code](https://github.com/IST-DASLab/QIGen)

Abstract:

We present ongoing work on a new automatic code generation approach for supporting quantized generative inference on LLMs such as LLaMA or OPT on off-the-shelf CPUs. Our approach is informed by the target architecture and a performance model, including both hardware characteristics and method-specific accuracy constraints. Results on CPU-based inference for LLaMA models show that our approach can lead to high performance and high accuracy, comparing favorably to the best existing open-source solution. A preliminary implementation is available
