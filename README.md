# AI-WeeklyTop5
Top 5 papers in AI every week

This repo hosts the papers covered in our weekly series of talks 'Top 5 AI papers this week' on the Clubhouse app.

2023

What follows is a simple explanation of each paper. Abstracts, links to the papers and code are here:
[July 1st Week](https://github.com/dataplayer12/AI-WeeklyTop5/blob/main/July-1st-week/README.md)

Here is my selection of the top 5 AI papers this week.

My contacts:   [GitHub](https://github.com/dataplayer12)   [Twitter](https://twitter.com/aibeginners?s=21&t=jYIYCzQQMszYs52sauII3w)   [Insta](https://instagram.com/iamjaiyam?igshid=MjEwN2IyYWYwYw==)   [Threads](https://www.threads.net/@iamjaiyam)   [LinkedIn](https://www.linkedin.com/in/jaiyam-sharma)

## Paper 1: ViT patch selectivity

CNNs build up hierarchal representations of images by aggregating local features across layers. Attention (ViTs) need no such buildup and directly work on global features throughout the network. The authors call this patch selectivity and simulate it in CNNs via data augmentation.
<img width="701" alt="1  patch selectivity" src="https://github.com/dataplayer12/AI-WeeklyTop5/assets/11517109/38bd919e-6c43-47a7-abfe-c8f0d4662f11">

The idea is simple. Replace patches in an image randomly with patches from another image (even though CNNs dont really use patches) and mix labels too.

Results: CNNs are better able to handle occlusions and become robust to information loss. My hypothesis is that such CNNs should make better backbones in object detection and segmentation models.

<img width="973" alt="1  ViT patch selectivity performance" src="https://github.com/dataplayer12/AI-WeeklyTop5/assets/11517109/117edb20-ecfc-4731-ae94-971c666e299d">



## Paper 2: Accelerate transformer inference on CPUs (yes CPUs!)

The latest Xeon CPUs have special hardware for vector neural network instructions (VNNIs) which can accelerate sparse matrix multiplies. This paper presents an easy to use python package using this hardware to accelerate transformer inference.

Their technique of choice is structured sparsity, they choose 4x1 blocks. What this means is that certain cols of weight matrix are set to 0 (white color) and the corresponding rows of input matrix are masked out. The non-zero, non masked entries are then fed into VNNIs which make quick work of them.
<img width="1177" alt="2  Intel transformer inference" src="https://github.com/dataplayer12/AI-WeeklyTop5/assets/11517109/55cefc74-02c0-475b-be66-10a6b2d7a2f4">


The results are astounding. On BERT like models, they get anywhere from 16-37x speedup from onnx-runtime and unto 72x compared to PyTorch. My impression is that while this will not replace GPUs, in a world with GPU shortage, this is an excellent way to extract more juice out of companies’ existing hardware. I tried their python package and found some problems for which I have opened an issue on their GitHub repo.
https://github.com/intel/intel-extension-for-transformers/issues/75

<img width="1443" alt="2  Intel transformer performance" src="https://github.com/dataplayer12/AI-WeeklyTop5/assets/11517109/60e66354-2937-444c-b402-a54397bc1f7a">



## Paper 3: FasterSAM, Segment Anything on Mobile

Meta’s segment anything model has been extremely influential recently in computer vision. But SAM is large and cannot run on small resource constrained devices. The encoder in SAM is a ViT but the decoder is very light. 

The keyword here is knowledge distillation (KD), but there is a twist in how KD is implemented. Instead of letting the encore and decoder train together, the authors copy the lightweight decoder from the original SAM model and distill only the encoder.
<img width="1415" alt="3  Decoupled distillation SAM model" src="https://github.com/dataplayer12/AI-WeeklyTop5/assets/11517109/6c28f389-36e6-426d-9d66-d4f7fef6fb10">


The results are amazing. With less than 1% of training resources this decoupled KD strategy outperforms coupled KD. MobileSAM is ~55x faster than the original SAM and outperforms FastSAM introduced just a few weeks ago.
<img width="1380" alt="3  Faster SAM performance" src="https://github.com/dataplayer12/AI-WeeklyTop5/assets/11517109/7b61fc55-66cd-4f60-abed-7682d60cd452">


## Paper 4: LongNet Scaling transformers to a billion tokens

Scaling context windows in transformers has become the arms race of 2023 😂 In this work, the authors propose dilated attention. In contrast to vanilla self attention which has O(N^2*d) complexity, dilated attention has O(N*d) complexity. There are 3 key ideas to understand
Long sequences of N tokens are split into w segments and these segments are treated independently. This allows parallelizing training and inference across GPUs easily.
Within a segment, r-fold subsampling is used to further reduce the segment length and these subsampled sequences are fed into vanilla self attention module, resulting in outputs O.
Since both 1 and 2 lead to loss of information w.r.t. vanilla self attention, to capture some of it back, w and r are varied k times and all the O’s from each such dilated attention are combined with a weighted average.

This picture nicely represents the above 3 ideas:
<img width="909" alt="4  LongNet dilated self attention" src="https://github.com/dataplayer12/AI-WeeklyTop5/assets/11517109/bf3ff7d3-db26-4b9e-9d29-3d003e8341fc">


The results are amazing and not so amazing at the same time 🙃 The amazing part is that dilated attention outperforms even vanilla attention for context windows up to 32k as shown in the figure below. Note that lower perplexity is better. This strongly suggests that dilated attention is better understood as a regularization technique rather than as an approximation to self attention.
<img width="856" alt="4  LongNet performance" src="https://github.com/dataplayer12/AI-WeeklyTop5/assets/11517109/25f5a450-d7db-4fb0-9232-e3cf84369e98">

The not so amazing thing is that while the authors have verified runtime scaling up to 1B tokens, they have not verified model performance when it is trained with a 1B context window. It remains an open question whether the performance is retained upto 5 orders of magnitude larger context windows (1B vs 32k). Perhaps follow-up work will address this.

## Paper 5: Trainable Transformer in Transformer

This paper is trying to solve the same problem as LongNet paper, but adopts a very different approach. In context learning (ICL) has been a game-changer for language models. Recent work has shown that ICL can be attributed to the ability of LLMs to simulate the fine-tuning (forward and backward pass) of small internal models within the forward pass of a single large transformer model. The authors study this phenomenon and propose a more methodical way of simulating such auxiliary models.
<img width="1159" alt="5  transformer in transformer arch" src="https://github.com/dataplayer12/AI-WeeklyTop5/assets/11517109/3cf9e515-3c48-45e9-805b-03c852037d24">


The full construction is somewhat complex, but involves 4 basic layers: linear, self attention, layer norm and activation layers (duh)
These 4 types of layers form the basis of forward, awkward and descent modules. One neat insight is that the weights of the small auxiliary model are represented as activations (and not weights) of the larger model. These so called prefix embeddings are necessary since  a neural net cannot modify its weights during a forward pass. This is where the ‘trainable’ in the title comes from since by modifying the activations during the forward pass of the large model, we can simulate the backward pass of the smaller auxiliary model.
<img width="1168" alt="5  transformer in transformer performance" src="https://github.com/dataplayer12/AI-WeeklyTop5/assets/11517109/c25eaedd-9642-41aa-8129-023e68e19a52">


The results are promising. For example a 2B parameter model which simulates a 125M OPT model as auxiliary can improve the performance of the vanilla model by 0.3-0.7 points. This paper presents an interesting contrast from the latest trend in LLM research. Rather than trying to extend the context window to millions or billions of tokens, the authors adopt a somewhat principled approach. The results are good but not amazing and I think it is because the auxiliary models are relatively large compared to the parent model. The same approach with larger parents, smaller auxiliaries and much more data could lead to impressive gains without having to extend the context window of vanilla models.


#weeklytop5 
