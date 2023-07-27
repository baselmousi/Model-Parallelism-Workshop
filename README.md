# Model-Parallelism-Workshop
Code and notes associated with the model parallelism workshop. The workshop was delivered by Nvidia. 

# Slides 
You can access the workshop slides via this [link](https://drive.google.com/drive/folders/1ngVnPV90p7OMoZ6dQLysZwcu45vs-CNb?usp=drive_link). Slides 1 and 2 correspond to Lab 1 and Slides 3 correspond to Lab 2.

# Lab 1 
Lab 1 covers the material needed to scale the training of large neural models to multiple gpus.

## Notebooks summary 

1. In notebook 01, we give an overview of the class environment and we introduce some basic slurm commands. Throughout the workshop, we will use two nodes each containing two gpus.
2.  In notebook 02, we give an introduction about the distributed training strategies and we use the pytorch distributed launcher to scale the pretraining of GPT to multiple gpus within the same node.
3. In notebook 03, we scale the training to multiple nodes and we profile the training using the pytorch profiler. We also introduce the concept of hybrid parallelism via running the pretraining using tensor parallelism and  pipeline parallelism.
4. In notebook 04, we introduce possbile optimizations to the pretraining of gpt. We present concepts like mixed precision training, activation checkpointing, and gradient accumulation. Moreover, the notebook introduces some useful utils (computing number of parameters of a a model and estimating the peak flops and the amount of time needed to train the model)
5. In notebook 05, we scale the training of an image classifier using deepspeed and the zero redundancy optimizer
6. In notebook 06, we introduce the concept of a mixture of experts architecture and shows how we can add 'expert layers' to an architecture using deepspeed

## Papers 

1. [Megatron-LM: Training Multi-Billion Parameter Language Models Using Model Parallelism](https://arxiv.org/abs/1909.08053)
2. [ZeRO: Memory Optimizations Toward Training Trillion Parameter Models](https://arxiv.org/abs/1910.02054)
3. 
# Lab 2 
Lab 2 covers the material needed to deploy a GPT model into production using the nvidia's Faster Transformer library and the nvidia's triton server

## Notebooks summary

1. In notebook 02, we deployed a 6B GPT-J model using nothing but pytorch and the transformers library. We used the deployed instance to perform few shots learning on the task of machine translation. Finally, we measured the inference time to use as a baseline for the next two notebooks.
2. In notebook 03, we deployed the same model using the nvidia’s Faster Transformer Library. We ran the inference on one GPU and then we extended it to two GPUS using tensor parallelism.
3. In notebook 04, we deployed the model into production using nvidia’s triton server

