# Token-Level Pipeline Parallelism for increased attention in Transformer model

## Abstract

With Large Language Models (LLMs) getting bigger on a daily basis and requiring more data to be trained, computational resource conservation has become an important metric of consideration. This project aims to perform a token-level pipeline parallelized model of training an LLM. The token-level pipelining will also be a useful method to process greater chunks of text, thus enabling the possibility of more attention on specific words in a passage. We will use tools such as NeAt vision, which map attention heads, to identify and compare changes in attention values and mappings between a traditionally trained LLM and our LLM.

## Introduction

Typically for large models that do not fit on a single GPU, model parallelism is employed where certain parts of the model are placed on different GPUs. Although, if this is done naively for sequential models, the training process suffers from GPU underutilization since only one GPU is active at one time.

To alleviate this problem, pipeline parallelism splits the input minibatch into multiple microbatches and pipelines the execution of these microbatches across multiple GPUs. 

The aim of this is to reduce GPU-intensive training of LLMs, which not only has severe repercussions for the environment but is also incredibly inefficient in its processing. With LLMs and Transformers growing in predominance, we find that this is a problem that will likely increase for a significant amount of time. We aim to reduce this inefficiency and provide a pathway for future research in this field.

Secondly, we think that this will allow for greater attention in the Multi-Head Attention Layer of the model wherein we will use this parallelism to generate greater attention across sentences in the encoder layer. This will act as a basis for determining if we not just increase training speed and efficiency but also the individual attention heads getting better accuracy.
